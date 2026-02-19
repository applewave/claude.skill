# /publish — 페이지 퍼블리싱 5단계 워크플로우

**인자**: `$ARGUMENTS` = `<page>` (예: `login`, `mypage`)
- page: 퍼블리싱할 페이지 이름 (소문자, 하이픈 가능)

---

## 절대 규칙

- **5단계를 반드시 순서대로 완주한다. 중간에 멈추거나 "수정할까요?" 같은 질문으로 끊지 않는다.**
- 감으로 값을 넣지 않는다 — Figma 시안에서 측정할 수 없는 값은 반드시 확인 후 적용
- SPEC.md가 1차 기준, Figma는 시각적 레퍼런스/누락값 확인용

---

## 1단계: 분석

Figma 파일 키: `rI6fWsI9ydRJrk0AWdX72N`

1. `get_metadata`로 Figma 파일에서 해당 페이지 노드를 찾는다
   - 데스크톱: `wackywily_` 접두사
   - 모바일: `m_wackywily_` 접두사
2. `get_screenshot`으로 데스크톱 시안 캡처 → `docs/guide/design/<page>/figma-desktop.png` 저장
3. `get_design_context`로 실측값 추출:
   - 폰트: size, weight, family, line-height
   - 간격: padding, margin, gap
   - 색상: text, background, border
   - 레이아웃: flex/grid, direction, align, position, object-fit
4. 모바일 노드가 존재하면 모바일도 동일하게 분석
   - `get_screenshot` → `docs/guide/design/<page>/figma-mobile.png`
5. 숨겨진(hidden) 노드는 측정하지 않고 존재만 기록
6. `_variables.scss`의 기존 토큰과 대조하여 재사용 가능한 변수 식별

## 2단계: 분석 결과 문서 저장

`docs/guide/design/<page>/SPEC.md`에 실측값을 기록한다.

포함할 내용:
- Figma 노드 ID (데스크톱/모바일)
- 전체 레이아웃 구조 (섹션별 flex/grid 방향, 중첩)
- 섹션별 상세 스펙 (폰트, 색상, 간격, 크기)
- 사용하는 이미지 에셋 목록
- 모바일 차이점 (있을 경우)
- `_variables.scss` 매핑 테이블

## 3단계: 구현

**구현 시작 전 체크리스트:**
- [ ] 이미지 에셋이 `src/assets/images/`에 존재하는지 확인
- [ ] 레이아웃 구조(flex-direction, position, object-fit)를 SPEC.md에서 먼저 확인

**파일 생성/수정:**
1. `src/sections/<page>-content.html` — 본문 HTML
2. `src/pages/<page>.html` — 페이지 조립 (@@include 사용)
3. `src/assets/scss/_<page>.scss` — SCSS 스타일 (BEM 네이밍)
4. `src/assets/scss/common.scss` — `@import '<page>'` 추가
5. `src/index.html` — 페이지 목록 테이블에 행 추가

**HTML 페이지 템플릿:**
```html
@@include('partials/head.html', {
  "title": "Wacky Willy - <Page Title>",
  "description": "Wacky Willy",
  "cssPath": "../assets/css/common.css",
  "bodyClass": "page-<page>",
  "extraHead": ""
})
@@include('partials/header.html', { "imgPath": "../assets/images", "mobileTitle": "<MOBILE_TITLE>" })
<main>
  @@include('sections/<page>-content.html', { "imgPath": "../assets/images" })
</main>
@@include('partials/footer.html', { "jsPath": "../assets/js", "imgPath": "../assets/images", "scripts": "" })
```

**모바일 대응 (모바일 Figma 존재 시):**
- 데스크톱 구현 후 `@include mobile { }` 블록 추가
- 모바일 전용 HTML 요소는 데스크톱에서 `display: none`
- breakpoint: `@include mobile` = `max-width: 767px`

## 4단계: 검증

```bash
npm run build
```

빌드 성공 후 Puppeteer로 스크린샷 캡처:

```javascript
const puppeteer = require('puppeteer');
(async () => {
  const browser = await puppeteer.launch({ headless: true, args: ['--no-sandbox'] });
  const page = await browser.newPage();

  // 데스크톱 (1920px)
  await page.setViewport({ width: 1920, height: 1080, deviceScaleFactor: 1 });
  await page.goto('file:///Users/ohjongkwon/Project/html/html.wackywilly.tw/docs/pages/<page>.html', { waitUntil: 'networkidle0' });
  await page.screenshot({ path: '/tmp/<page>-desktop.png', fullPage: true });

  // 모바일 (375px) — 모바일 Figma가 있는 경우
  await page.setViewport({ width: 375, height: 812, deviceScaleFactor: 1 });
  await page.goto('file:///Users/ohjongkwon/Project/html/html.wackywilly.tw/docs/pages/<page>.html', { waitUntil: 'networkidle0' });
  await page.screenshot({ path: '/tmp/<page>-mobile.png', fullPage: true });

  await browser.close();
})();
```

Puppeteer는 `/tmp/node_modules/puppeteer`에 설치되어 있음.

**비교 기준:**
1. 데스크톱 (1920px): Figma 데스크톱 시안과 비교
2. 모바일 (375px): Figma 모바일 시안과 비교
3. 레이아웃 깨짐 없음: 콘텐츠 잘림, 오버플로 없음
4. 기존 페이지 회귀 없음

차이 발견 시 수정 후 재빌드 → 재캡처 → 재비교. 통과할 때까지 반복.

## 5단계: commit + push

모든 검증 통과 후:

```bash
git add {변경된 파일들}
git commit -m "<page> 페이지 퍼블리싱 — 데스크톱(+모바일) 구현

Co-Authored-By: Claude Opus 4.6 <noreply@anthropic.com>"
git push
```

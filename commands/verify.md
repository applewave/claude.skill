# /verify — 페이지 검증 (빌드 + 스크린샷 + Figma 비교)

**인자**: `$ARGUMENTS` = `<page>` (예: `main`, `plp`, `pdp`, `cart`, `offline`)

---

## 수행할 작업

### 1. 빌드

```bash
npm run build
```

빌드 실패 시 SCSS/HTML 에러를 수정하고 재빌드.

### 2. 스크린샷 캡처

Puppeteer로 캡처 (`/tmp/node_modules/puppeteer` 사용):

```javascript
const puppeteer = require('puppeteer');
(async () => {
  const browser = await puppeteer.launch({ headless: true, args: ['--no-sandbox'] });
  const page = await browser.newPage();

  // 데스크톱
  await page.setViewport({ width: 1920, height: 1080, deviceScaleFactor: 1 });
  await page.goto('file:///Users/ohjongkwon/Project/html/html.wackywilly.tw/docs/pages/<page>.html', { waitUntil: 'networkidle0' });
  await page.screenshot({ path: '/tmp/<page>-desktop.png', fullPage: true });

  // 모바일
  await page.setViewport({ width: 375, height: 812, deviceScaleFactor: 1 });
  await page.goto('file:///Users/ohjongkwon/Project/html/html.wackywilly.tw/docs/pages/<page>.html', { waitUntil: 'networkidle0' });
  await page.screenshot({ path: '/tmp/<page>-mobile.png', fullPage: true });

  await browser.close();
})();
```

### 3. Figma 시안과 비교

1. `docs/guide/design/<page>/figma-desktop.png`와 `/tmp/<page>-desktop.png` 비교
2. `docs/guide/design/<page>/figma-mobile.png`와 `/tmp/<page>-mobile.png` 비교 (모바일 시안이 있는 경우)
3. `docs/guide/design/<page>/SPEC.md`의 스펙과 구현 대조

### 4. 비교 기준

- 레이아웃 구조 (flex/grid 방향, 정렬)
- 폰트 (size, weight, color)
- 간격 (padding, margin, gap)
- 색상 (배경, 테두리, 텍스트)
- 이미지 비율/크기
- 콘텐츠 잘림/오버플로 없음
- 기존 페이지 회귀 없음

### 5. 수정 반복

차이 발견 시:
1. SCSS/HTML 수정
2. `npm run build`
3. 재캡처
4. 재비교

모든 차이 해소될 때까지 반복.

### 6. 결과 보고

최종 비교 결과를 요약하여 보고:
- PASS 항목
- 수정한 항목
- 남은 이슈 (있을 경우)

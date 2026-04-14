# /new-page — 새 페이지 스캐폴딩

**인자**: `$ARGUMENTS` = `<page> <korean-name> <section>` (예: `login 로그인 member`, `mypage 마이페이지 member`)
- page: 페이지 슬러그 (소문자, 하이픈 가능)
- korean-name: 한글 페이지명
- section: index.html 테이블의 section 값

---

## 수행할 작업

아래 파일들을 순서대로 생성/수정한다. **모든 단계를 한번에 완료한다.**

### 1. `src/sections/<page>-content.html` 생성

```html
<section class="<page>">
  <div class="inner">
    <!-- TODO: Figma 분석 후 구현 -->
  </div>
</section>
```

### 2. `src/pages/<page>.html` 생성

```html
@@include('partials/head.html', {
  "title": "Wacky Willy - <Korean Name>",
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

### 3. `src/assets/scss/_<page>.scss` 생성

```scss
// ============================================
// <page>.scss — <Korean Name>
// ============================================

.<page> {
  // TODO: Figma 분석 후 구현
}
```

### 4. `src/assets/scss/common.scss` 수정

`// Page Styles` 섹션에 `@import '<page>';` 추가.

### 5. `src/index.html` 수정

`<tbody>` 안에 새 행 추가. UI ID는 기존 마지막 행 + 1.

```html
<tr>
  <td>{next UI ID}</td>
  <td><section></td>
  <td></td>
  <td></td>
  <td></td>
  <td></td>
  <td></td>
  <td><a href="pages/<page>.html"><korean-name></a></td>
  <td><a class="gh-link" data-path="docs/guide/design/<page>/SPEC.md">GitHub</a><span
      class="link-sep">|</span><a href="guide/design/<page>/SPEC.md">Local</a></td>
  <td><a href="guide/design/<page>/figma-desktop.png">Desktop</a><span
      class="link-sep">|</span><a href="guide/design/<page>/figma-mobile.png">Mobile</a></td>
  <td></td>
</tr>
```

### 6. `docs/guide/design/<page>/` 디렉토리 생성

```bash
mkdir -p docs/guide/design/<page>
```

### 7. 빌드 확인

```bash
npm run build
```

빌드 성공 확인 후 완료 메시지 출력.

---

## 완료 후 안내

스캐폴딩 완료 후 다음 단계 안내:
- `/publish <page>` 로 Figma 분석 → 구현 → 검증 → 커밋 워크플로우 실행

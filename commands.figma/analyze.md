# /analyze — Figma 분석 + SPEC.md 생성 (1~2단계)

**인자**: `$ARGUMENTS` = `<page> [nodeId]` (예: `login 525:678`, `mypage`)
- page: 페이지 이름
- nodeId: (선택) Figma 노드 ID. 생략 시 자동 검색

---

## 수행할 작업

### 1단계: Figma 분석

Figma 파일 키: `rI6fWsI9ydRJrk0AWdX72N`

**노드 찾기:**
- nodeId가 주어진 경우 해당 노드 사용
- 주어지지 않은 경우: `get_metadata(nodeId="0:1")`로 페이지 목록 조회 → `wackywily_<page>` 노드 검색

**데스크톱 분석:**
1. `get_screenshot(nodeId, fileKey)` → Figma 시안 캡처
2. `get_design_context(nodeId, fileKey)` → 실측값 추출

**모바일 분석:**
1. `m_wackywily_<page>` 노드 검색
2. 존재하면 동일하게 `get_screenshot` + `get_design_context`

**추출할 항목:**
- 폰트: font-family, font-size, font-weight, line-height, color
- 간격: padding, margin, gap
- 레이아웃: display, flex-direction, align-items, justify-content, position, grid-template
- 크기: width, height, min/max-width, min/max-height
- 시각: background-color, border, border-radius, box-shadow, opacity
- 이미지: object-fit, aspect-ratio
- 숨겨진 노드: 존재만 기록

**`_variables.scss` 대조:**
- 추출한 값을 기존 변수와 매핑
- 새 토큰 발견 시 별도 기록

### 2단계: SPEC.md 저장

`docs/guide/design/<page>/SPEC.md`에 저장.

**문서 구조:**
```markdown
# <Page Name> 페이지 디자인 스펙

## Figma 정보
- 데스크톱 노드: `<nodeId>`
- 모바일 노드: `<nodeId>` (있을 경우)

## 전체 레이아웃

(섹션 구조, flex/grid 방향, 중첩 관계)

## 섹션별 상세

### 섹션명
- 폰트: ...
- 색상: ...
- 간격: ...
- 레이아웃: ...

## 이미지 에셋
| 파일명 | 크기 | 용도 |
|--------|------|------|

## 모바일 차이점 (있을 경우)

## _variables.scss 매핑
| 값 | 변수 | 비고 |
|----|------|------|
```

**시안 캡처 저장:**
- `docs/guide/design/<page>/figma-desktop.png`
- `docs/guide/design/<page>/figma-mobile.png` (모바일 존재 시)

### 완료 후 안내

분석 완료 후 다음 단계 안내:
- 구현으로 진행하려면 `/publish <page>` 또는 직접 3단계부터 수행

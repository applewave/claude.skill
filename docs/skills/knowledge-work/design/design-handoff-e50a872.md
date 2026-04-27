# design-handoff

## 요약

Generate developer handoff specs from a design. Use when a design is ready for engineering and needs a spec sheet covering layout, design tokens, component props, interaction states, responsive breakpoints, edge cases, and animation details.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | design |
| 원본 경로 | `knowledge-work-plugins/design/skills/design-handoff/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/design/design-handoff-e50a872.md` |
| 입력 힌트 | `<Figma URL or design description>` |

## 언제 쓰나

Generate developer handoff specs from a design. Use when a design is ready for engineering and needs a spec sheet covering layout, design tokens, component props, interaction states, responsive breakpoints, edge cases, and animation details.

## 주요 내용

- **사용 방식**: /design-handoff $ARGUMENTS Generate handoff specs for: @$1 If a Figma URL is provided, pull the design from Figma. Otherwise, work from the provided description or screenshot.
- **진행 방식**: **Don't assume** — If it's not specified, the developer will guess. Specify everything. **Use tokens, not values** — Reference `spacing-md` not `16px`. **Show all states** — Default, hover, active, disabled, loading, error, empty. **Describe the why** — "This collapses on mobile because users primarily use one-handed" helps developers make good judgment calls.

## 원본 문서 구조

- Usage
- What to Include
  - Visual Specifications
  - Interaction Specifications
  - Content Specifications
  - Edge Cases
  - Accessibility
- Principles
- Output
- Handoff Spec: [Feature/Screen Name]
  - Overview
  - Layout
  - Design Tokens Used
  - Components
  - States and Interactions
  - Responsive Behavior
  - Edge Cases
  - Animation / Motion
  - Accessibility Notes
- If Connectors Available
- Tips

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/design/skills/design-handoff/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

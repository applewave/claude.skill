# migrate-to-shoehorn

## 요약

Migrate test files from `as` type assertions to @total-typescript/shoehorn. Use when user mentions shoehorn, wants to replace `as` in tests, or needs partial test data.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/migrate-to-shoehorn/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/migrate-to-shoehorn-f891ce5.md` |

## 언제 쓰나

Migrate test files from `as` type assertions to @total-typescript/shoehorn. Use when user mentions shoehorn, wants to replace `as` in tests, or needs partial test data.

## 주요 내용

- **진행 방식**: **Gather requirements** - ask user: What test files have `as` assertions causing problems? Are they dealing with large objects where only some properties matter? Do they need to pass intentionally wrong data for error testing? **Install and migrate**: [ ] Install: `npm i @total-typescript/shoehorn` [ ] Find test files with `as` assertions: `grep -r " as [A-Z]" --include="*.test.ts" --include="*.spec.ts"` [ ] Replace `as Type` with `fromPartial()` [ ] Replace `as unknown as Type` with `fromAny()` [ ] Add imports from `@total-typescript/shoehorn` [ ] Run type check to verify

## 원본 문서 구조

- Why shoehorn?
- Install
- Migration patterns
  - Large objects with few needed properties
  - `as Type` → `fromPartial()`
  - `as unknown as Type` → `fromAny()`
- When to use each
- Workflow

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/migrate-to-shoehorn/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

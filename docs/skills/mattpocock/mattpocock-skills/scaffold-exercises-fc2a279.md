# scaffold-exercises

## 요약

Create exercise directory structures with sections, problems, solutions, and explainers that pass linting. Use when user wants to scaffold exercises, create exercise stubs, or set up a new course section.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/scaffold-exercises/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/scaffold-exercises-fc2a279.md` |

## 언제 쓰나

Create exercise directory structures with sections, problems, solutions, and explainers that pass linting. Use when user wants to scaffold exercises, create exercise stubs, or set up a new course section.

## 주요 내용

- **진행 방식**: **Parse the plan** - extract section names, exercise names, and variant types **Create directories** - `mkdir -p` for each path **Create stub readmes** - one `readme.md` per variant folder with a title **Run lint** - `pnpm ai-hero-cli internal lint` to validate **Fix any errors** - iterate until lint passes

## 원본 문서 구조

- Directory naming
- Exercise variants
- Required files
- Workflow
- Lint rules summary
- Moving/renaming exercises
- Example: stubbing from a plan

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/scaffold-exercises/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

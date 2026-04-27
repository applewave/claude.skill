# prd-to-issues

## 요약

Break a PRD into independently-grabbable GitHub issues using tracer-bullet vertical slices. Use when user wants to convert a PRD to issues, create implementation tickets, or break down a PRD into work items.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/prd-to-issues/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/prd-to-issues-24daae7.md` |

## 언제 쓰나

Break a PRD into independently-grabbable GitHub issues using tracer-bullet vertical slices. Use when user wants to convert a PRD to issues, create implementation tickets, or break down a PRD into work items.

## 주요 내용

- **진행 방식**: 1. Locate the PRD Ask the user for the PRD GitHub issue number (or URL). If the PRD is not already in your context window, fetch it with `gh issue view <number>` (with comments). 2. Explore the codebase (optional) If you have not already explored the codebase, do so to understand the current state of the code. 3. Draft vertical slices Break the PRD into **tracer bullet** issues. Each issue is a thin vertical slice that cuts through ALL integration layers end-to-end, NOT a horizontal slice of one layer. Slices may be 'HITL' or 'AFK'. HITL slices require human interaction, such as an architectural decision or a design review. AFK slices can be implemented and merged without human interaction. Prefer AFK over HITL where possible. <vertical-slice-rules> Each slice delivers a narrow but COMPLETE path through every layer (schema, API, UI, tests) A completed slice is demoable or verifiable on its own Prefer many thin slices over few thick ones </vertical-slice-rules> 4. Quiz the user Present...

## 원본 문서 구조

- Process
  - 1. Locate the PRD
  - 2. Explore the codebase (optional)
  - 3. Draft vertical slices
  - 4. Quiz the user
  - 5. Create the GitHub issues
- Parent PRD
- What to build
- Acceptance criteria
- Blocked by
- User stories addressed

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/prd-to-issues/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

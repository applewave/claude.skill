# prd-to-plan

## 요약

Turn a PRD into a multi-phase implementation plan using tracer-bullet vertical slices, saved as a local Markdown file in ./plans/. Use when user wants to break down a PRD, create an implementation plan, plan phases from a PRD, or mentions "tracer bullets".

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/prd-to-plan/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/prd-to-plan-d90b855.md` |

## 언제 쓰나

Turn a PRD into a multi-phase implementation plan using tracer-bullet vertical slices, saved as a local Markdown file in ./plans/. Use when user wants to break down a PRD, create an implementation plan, plan phases from a PRD, or mentions "tracer bullets".

## 주요 내용

- **진행 방식**: 1. Confirm the PRD is in context The PRD should already be in the conversation. If it isn't, ask the user to paste it or point you to the file. 2. Explore the codebase If you have not already explored the codebase, do so to understand the current architecture, existing patterns, and integration layers. 3. Identify durable architectural decisions Before slicing, identify high-level decisions that are unlikely to change throughout implementation: Route structures / URL patterns Database schema shape Key data models Authentication / authorization approach Third-party service boundaries These go in the plan header so every phase can reference them. 4. Draft vertical slices Break the PRD into **tracer bullet** phases. Each phase is a thin vertical slice that cuts through ALL integration layers end-to-end, NOT a horizontal slice of one layer. <vertical-slice-rules> Each slice delivers a narrow but COMPLETE path through every layer (schema, API, UI, tests) A completed slice is demoable or ve...

## 원본 문서 구조

- Process
  - 1. Confirm the PRD is in context
  - 2. Explore the codebase
  - 3. Identify durable architectural decisions
  - 4. Draft vertical slices
  - 5. Quiz the user
  - 6. Write the plan file
- Architectural decisions
- Phase 1: <Title>
  - What to build
  - Acceptance criteria
- Phase 2: <Title>
  - What to build
  - Acceptance criteria

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/prd-to-plan/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

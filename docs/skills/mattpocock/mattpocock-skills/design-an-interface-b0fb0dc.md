# design-an-interface

## 요약

Generate multiple radically different interface designs for a module using parallel sub-agents. Use when user wants to design an API, explore interface options, compare module shapes, or mentions "design it twice".

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/design-an-interface/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/design-an-interface-b0fb0dc.md` |

## 언제 쓰나

Generate multiple radically different interface designs for a module using parallel sub-agents. Use when user wants to design an API, explore interface options, compare module shapes, or mentions "design it twice".

## 주요 내용

- **진행 방식**: 1. Gather Requirements Before designing, understand: [ ] What problem does this module solve? [ ] Who are the callers? (other modules, external users, tests) [ ] What are the key operations? [ ] Any constraints? (performance, compatibility, existing patterns) [ ] What should be hidden inside vs exposed? Ask: "What does this module need to do? Who will use it?" 2. Generate Designs (Parallel Sub-Agents) Spawn 3+ sub-agents simultaneously using Task tool. Each must produce a **radically different** approach. Prompt template for each sub-agent: Design an interface for: [module description] Requirements: [gathered requirements] Constraints for this design: [assign a different constraint to each agent] Agent 1: "Minimize method count - aim for 1-3 methods max" Agent 2: "Maximize flexibility - support many use cases" Agent 3: "Optimize for the most common case" Agent 4: "Take inspiration from [specific paradigm/library]" Output format: Interface signature (types/methods) Usage example (how c...

## 원본 문서 구조

- Workflow
  - 1. Gather Requirements
  - 2. Generate Designs (Parallel Sub-Agents)
  - 3. Present Designs
  - 4. Compare Designs
  - 5. Synthesize
- Evaluation Criteria
- Anti-Patterns

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/design-an-interface/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

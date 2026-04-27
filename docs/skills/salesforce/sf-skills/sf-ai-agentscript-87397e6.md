# sf-ai-agentscript

## 요약

Agent Script DSL for deterministic Agentforce agents. TRIGGER when: user writes or edits .agent files, builds FSM-based agents, uses Agent Script CLI (sf agent generate authoring-bundle, sf agent validate authoring-bundle, sf agent preview, sf agent publish authoring-bundle, sf agent activate), or asks about deterministic agent patterns, slot filling, or instruction resolution. DO NOT TRIGGER when: Builder metadata work (use sf-ai-agentforce), agent testing (use sf-ai-agentforce-testing), or persona design (use sf-ai-agentforce-persona).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-ai-agentscript/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-ai-agentscript-87397e6.md` |
| 라이선스 | MIT |

## 언제 쓰나

Agent Script DSL for deterministic Agentforce agents. TRIGGER when: user writes or edits .agent files, builds FSM-based agents, uses Agent Script CLI (sf agent generate authoring-bundle, sf agent validate authoring-bundle, sf agent preview, sf agent publish authoring-bundle, sf agent activate), or asks about deterministic agent patterns, slot filling, or instruction resolution. DO NOT TRIGGER when: Builder metadata work (use sf-ai-agentforce), agent testing (use sf-ai-agentforce-testing), or persona design (use sf-ai-agentforce-persona).

## 주요 내용

- 원본 설명과 문서 구조를 기준으로 필요한 시점에 참조합니다.

## 원본 문서 구조

- When This Skill Owns the Task
- Right-Size Determinism
- Required Context to Gather First
- Activation Checklist
- Non-Negotiable Rules
  - 1) Service Agent vs Employee Agent
  - 2) Recommended top-level block convention
  - 3) Critical config fields
  - 4) Syntax blockers you should treat as immediate failures
- Recommended Workflow
- Recommended Authoring Workflow
  - Phase 1 — design the agent
  - Phase 2 — author the `.agent`
  - Default authoring stance
  - Phase 3 — validate continuously
  - Phase 4 — preview smoke test
  - Phase 5 — publish and activate
- Deterministic Building Blocks
- Cross-Skill Integration
- Cross-Skill Orchestration
- High-Signal Failure Patterns
- Reference Map
  - Start here
  - Publish / runtime safety
  - Architecture / reasoning
  - Validation / testing / debugging
  - Examples / scaffolds
  - Project documentation
- Score Guide
- Official Resources

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-ai-agentscript/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

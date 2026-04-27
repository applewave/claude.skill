# sf-ai-agentforce-testing

## 요약

Agentforce agent testing with dual-track workflow and 100-point scoring. TRIGGER when: user tests Agentforce agents, runs sf agent test commands, creates test specs, validates topic routing, or analyzes agent test coverage. DO NOT TRIGGER when: Apex unit tests (use sf-testing), building agents (use sf-ai-agentforce), or Agent Script DSL (use sf-ai-agentscript).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-ai-agentforce-testing/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-ai-agentforce-testing-b8eb04b.md` |
| 라이선스 | MIT |

## 언제 쓰나

Agentforce agent testing with dual-track workflow and 100-point scoring. TRIGGER when: user tests Agentforce agents, runs sf agent test commands, creates test specs, validates topic routing, or analyzes agent test coverage. DO NOT TRIGGER when: Apex unit tests (use sf-testing), building agents (use sf-ai-agentforce), or Agent Script DSL (use sf-ai-agentscript).

## 주요 내용

- **진행 방식**: Track A — Multi-turn API testing (primary) Use when you need: multi-turn conversation testing topic re-matching validation context preservation checks escalation or action-chain analysis across turns Requires: ECA / auth setup agent runtime access Track B — CLI Testing Center (secondary) Use when you need: org-native `sf agent test` workflows test spec YAML execution quick single-utterance validation CLI-centered CI/CD usage where Testing Center is available Quick manual path For manual validation without full formal testing, use preview workflows first, then escalate to Track A or B as needed.
- **산출물**: When finishing a run, report in this order: **Test track used** **What was executed** **Pass/fail summary** **Coverage gaps** **Root-cause themes** **Recommended fix loop / next test step** Suggested shape: Agent: <name> Track: Multi-turn API | CLI Testing Center | Preview Executed: <specs / scenarios / turns> Result: <passed / partial / failed> Coverage: <topics, actions, guardrails, context> Issues: <highest-signal failures> Next step: <fix, republish, rerun, or expand coverage>

## 원본 문서 구조

- When This Skill Owns the Task
- Core Operating Rules
  - Script path rule
- Required Context to Gather First
- Dual-Track Workflow
  - Track A — Multi-turn API testing (primary)
  - Track B — CLI Testing Center (secondary)
  - Quick manual path
- Recommended Workflow
  - 1. Discover and verify
  - 2. Plan tests
  - 3. Execute the right track
    - Track A
    - Track B
  - 4. Classify failures
  - 5. Run fix loop
- Testing Guardrails
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Execution / auth
  - Coverage / fix loops
  - Advanced / specialized
  - Templates / assets
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-ai-agentforce-testing/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

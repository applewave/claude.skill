# sf-apex

## 요약

Generates and reviews Salesforce Apex code with 150-point scoring. TRIGGER when: user writes, reviews, or fixes Apex classes, triggers, test classes, batch/queueable/schedulable jobs, or touches .cls/.trigger files. DO NOT TRIGGER when: LWC JavaScript (use sf-lwc), Flow XML (use sf-flow), SOQL-only queries (use sf-soql), or non-Salesforce code.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-apex/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-apex-e77c7a7.md` |
| 라이선스 | MIT |

## 언제 쓰나

Generates and reviews Salesforce Apex code with 150-point scoring. TRIGGER when: user writes, reviews, or fixes Apex classes, triggers, test classes, batch/queueable/schedulable jobs, or touches .cls/.trigger files. DO NOT TRIGGER when: LWC JavaScript (use sf-lwc), Flow XML (use sf-flow), SOQL-only queries (use sf-soql), or non-Salesforce code.

## 주요 내용

- **진행 방식**: 1. Discover local architecture Check for: existing trigger handlers / frameworks service-selector-domain conventions related tests and data factories invocable or async patterns already used in the repo 2. Choose the smallest correct pattern 3. Author with guardrails Generate code that is: bulk-safe sharing-aware CRUD/FLS-safe where applicable testable in isolation consistent with project naming and layering 4. Validate and score Evaluate against the 150-point rubric before handoff. 5. Hand off deploy/test next steps When org validation is needed, hand off to: [sf-testing](../sf-testing/SKILL.md) for test execution loops [sf-deploy](../sf-deploy/SKILL.md) for deploy / dry-run / verification
- **산출물**: When finishing, report in this order: **What was created or reviewed** **Files changed** **Key design decisions** **Risk / guardrail notes** **Test guidance** **Deployment guidance** Suggested shape: Apex work: <summary> Files: <paths> Design: <pattern / framework choices> Risks: <security, bulkification, async, dependency notes> Tests: <what to run / add> Deploy: <dry-run or next step>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Discover local architecture
  - 2. Choose the smallest correct pattern
  - 3. Author with guardrails
  - 4. Validate and score
  - 5. Hand off deploy/test next steps
- Generation Guardrails
- High-Signal Build Rules
  - Trigger architecture
  - Async choice
  - Testing minimums
  - Modern Apex expectations
- Output Format
- LSP Validation Note
- Cross-Skill Integration
- Reference Map
  - Start here
  - High-signal checklists
  - Specialized patterns
  - Troubleshooting / validation
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-apex/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

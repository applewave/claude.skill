# sf-flow

## 요약

Creates and validates Salesforce Flows with 110-point scoring. TRIGGER when: user builds or edits record-triggered, screen, autolaunched, or scheduled flows, or touches .flow-meta.xml files. DO NOT TRIGGER when: Apex automation (use sf-apex), process builder migration questions only, or non-Flow declarative config (use sf-metadata).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-flow/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-flow-0eb8c5c.md` |
| 라이선스 | MIT |

## 언제 쓰나

Creates and validates Salesforce Flows with 110-point scoring. TRIGGER when: user builds or edits record-triggered, screen, autolaunched, or scheduled flows, or touches .flow-meta.xml files. DO NOT TRIGGER when: Apex automation (use sf-apex), process builder migration questions only, or non-Flow declarative config (use sf-metadata).

## 주요 내용

- **진행 방식**: 1. Choose the right automation tool Before building, confirm Flow is the right answer rather than: formula field validation rule roll-up summary Apex 2. Choose the right Flow type 3. Start from a template Prefer the provided assets: `assets/record-triggered-before-save.xml` `assets/record-triggered-after-save.xml` `assets/screen-flow-template.xml` `assets/autolaunched-flow-template.xml` `assets/scheduled-flow-template.xml` `assets/platform-event-flow-template.xml` `assets/ai-decision-template.xml` `assets/subflows/` 4. Validate against Flow guardrails Focus on: no DML in loops no Get Records inside loops proper fault paths correct trigger conditions safe subflow composition AI Decision elements not placed inside loops (credit cost per iteration) AI Decision prompts include merge field references for data context 5. Hand off deployment and testing Use: [sf-deploy](../sf-deploy/SKILL.md) for deploy / dry-run [sf-data](../sf-data/SKILL.md) for high-volume test data
- **산출물**: When finishing, report in this order: **Flow type and goal** **Files created or updated** **Architecture choices** **Bulk/error-handling notes** **Deploy/testing next steps** Suggested shape: Flow: <name> Type: <flow type> Files: <paths> Design: <trigger choice, subflows, key decisions> Risks: <bulk safety, fault paths, dependencies> Next step: <dry-run deploy, activate, or test>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Choose the right automation tool
  - 2. Choose the right Flow type
  - 3. Start from a template
  - 4. Validate against Flow guardrails
  - 5. Hand off deployment and testing
- High-Signal Rules
  - Flow architecture
  - Bulk safety
  - Error handling
- Output Format
- Flow Testing (CLI)
- Cross-Skill Integration
- Reference Map
  - Start here
  - Design / orchestration
  - AI Decision
  - Screen / integration / troubleshooting
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-flow/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

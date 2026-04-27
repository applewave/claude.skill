# sf-debug

## 요약

Salesforce debug log analysis and troubleshooting with 100-point scoring. TRIGGER when: user analyzes debug logs, hits governor limits, reads stack traces, or touches .log files from Salesforce orgs. DO NOT TRIGGER when: running Apex tests (use sf-testing), fixing Apex code (use sf-apex), or Agentforce session tracing (use sf-ai-agentforce-observability).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-debug/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-debug-6cdd7de.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce debug log analysis and troubleshooting with 100-point scoring. TRIGGER when: user analyzes debug logs, hits governor limits, reads stack traces, or touches .log files from Salesforce orgs. DO NOT TRIGGER when: running Apex tests (use sf-testing), fixing Apex code (use sf-apex), or Agentforce session tracing (use sf-ai-agentforce-observability).

## 주요 내용

- **진행 방식**: 1. Retrieve logs sf apex list log --target-org <alias> --json sf apex get log --log-id <id> --target-org <alias> sf apex tail log --target-org <alias> --color 2. Analyze in this order entry point and transaction type exceptions / fatal errors governor limits repeated SOQL / DML patterns CPU / heap hotspots callout timing and external failures 3. Classify severity **Critical** — runtime failure, hard limit, corruption risk **Warning** — near-limit, non-selective query, slow path **Info** — optimization opportunity or hygiene issue 4. Recommend the smallest correct fix Prefer fixes that are: root-cause oriented bulk-safe testable easy to verify with a rerun Expanded workflow: [references/analysis-playbook.md](references/analysis-playbook.md)
- **산출물**: When finishing analysis, report in this order: **What failed** **Where it failed** (class / method / line / transaction stage) **Why it failed** (root cause, not just symptom) **How severe it is** **Recommended fix** **Verification step** Suggested shape: Issue: <summary> Location: <class / line / transaction> Root cause: <explanation> Severity: Critical | Warning | Info Fix: <specific action> Verify: <test or rerun step>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Retrieve logs
  - 2. Analyze in this order
  - 3. Classify severity
  - 4. Recommend the smallest correct fix
- High-Signal Issue Patterns
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Deep references
  - Rubric
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-debug/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

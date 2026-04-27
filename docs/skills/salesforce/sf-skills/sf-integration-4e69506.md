# sf-integration

## 요약

Salesforce integration architecture with 120-point scoring. TRIGGER when: user sets up Named Credentials, External Services, REST/SOAP callouts, Platform Events, CDC, or touches .namedCredential-meta.xml files. DO NOT TRIGGER when: Connected App/OAuth config (use sf-connected-apps), Apex-only logic (use sf-apex), or data import/export (use sf-data).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-integration/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-integration-4e69506.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce integration architecture with 120-point scoring. TRIGGER when: user sets up Named Credentials, External Services, REST/SOAP callouts, Platform Events, CDC, or touches .namedCredential-meta.xml files. DO NOT TRIGGER when: Connected App/OAuth config (use sf-connected-apps), Apex-only logic (use sf-apex), or data import/export (use sf-data).

## 주요 내용

- **진행 방식**: 1. Choose the integration pattern 2. Choose the auth model Prefer secure runtime-managed auth: Named Credentials / External Credentials OAuth or JWT via the right credential model no hardcoded secrets in code 3. Generate from the right templates Use the provided assets under: `assets/named-credentials/` `assets/external-credentials/` `assets/external-services/` `assets/callouts/` `assets/platform-events/` `assets/cdc/` `assets/soap/` 4. Validate operational safety Check: timeout and retry handling async strategy for trigger-originated work logging / observability event retention and subscriber implications 5. Hand off deployment or implementation details Use: [sf-deploy](../sf-deploy/SKILL.md) for deployment [sf-apex](../sf-apex/SKILL.md) for deeper service / retry code [sf-flow](../sf-flow/SKILL.md) for declarative HTTP callout orchestration
- **산출물**: When finishing, report in this order: **Integration pattern chosen** **Auth model chosen** **Files created or updated** **Operational safeguards** **Deployment / testing next step** Suggested shape: Integration: <summary> Pattern: <named credential / external service / event / cdc / callout> Files: <paths> Safety: <timeouts, retries, async, logging> Next step: <deploy, register, test, or implement>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Choose the integration pattern
  - 2. Choose the auth model
  - 3. Generate from the right templates
  - 4. Validate operational safety
  - 5. Hand off deployment or implementation details
- High-Signal Rules
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Event-driven / platform patterns
  - CLI / automation / scoring
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-integration/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

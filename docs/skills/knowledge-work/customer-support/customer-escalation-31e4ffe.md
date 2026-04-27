# customer-escalation

## 요약

Package an escalation for engineering, product, or leadership with full context. Use when a bug needs engineering attention beyond normal support, multiple customers report the same issue, a customer is threatening to churn, or an issue has sat unresolved past its SLA.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | customer-support |
| 원본 경로 | `knowledge-work-plugins/customer-support/skills/customer-escalation/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/customer-support/customer-escalation-31e4ffe.md` |
| 입력 힌트 | `<issue summary> [customer name]` |

## 언제 쓰나

Package an escalation for engineering, product, or leadership with full context. Use when a bug needs engineering attention beyond normal support, multiple customers report the same issue, a customer is threatening to churn, or an issue has sat unresolved past its SLA.

## 주요 내용

- **사용 방식**: /customer-escalation <issue description> [customer name or account] Examples: `/customer-escalation API returning 500 errors intermittently for Acme Corp` `/customer-escalation Data export is missing rows — 3 customers reported this week` `/customer-escalation SSO login loop affecting all Enterprise customers` `/customer-escalation Customer threatening to churn over missing audit log feature`
- **진행 방식**: 1. Understand the Issue Parse the input and determine: **What's broken or needed**: The core technical or product issue **Who's affected**: Specific customer(s), segment, or all users **How long**: When did this start? How long has the customer been waiting? **What's been tried**: Any troubleshooting or workarounds attempted **Why escalate now**: What makes this need attention beyond normal support Use the "When to Escalate vs. Handle in Support" criteria below to confirm this warrants escalation. 2. Gather Context Pull together relevant information from available sources: **~~support platform**: Related tickets, timeline of communications, previous troubleshooting **~~CRM** (if connected): Account details, key contacts, previous escalations **~~chat**: Internal discussions about this issue, similar reports from other customers **~~project tracker** (if connected): Related bug reports or feature requests, engineering status **~~knowledge base**: Known issues or workarounds, relevant d...

## 원본 문서 구조

- Usage
- Workflow
  - 1. Understand the Issue
  - 2. Gather Context
  - 3. Assess Business Impact
  - 4. Determine Escalation Target
  - 5. Structure Reproduction Steps (for bugs)
  - 6. Generate Escalation Brief
- ESCALATION: [One-line summary]
  - Impact
  - Issue Description
  - What's Been Tried
  - Reproduction Steps
  - Customer Communication
  - What's Needed
  - Supporting Context
  - 7. Offer Next Steps
- When to Escalate vs. Handle in Support
  - Handle in Support When:
  - Escalate When:
- Escalation Tiers
  - L1 → L2 (Support Escalation)
  - L2 → Engineering
  - L2 → Product
  - Any → Security
  - Any → Leadership
- Business Impact Assessment
  - Impact Dimensions
  - Severity Shorthand
- Writing Reproduction Steps
- Follow-up Cadence After Escalation
  - Follow-up Actions
- De-escalation
- Escalation Best Practices

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/customer-support/skills/customer-escalation/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

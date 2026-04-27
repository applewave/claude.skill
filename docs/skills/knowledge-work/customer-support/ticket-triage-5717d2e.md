# ticket-triage

## 요약

Triage and prioritize a support ticket or customer issue. Use when a new ticket comes in and needs categorization, assigning P1-P4 priority, deciding which team should handle it, or checking whether it's a duplicate or known issue before routing.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | customer-support |
| 원본 경로 | `knowledge-work-plugins/customer-support/skills/ticket-triage/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/customer-support/ticket-triage-5717d2e.md` |
| 입력 힌트 | `<ticket or issue description>` |

## 언제 쓰나

Triage and prioritize a support ticket or customer issue. Use when a new ticket comes in and needs categorization, assigning P1-P4 priority, deciding which team should handle it, or checking whether it's a duplicate or known issue before routing.

## 주요 내용

- **사용 방식**: /ticket-triage <ticket text, customer message, or issue description> Examples: `/ticket-triage Customer says their dashboard has been showing a blank page since this morning` `/ticket-triage "I was charged twice for my subscription this month"` `/ticket-triage User can't connect their SSO — getting a 403 error on the callback URL` `/ticket-triage Feature request: they want to export reports as PDF`
- **진행 방식**: 1. Parse the Issue Read the input and extract: **Core problem**: What is the customer actually experiencing? **Symptoms**: What specific behavior or error are they seeing? **Customer context**: Who is this? Any account details, plan level, or history available? **Urgency signals**: Are they blocked? Is this production? How many users affected? **Emotional state**: Frustrated, confused, matter-of-fact, escalating? 2. Categorize and Prioritize Using the category taxonomy and priority framework below: Assign a **primary category** (bug, how-to, feature request, billing, account, integration, security, data, performance) and an optional secondary category Assign a **priority** (P1–P4) based on impact and urgency Identify the **product area** the issue maps to 3. Check for Duplicates and Known Issues Before routing, check available sources: **~~support platform**: Search for similar open or recently resolved tickets **~~knowledge base**: Check for known issues or existing documentation **~...

## 원본 문서 구조

- Usage
- Workflow
  - 1. Parse the Issue
  - 2. Categorize and Prioritize
  - 3. Check for Duplicates and Known Issues
  - 4. Determine Routing
  - 5. Generate Triage Output
- Triage: [One-line issue summary]
  - Issue Summary
  - Key Details
  - Routing Recommendation
  - Suggested Initial Response
  - Internal Notes
  - 6. Offer Next Steps
- Category Taxonomy
  - Category Determination Tips
- Priority Framework
  - P1 — Critical
  - P2 — High
  - P3 — Medium
  - P4 — Low
  - Priority Escalation Triggers
- Routing Rules
- Duplicate Detection
- Auto-Response Templates by Category
  - Bug — Initial Response
  - How-to — Initial Response
  - Feature Request — Initial Response
  - Billing — Initial Response
  - Security — Initial Response
- Triage Best Practices

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/customer-support/skills/ticket-triage/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

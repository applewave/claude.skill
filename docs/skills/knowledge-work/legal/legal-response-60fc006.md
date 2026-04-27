# legal-response

## 요약

Generate a response to a common legal inquiry using configured templates, with built-in escalation checks for situations that shouldn't use a templated reply. Use when responding to data subject requests, litigation hold notices, vendor legal questions, NDA requests from business teams, or subpoenas.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | legal |
| 원본 경로 | `knowledge-work-plugins/legal/skills/legal-response/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/legal/legal-response-60fc006.md` |
| 입력 힌트 | `[inquiry-type]` |

## 언제 쓰나

Generate a response to a common legal inquiry using configured templates, with built-in escalation checks for situations that shouldn't use a templated reply. Use when responding to data subject requests, litigation hold notices, vendor legal questions, NDA requests from business teams, or subpoenas.

## 주요 내용

- **진행 방식**: Step 1: Identify Inquiry Type Accept the inquiry type from the user. If the type is ambiguous, show available categories and ask for clarification. Step 2: Load Template Look for templates in local settings (e.g., `legal.local.md` or a templates directory). **If templates are configured:** Load the appropriate template for the inquiry type Identify required variables (recipient name, dates, specific details) **If no templates are configured:** Inform the user that no templates were found for this inquiry type Offer to help create a template (see Template Creation Guide below) Provide a reasonable default response structure based on the inquiry type Step 3: Check Escalation Triggers Before generating any response, evaluate whether this situation has characteristics that should NOT use a templated response. Universal Escalation Triggers (Apply to All Categories) The matter involves potential litigation or regulatory investigation The inquiry is from a regulator, government agency, or la...

## 원본 문서 구조

- Invocation
- Workflow
  - Step 1: Identify Inquiry Type
  - Step 2: Load Template
  - Step 3: Check Escalation Triggers
    - Universal Escalation Triggers (Apply to All Categories)
    - Data Subject Request Escalation Triggers
    - Discovery Hold Escalation Triggers
    - Vendor Question Escalation Triggers
    - NDA Request Escalation Triggers
    - Subpoena / Legal Process Escalation Triggers
  - Step 4: Gather Specific Details
  - Step 5: Generate Response
    - Customization Guidelines
  - Step 6: Template Creation (If No Template Exists)
- Response Categories
  - 1. Data Subject Requests (DSRs)
  - 2. Discovery Holds (Litigation Holds)
  - 3. Privacy Inquiries
  - 4. Vendor Legal Questions
  - 5. NDA Requests
  - 6. Subpoena / Legal Process
  - 7. Insurance Notifications
- Template Management Methodology
  - Template Organization
  - Template Lifecycle
- Template Creation Guide
  - 1. Define the Use Case
  - 2. Identify Required Elements
  - 3. Define Variables
  - 4. Draft the Template
  - 5. Define Escalation Triggers
  - 6. Add Metadata
  - Template Format
- Template: {{template_name}}
  - Use When

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/legal/skills/legal-response/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

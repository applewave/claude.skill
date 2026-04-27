# triage-nda

## 요약

Rapidly triage an incoming NDA and classify it as GREEN (standard approval), YELLOW (counsel review), or RED (full legal review). Use when a new NDA arrives from sales or business development, when screening for embedded non-solicits, non-competes, or missing carveouts, or when deciding whether an NDA can be signed under standard delegation.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | legal |
| 원본 경로 | `knowledge-work-plugins/legal/skills/triage-nda/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/legal/triage-nda-c489f96.md` |
| 입력 힌트 | `<NDA file or text>` |

## 언제 쓰나

Rapidly triage an incoming NDA and classify it as GREEN (standard approval), YELLOW (counsel review), or RED (full legal review). Use when a new NDA arrives from sales or business development, when screening for embedded non-solicits, non-competes, or missing carveouts, or when deciding whether an NDA can be signed under standard delegation.

## 주요 내용

- **진행 방식**: Step 1: Accept the NDA Accept the NDA in any format: **File upload**: PDF, DOCX, or other document format **URL**: Link to the NDA in a document system **Pasted text**: NDA text pasted directly If no NDA is provided, prompt the user to supply one. Step 2: Load NDA Playbook Look for NDA screening criteria in local settings (e.g., `legal.local.md`). The NDA playbook should define: Mutual vs. unilateral requirements Acceptable term lengths Required carveouts Prohibited provisions Organization-specific requirements **If no NDA playbook is configured:** Proceed with reasonable market-standard defaults Note clearly that defaults are being used Defaults applied: Mutual obligations required (unless the organization is only disclosing) Term: 2-3 years standard, up to 5 years for trade secrets Standard carveouts required: independently developed, publicly available, rightfully received from third party, required by law No non-solicitation or non-compete provisions No residuals clause (or narrow...

## 원본 문서 구조

- Invocation
- Workflow
  - Step 1: Accept the NDA
  - Step 2: Load NDA Playbook
  - Step 3: Quick Screen
    - 1. Agreement Structure
    - 2. Definition of Confidential Information
    - 3. Obligations of Receiving Party
    - 4. Standard Carveouts
    - 5. Permitted Disclosures
    - 6. Term and Duration
    - 7. Return and Destruction
    - 8. Remedies
    - 9. Problematic Provisions to Flag
    - 10. Governing Law and Jurisdiction
  - Step 4: Classify
    - GREEN -- Standard Approval
    - YELLOW -- Counsel Review Needed
    - RED -- Significant Issues
  - Step 5: Generate Triage Report
- NDA Triage Report
- Screening Results
- Issues Found
  - [Issue 1 -- YELLOW/RED]
- Recommendation
- Next Steps
  - Step 6: Routing Suggestion
- Common NDA Issues and Standard Positions
  - Issue: Overbroad Definition of Confidential Information
  - Issue: Missing Independent Development Carveout
  - Issue: Non-Solicitation of Employees
  - Issue: Broad Residuals Clause
  - Issue: Perpetual Confidentiality Obligation
- Notes

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/legal/skills/triage-nda/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# review-contract

## 요약

Review a contract against your organization's negotiation playbook — flag deviations, generate redlines, provide business impact analysis. Use when reviewing vendor or customer agreements, when you need clause-by-clause analysis against standard positions, or when preparing a negotiation strategy with prioritized redlines and fallback positions.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | legal |
| 원본 경로 | `knowledge-work-plugins/legal/skills/review-contract/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/legal/review-contract-b33cd7d.md` |
| 입력 힌트 | `<contract file or text>` |

## 언제 쓰나

Review a contract against your organization's negotiation playbook — flag deviations, generate redlines, provide business impact analysis. Use when reviewing vendor or customer agreements, when you need clause-by-clause analysis against standard positions, or when preparing a negotiation strategy with prioritized redlines and fallback positions.

## 주요 내용

- **진행 방식**: Step 1: Accept the Contract Accept the contract in any of these formats: **File upload**: PDF, DOCX, or other document format **URL**: Link to a contract in your CLM, cloud storage (e.g., Box, Egnyte, SharePoint), or other document system **Pasted text**: Contract text pasted directly into the conversation If no contract is provided, prompt the user to supply one. Step 2: Gather Context Ask the user for context before beginning the review: **Which side are you on?** (vendor/supplier, customer/buyer, licensor, licensee, partner -- or other) **Deadline**: When does this need to be finalized? (Affects prioritization of issues) **Focus areas**: Any specific concerns? (e.g., "data protection is critical", "we need flexibility on term", "IP ownership is the key issue") **Deal context**: Any relevant business context? (e.g., deal size, strategic importance, existing relationship) If the user provides partial context, proceed with what you have and note assumptions. Step 3: Load the Playbook...
- **산출물**: Structure the output as:

## 원본 문서 구조

- Invocation
- Workflow
  - Step 1: Accept the Contract
  - Step 2: Gather Context
  - Step 3: Load the Playbook
  - Step 4: Clause-by-Clause Analysis
    - Detailed Clause Guidance
  - Step 5: Flag Deviations
    - GREEN -- Acceptable
    - YELLOW -- Negotiate
    - RED -- Escalate
  - Step 6: Generate Redline Suggestions
    - Redline Generation Best Practices
    - Redline Format
  - Step 7: Business Impact Summary
    - Negotiation Priority Framework
  - Step 8: CLM Routing (If Connected)
- Output Format
- Contract Review Summary
- Key Findings
- Clause-by-Clause Analysis
  - [Clause Category] -- [GREEN/YELLOW/RED]
- Negotiation Strategy
- Next Steps
- Notes

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/legal/skills/review-contract/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

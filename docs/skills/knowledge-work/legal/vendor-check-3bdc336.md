# vendor-check

## 요약

Check the status of existing agreements with a vendor across all connected systems — CLM, CRM, email, and document storage — with gap analysis and upcoming deadlines. Use when onboarding or renewing a vendor, when you need a consolidated view of what's signed and what's missing (MSA, DPA, SOW), or when checking for approaching expirations and surviving obligations.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | legal |
| 원본 경로 | `knowledge-work-plugins/legal/skills/vendor-check/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/legal/vendor-check-3bdc336.md` |
| 입력 힌트 | `[vendor name]` |

## 언제 쓰나

Check the status of existing agreements with a vendor across all connected systems — CLM, CRM, email, and document storage — with gap analysis and upcoming deadlines. Use when onboarding or renewing a vendor, when you need a consolidated view of what's signed and what's missing (MSA, DPA, SOW), or when checking for approaching expirations and surviving obligations.

## 주요 내용

- **진행 방식**: Step 1: Identify the Vendor Accept the vendor name from the user. Handle common variations: Full legal name vs. trade name (e.g., "Alphabet Inc." vs. "Google") Abbreviations (e.g., "AWS" vs. "Amazon Web Services") Parent/subsidiary relationships Ask the user to clarify if the vendor name is ambiguous. Step 2: Search Connected Systems Search for the vendor across all available connected systems, in priority order: CLM (Contract Lifecycle Management) -- If Connected Search for all contracts involving the vendor: Active agreements Expired agreements (last 3 years) Agreements in negotiation or pending signature Amendments and addenda CRM -- If Connected Search for the vendor/account record: Account status and relationship type Associated opportunities or deals Contact information for vendor's legal/contracts team Email -- If Connected Search for recent relevant correspondence: Contract-related emails (last 6 months) NDA or agreement attachments Negotiation threads Documents (e.g., Box, Eg...

## 원본 문서 구조

- Invocation
- Workflow
  - Step 1: Identify the Vendor
  - Step 2: Search Connected Systems
    - CLM (Contract Lifecycle Management) -- If Connected
    - CRM -- If Connected
    - Email -- If Connected
    - Documents (e.g., Box, Egnyte, SharePoint) -- If Connected
    - Chat (e.g., Slack, Teams) -- If Connected
  - Step 3: Compile Agreement Status
  - Step 4: Gap Analysis
- Agreement Coverage
  - Step 5: Generate Report
- Vendor Agreement Status: [Vendor Name]
- Relationship Overview
- Agreement Summary
  - [Agreement Type 1] -- [Status]
  - [Agreement Type 2] -- [Status]
- Gap Analysis
- Upcoming Actions
- Notes
  - Step 6: Handle Missing Sources
- Notes

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/legal/skills/vendor-check/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

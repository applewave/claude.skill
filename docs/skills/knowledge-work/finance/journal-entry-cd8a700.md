# journal-entry

## 요약

Prepare journal entries with proper debits, credits, and supporting detail. Use when booking month-end accruals (AP, payroll, prepaid), recording depreciation or amortization, posting revenue recognition or deferred revenue adjustments, or documenting an entry for audit review.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | finance |
| 원본 경로 | `knowledge-work-plugins/finance/skills/journal-entry/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/finance/journal-entry-cd8a700.md` |
| 입력 힌트 | `<entry type> [period]` |

## 언제 쓰나

Prepare journal entries with proper debits, credits, and supporting detail. Use when booking month-end accruals (AP, payroll, prepaid), recording depreciation or amortization, posting revenue recognition or deferred revenue adjustments, or documenting an entry for audit review.

## 주요 내용

- **사용 방식**: /je <type> <period> Arguments `type` — The journal entry type. One of: `ap-accrual` — Accounts payable accruals for goods/services received but not yet invoiced `fixed-assets` — Depreciation and amortization entries for fixed assets and intangibles `prepaid` — Amortization of prepaid expenses (insurance, software, rent, etc.) `payroll` — Payroll accruals including salaries, benefits, taxes, and bonus accruals `revenue` — Revenue recognition entries including deferred revenue adjustments `period` — The accounting period (e.g., `2024-12`, `2024-Q4`, `2024`)
- **진행 방식**: 1. Gather Source Data If ~~erp or ~~data warehouse is connected: Pull the trial balance for the specified period Pull subledger detail for the relevant accounts Pull prior period entries of the same type for reference Identify the current GL balances for affected accounts If no data source is connected: > Connect ~~erp or ~~data warehouse to pull GL data automatically. You can also paste trial balance data or upload a spreadsheet. Prompt the user to provide: Trial balance or GL balances for affected accounts Subledger detail or supporting schedules Prior period entries for reference (optional) 2. Calculate the Entry Based on the JE type: **AP Accrual:** Identify goods/services received but not invoiced by period end Calculate accrual amounts from PO receipts, contracts, or estimates Debit: Expense accounts (or asset accounts for capitalizable items) Credit: Accrued liabilities **Fixed Assets:** Pull the fixed asset register or depreciation schedule Calculate period depreciation by ass...

## 원본 문서 구조

- Usage
  - Arguments
- Workflow
  - 1. Gather Source Data
  - 2. Calculate the Entry
  - 3. Generate the Journal Entry
  - 4. Review Checklist
  - 5. Output

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/finance/skills/journal-entry/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

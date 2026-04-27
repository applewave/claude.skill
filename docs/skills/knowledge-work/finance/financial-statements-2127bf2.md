# financial-statements

## 요약

Generate financial statements (income statement, balance sheet, cash flow) with period-over-period comparison and variance analysis. Use when preparing a monthly or quarterly P&L, closing the books and need to flag material variances, comparing actuals to budget, building a financial summary for leadership review, or looking up GAAP presentation requirements and period-end adjustments.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | finance |
| 원본 경로 | `knowledge-work-plugins/finance/skills/financial-statements/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/finance/financial-statements-2127bf2.md` |
| 입력 힌트 | `<frequency> <period>` |

## 언제 쓰나

Generate financial statements (income statement, balance sheet, cash flow) with period-over-period comparison and variance analysis. Use when preparing a monthly or quarterly P&L, closing the books and need to flag material variances, comparing actuals to budget, building a financial summary for leadership review, or looking up GAAP presentation requirements and period-end adjustments.

## 주요 내용

- **사용 방식**: /financial-statements <period-type> <period> Arguments `period-type` — The reporting period type: `monthly` — Single month P&L with prior month and prior year month comparison `quarterly` — Quarter P&L with prior quarter and prior year quarter comparison `annual` — Full year P&L with prior year comparison `ytd` — Year-to-date P&L with prior year YTD comparison `period` — The period to report (e.g., `2024-12`, `2024-Q4`, `2024`)
- **진행 방식**: 1. Gather Financial Data If ~~erp or ~~data warehouse is connected: Pull trial balance or income statement data for the specified period Pull comparison period data (prior period, prior year, budget/forecast) Pull account hierarchy and groupings for presentation If no data source is connected: > Connect ~~erp or ~~data warehouse to pull financial data automatically. You can also paste trial balance data, upload a spreadsheet, or provide income statement data for analysis. Prompt the user to provide: Current period revenue and expense data (by account or category) Comparison period data (prior period, prior year, and/or budget) Any known adjustments or reclassifications 2. Generate Income Statement Present in standard multi-column format: INCOME STATEMENT Period: [Period description] (in thousands, unless otherwise noted) Current Prior Variance Variance Budget Budget Period Period ($) (%) Amount Var ($) -------- -------- -------- -------- -------- --------

## 원본 문서 구조

- Usage
  - Arguments
- Workflow
  - 1. Gather Financial Data
  - 2. Generate Income Statement
  - 3. Variance Analysis
    - Variance Calculation
    - Materiality Thresholds
    - Variance Decomposition
    - Investigation and Narrative
  - 4. Key Metrics Summary
  - 5. Material Variance Summary
  - 6. Output
- GAAP Presentation Requirements
  - Income Statement (ASC 220 / IAS 1)
  - Balance Sheet (ASC 210 / IAS 1)
  - Cash Flow Statement (ASC 230 / IAS 7)
- Balance Sheet Reference Format
- Cash Flow Statement Reference Format (Indirect Method)
- Common Adjustments and Reclassifications
  - Period-End Adjustments
  - Reclassifications

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/finance/skills/financial-statements/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# sox-testing

## 요약

Generate SOX sample selections, testing workpapers, and control assessments. Use when planning quarterly or annual SOX 404 testing, pulling a sample for a control (revenue, P2P, ITGC, close), building a testing workpaper template, or evaluating and classifying a control deficiency.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | finance |
| 원본 경로 | `knowledge-work-plugins/finance/skills/sox-testing/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/finance/sox-testing-2678a53.md` |
| 입력 힌트 | `<control area> [period]` |

## 언제 쓰나

Generate SOX sample selections, testing workpapers, and control assessments. Use when planning quarterly or annual SOX 404 testing, pulling a sample for a control (revenue, P2P, ITGC, close), building a testing workpaper template, or evaluating and classifying a control deficiency.

## 주요 내용

- **사용 방식**: /sox <control-area> <period> Arguments `control-area` — The control area to test: `revenue-recognition` — Revenue cycle controls (order-to-cash) `procure-to-pay` or `p2p` — Procurement and AP controls (purchase-to-pay) `payroll` — Payroll processing and compensation controls `financial-close` — Period-end close and reporting controls `treasury` — Cash management and treasury controls `fixed-assets` — Capital asset lifecycle controls `inventory` — Inventory valuation and management controls `itgc` — IT general controls (access, change management, operations) `entity-level` — Entity-level and monitoring controls `journal-entries` — Journal entry processing controls Any specific control ID or name `period` — The testing period (e.g., `2024-Q4`, `2024`, `2024-H2`)
- **진행 방식**: 1. Identify Controls to Test Based on the control area, identify the key controls. Present the control matrix: **Control types:** **Automated:** System-enforced controls with no manual intervention **Manual:** Controls performed by personnel with judgment **IT-dependent manual:** Manual controls that rely on system-generated data **Assertions (CEAVOP):** **C**ompleteness — All transactions are recorded **E**xistence/Occurrence — Transactions actually occurred **A**ccuracy — Amounts are correctly recorded **V**aluation — Assets/liabilities are properly valued **O**bligations/Rights — Entity has rights to assets, obligations for liabilities **P**resentation/Disclosure — Properly classified and disclosed 2. Determine Sample Size Calculate sample sizes based on control frequency and risk: Adjust for: **Risk level:** Higher risk controls require larger samples **Prior year results:** Controls with prior deficiencies need larger samples **Reliance:** Controls relied upon by external auditor...

## 원본 문서 구조

- Usage
  - Arguments
- Workflow
  - 1. Identify Controls to Test
  - 2. Determine Sample Size
  - 3. Generate Sample Selection
  - 4. Create Testing Workpaper
  - 5. Provide Common Control Templates
  - 6. Document Control Assessment
  - 7. Output

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/finance/skills/sox-testing/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# validate-data

## 요약

QA an analysis before sharing -- methodology, accuracy, and bias checks. Use when reviewing an analysis before a stakeholder presentation, spot-checking calculations and aggregation logic, verifying a SQL query's results look right, or assessing whether conclusions are actually supported by the data.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | data |
| 원본 경로 | `knowledge-work-plugins/data/skills/validate-data/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/data/validate-data-6c96bf2.md` |
| 입력 힌트 | `<analysis to review>` |

## 언제 쓰나

QA an analysis before sharing -- methodology, accuracy, and bias checks. Use when reviewing an analysis before a stakeholder presentation, spot-checking calculations and aggregation logic, verifying a SQL query's results look right, or assessing whether conclusions are actually supported by the data.

## 주요 내용

- **사용 방식**: /validate-data <analysis to review> The analysis can be: A document or report in the conversation A file (markdown, notebook, spreadsheet) SQL queries and their results Charts and their underlying data A description of methodology and findings
- **진행 방식**: 1. Review Methodology and Assumptions Examine: **Question framing**: Is the analysis answering the right question? Could the question be interpreted differently? **Data selection**: Are the right tables/datasets being used? Is the time range appropriate? **Population definition**: Is the analysis population correctly defined? Are there unintended exclusions? **Metric definitions**: Are metrics defined clearly and consistently? Do they match how stakeholders understand them? **Baseline and comparison**: Is the comparison fair? Are time periods, cohort sizes, and contexts comparable? 2. Run the Pre-Delivery QA Checklist Work through the checklist below — data quality, calculation, reasonableness, and presentation checks. 3. Check for Common Analytical Pitfalls Systematically review against the detailed pitfall catalog below (join explosion, survivorship bias, incomplete period comparison, denominator shifting, average of averages, timezone mismatches, selection bias). 4. Verify Calculat...

## 원본 문서 구조

- Usage
- Workflow
  - 1. Review Methodology and Assumptions
  - 2. Run the Pre-Delivery QA Checklist
  - 3. Check for Common Analytical Pitfalls
  - 4. Verify Calculations and Aggregations
  - 5. Assess Visualizations
  - 6. Evaluate Narrative and Conclusions
  - 7. Suggest Improvements
  - 8. Generate Confidence Assessment
- Output Format
- Validation Report
  - Overall Assessment: [Ready to share | Share with caveats | Needs revision]
  - Methodology Review
  - Issues Found
  - Calculation Spot-Checks
  - Visualization Review
  - Suggested Improvements
  - Required Caveats for Stakeholders
- Pre-Delivery QA Checklist
  - Data Quality Checks
  - Calculation Checks
  - Reasonableness Checks
  - Presentation Checks
- Common Data Analysis Pitfalls
  - Join Explosion
  - Survivorship Bias
  - Incomplete Period Comparison
  - Denominator Shifting
  - Average of Averages
  - Timezone Mismatches
  - Selection Bias in Segmentation
  - Other Statistical Traps
- Result Sanity Checking
  - Magnitude Checks
  - Cross-Validation Techniques

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/data/skills/validate-data/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

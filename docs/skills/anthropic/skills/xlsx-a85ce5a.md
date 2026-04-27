# xlsx

## 요약

Use this skill any time a spreadsheet file is the primary input or output. This means any task where the user wants to: open, read, edit, or fix an existing .xlsx, .xlsm, .csv, or .tsv file (e.g., adding columns, computing formulas, formatting, charting, cleaning messy data); create a new spreadsheet from scratch or from other data sources; or convert between tabular file formats. Trigger especially when the user references a spreadsheet file by name or path — even casually (like \"the xlsx in my downloads\") — and wants something done to it or produced from it. Also trigger for cleaning or restructuring messy tabular data files (malformed rows, misplaced headers, junk data) into proper spreadsheets. The deliverable must be a spreadsheet file. Do NOT trigger when the primary deliverable is a Word document, HTML report, standalone Python script, database pipeline, or Google Sheets API in...

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Anthropic Skills |
| 영역 | skills |
| 원본 경로 | `skills/skills/xlsx/SKILL.md` |
| 상세 파일 | `docs/skills/anthropic/skills/xlsx-a85ce5a.md` |
| 라이선스 | Proprietary. LICENSE.txt has complete terms |

## 언제 쓰나

Use this skill any time a spreadsheet file is the primary input or output. This means any task where the user wants to: open, read, edit, or fix an existing .xlsx, .xlsm, .csv, or .tsv file (e.g., adding columns, computing formulas, formatting, charting, cleaning messy data); create a new spreadsheet from scratch or from other data sources; or convert between tabular file formats. Trigger especially when the user references a spreadsheet file by name or path — even casually (like \"the xlsx in my downloads\") — and wants something done to it or produced from it. Also trigger for cleaning or restructuring messy tabular data files (malformed rows, misplaced headers, junk data) into proper spreadsheets. The deliverable must be a spreadsheet file. Do NOT trigger when the primary deliverable is a Word document, HTML report, standalone Python script, database pipeline, or Google Sheets API integration, even if tabular data is involved.

## 주요 내용

- 원본 설명과 문서 구조를 기준으로 필요한 시점에 참조합니다.

## 원본 문서 구조

- All Excel files
  - Professional Font
  - Zero Formula Errors
  - Preserve Existing Templates (when updating templates)
- Financial models
  - Color Coding Standards
    - Industry-Standard Color Conventions
  - Number Formatting Standards
    - Required Format Rules
  - Formula Construction Rules
    - Assumptions Placement
    - Formula Error Prevention
    - Documentation Requirements for Hardcodes
- Overview
- Important Requirements
- Reading and analyzing data
  - Data analysis with pandas
- Excel File Workflows
- CRITICAL: Use Formulas, Not Hardcoded Values
  - ❌ WRONG - Hardcoding Calculated Values
  - ✅ CORRECT - Using Excel Formulas
- Common Workflow
  - Creating new Excel files
  - Editing existing Excel files
- Recalculating formulas
- Formula Verification Checklist
  - Essential Verification
  - Common Pitfalls
  - Formula Testing Strategy
  - Interpreting scripts/recalc.py Output
- Best Practices
  - Library Selection
  - Working with openpyxl
  - Working with pandas
- Code Style Guidelines

## 관리 메모

- 이 문서는 원본 `skills/skills/xlsx/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

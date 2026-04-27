# instrument-data-to-allotrope

## 요약

Convert laboratory instrument output files (PDF, CSV, Excel, TXT) to Allotrope Simple Model (ASM) JSON format or flattened 2D CSV. Use this skill when scientists need to standardize instrument data for LIMS systems, data lakes, or downstream analysis. Supports auto-detection of instrument types. Outputs include full ASM JSON, flattened CSV for easy import, and exportable Python code for data engineers. Common triggers include converting instrument files, standardizing lab data, preparing data for upload to LIMS/ELN systems, or generating parser code for production pipelines.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | bio-research |
| 원본 경로 | `knowledge-work-plugins/bio-research/skills/instrument-data-to-allotrope/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/bio-research/instrument-data-to-allotrope-3fbcdd4.md` |

## 언제 쓰나

Convert laboratory instrument output files (PDF, CSV, Excel, TXT) to Allotrope Simple Model (ASM) JSON format or flattened 2D CSV. Use this skill when scientists need to standardize instrument data for LIMS systems, data lakes, or downstream analysis. Supports auto-detection of instrument types. Outputs include full ASM JSON, flattened CSV for easy import, and exportable Python code for data engineers. Common triggers include converting instrument files, standardizing lab data, preparing data for upload to LIMS/ELN systems, or generating parser code for production pipelines.

## 주요 내용

- **사용 방식**: Example 1: Vi-CELL BLU file User: "Convert this cell counting data to Allotrope format" [uploads viCell_Results.xlsx] Claude: Detects Vi-CELL BLU (95% confidence) Converts using allotropy native parser Outputs: viCell_Results_asm.json (full ASM) viCell_Results_flat.csv (2D format) viCell_parser.py (exportable code) Example 2: Request for code handoff User: "I need to give our data engineer code to parse NanoDrop files" Claude: Generates self-contained Python script Includes sample input/output Documents all assumptions Provides Jupyter notebook version Example 3: LIMS-ready flattened output User: "Convert this ELISA data to a CSV I can upload to our LIMS" Claude: Parses plate reader data Generates flattened CSV with columns: sample_identifier, well_position, measurement_value, measurement_unit instrument_serial_number, analysis_datetime, assay_type Validates against common LIMS import r...
- **진행 방식**: **Detect instrument type** from file contents (auto-detect or user-specified) **Parse file** using allotropy library (native) or flexible fallback parser **Generate outputs**: ASM JSON (full semantic structure) Flattened CSV (2D tabular format) Python parser code (for data engineer handoff) **Deliver** files with summary and usage instructions > **When Uncertain:** If you're unsure how to map a field to ASM (e.g., is this raw data or calculated? device setting or environmental condition?), ask the user for clarification. Refer to `references/field_classification_guide.md` for guidance, but when ambiguity remains, confirm with the user rather than guessing.
- **산출물**: **ASM JSON (default)** - Full semantic structure with ontology URIs Best for: LIMS systems expecting ASM, data lakes, long-term archival Validates against Allotrope schemas **Flattened CSV** - 2D tabular representation Best for: Quick analysis, Excel users, systems without JSON support Each measurement becomes one row with metadata repeated **Both** - Generate both formats for maximum flexibility

## 원본 문서 구조

- Workflow Overview
- Quick Start
- Output Format Selection
- Calculated Data Handling
- Validation
- Supported Instruments
- Detection & Parsing Strategy
  - Tier 1: Native allotropy parsing (PREFERRED)
  - Tier 2: Flexible fallback parsing
  - Tier 3: PDF extraction
- Pre-Parsing Checklist
- Common Mistakes to Avoid
- Code Export for Data Engineers
- File Structure
- Usage Examples
  - Example 1: Vi-CELL BLU file
  - Example 2: Request for code handoff
  - Example 3: LIMS-ready flattened output
- Implementation Notes
  - Installing allotropy
  - Handling parse failures
  - ASM Schema Validation

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/bio-research/skills/instrument-data-to-allotrope/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

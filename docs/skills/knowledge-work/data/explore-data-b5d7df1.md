# explore-data

## 요약

Profile and explore a dataset to understand its shape, quality, and patterns. Use when encountering a new table or file, checking null rates and column distributions, spotting data quality issues like duplicates or suspicious values, or deciding which dimensions and metrics to analyze.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | data |
| 원본 경로 | `knowledge-work-plugins/data/skills/explore-data/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/data/explore-data-b5d7df1.md` |
| 입력 힌트 | `<table or file>` |

## 언제 쓰나

Profile and explore a dataset to understand its shape, quality, and patterns. Use when encountering a new table or file, checking null rates and column distributions, spotting data quality issues like duplicates or suspicious values, or deciding which dimensions and metrics to analyze.

## 주요 내용

- **사용 방식**: /explore-data <table_name or file>
- **진행 방식**: 1. Access the Data **If a data warehouse MCP server is connected:** Resolve the table name (handle schema prefixes, suggest matches if ambiguous) Query table metadata: column names, types, descriptions if available Run profiling queries against the live data **If a file is provided (CSV, Excel, Parquet, JSON):** Read the file and load into a working dataset Infer column types from the data **If neither:** Ask the user to provide a table name (with their warehouse connected) or upload a file If they describe a table schema, provide guidance on what profiling queries to run 2. Understand Structure Before analyzing any data, understand its structure: **Table-level questions:** How many rows and columns? What is the grain (one row per what)? What is the primary key? Is it unique? When was the data last updated? How far back does the data go? **Column classification** — categorize each column as one of: **Identifier**: Unique keys, foreign keys, entity IDs **Dimension**: Categorical attrib...

## 원본 문서 구조

- Usage
- Workflow
  - 1. Access the Data
  - 2. Understand Structure
  - 3. Generate Data Profile
  - 4. Identify Data Quality Issues
  - 5. Discover Relationships and Patterns
  - 6. Suggest Interesting Dimensions and Metrics
  - 7. Recommend Follow-Up Analyses
- Output Format
- Data Profile: [table_name]
  - Overview
  - Column Details
  - Data Quality Issues
  - Recommended Explorations
- Quality Assessment Framework
  - Completeness Score
  - Consistency Checks
  - Accuracy Indicators
  - Timeliness Assessment
- Pattern Discovery Techniques
  - Distribution Analysis
  - Temporal Patterns
  - Segmentation Discovery
  - Correlation Exploration
- Schema Understanding and Documentation
  - Schema Documentation Template
- Table: [schema.table_name]
  - Key Columns
  - Relationships
  - Known Issues
  - Common Query Patterns
  - Schema Exploration Queries
  - Lineage and Dependencies
- Tips

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/data/skills/explore-data/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

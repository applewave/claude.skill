# write-query

## 요약

Write optimized SQL for your dialect with best practices. Use when translating a natural-language data need into SQL, building a multi-CTE query with joins and aggregations, optimizing a query against a large partitioned table, or getting dialect-specific syntax for Snowflake, BigQuery, Postgres, etc.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | data |
| 원본 경로 | `knowledge-work-plugins/data/skills/write-query/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/data/write-query-d0ea7ca.md` |
| 입력 힌트 | `<description of what data you need>` |

## 언제 쓰나

Write optimized SQL for your dialect with best practices. Use when translating a natural-language data need into SQL, building a multi-CTE query with joins and aggregations, optimizing a query against a large partitioned table, or getting dialect-specific syntax for Snowflake, BigQuery, Postgres, etc.

## 주요 내용

- **사용 방식**: /write-query <description of what data you need>
- **진행 방식**: 1. Understand the Request Parse the user's description to identify: **Output columns**: What fields should the result include? **Filters**: What conditions limit the data (time ranges, segments, statuses)? **Aggregations**: Are there GROUP BY operations, counts, sums, averages? **Joins**: Does this require combining multiple tables? **Ordering**: How should results be sorted? **Limits**: Is there a top-N or sample requirement? 2. Determine SQL Dialect If the user's SQL dialect is not already known, ask which they use: **PostgreSQL** (including Aurora, RDS, Supabase, Neon) **Snowflake** **BigQuery** (Google Cloud) **Redshift** (Amazon) **Databricks SQL** **MySQL** (including Aurora MySQL, PlanetScale) **SQL Server** (Microsoft) **DuckDB** **SQLite** **Other** (ask for specifics) Remember the dialect for future queries in the same session. 3. Discover Schema (If Warehouse Connected) If a data warehouse MCP server is connected: Search for relevant tables based on the user's description I...

## 원본 문서 구조

- Usage
- Workflow
  - 1. Understand the Request
  - 2. Determine SQL Dialect
  - 3. Discover Schema (If Warehouse Connected)
  - 4. Write the Query
  - 5. Present the Query
  - 6. Offer to Execute
- Examples
- Tips

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/data/skills/write-query/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

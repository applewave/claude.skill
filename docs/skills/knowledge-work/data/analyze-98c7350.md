# analyze

## 요약

Answer data questions -- from quick lookups to full analyses. Use when looking up a single metric, investigating what's driving a trend or drop, comparing segments over time, or preparing a formal data report for stakeholders.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | data |
| 원본 경로 | `knowledge-work-plugins/data/skills/analyze/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/data/analyze-98c7350.md` |
| 입력 힌트 | `<question>` |

## 언제 쓰나

Answer data questions -- from quick lookups to full analyses. Use when looking up a single metric, investigating what's driving a trend or drop, comparing segments over time, or preparing a formal data report for stakeholders.

## 주요 내용

- **사용 방식**: /analyze <natural language question>
- **진행 방식**: 1. Understand the Question Parse the user's question and determine: **Complexity level**: **Quick answer**: Single metric, simple filter, factual lookup (e.g., "How many users signed up last week?") **Full analysis**: Multi-dimensional exploration, trend analysis, comparison (e.g., "What's driving the drop in conversion rate?") **Formal report**: Comprehensive investigation with methodology, caveats, and recommendations (e.g., "Prepare a quarterly business review of our subscription metrics") **Data requirements**: Which tables, metrics, dimensions, and time ranges are needed **Output format**: Number, table, chart, narrative, or combination 2. Gather Data **If a data warehouse MCP server is connected:** Explore the schema to find relevant tables and columns Write SQL query(ies) to extract the needed data Execute the query and retrieve results If the query fails, debug and retry (check column names, table references, syntax for the specific dialect) If results look unexpected, run san...

## 원본 문서 구조

- Usage
- Workflow
  - 1. Understand the Question
  - 2. Gather Data
  - 3. Analyze
  - 4. Validate Before Presenting
  - 5. Present Findings
  - 6. Visualize Where Helpful
- Examples
- Tips

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/data/skills/analyze/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

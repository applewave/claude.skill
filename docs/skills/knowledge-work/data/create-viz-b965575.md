# create-viz

## 요약

Create publication-quality visualizations with Python. Use when turning query results or a DataFrame into a chart, selecting the right chart type for a trend or comparison, generating a plot for a report or presentation, or needing an interactive chart with hover and zoom.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | data |
| 원본 경로 | `knowledge-work-plugins/data/skills/create-viz/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/data/create-viz-b965575.md` |
| 입력 힌트 | `<data source> [chart type]` |

## 언제 쓰나

Create publication-quality visualizations with Python. Use when turning query results or a DataFrame into a chart, selecting the right chart type for a trend or comparison, generating a plot for a report or presentation, or needing an interactive chart with hover and zoom.

## 주요 내용

- **사용 방식**: /create-viz <data source> [chart type] [additional instructions]
- **진행 방식**: 1. Understand the Request Determine: **Data source**: Query results, pasted data, CSV/Excel file, or data to be queried **Chart type**: Explicitly requested or needs to be recommended **Purpose**: Exploration, presentation, report, dashboard component **Audience**: Technical team, executives, external stakeholders 2. Get the Data **If data warehouse is connected and data needs querying:** Write and execute the query Load results into a pandas DataFrame **If data is pasted or uploaded:** Parse the data into a pandas DataFrame Clean and prepare as needed (type conversions, null handling) **If data is from a previous analysis in the conversation:** Reference the existing data 3. Select Chart Type If the user didn't specify a chart type, recommend one based on the data and question: Explain the recommendation briefly if the user didn't specify. 4. Generate the Visualization Write Python code using one of these libraries based on the need: **matplotlib + seaborn**: Best for static, publica...

## 원본 문서 구조

- Usage
- Workflow
  - 1. Understand the Request
  - 2. Get the Data
  - 3. Select Chart Type
  - 4. Generate the Visualization
  - 5. Apply Design Best Practices
  - 6. Save and Present
- Examples
- Tips

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/data/skills/create-viz/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

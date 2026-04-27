# build-dashboard

## 요약

Build an interactive HTML dashboard with charts, filters, and tables. Use when creating an executive overview with KPI cards, turning query results into a shareable self-contained report, building a team monitoring snapshot, or needing multiple charts with filters in one browser-openable file.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | data |
| 원본 경로 | `knowledge-work-plugins/data/skills/build-dashboard/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/data/build-dashboard-2f51c3e.md` |
| 입력 힌트 | `<description> [data source]` |

## 언제 쓰나

Build an interactive HTML dashboard with charts, filters, and tables. Use when creating an executive overview with KPI cards, turning query results into a shareable self-contained report, building a team monitoring snapshot, or needing multiple charts with filters in one browser-openable file.

## 주요 내용

- **사용 방식**: /build-dashboard <description of dashboard> [data source]
- **진행 방식**: 1. Understand the Dashboard Requirements Determine: **Purpose**: Executive overview, operational monitoring, deep-dive analysis, team reporting **Audience**: Who will use this dashboard? **Key metrics**: What numbers matter most? **Dimensions**: What should users be able to filter or slice by? **Data source**: Live query, pasted data, CSV file, or sample data 2. Gather the Data **If data warehouse is connected:** Query the necessary data Embed the results as JSON within the HTML file **If data is pasted or uploaded:** Parse and clean the data Embed as JSON in the dashboard **If working from a description without data:** Create a realistic sample dataset matching the described schema Note in the dashboard that it uses sample data Provide instructions for swapping in real data 3. Design the Dashboard Layout Follow a standard dashboard layout pattern: ┌──────────────────────────────────────────────────┐ │ Dashboard Title [Filters ▼] │ ├────────────┬────────────┬────────────┬───────────┤

## 원본 문서 구조

- Usage
- Workflow
  - 1. Understand the Dashboard Requirements
  - 2. Gather the Data
  - 3. Design the Dashboard Layout
  - 4. Build the HTML Dashboard
  - 5. Implement Chart Types
  - 6. Add Interactivity
  - 7. Save and Open
- Base Template
- KPI Card Pattern
- Chart.js Integration
  - Chart Container Pattern
  - Line Chart
  - Bar Chart
  - Doughnut Chart
  - Updating Charts on Filter Change
- Filter and Interactivity Implementation
  - Dropdown Filter
  - Date Range Filter
  - Combined Filter Logic
  - Sortable Table
- CSS Styling for Dashboards
  - Color System
  - Layout
  - KPI Cards
  - Chart Containers
  - Filters
  - Data Table
  - Responsive Design
- Performance Considerations for Large Datasets
  - Data Size Guidelines
  - Pre-Aggregation Pattern
  - Chart Performance
  - DOM Performance
- Examples

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/data/skills/build-dashboard/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# sf-industry-commoncore-flexcard

## 요약

OmniStudio FlexCard creation and validation with 130-point scoring. Use when building at-a-glance UI cards, configuring data source bindings to Integration Procedures, or reviewing existing FlexCard definitions for accessibility and performance. TRIGGER when: user creates FlexCards, configures data sources, designs card layouts, or asks about OmniUiCard metadata. DO NOT TRIGGER when: building OmniScripts (use sf-industry-commoncore-omniscript), creating Integration Procedures (use sf-industry-commoncore-integration-procedure), or analyzing dependencies (use sf-industry-commoncore-omnistudio-analyze).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-industry-commoncore-flexcard/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-industry-commoncore-flexcard-adf590e.md` |
| 라이선스 | MIT |

## 언제 쓰나

OmniStudio FlexCard creation and validation with 130-point scoring. Use when building at-a-glance UI cards, configuring data source bindings to Integration Procedures, or reviewing existing FlexCard definitions for accessibility and performance. TRIGGER when: user creates FlexCards, configures data sources, designs card layouts, or asks about OmniUiCard metadata. DO NOT TRIGGER when: building OmniScripts (use sf-industry-commoncore-omniscript), creating Integration Procedures (use sf-industry-commoncore-integration-procedure), or analyzing dependencies (use sf-industry-commoncore-omnistudio-analyze).

## 주요 내용

- **진행 방식**: Phase 1: Requirements Gathering Before building, clarify these with the stakeholder: Phase 2: Design & Layout Card Layout Options Data Source Configuration Each FlexCard data source connects to an Integration Procedure (or other source type) and maps response fields to display elements. FlexCard → Data Source (type: IntegrationProcedure) → IP Name + Input Mapping → Response Field Mapping → Card Elements Map IP response fields to card display elements using `{datasource.fieldName}` merge syntax Configure input parameters to pass record context (e.g., `{recordId}`) to the IP Set data source order when multiple sources feed the same card Action Button Design Conditional Visibility Show/hide fields based on data values using visibility conditions Show/hide entire card states based on data source results Display empty-state messaging when data source returns no records Phase 3: Generation & Validation Generate the FlexCard definition JSON Validate all data source references resolve to acti...

## 원본 문서 구조

- Core Responsibilities
- Document Map
- CRITICAL: Orchestration Order
- Key Insights
- Workflow (5-Phase Pattern)
  - Phase 1: Requirements Gathering
  - Phase 2: Design & Layout
    - Card Layout Options
    - Data Source Configuration
    - Action Button Design
    - Conditional Visibility
  - Phase 3: Generation & Validation
  - Phase 4: Deployment
  - Phase 5: Testing
- Generation Guardrails
- Scoring Rubric (130 Points)
  - Scoring Breakdown Detail
    - Design & Layout (25 points)
    - Data Binding (20 points)
    - Actions & Navigation (20 points)
    - Styling (20 points)
    - Accessibility (15 points)
    - Testing (15 points)
    - Performance (15 points)
- CLI Commands
- Data Source Binding
  - FlexCard Data Source Configuration
  - Data Source Types
  - Field Mapping from IP Response
  - Input Parameter Mapping
- Cross-Skill Integration
- Edge Cases
- FlexCard vs LWC Decision Guide
- Dependencies
- External References
- License

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-industry-commoncore-flexcard/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

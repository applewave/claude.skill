# sf-industry-commoncore-omniscript

## 요약

OmniStudio OmniScript creation and validation with 120-point scoring. Use when building guided digital experiences, multi-step forms, or interactive processes that orchestrate Integration Procedures and Data Mappers. TRIGGER when: user creates OmniScripts, designs step flows, configures element types, or reviews existing OmniScript configurations. DO NOT TRIGGER when: building FlexCards (use sf-industry-commoncore-flexcard), creating Integration Procedures directly (use sf-industry-commoncore-integration-procedure), or analyzing dependencies (use sf-industry-commoncore-omnistudio-analyze).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-industry-commoncore-omniscript/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-industry-commoncore-omniscript-6f7ce14.md` |
| 라이선스 | MIT |

## 언제 쓰나

OmniStudio OmniScript creation and validation with 120-point scoring. Use when building guided digital experiences, multi-step forms, or interactive processes that orchestrate Integration Procedures and Data Mappers. TRIGGER when: user creates OmniScripts, designs step flows, configures element types, or reviews existing OmniScript configurations. DO NOT TRIGGER when: building FlexCards (use sf-industry-commoncore-flexcard), creating Integration Procedures directly (use sf-industry-commoncore-integration-procedure), or analyzing dependencies (use sf-industry-commoncore-omnistudio-analyze).

## 주요 내용

- **진행 방식**: Phase 1: Requirements Gathering **Before building, evaluate alternatives**: OmniScripts are best for complex, multi-step guided processes. For simple single-screen data entry, consider Screen Flows. For data display without interaction, consider FlexCards. **Ask the user** to gather: **Type**: The process category (e.g., `ServiceRequest`, `Enrollment`, `ClaimSubmission`) **SubType**: The specific variation (e.g., `NewCase`, `UpdateAddress`, `FileAppeal`) **Language**: Typically `English` unless multi-language support is required **Purpose**: What business process this OmniScript guides the user through **Target org**: Org alias for deployment **Data sources**: Which objects/APIs need to be queried or updated **Then**: Check existing OmniScripts to avoid duplication, identify reusable Integration Procedures or DataRaptors, and map the dependency chain. Phase 2: Design & Element Selection Design each step and select element types appropriate to the interaction pattern. Container Element...

## 원본 문서 구조

- Quick Reference
- Core Responsibilities
- CRITICAL: Orchestration Order
- Key Insights
- Workflow Design (5-Phase Pattern)
  - Phase 1: Requirements Gathering
  - Phase 2: Design & Element Selection
    - Container Elements
    - Input Elements
    - Display Elements
    - Action Elements
    - Logic Elements
  - Phase 3: Generation & Validation
  - Phase 4: Deployment
  - Phase 5: Testing
- Generation Guardrails (MANDATORY)
- Scoring: 120 Points Across 6 Categories
  - Design & Structure (25 points)
  - Data Integration (20 points)
  - Error Handling (20 points)
  - Performance (20 points)
  - User Experience (20 points)
  - Security (15 points)
- CLI Commands
- Cross-Skill Integration
- Edge Cases
- Notes
- License

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-industry-commoncore-omniscript/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

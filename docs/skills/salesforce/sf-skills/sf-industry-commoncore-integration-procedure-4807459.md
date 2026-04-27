# sf-industry-commoncore-integration-procedure

## 요약

OmniStudio Integration Procedure creation and validation with 110-point scoring. Use when building server-side process orchestrations that combine Data Mapper actions, Apex Remote Actions, HTTP callouts, and conditional logic. TRIGGER when: user creates Integration Procedures, adds Data Mapper steps, configures Remote Actions, or reviews existing IP configurations. DO NOT TRIGGER when: building OmniScripts (use sf-industry-commoncore-omniscript), creating Data Mappers directly (use sf-industry-commoncore-datamapper), or analyzing cross-component dependencies (use sf-industry-commoncore-omnistudio-analyze).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-industry-commoncore-integration-procedure/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-industry-commoncore-integration-procedure-4807459.md` |
| 라이선스 | MIT |

## 언제 쓰나

OmniStudio Integration Procedure creation and validation with 110-point scoring. Use when building server-side process orchestrations that combine Data Mapper actions, Apex Remote Actions, HTTP callouts, and conditional logic. TRIGGER when: user creates Integration Procedures, adds Data Mapper steps, configures Remote Actions, or reviews existing IP configurations. DO NOT TRIGGER when: building OmniScripts (use sf-industry-commoncore-omniscript), creating Data Mappers directly (use sf-industry-commoncore-datamapper), or analyzing cross-component dependencies (use sf-industry-commoncore-omnistudio-analyze).

## 주요 내용

- **진행 방식**: Phase 1: Requirements Gathering **Before building, evaluate alternatives**: Sometimes a single DataRaptor, an Apex service, or a Flow is the better choice. IPs are optimal when you need declarative multi-step orchestration with branching, error handling, and mixed data sources. **Ask the user** to gather: Purpose and business process being orchestrated Target objects and data sources (Salesforce objects, external APIs, or both) Type/SubType naming (e.g., `Type=OrderProcessing`, `SubType=Standard`) Target org alias for deployment **Then**: Check existing IPs via CLI query (see CLI Commands below), identify reusable DataRaptors/Data Mappers, and review dependent components with sf-industry-commoncore-omnistudio-analyze. Phase 2: Design & Element Selection **Naming Convention**: `[Type]_[SubType]` using PascalCase. Element names within the IP should describe their action clearly (e.g., `GetAccountDetails`, `ValidateInput`, `CreateOrderRecord`). **Data Flow**: Design the element chain so...

## 원본 문서 구조

- Quick Reference
- Core Responsibilities
- CRITICAL: Orchestration Order
- Key Insights
- Workflow Design (5-Phase Pattern)
  - Phase 1: Requirements Gathering
  - Phase 2: Design & Element Selection
  - Phase 3: Generation & Validation
  - Generation Guardrails (MANDATORY)
  - Phase 4: Deployment
  - Phase 5: Testing
- Scoring Breakdown
  - Design & Structure (20 points)
  - Data Operations (25 points)
  - Error Handling (20 points)
  - Performance (20 points)
  - Security (15 points)
  - Documentation (10 points)
- CLI Commands
- Cross-Skill Integration
- Edge Cases
- Notes
- License

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-industry-commoncore-integration-procedure/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

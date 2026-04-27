# sf-industry-commoncore-datamapper

## 요약

OmniStudio Data Mapper (formerly DataRaptor) creation and validation with 100-point scoring. Use when building Extract, Transform, Load, or Turbo Extract Data Mappers, mapping Salesforce object fields, or reviewing existing Data Mapper configurations. TRIGGER when: user creates Data Mappers, configures field mappings, works with OmniDataTransform metadata, or asks about DataRaptor/Data Mapper patterns. DO NOT TRIGGER when: building Integration Procedures (use sf-industry-commoncore-integration-procedure), authoring OmniScripts (use sf-industry-commoncore-omniscript), or analyzing cross-component dependencies (use sf-industry-commoncore-omnistudio-analyze).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-industry-commoncore-datamapper/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-industry-commoncore-datamapper-d46fa34.md` |
| 라이선스 | MIT |

## 언제 쓰나

OmniStudio Data Mapper (formerly DataRaptor) creation and validation with 100-point scoring. Use when building Extract, Transform, Load, or Turbo Extract Data Mappers, mapping Salesforce object fields, or reviewing existing Data Mapper configurations. TRIGGER when: user creates Data Mappers, configures field mappings, works with OmniDataTransform metadata, or asks about DataRaptor/Data Mapper patterns. DO NOT TRIGGER when: building Integration Procedures (use sf-industry-commoncore-integration-procedure), authoring OmniScripts (use sf-industry-commoncore-omniscript), or analyzing cross-component dependencies (use sf-industry-commoncore-omnistudio-analyze).

## 주요 내용

- **진행 방식**: Phase 1: Requirements Gathering **Ask the user** to gather: Data Mapper type (Extract, Transform, Load, Turbo Extract) Target Salesforce object(s) and fields Target org alias Consuming component (Integration Procedure, OmniScript, or FlexCard name) Data volume expectations (record counts, frequency) **Then**: Check existing Data Mappers: `Glob: **/OmniDataTransform*` Check existing OmniStudio metadata: `Glob: **/omnistudio/**` Create a task list Phase 2: Design & Type Selection **Naming Format**: `[Prefix][Object]_[Purpose]` using PascalCase **Examples**: `DR_Extract_Account_Details` -- Extract Account with related Contacts `DR_TurboExtract_Case_List` -- High-volume Case list for FlexCard `DR_Transform_Lead_Flatten` -- Flatten nested Lead data structure `DR_Load_Opportunity_Create` -- Insert Opportunity records Phase 3: Generation & Validation **For Generation**: Define the OmniDataTransform record (Name, Type, Active status) Define OmniDataTransformItem records (field mappings, input...

## 원본 문서 구조

- Core Responsibilities
- CRITICAL: Orchestration Order
- Key Insights
- Workflow (5-Phase Pattern)
  - Phase 1: Requirements Gathering
  - Phase 2: Design & Type Selection
  - Phase 3: Generation & Validation
  - Generation Guardrails (MANDATORY)
  - Phase 4: Deployment
  - Phase 5: Testing & Documentation
- Best Practices (100-Point Scoring)
- CLI Commands
  - Query Existing Data Mappers
  - Query Data Mapper Field Mappings
  - Retrieve Data Mapper Metadata
  - Deploy Data Mapper Metadata
- Cross-Skill Integration
- Edge Cases
- Notes
- License

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-industry-commoncore-datamapper/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

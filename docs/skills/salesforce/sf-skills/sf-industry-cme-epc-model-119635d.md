# sf-industry-cme-epc-model

## 요약

Salesforce Industries CME EPC product-modeling skill for Product2-based catalog creation. Use when creating EPC products, configuring product attributes, building offer bundles with Product Child Items, or reviewing EPC DataPack JSON metadata for product catalog changes. TRIGGER when: user creates or updates Product2 EPC records, AttributeAssignment payloads, AttributeMetadata/AttributeDefaultValues, Offer bundles, or ProductChildItem relationships. DO NOT TRIGGER when: designing OmniScripts/FlexCards/Integration Procedures (use sf-industry-commoncore-* skills), implementing Apex business logic (use sf-apex), or troubleshooting deployment pipelines (use sf-deploy).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-industry-cme-epc-model/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-industry-cme-epc-model-119635d.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Industries CME EPC product-modeling skill for Product2-based catalog creation. Use when creating EPC products, configuring product attributes, building offer bundles with Product Child Items, or reviewing EPC DataPack JSON metadata for product catalog changes. TRIGGER when: user creates or updates Product2 EPC records, AttributeAssignment payloads, AttributeMetadata/AttributeDefaultValues, Offer bundles, or ProductChildItem relationships. DO NOT TRIGGER when: designing OmniScripts/FlexCards/Integration Procedures (use sf-industry-commoncore-* skills), implementing Apex business logic (use sf-apex), or troubleshooting deployment pipelines (use sf-deploy).

## 주요 내용

- **진행 방식**: Phase 1: Identify Catalog Intent Ask for: Product type: **spec product** or **offer bundle** Domain taxonomy: Family, Type/SubType, category path, and channel Attribute requirements: required/optional, picklist values, default values Bundle composition: child products, quantity constraints, optional vs required Target org namespace model: `%vlocity_namespace%`, `vlocity_cmt`, or Core Phase 1A: Clarifying Questions for Complete Bundle (Mandatory) Before generating a new offer bundle payload, ask clarifying questions until all required inputs are known. Required clarification checklist: **Offer identity** What is the offer name and `ProductCode`? Is this net-new or an update to an existing Product2 offer? **Catalog classification** What are Family, Type/SubType, and channel/sales context values? Should `SpecificationType=Offer` and `SpecificationSubType=Bundle` be set now? **Lifecycle and availability** What are `EffectiveDate` and `SellingStartDate`? Should `IsActive` and `%vlocity_nam...

## 원본 문서 구조

- Quick Reference
- Asset Template Set
- Core Responsibilities
- Invocation Rules (Mandatory)
- Workflow (Create/Review)
  - Phase 1: Identify Catalog Intent
  - Phase 1A: Clarifying Questions for Complete Bundle (Mandatory)
  - Phase 2: Build Product2 Backbone
  - Phase 3: Add Attributes
  - Phase 4: Build Offer Bundles
  - Phase 4B: Generate Companion Metadata Files
  - Phase 5: Validate and Handoff
- Generation Guardrails (Mandatory)
- Scoring Model (120 Points)
  - 1) Catalog Identity and Naming (20)
  - 2) EPC Product Structure (20)
  - 3) Attribute Modeling (25)
  - 4) Offer Bundle Composition (25)
  - 5) DataPack Integrity (15)
  - 6) Documentation and Handoff (15)
- CLI and Validation Commands
- Sample Skill Invocation Commands
- Cross-Skill Integration
- External References
- Notes
- License

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-industry-cme-epc-model/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

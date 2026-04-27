# sf-industry-commoncore-callable-apex

## 요약

Salesforce Industries Common Core (OmniStudio/Vlocity) Apex callable generation and review with 120-point scoring. TRIGGER when: user creates or reviews System.Callable classes, migrates `VlocityOpenInterface` / `VlocityOpenInterface2`, or builds Industries callable extensions used by OmniStudio, Integration Procedures, or DataRaptors. DO NOT TRIGGER when: generic Apex classes/triggers (use sf-apex), building Integration Procedures (use sf-industry-commoncore-integration-procedure), authoring OmniScripts (use sf-industry-commoncore-omniscript), configuring Data Mappers (use sf-industry-commoncore-datamapper), or analyzing namespace/dependency issues (use sf-industry-commoncore-omnistudio-analyze).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-industry-commoncore-callable-apex/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-industry-commoncore-callable-apex-837055a.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Industries Common Core (OmniStudio/Vlocity) Apex callable generation and review with 120-point scoring. TRIGGER when: user creates or reviews System.Callable classes, migrates `VlocityOpenInterface` / `VlocityOpenInterface2`, or builds Industries callable extensions used by OmniStudio, Integration Procedures, or DataRaptors. DO NOT TRIGGER when: generic Apex classes/triggers (use sf-apex), building Integration Procedures (use sf-industry-commoncore-integration-procedure), authoring OmniScripts (use sf-industry-commoncore-omniscript), configuring Data Mappers (use sf-industry-commoncore-datamapper), or analyzing namespace/dependency issues (use sf-industry-commoncore-omnistudio-analyze).

## 주요 내용

- **진행 방식**: Phase 1: Requirements Gathering Ask for: Entry point (OmniScript, Integration Procedure, DataRaptor, or other Industries hook) Action names (strings passed into `call`) Input/output contract (required keys, types, and response shape) Data access needs (objects/fields, CRUD/FLS rules) Side effects (DML, callouts, async requirements) Then: Scan for existing callable classes: `Glob: **/*Callable*.cls` Identify shared utilities or base classes used for Industries extensions Create a task list Phase 2: Design & Contract Definition **Define the callable contract**: Action list (explicit, versioned strings) Input schema (required keys + types) Output schema (consistent response envelope) **Recommended response envelope**: { "success": true|false, "data": {...}, "errors": [ { "code": "...", "message": "..." } ] } **Action dispatch rules**: Use `switch on action` Default case throws a typed exception No dynamic method invocation or reflection **VlocityOpenInterface / VlocityOpenInterface2 cont...

## 원본 문서 구조

- Core Responsibilities
- Workflow (4-Phase Pattern)
  - Phase 1: Requirements Gathering
  - Phase 2: Design & Contract Definition
  - Phase 3: Implementation Pattern
  - Phase 4: Testing & Validation
- Migration: VlocityOpenInterface to System.Callable
- Best Practices (120-Point Scoring)
- ⛔ Guardrails (Mandatory)
- Common Anti-Patterns
- Cross-Skill Integration
- Reference Skill
- Bundled Examples
- Notes

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-industry-commoncore-callable-apex/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# sf-data

## 요약

Salesforce data operations with 130-point scoring. TRIGGER when: user creates test data, performs bulk import/export, uses sf data CLI commands, or needs data factory patterns for Apex tests. DO NOT TRIGGER when: SOQL query writing only (use sf-soql), Apex test execution (use sf-testing), or metadata deployment (use sf-deploy).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-data/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-data-2411aee.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce data operations with 130-point scoring. TRIGGER when: user creates test data, performs bulk import/export, uses sf data CLI commands, or needs data factory patterns for Apex tests. DO NOT TRIGGER when: SOQL query writing only (use sf-soql), Apex test execution (use sf-testing), or metadata deployment (use sf-deploy).

## 주요 내용

- **진행 방식**: 1. Verify prerequisites Confirm object / field availability, org auth, and required parent records. 2. Run describe-first pre-flight validation when schema is uncertain Before creating or updating records, use object describe data to validate: required fields createable vs non-createable fields picklist values relationship fields and parent requirements Example pattern: sf sobject describe --sobject ObjectName --target-org <alias> --json Helpful filters: Required + createable fields jq '.result.fields[] | select(.nillable==false and .createable==true) | {name, type}' Valid picklist values for one field jq '.result.fields[] | select(.name=="StageName") | .picklistValues[].value' Fields that cannot be set on create jq '.result.fields[] | select(.createable==false) | .name' 3. Choose the smallest correct mechanism 4. Execute or generate assets Use the built-in templates under `assets/` when they fit: `assets/factories/` `assets/bulk/` `assets/cleanup/` `assets/soql/` `assets/csv/` `asset...
- **산출물**: When finishing, report in this order: **Operation performed** **Objects and counts** **Target org or local artifact path** **Record IDs / output files** **Verification result** **Cleanup instructions** Suggested shape: Data operation: <create / update / delete / export / seed> Objects: <object + counts> Target: <org alias or local path> Artifacts: <record ids / csv / apex / json files> Verification: <passed / partial / failed> Cleanup: <exact delete or rollback guidance>

## 원본 문서 구조

- When This Skill Owns the Task
- Important Mode Decision
- Required Context to Gather First
- Core Operating Rules
- Recommended Workflow
  - 1. Verify prerequisites
  - 2. Run describe-first pre-flight validation when schema is uncertain
  - 3. Choose the smallest correct mechanism
  - 4. Execute or generate assets
  - 5. Verify results
  - 6. Apply a bounded retry strategy
  - 7. Leave cleanup guidance
- High-Signal Rules
  - Bulk safety
  - Data integrity
  - Cleanup discipline
- Common Failure Patterns
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Query / bulk / cleanup
  - Examples / limits
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-data/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

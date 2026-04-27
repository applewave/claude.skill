# sf-metadata

## 요약

Salesforce metadata generation and querying with 120-point scoring. TRIGGER when: user creates custom objects, fields, validation rules, or touches .object-meta.xml, .field-meta.xml, .profile-meta.xml files. DO NOT TRIGGER when: permission set analysis (use sf-permissions), deploying metadata (use sf-deploy), or Flow XML (use sf-flow).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-metadata/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-metadata-eee115f.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce metadata generation and querying with 120-point scoring. TRIGGER when: user creates custom objects, fields, validation rules, or touches .object-meta.xml, .field-meta.xml, .profile-meta.xml files. DO NOT TRIGGER when: permission set analysis (use sf-permissions), deploying metadata (use sf-deploy), or Flow XML (use sf-flow).

## 주요 내용

- **진행 방식**: 1. Choose the mode 2. Start from templates or CLI describe data For generation, use the assets under: `assets/objects/` `assets/fields/` `assets/permission-sets/` `assets/profiles/` `assets/record-types/` `assets/validation-rules/` `assets/layouts/` For querying, prefer `sf` metadata and `sobject describe` commands. Recent SDR/CLI support worth knowing when reading older examples: `CnfgItemSourceDefinition`, `ExtlClntAppOauthSecuritySettings`, and `UIBundle` are now source-supported under their current names. See [references/metadata-types-reference.md](references/metadata-types-reference.md). 3. Validate metadata quality Check: naming conventions structural correctness field-type fit security / FLS implications downstream deployment dependencies 4. Plan permission impact by default When new custom fields or objects are created: default to generating or updating a Permission Set unless the user opts out include `fieldPermissions` for **eligible custom fields** note any metadata catego...
- **산출물**: When finishing, report in this order: **Metadata created or queried** **Files created or updated** **Key schema/security decisions** **Permission / layout follow-ups** **Deploy next step** Suggested shape: Metadata task: <generate / query> Items: <objects, fields, rules, layouts, permsets> Files: <paths> Notes: <naming, field types, security, dependencies> Next step: <deploy, assign permset, or verify in Setup>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Choose the mode
  - 2. Start from templates or CLI describe data
  - 3. Validate metadata quality
  - 4. Plan permission impact by default
  - 5. Hand off deployment
- High-Signal Rules
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Security / scoring / examples
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-metadata/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

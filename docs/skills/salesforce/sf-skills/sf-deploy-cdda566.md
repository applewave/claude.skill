# sf-deploy

## 요약

Salesforce DevOps automation using sf CLI v2. TRIGGER when: user deploys metadata, creates/manages scratch orgs or sandboxes, sets up CI/CD pipelines, or troubleshoots deployment errors with sf project deploy. DO NOT TRIGGER when: writing Apex/LWC code (use sf-apex/sf-lwc), creating metadata XML (use sf-metadata), or querying org data (use sf-data).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-deploy/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-deploy-cdda566.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce DevOps automation using sf CLI v2. TRIGGER when: user deploys metadata, creates/manages scratch orgs or sandboxes, sets up CI/CD pipelines, or troubleshoots deployment errors with sf project deploy. DO NOT TRIGGER when: writing Apex/LWC code (use sf-apex/sf-lwc), creating metadata XML (use sf-metadata), or querying org data (use sf-data).

## 주요 내용

- **진행 방식**: 1. Preflight Confirm auth, repo shape, package directories, and target scope. 2. Validate first sf project deploy start --dry-run --source-dir force-app --target-org <alias> --wait 30 --json Use manifest- or metadata-scoped validation when the change set is targeted. 3. If validation succeeds, offer the next safe workflow After a successful validation, guide the user to the correct next action: deploy now assign permission sets create test data via [sf-data](../sf-data/SKILL.md) run tests / smoke checks orchestrate multiple post-deploy steps in order 4. Deploy the smallest correct scope source-dir deploy sf project deploy start --source-dir force-app --target-org <alias> --wait 30 --json manifest deploy sf project deploy start --manifest manifest/package.xml --target-org <alias> --test-level RunLocalTests --wait 30 --json manifest deploy with Spring '26 relevant-test selection sf project deploy start --manifest manifest/package.xml --target-org <alias> --test-level RunRelevantTests --...

## 원본 문서 구조

- When This Skill Owns the Task
- Critical Operating Rules
  - Default deployment order
- Required Context to Gather First
- Recommended Workflow
  - 1. Preflight
  - 2. Validate first
  - 3. If validation succeeds, offer the next safe workflow
  - 4. Deploy the smallest correct scope
  - 5. Verify
  - 6. Report clearly
- High-Signal Failure Patterns
- CI/CD Guidance
- Agentforce Deployment Note
- Cross-Skill Integration
- Reference Map
  - Start here
  - Specialized deployment safety
- Score Guide
- Completion Format

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-deploy/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

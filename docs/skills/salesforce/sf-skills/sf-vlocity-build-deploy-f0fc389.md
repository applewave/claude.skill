# sf-vlocity-build-deploy

## 요약

Salesforce Industries DataPack deployment automation using Vlocity Build. TRIGGER when: user deploys or validates OmniStudio/Vlocity DataPacks with vlocity commands (packDeploy/packRetry/packExport/packGetDiffs), sets up DataPack CI/CD pipelines, or troubleshoots DataPack migration errors. DO NOT TRIGGER when: deploying Salesforce metadata with sf project deploy (use sf-deploy), authoring OmniStudio artifacts (use sf-industry-commoncore-*), or writing Apex/LWC business logic (use sf-apex/sf-lwc).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-vlocity-build-deploy/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-vlocity-build-deploy-f0fc389.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Industries DataPack deployment automation using Vlocity Build. TRIGGER when: user deploys or validates OmniStudio/Vlocity DataPacks with vlocity commands (packDeploy/packRetry/packExport/packGetDiffs), sets up DataPack CI/CD pipelines, or troubleshoots DataPack migration errors. DO NOT TRIGGER when: deploying Salesforce metadata with sf project deploy (use sf-deploy), authoring OmniStudio artifacts (use sf-industry-commoncore-*), or writing Apex/LWC business logic (use sf-apex/sf-lwc).

## 주요 내용

- **진행 방식**: 1. Ensure tool readiness npm install --global vlocity vlocity help 2. Validate project data locally vlocity -sfdx.username <source-alias> -job <job-file>.yaml validateLocalData Use `--fixLocalGlobalKeys` only when explicitly requested and after explaining impact. 3. Export from source (when needed) vlocity -sfdx.username <source-alias> -job <job-file>.yaml packExport vlocity -sfdx.username <source-alias> -job <job-file>.yaml packRetry 4. Deploy to target vlocity -sfdx.username <target-alias> -job <job-file>.yaml packDeploy vlocity -sfdx.username <target-alias> -job <job-file>.yaml packRetry 5. Continue interrupted jobs vlocity -sfdx.username <target-alias> -job <job-file>.yaml packContinue 6. Verify post-deploy parity vlocity -sfdx.username <target-alias> -job <job-file>.yaml packGetDiffs Job-file starter: [references/job-file-template.md](references/job-file-template.md)

## 원본 문서 구조

- When This Skill Owns the Task
- Critical Operating Rules
- Required Context to Gather First
- Recommended Workflow
  - 1. Ensure tool readiness
  - 2. Validate project data locally
  - 3. Export from source (when needed)
  - 4. Deploy to target
  - 5. Continue interrupted jobs
  - 6. Verify post-deploy parity
- High-Signal Failure Patterns
- CI/CD Guidance
- Cross-Skill Integration
- Reference Map
  - Start here
  - External reference
- Completion Format

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-vlocity-build-deploy/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# sf-datacloud

## 요약

Salesforce Data Cloud product orchestrator for connect→prepare→harmonize→segment→act workflows. TRIGGER when: user needs a multi-step Data Cloud pipeline, asks to set up or troubleshoot Data Cloud across phases, manages data spaces or data kits, or wants a cross-phase `sf data360` workflow. DO NOT TRIGGER when: work is isolated to a single phase (use the matching sf-datacloud-* skill), the task is STDM/session tracing/parquet telemetry (use sf-ai-agentforce-observability), standard CRM SOQL (use sf-soql), or Apex implementation (use sf-apex).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-datacloud/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-datacloud-97db2db.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Data Cloud product orchestrator for connect→prepare→harmonize→segment→act workflows. TRIGGER when: user needs a multi-step Data Cloud pipeline, asks to set up or troubleshoot Data Cloud across phases, manages data spaces or data kits, or wants a cross-phase `sf data360` workflow. DO NOT TRIGGER when: work is isolated to a single phase (use the matching sf-datacloud-* skill), the task is STDM/session tracing/parquet telemetry (use sf-ai-agentforce-observability), standard CRM SOQL (use sf-soql), or Apex implementation (use sf-apex).

## 주요 내용

- **진행 방식**: 1. Verify the runtime and auth Confirm: `sf` is installed the community Data Cloud plugin is linked the target org is authenticated Recommended checks: sf data360 man sf org display -o <alias> bash ~/.claude/skills/sf-datacloud/scripts/verify-plugin.sh <alias> Treat `sf data360 doctor` as a broad health signal, not the sole gate. On partially provisioned orgs it can fail even when read-only command families like connectors, DMOs, or segments still work. 2. Classify readiness before changing anything Run the shared classifier first: node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --json Only use a query-plane probe after you know the table name is real: node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --phase retrieve --describe-table MyDMO__dlm --json Use the classifier to distinguish: empty-but-enabled modules feature-gated modules query-plane issues runtime/auth failures 3. Discover existing state with read-only commands Use targeted inspecti...
- **산출물**: When finishing, report in this order: **Task classification** **Runtime status** **Readiness classification** **Phase(s) involved** **Commands or artifacts used** **Verification result** **Next recommended step** Suggested shape: Data Cloud task: <setup / inspect / troubleshoot / migrate> Runtime: <plugin ready / missing / partially verified> Readiness: <ready / ready_empty / partial / feature_gated / blocked> Phases: <connect / prepare / harmonize / segment / act / retrieve> Artifacts: <json files, commands, scripts> Verification: <passed / partial / blocked> Next step: <next phase, setup guidance, or cross-skill handoff>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Core Operating Rules
- Recommended Workflow
  - 1. Verify the runtime and auth
  - 2. Classify readiness before changing anything
  - 3. Discover existing state with read-only commands
  - 4. Localize the phase
  - 5. Choose deterministic artifacts when possible
  - 6. Verify after each phase
- High-Signal Gotchas
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Phase skills
  - Deterministic helpers

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-datacloud/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# sf-datacloud-retrieve

## 요약

Salesforce Data Cloud Retrieve phase. TRIGGER when: user runs Data Cloud SQL, describe, async queries, vector search, search-index workflows, or metadata introspection for Data Cloud objects. DO NOT TRIGGER when: the task is standard CRM SOQL (use sf-soql), segment creation or calculated insight design (use sf-datacloud-segment), or STDM/session tracing/parquet analysis (use sf-ai-agentforce-observability).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-datacloud-retrieve/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-datacloud-retrieve-bb492e5.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Data Cloud Retrieve phase. TRIGGER when: user runs Data Cloud SQL, describe, async queries, vector search, search-index workflows, or metadata introspection for Data Cloud objects. DO NOT TRIGGER when: the task is standard CRM SOQL (use sf-soql), segment creation or calculated insight design (use sf-datacloud-segment), or STDM/session tracing/parquet analysis (use sf-ai-agentforce-observability).

## 주요 내용

- **진행 방식**: 1. Classify readiness for retrieve work node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --phase retrieve --json optional query-plane probe, only with a real table name node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --phase retrieve --describe-table MyDMO__dlm --json 2. Choose the smallest correct query shape sf data360 query sql -o <org> --sql 'SELECT COUNT(*) FROM "ssot__Individual__dlm"' 2>/dev/null sf data360 query sqlv2 -o <org> --sql 'SELECT * FROM "ssot__Individual__dlm"' 2>/dev/null sf data360 query async-create -o <org> --sql 'SELECT * FROM "ssot__Individual__dlm"' 2>/dev/null 3. Use describe before guessing fields sf data360 query describe -o <org> --table ssot__Individual__dlm 2>/dev/null 4. Use vector or hybrid search only when an index exists sf data360 search-index list -o <org> 2>/dev/null sf data360 query vector -o <org> --index Knowledge_Index --query "reset password" --limit 5 2>/dev/null sf data360 query hybrid -o <org> --in...
- **산출물**: Retrieve task: <sql / sqlv2 / async / describe / vector / search-index> Target org: <alias> Target object: <table or index> Commands: <key commands run> Verification: <query rows / schema / status> Next step: <segment / harmonize / follow-up>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Core Operating Rules
- Recommended Workflow
  - 1. Classify readiness for retrieve work
  - 2. Choose the smallest correct query shape
  - 3. Use describe before guessing fields
  - 4. Use vector or hybrid search only when an index exists
  - 5. Reuse curated search-index examples when creating indexes
- High-Signal Gotchas
- Output Format
- References

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-datacloud-retrieve/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

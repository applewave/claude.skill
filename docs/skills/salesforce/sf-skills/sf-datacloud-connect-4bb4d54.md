# sf-datacloud-connect

## 요약

Salesforce Data Cloud Connect phase. TRIGGER when: user manages Data Cloud connections, connectors, connector metadata, tests a connection, browses source objects or databases, or sets up a new source system. DO NOT TRIGGER when: the task is about data streams or DLOs (use sf-datacloud-prepare), DMOs or identity resolution (use sf-datacloud-harmonize), retrieval/search (use sf-datacloud-retrieve), or STDM telemetry (use sf-ai-agentforce-observability).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-datacloud-connect/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-datacloud-connect-4bb4d54.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Data Cloud Connect phase. TRIGGER when: user manages Data Cloud connections, connectors, connector metadata, tests a connection, browses source objects or databases, or sets up a new source system. DO NOT TRIGGER when: the task is about data streams or DLOs (use sf-datacloud-prepare), DMOs or identity resolution (use sf-datacloud-harmonize), retrieval/search (use sf-datacloud-retrieve), or STDM telemetry (use sf-ai-agentforce-observability).

## 주요 내용

- **진행 방식**: 1. Classify readiness for connect work node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --phase connect --json 2. Discover connector types sf data360 connection connector-list -o <org> 2>/dev/null sf data360 data-stream list -o <org> 2>/dev/null 3. Inspect connections by type sf data360 connection list -o <org> --connector-type SalesforceDotCom 2>/dev/null sf data360 connection list -o <org> --connector-type REDSHIFT 2>/dev/null sf data360 connection list -o <org> --connector-type SNOWFLAKE 2>/dev/null 4. Inspect a specific connection or uploaded schema sf data360 connection get -o <org> --name <connection> 2>/dev/null sf data360 connection objects -o <org> --name <connection> 2>/dev/null sf data360 connection fields -o <org> --name <connection> 2>/dev/null sf data360 connection schema-get -o <org> --name <connection-id> 2>/dev/null 5. Test or create only after discovery sf data360 connection test -o <org> --name <connection> --connector-type <type> 2>/dev/null sf...
- **산출물**: Connect task: <inspect / create / test / update> Connector type: <SalesforceDotCom / REDSHIFT / SNOWFLAKE / SPUnstructuredDocument / IngestApi / ...> Target org: <alias> Commands: <key commands run> Verification: <passed / partial / blocked> Next step: <prepare phase or connector follow-up>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Core Operating Rules
- Recommended Workflow
  - 1. Classify readiness for connect work
  - 2. Discover connector types
  - 3. Inspect connections by type
  - 4. Inspect a specific connection or uploaded schema
  - 5. Test or create only after discovery
  - 6. Start from curated example payloads for external connectors
  - 7. Discover payload fields for unknown connector types
- High-Signal Gotchas
- Output Format
- References

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-datacloud-connect/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

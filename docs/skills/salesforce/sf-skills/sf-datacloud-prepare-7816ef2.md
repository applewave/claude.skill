# sf-datacloud-prepare

## 요약

Salesforce Data Cloud Prepare phase. TRIGGER when: user creates or manages Data Cloud data streams, DLOs, transforms, or Document AI configurations, or asks about ingestion into Data Cloud. DO NOT TRIGGER when: the task is connection setup only (use sf-datacloud-connect), DMOs and identity resolution (use sf-datacloud-harmonize), or query/search work (use sf-datacloud-retrieve).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-datacloud-prepare/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-datacloud-prepare-7816ef2.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Data Cloud Prepare phase. TRIGGER when: user creates or manages Data Cloud data streams, DLOs, transforms, or Document AI configurations, or asks about ingestion into Data Cloud. DO NOT TRIGGER when: the task is connection setup only (use sf-datacloud-connect), DMOs and identity resolution (use sf-datacloud-harmonize), or query/search work (use sf-datacloud-retrieve).

## 주요 내용

- **진행 방식**: 1. Classify readiness for prepare work node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --phase prepare --json 2. Inspect existing ingestion assets sf data360 data-stream list -o <org> 2>/dev/null sf data360 dlo list -o <org> 2>/dev/null 3. Confirm the stream category before creation Use these rules when suggesting categories: When the source is ambiguous, ask the user explicitly whether the dataset should be treated as `Profile`, `Engagement`, or `Other`. 4. Create or inspect streams intentionally sf data360 data-stream get -o <org> --name <stream> 2>/dev/null sf data360 data-stream create-from-object -o <org> --object Contact --connection SalesforceDotCom_Home 2>/dev/null sf data360 data-stream create -o <org> -f stream.json 2>/dev/null sf data360 data-stream run -o <org> --name <stream> 2>/dev/null 5. Check DLO shape sf data360 dlo get -o <org> --name Contact_Home__dll 2>/dev/null 6. Choose the right refresh mechanism Use the smaller refresh scope that matches t...
- **산출물**: Prepare task: <stream / dlo / transform / docai> Source: <connection + object> Target org: <alias> Artifacts: <stream names / dlo names / json definitions> Verification: <passed / partial / blocked> Next step: <harmonize or retrieve>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Core Operating Rules
- Recommended Workflow
  - 1. Classify readiness for prepare work
  - 2. Inspect existing ingestion assets
  - 3. Confirm the stream category before creation
  - 4. Create or inspect streams intentionally
  - 5. Check DLO shape
  - 6. Choose the right refresh mechanism
  - 7. Handle unstructured sources deliberately
  - 8. Use the local Ingestion API example for send-data workflows
  - 9. Only then move into harmonization
- High-Signal Gotchas
- Output Format
- References

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-datacloud-prepare/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

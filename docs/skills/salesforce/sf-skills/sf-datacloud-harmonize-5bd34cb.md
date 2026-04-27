# sf-datacloud-harmonize

## 요약

Salesforce Data Cloud Harmonize phase. TRIGGER when: user works with DMOs, mappings, relationships, identity resolution, unified profiles, data graphs, or universal IDs. DO NOT TRIGGER when: the task is only about streams/DLOs (use sf-datacloud-prepare), segments/insights (use sf-datacloud-segment), retrieval/search (use sf-datacloud-retrieve), or STDM/session tracing (use sf-ai-agentforce-observability).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-datacloud-harmonize/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-datacloud-harmonize-5bd34cb.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Data Cloud Harmonize phase. TRIGGER when: user works with DMOs, mappings, relationships, identity resolution, unified profiles, data graphs, or universal IDs. DO NOT TRIGGER when: the task is only about streams/DLOs (use sf-datacloud-prepare), segments/insights (use sf-datacloud-segment), retrieval/search (use sf-datacloud-retrieve), or STDM/session tracing (use sf-ai-agentforce-observability).

## 주요 내용

- **진행 방식**: 1. Classify readiness for harmonize work node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --phase harmonize --json 2. Inspect the catalog sf data360 dmo list --all -o <org> 2>/dev/null sf data360 identity-resolution list -o <org> 2>/dev/null 3. Inspect schema before mapping sf data360 query describe -o <org> --table ssot__Individual__dlm 2>/dev/null sf data360 dmo get -o <org> --name ssot__Individual__dlm --json 2>/dev/null 4. Create or review mappings intentionally sf data360 dmo mapping-list -o <org> --source Contact_Home__dll --target ssot__Individual__dlm 2>/dev/null sf data360 dmo map-to-canonical -o <org> --dlo Contact_Home__dll --dmo ssot__Individual__dlm --dry-run 2>/dev/null 5. Run IR only after mappings are trustworthy sf data360 identity-resolution create -o <org> -f ir-ruleset.json 2>/dev/null sf data360 identity-resolution run -o <org> --name Main 2>/dev/null
- **산출물**: Harmonize task: <dmo / mapping / relationship / ir / data-graph> Source/target: <dlo → dmo or ruleset/graph names> Target org: <alias> Artifacts: <json files / commands> Verification: <passed / partial / blocked> Next step: <segment / retrieve / follow-up>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Core Operating Rules
- Recommended Workflow
  - 1. Classify readiness for harmonize work
  - 2. Inspect the catalog
  - 3. Inspect schema before mapping
  - 4. Create or review mappings intentionally
  - 5. Run IR only after mappings are trustworthy
- High-Signal Gotchas
- Output Format
- References

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-datacloud-harmonize/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

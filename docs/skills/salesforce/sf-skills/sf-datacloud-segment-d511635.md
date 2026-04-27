# sf-datacloud-segment

## 요약

Salesforce Data Cloud Segment phase. TRIGGER when: user creates or publishes segments, manages calculated insights, inspects segment counts or membership, or troubleshoots audience SQL in Data Cloud. DO NOT TRIGGER when: the task is DMO/mapping/identity-resolution work (use sf-datacloud-harmonize), activation work (use sf-datacloud-act), query/search-index work (use sf-datacloud-retrieve), or STDM/session tracing (use sf-ai-agentforce-observability).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-datacloud-segment/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-datacloud-segment-d511635.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Data Cloud Segment phase. TRIGGER when: user creates or publishes segments, manages calculated insights, inspects segment counts or membership, or troubleshoots audience SQL in Data Cloud. DO NOT TRIGGER when: the task is DMO/mapping/identity-resolution work (use sf-datacloud-harmonize), activation work (use sf-datacloud-act), query/search-index work (use sf-datacloud-retrieve), or STDM/session tracing (use sf-ai-agentforce-observability).

## 주요 내용

- **진행 방식**: 1. Classify readiness for segment work node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --phase segment --json 2. Inspect current state sf data360 segment list -o <org> 2>/dev/null sf data360 calculated-insight list -o <org> 2>/dev/null 3. Create with reusable JSON definitions sf data360 segment create -o <org> -f segment.json --api-version 64.0 2>/dev/null sf data360 calculated-insight create -o <org> -f ci.json 2>/dev/null 4. Publish or run explicitly sf data360 segment publish -o <org> --name My_Segment 2>/dev/null sf data360 calculated-insight run -o <org> --name Lifetime_Value 2>/dev/null 5. Verify with counts or SQL sf data360 segment count -o <org> --name My_Segment 2>/dev/null sf data360 query sql -o <org> --sql 'SELECT COUNT(*) FROM "UnifiedssotIndividualMain__dlm"' 2>/dev/null
- **산출물**: Segment task: <segment / calculated-insight> Action: <create / publish / inspect / troubleshoot> Target org: <alias> Artifacts: <definition files / commands> Verification: <member count / query result / publish state> Next step: <act / retrieve / follow-up>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Core Operating Rules
- Recommended Workflow
  - 1. Classify readiness for segment work
  - 2. Inspect current state
  - 3. Create with reusable JSON definitions
  - 4. Publish or run explicitly
  - 5. Verify with counts or SQL
- High-Signal Gotchas
- Output Format
- References

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-datacloud-segment/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

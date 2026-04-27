# sf-datacloud-act

## 요약

Salesforce Data Cloud Act phase. TRIGGER when: user manages activations, activation targets, data actions, or downstream delivery of Data Cloud audiences and data. DO NOT TRIGGER when: the task is segment creation (use sf-datacloud-segment), data retrieval/search work (use sf-datacloud-retrieve), or STDM/session tracing (use sf-ai-agentforce-observability).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-datacloud-act/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-datacloud-act-fcf8601.md` |
| 라이선스 | MIT |

## 언제 쓰나

Salesforce Data Cloud Act phase. TRIGGER when: user manages activations, activation targets, data actions, or downstream delivery of Data Cloud audiences and data. DO NOT TRIGGER when: the task is segment creation (use sf-datacloud-segment), data retrieval/search work (use sf-datacloud-retrieve), or STDM/session tracing (use sf-ai-agentforce-observability).

## 주요 내용

- **진행 방식**: 1. Classify readiness for act work node ~/.claude/skills/sf-datacloud/scripts/diagnose-org.mjs -o <org> --phase act --json 2. Inspect destinations first sf data360 activation platforms -o <org> 2>/dev/null sf data360 activation-target list -o <org> 2>/dev/null sf data360 data-action-target list -o <org> 2>/dev/null 3. Create the destination before the activation sf data360 activation-target create -o <org> -f target.json 2>/dev/null sf data360 data-action-target create -o <org> -f target.json 2>/dev/null 4. Create the activation or data action sf data360 activation create -o <org> -f activation.json 2>/dev/null sf data360 data-action create -o <org> -f action.json 2>/dev/null 5. Verify downstream readiness sf data360 activation list -o <org> 2>/dev/null sf data360 activation data -o <org> --name <activation> 2>/dev/null
- **산출물**: Act task: <activation / activation-target / data-action / data-action-target> Destination: <platform or target> Target org: <alias> Artifacts: <definition files / commands> Verification: <listed / created / blocked> Next step: <destination validation or downstream testing>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Core Operating Rules
- Recommended Workflow
  - 1. Classify readiness for act work
  - 2. Inspect destinations first
  - 3. Create the destination before the activation
  - 4. Create the activation or data action
  - 5. Verify downstream readiness
- High-Signal Gotchas
- Output Format
- References

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-datacloud-act/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

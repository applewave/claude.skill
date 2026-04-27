# debug-zoom

## 요약

Debug a broken Zoom integration by isolating the failure point and routing into the right Zoom references. Use when auth, API, webhook, SDK, or MCP behavior is failing and you need a ranked hypothesis list plus verification steps.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/debug-zoom/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/debug-zoom-43e1e67.md` |
| 입력 힌트 | `<symptoms, error, or failing flow>` |

## 언제 쓰나

Debug a broken Zoom integration by isolating the failure point and routing into the right Zoom references. Use when auth, API, webhook, SDK, or MCP behavior is failing and you need a ranked hypothesis list plus verification steps.

## 주요 내용

- **사용 방식**: /debug-zoom $ARGUMENTS
- **진행 방식**: Identify the failing layer: auth, API request, webhook, SDK init, media/session behavior, or MCP transport. Ask for the minimum missing evidence: exact error, platform, request/response, event payload, or code path. Produce 2-4 plausible causes ranked by likelihood. Route to the most relevant deep references in `skills/`. Give a short verification plan so the user can confirm the fix.
- **산출물**: Most likely failure layer Ranked hypotheses Targeted fix steps Verification checklist Relevant skill links

## 원본 문서 구조

- Usage
- Workflow
- Output
- Related Skills

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/debug-zoom/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

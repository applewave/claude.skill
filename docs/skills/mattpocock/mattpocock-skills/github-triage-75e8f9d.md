# github-triage

## 요약

Triage GitHub issues through a label-based state machine with interactive grilling sessions. Use when user wants to triage issues, review incoming bugs or feature requests, prepare issues for an AFK agent, or manage issue workflow.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/github-triage/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/github-triage-75e8f9d.md` |

## 언제 쓰나

Triage GitHub issues through a label-based state machine with interactive grilling sessions. Use when user wants to triage issues, review incoming bugs or feature requests, prepare issues for an AFK agent, or manage issue workflow.

## 주요 내용

- **진행 방식**: When the maintainer asks for an overview, query GitHub and present a summary grouped into three buckets: **Unlabeled issues** — new, no labels at all. These have never been triaged. **`needs-triage` issues** — maintainer needs to evaluate or continue evaluating. **`needs-info` issues with new activity** — the reporter has commented since the last triage notes comment. Check comment timestamps to determine this. Display counts per group. Within each group, show issues oldest first (longest-waiting gets attention first). For each issue, show: number, title, age, and a one-line summary of the issue body. Let the maintainer pick which issue to dive into.
- **산출물**: When moving an issue to `needs-info`, post a comment that captures the grilling progress and tells the reporter what's needed:

## 원본 문서 구조

- Reference docs
- Labels
- State Machine
- Invocation
- Workflow: Show What Needs Attention
- Workflow: Triage a Specific Issue
  - Step 1: Gather context
  - Step 2: Present a recommendation
  - Step 3: Bug reproduction (bugs only)
  - Step 4: Grilling session (if needed)
  - Step 5: Apply the outcome
- Workflow: Quick State Override
- Needs Info Output
- Triage Notes
- Resuming Previous Sessions

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/github-triage/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

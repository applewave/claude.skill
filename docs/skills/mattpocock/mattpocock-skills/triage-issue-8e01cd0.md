# triage-issue

## 요약

Triage a bug or issue by exploring the codebase to find root cause, then create a GitHub issue with a TDD-based fix plan. Use when user reports a bug, wants to file an issue, mentions "triage", or wants to investigate and plan a fix for a problem.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/triage-issue/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/triage-issue-8e01cd0.md` |

## 언제 쓰나

Triage a bug or issue by exploring the codebase to find root cause, then create a GitHub issue with a TDD-based fix plan. Use when user reports a bug, wants to file an issue, mentions "triage", or wants to investigate and plan a fix for a problem.

## 주요 내용

- **진행 방식**: 1. Capture the problem Get a brief description of the issue from the user. If they haven't provided one, ask ONE question: "What's the problem you're seeing?" Do NOT ask follow-up questions yet. Start investigating immediately. 2. Explore and diagnose Use the Agent tool with subagent_type=Explore to deeply investigate the codebase. Your goal is to find: **Where** the bug manifests (entry points, UI, API responses) **What** code path is involved (trace the flow) **Why** it fails (the root cause, not just the symptom) **What** related code exists (similar patterns, tests, adjacent modules) Look at: Related source files and their dependencies Existing tests (what's tested, what's missing) Recent changes to affected files (`git log` on relevant files) Error handling in the code path Similar patterns elsewhere in the codebase that work correctly 3. Identify the fix approach Based on your investigation, determine: The minimal change needed to fix the root cause Which modules/interfaces are...

## 원본 문서 구조

- Process
  - 1. Capture the problem
  - 2. Explore and diagnose
  - 3. Identify the fix approach
  - 4. Design TDD fix plan
  - 5. Create the GitHub issue
- Problem
- Root Cause Analysis
- TDD Fix Plan
- Acceptance Criteria

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/triage-issue/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

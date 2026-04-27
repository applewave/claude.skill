# claude-api

## 요약

Build, debug, and optimize Claude API / Anthropic SDK apps. Apps built with this skill should include prompt caching. TRIGGER when: code imports anthropic/@anthropic-ai/sdk; user asks to use the Claude API, Anthropic SDKs, or Managed Agents (/v1/agents, /v1/sessions, /v1/environments). DO NOT TRIGGER when: code imports `openai`/other AI SDK, general programming, or ML/data-science tasks.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Anthropic Skills |
| 영역 | skills |
| 원본 경로 | `skills/skills/claude-api/SKILL.md` |
| 상세 파일 | `docs/skills/anthropic/skills/claude-api-fd6cf59.md` |
| 라이선스 | Complete terms in LICENSE.txt |

## 언제 쓰나

Build, debug, and optimize Claude API / Anthropic SDK apps. Apps built with this skill should include prompt caching. TRIGGER when: code imports anthropic/@anthropic-ai/sdk; user asks to use the Claude API, Anthropic SDKs, or Managed Agents (/v1/agents, /v1/sessions, /v1/environments). DO NOT TRIGGER when: code imports `openai`/other AI SDK, general programming, or ML/data-science tasks.

## 주요 내용

- **산출물**: When the user asks you to add, modify, or implement a Claude feature, your code must call Claude through one of: **The official Anthropic SDK** for the project's language (`anthropic`, `@anthropic-ai/sdk`, `com.anthropic.*`, etc.). This is the default whenever a supported SDK exists for the project. **Raw HTTP** (`curl`, `requests`, `fetch`, `httpx`, etc.) — only when the user explicitly asks for cURL/REST/raw HTTP, the project is a shell/cURL project, or the language has no official SDK. Never mix the two — don't reach for `requests`/`fetch` in a Python or TypeScript project just because it feels lighter. Never fall back to OpenAI-compatible shims. **Never guess SDK usage.** Function names...

## 원본 문서 구조

- Before You Start
- Output Requirement
- Defaults
- Subcommands
- Language Detection
  - Language-Specific Feature Support
- Which Surface Should I Use?
  - Decision Tree
  - Should I Build an Agent?
- Architecture
- Current Models (cached: 2026-02-17)
- Thinking & Effort (Quick Reference)
- Compaction (Quick Reference)
- Prompt Caching (Quick Reference)
- Managed Agents (Beta)
- Reading Guide
  - Quick Task Reference
  - Claude API (Full File Reference)
- When to Use WebFetch
- Common Pitfalls

## 관리 메모

- 이 문서는 원본 `skills/skills/claude-api/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# discover-brand

## 요약

This skill orchestrates autonomous discovery of brand materials across enterprise platforms (Notion, Confluence, Google Drive, Box, SharePoint, Figma, Gong, Granola, Slack). It should be used when the user asks to "discover brand materials", "find brand documents", "search for brand guidelines", "audit brand content", "what brand materials do we have", "find our style guide", "where are our brand docs", "do we have a style guide", "discover brand voice", "brand content audit", or "find brand assets".

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/brand-voice |
| 원본 경로 | `knowledge-work-plugins/partner-built/brand-voice/skills/discover-brand/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-brand-voice/discover-brand-484dcf3.md` |

## 언제 쓰나

This skill orchestrates autonomous discovery of brand materials across enterprise platforms (Notion, Confluence, Google Drive, Box, SharePoint, Figma, Gong, Granola, Slack). It should be used when the user asks to "discover brand materials", "find brand documents", "search for brand guidelines", "audit brand content", "what brand materials do we have", "find our style guide", "where are our brand docs", "do we have a style guide", "discover brand voice", "brand content audit", or "find brand assets".

## 주요 내용

- **진행 방식**: 0. Orient the User Before starting, briefly explain what's about to happen so the user knows what to expect: "Here's how brand discovery works: **Search** — I'll search your connected platforms (Notion, Google Drive, Slack, etc.) for brand-related materials: style guides, pitch decks, templates, transcripts, and more. **Analyze** — I'll categorize and rank what I find, pull the best sources, and produce a discovery report with what I found, any conflicts, and open questions. **Generate guidelines** — Once you've reviewed the report, I can generate a structured brand voice guideline document from the results. **Save** — Guidelines are saved to `.claude/brand-voice-guidelines.md` in your working folder once you approve them. Nothing is written until that step. The search usually takes a few minutes depending on how many platforms are connected. Ready to get started?" Wait for the user to confirm before proceeding. If they have questions about the process, answer them first. 1. Check Set...

## 원본 문서 구조

- Discovery Workflow
  - 0. Orient the User
  - 1. Check Settings
  - 2. Validate Platform Coverage
  - 3. Confirm Scope with User
  - 4. Delegate to Discover-Brand Agent
  - 5. Present Discovery Report
  - 6. Offer Next Steps
- Open Questions
- Integration with Other Skills
- Error Handling
- Reference Files

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/brand-voice/skills/discover-brand/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

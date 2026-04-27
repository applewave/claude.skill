# compose-outreach

## 요약

Generate personalized outreach messages using Common Room signals. Triggers on 'draft outreach to [person]', 'write an email to [name]', 'compose a message for [contact]', or any outreach drafting request.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/common-room |
| 원본 경로 | `knowledge-work-plugins/partner-built/common-room/skills/compose-outreach/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-common-room/compose-outreach-dfb1401.md` |

## 언제 쓰나

Generate personalized outreach messages using Common Room signals. Triggers on 'draft outreach to [person]', 'write an email to [name]', 'compose a message for [contact]', or any outreach drafting request.

## 주요 내용

- **진행 방식**: Step 1: Look Up the Target Use Common Room MCP tools to find and retrieve data for the target (company and/or specific contact). Pull: Recent product activity and engagement signals Community activity (posts, questions, reactions) 3rd-party intent signals (job postings, news, funding) Relationship history (prior contact, meetings, email opens) If the user specified a person, run contact-level research. If only a company was given, identify the best contact to target based on title, engagement, and role. Step 2: Web Search for External Hooks (If CR Signals Are Thin) If CR returned strong signals (recent activity, engagement, product usage), those should drive personalization — skip web search. If CR signals are thin or the prospect has little CR activity, run a web search for external hooks: **What to search:** `"[company name]" funding OR acquisition OR launch OR announcement` — last 30 days `"[contact full name]" "[company name]"` — look for recent articles, interviews, LinkedIn post...

## 원본 문서 구조

- Outreach Process
  - Step 1: Look Up the Target
  - Step 2: Web Search for External Hooks (If CR Signals Are Thin)
  - Step 3: Spark Enrichment (If Available)
  - Step 4: Identify the Best Hooks
  - Step 5: Generate All Three Formats
  - Step 6: Annotate Your Choices
- Output Format
- Outreach for [Name / Company]
  - 📧 Email
  - 📞 Call Script
  - 💼 LinkedIn Message
  - Signal Notes
- When Signal Data Is Sparse
- Outreach for [Name / Company] — Limited Data
- Quality Standards
- Reference Files

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/common-room/skills/compose-outreach/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

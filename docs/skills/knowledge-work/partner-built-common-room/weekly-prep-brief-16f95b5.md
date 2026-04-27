# weekly-prep-brief

## 요약

Generate a comprehensive weekly briefing for all external calls in the next 7 days. Triggers on 'weekly prep brief', 'prepare my week', 'what calls do I have this week', 'Monday prep', or any weekly planning request.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/common-room |
| 원본 경로 | `knowledge-work-plugins/partner-built/common-room/skills/weekly-prep-brief/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-common-room/weekly-prep-brief-16f95b5.md` |

## 언제 쓰나

Generate a comprehensive weekly briefing for all external calls in the next 7 days. Triggers on 'weekly prep brief', 'prepare my week', 'what calls do I have this week', 'Monday prep', or any weekly planning request.

## 주요 내용

- **진행 방식**: Step 1: Get the Week's External Meetings **Option A — Calendar connected:** Use the `~~calendar` connector to fetch all meetings scheduled in the next 7 days (or a user-specified range). Filter to keep only external meetings — those with attendees from outside your organization. Discard internal-only meetings, one-on-ones with colleagues, and recurring internal syncs. Identify for each external meeting: Company name Meeting date and time External attendee names and email addresses **Option B — No calendar connected:** Ask the user: "To build your weekly prep brief, I'll need your upcoming external calls. Please list them: company name, date/time, and attendee names." Accept freeform input and parse it into a structured list before proceeding. Step 2: Confirm the Meeting List Present the identified meetings to the user for confirmation before beginning research: > "Here are the external calls I found for this week. Let me know if anything's missing or should be excluded: > - [Company]...
- **산출물**: Weekly Prep Brief — Week of [Date]

## 원본 문서 구조

- Briefing Process
  - Step 1: Get the Week's External Meetings
  - Step 2: Confirm the Meeting List
  - Step 3: Research Each Meeting
  - Step 4: Synthesize the Weekly Brief
- Output Format
- Week Overview
- [Monday / Tuesday / etc.]
  - [Company Name] — [Time]
- When a Meeting Has Sparse Data
  - [Company Name] — [Time] ⚠️ Limited Data
- Quality Standards
- Reference Files

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/common-room/skills/weekly-prep-brief/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

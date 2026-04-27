# call-prep

## 요약

Prepare for a customer or prospect call using Common Room signals. Triggers on 'prep me for my call with [company]', 'prepare for a meeting with [company]', 'what should I know before talking to [company]', or any call preparation request.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/common-room |
| 원본 경로 | `knowledge-work-plugins/partner-built/common-room/skills/call-prep/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-common-room/call-prep-0d60d31.md` |

## 언제 쓰나

Prepare for a customer or prospect call using Common Room signals. Triggers on 'prep me for my call with [company]', 'prepare for a meeting with [company]', 'what should I know before talking to [company]', or any call preparation request.

## 주요 내용

- **진행 방식**: Step 1: Identify the Account and Attendees Parse what the user has provided: **Company name** — required; look up the account in Common Room **Attendee names** — optional; if provided, research each one **Calendar lookup:** If a `~~calendar` connector is available, search for upcoming meetings with the named company to automatically surface attendee names, meeting time, and any meeting notes or agenda. Use this to fill gaps the user didn't provide. If neither attendees nor a calendar match can be found, ask: "Who will be on the call from [Company]? I can research each attendee to make your prep more useful." Step 2: Run Account Research Use the account-research skill process to build a full account snapshot. For call prep, prioritize: Recent product signals (what are they doing in the product right now?) Open opportunities or renewal timeline Any risk signals (declining usage, support tickets, churned seats) Key recent events (funding, executive change, new hire) When reviewing activi...
- **산출물**: The output adapts to how much data Common Room returned. Only include sections where you have real data. Never fill a section with invented details. When data is rich (multiple field groups returned, activity history, scores, signals):

## 원본 문서 구조

- Prep Process
  - Step 1: Identify the Account and Attendees
  - Step 2: Run Account Research
  - Step 3: Run Contact Research for Each Attendee
  - Step 4: Synthesize Talking Points and Objectives
  - Step 5: Recency Check (Web Search)
- Output Format
  - When data is rich (multiple field groups returned, activity history, scores, signals):
- Call Prep: [Company] — [Date/Time if known]
  - Company Snapshot
  - Attendee Profiles
  - Signal Highlights
  - Talking Points
  - Likely Topics / Objections to Prepare For
  - Recommended Call Outcome
  - When data is sparse (few fields returned, no activity, null sparkSummary):
- Call Prep: [Company] — [Date/Time if known]
  - What I Found
  - Web Search Results
  - Suggested Next Steps
- Quality Standards
- Reference Files

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/common-room/skills/call-prep/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

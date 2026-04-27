# kb-article

## 요약

Draft a knowledge base article from a resolved issue or common question. Use when a ticket resolution is worth documenting for self-service, the same question keeps coming up, a workaround needs to be published, or a known issue should be communicated to customers.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | customer-support |
| 원본 경로 | `knowledge-work-plugins/customer-support/skills/kb-article/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/customer-support/kb-article-7b3416f.md` |
| 입력 힌트 | `<resolved issue or ticket>` |

## 언제 쓰나

Draft a knowledge base article from a resolved issue or common question. Use when a ticket resolution is worth documenting for self-service, the same question keeps coming up, a workaround needs to be published, or a known issue should be communicated to customers.

## 주요 내용

- **사용 방식**: /kb-article <resolved issue, ticket reference, or topic description> Examples: `/kb-article How to configure SSO with Okta — resolved this for 3 customers last month` `/kb-article Ticket #4521 — customer couldn't export data over 10k rows` `/kb-article Common question: how to set up webhook notifications` `/kb-article Known issue: dashboard charts not loading on Safari 16`
- **진행 방식**: 1. Understand the Source Material Parse the input to identify: **What was the problem?** The original issue, question, or error **What was the solution?** The resolution, workaround, or answer **Who does this affect?** User type, plan level, or configuration **How common is this?** One-off or recurring issue **What article type fits best?** How-to, troubleshooting, FAQ, known issue, or reference (see article types below) If a ticket reference is provided, look up the full context: **~~support platform**: Pull the ticket thread, resolution, and any internal notes **~~knowledge base**: Check if a similar article already exists (update vs. create new) **~~project tracker**: Check if there's a related bug or feature request 2. Draft the Article Using the article structure, formatting standards, and searchability best practices below: Follow the template for the chosen article type (how-to, troubleshooting, FAQ, known issue, or reference) Apply the searchability best practices: customer-la...

## 원본 문서 구조

- Usage
- Workflow
  - 1. Understand the Source Material
  - 2. Draft the Article
  - 3. Generate the Article
- KB Article Draft
  - Publishing Notes
  - 4. Offer Next Steps
- Article Structure and Formatting Standards
  - Universal Article Elements
  - Formatting Rules
- Writing for Searchability
  - Title Best Practices
  - Keyword Optimization
  - Opening Sentence Formula
- Article Type Templates
  - How-to Articles
- Prerequisites
- Steps
  - 1. [Action]
  - 2. [Action]
- Verify It Worked
- Common Issues
- Related Articles
  - Troubleshooting Articles
- Symptoms
- Cause
- Solution
  - Option 1: [Primary fix]
  - Option 2: [Alternative if Option 1 doesn't work]
- Prevention
- Still Having Issues?
  - FAQ Articles
- Details
- Related Questions
  - Known Issue Articles

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/customer-support/skills/kb-article/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

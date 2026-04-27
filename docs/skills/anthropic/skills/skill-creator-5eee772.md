# skill-creator

## 요약

Create new skills, modify and improve existing skills, and measure skill performance. Use when users want to create a skill from scratch, edit, or optimize an existing skill, run evals to test a skill, benchmark skill performance with variance analysis, or optimize a skill's description for better triggering accuracy.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Anthropic Skills |
| 영역 | skills |
| 원본 경로 | `skills/skills/skill-creator/SKILL.md` |
| 상세 파일 | `docs/skills/anthropic/skills/skill-creator-5eee772.md` |

## 언제 쓰나

Create new skills, modify and improve existing skills, and measure skill performance. Use when users want to create a skill from scratch, edit, or optimize an existing skill, run evals to test a skill, benchmark skill performance with variance analysis, or optimize a skill's description for better triggering accuracy.

## 주요 내용

- 원본 설명과 문서 구조를 기준으로 필요한 시점에 참조합니다.

## 원본 문서 구조

- Communicating with the user
- Creating a skill
  - Capture Intent
  - Interview and Research
  - Write the SKILL.md
  - Skill Writing Guide
    - Anatomy of a Skill
    - Progressive Disclosure
    - Principle of Lack of Surprise
    - Writing Patterns
- Report structure
- Executive summary
- Key findings
- Recommendations
- Commit message format
  - Writing Style
  - Test Cases
- Running and evaluating test cases
  - Step 1: Spawn all runs (with-skill AND baseline) in the same turn
  - Step 2: While runs are in progress, draft assertions
  - Step 3: As runs complete, capture timing data
  - Step 4: Grade, aggregate, and launch the viewer
  - What the user sees in the viewer
  - Step 5: Read the feedback
- Improving the skill
  - How to think about improvements
  - The iteration loop
- Advanced: Blind comparison
- Description Optimization
  - Step 1: Generate trigger eval queries
  - Step 2: Review with user
  - Step 3: Run the optimization loop
  - How skill triggering works
  - Step 4: Apply the result
  - Package and Present (only if `present_files` tool is available)
- Claude.ai-specific instructions

## 관리 메모

- 이 문서는 원본 `skills/skills/skill-creator/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

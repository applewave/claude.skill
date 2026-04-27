# sf-testing

## 요약

Apex test execution, coverage analysis, and test-fix loops with 120-point scoring. TRIGGER when: user runs Apex tests, checks code coverage, fixes failing tests, or touches *Test.cls / *_Test.cls files. DO NOT TRIGGER when: writing Apex production code (use sf-apex), Agentforce agent testing (use sf-ai-agentforce-testing), or Jest/LWC tests (use sf-lwc).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-testing/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-testing-396bd91.md` |
| 라이선스 | MIT |

## 언제 쓰나

Apex test execution, coverage analysis, and test-fix loops with 120-point scoring. TRIGGER when: user runs Apex tests, checks code coverage, fixes failing tests, or touches *Test.cls / *_Test.cls files. DO NOT TRIGGER when: writing Apex production code (use sf-apex), Agentforce agent testing (use sf-ai-agentforce-testing), or Jest/LWC tests (use sf-lwc).

## 주요 내용

- **진행 방식**: 1. Discover test scope Identify: existing test classes target production classes test data factories / setup helpers 2. Run the smallest useful test set first Start narrow when debugging a failure; widen only after the fix is stable. 3. Analyze results Focus on: failing methods exception types and stack traces uncovered lines / weak coverage areas whether failures indicate bad test data, brittle assertions, or broken production logic 4. Run a disciplined fix loop When the issue is code or test quality: delegate code fixes to [sf-apex](../sf-apex/SKILL.md) when needed add or improve tests rerun focused tests before broader regression 5. Improve coverage intentionally Cover: positive path negative / exception path bulk path (251+ records where appropriate) callout or async path when relevant
- **산출물**: When finishing, report in this order: **What tests were run** **Pass/fail summary** **Coverage result** **Root-cause findings** **Fix or next-run recommendation** Suggested shape: Test run: <scope> Org: <alias> Result: <passed / partial / failed> Coverage: <percent / key classes> Issues: <highest-signal failures> Next step: <fix class, add test, rerun scope, or widen regression>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Discover test scope
  - 2. Run the smallest useful test set first
  - 3. Analyze results
  - 4. Run a disciplined fix loop
  - 5. Improve coverage intentionally
- High-Signal Rules
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Specialized guidance
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-testing/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

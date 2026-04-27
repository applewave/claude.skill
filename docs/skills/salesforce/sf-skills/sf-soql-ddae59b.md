# sf-soql

## 요약

SOQL query generation, optimization, and analysis with 100-point scoring. TRIGGER when: user writes, optimizes, or debugs SOQL/SOSL queries, touches .soql files, or asks about relationship queries, aggregates, or query performance. DO NOT TRIGGER when: bulk data operations (use sf-data), Apex DML logic (use sf-apex), or report/dashboard queries.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-soql/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-soql-ddae59b.md` |
| 라이선스 | MIT |

## 언제 쓰나

SOQL query generation, optimization, and analysis with 100-point scoring. TRIGGER when: user writes, optimizes, or debugs SOQL/SOSL queries, touches .soql files, or asks about relationship queries, aggregates, or query performance. DO NOT TRIGGER when: bulk data operations (use sf-data), Apex DML logic (use sf-apex), or report/dashboard queries.

## 주요 내용

- **진행 방식**: 1. Generate the simplest correct query Prefer: only needed fields clear WHERE criteria reasonable LIMIT when appropriate relationship depth only as deep as necessary 2. Choose the right query shape 3. Optimize for selectivity and safety Check: indexed / selective filters no unnecessary fields no avoidable wildcard or scan-heavy patterns security enforcement expectations 4. Validate execution path if needed If the user wants runtime verification, hand off execution to: [sf-data](../sf-data/SKILL.md)
- **산출물**: When finishing, report in this order: **Query purpose** **Final SOQL/SOSL** **Why this shape was chosen** **Optimization or security notes** **Execution suggestion if needed** Suggested shape: Query goal: <summary> Query: <soql or sosl> Design: <relationship / aggregate / filter choices> Notes: <selectivity, limits, security, governor awareness> Next step: <run in sf-data or embed in Apex>

## 원본 문서 구조

- When This Skill Owns the Task
- Required Context to Gather First
- Recommended Workflow
  - 1. Generate the simplest correct query
  - 2. Choose the right query shape
  - 3. Optimize for selectivity and safety
  - 4. Validate execution path if needed
- High-Signal Rules
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Specialized guidance
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-soql/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# sf-ai-agentforce-observability

## 요약

Agentforce session tracing extraction and analysis. TRIGGER when: user extracts STDM data from Data Cloud, analyzes agent session traces, debugs agent conversations via telemetry, or works with .parquet files from Agentforce. DO NOT TRIGGER when: testing agents (use sf-ai-agentforce-testing), Apex debug logs (use sf-debug), or building agents (use sf-ai-agentforce).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Salesforce Skills |
| 영역 | sf-skills |
| 원본 경로 | `sf-skills/skills/sf-ai-agentforce-observability/SKILL.md` |
| 상세 파일 | `docs/skills/salesforce/sf-skills/sf-ai-agentforce-observability-5f146b0.md` |
| 라이선스 | MIT |

## 언제 쓰나

Agentforce session tracing extraction and analysis. TRIGGER when: user extracts STDM data from Data Cloud, analyzes agent session traces, debugs agent conversations via telemetry, or works with .parquet files from Agentforce. DO NOT TRIGGER when: testing agents (use sf-ai-agentforce-testing), Apex debug logs (use sf-debug), or building agents (use sf-ai-agentforce).

## 주요 내용

- **진행 방식**: 1. Verify setup and auth Confirm Data 360 tracing exists and JWT/ECA auth is working. 2. Choose the extraction mode 3. Extract to Parquet Use the provided scripts under `scripts/` rather than reimplementing extraction logic. 4. Analyze with Polars Common analysis goals: session volume and duration topic distribution action step failures latency hotspots abandonment / escalation patterns session-level timeline reconstruction 5. Convert findings into next actions Typical outcomes: topic mismatch → improve routing or descriptions action failure → inspect Flow / Apex implementation latency issue → optimize downstream action path test gap → add targeted agent tests
- **산출물**: When finishing, report in this order: **What data was extracted or analyzed** **Scope** (org, dates, agent filter, session IDs) **Key findings** **Likely root causes** **Recommended next skill / next action** Suggested shape: Observability task: <extract / analyze / debug-session> Scope: <org, dates, agents, session ids> Artifacts: <directories / parquet files> Findings: <latency, routing, action, quality, abandonment patterns> Root cause: <best current explanation> Next step: <testing, agent fix, flow fix, apex fix>

## 원본 문서 구조

- When This Skill Owns the Task
- Prerequisites That Must Exist
- What This Skill Works With
  - Core storage / analysis model
  - Core STDM entities
- Required Context to Gather First
- Recommended Workflow
  - 1. Verify setup and auth
  - 2. Choose the extraction mode
  - 3. Extract to Parquet
  - 4. Analyze with Polars
  - 5. Convert findings into next actions
- High-Signal Operational Rules
- Output Format
- Cross-Skill Integration
- Reference Map
  - Start here
  - Data model / querying
  - Analysis / debugging
  - Auth / troubleshooting
- Score Guide

## 관리 메모

- 이 문서는 원본 `sf-skills/skills/sf-ai-agentforce-observability/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

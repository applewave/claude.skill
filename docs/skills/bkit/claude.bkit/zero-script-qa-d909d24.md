# zero-script-qa

## 요약

Zero Script QA - Testing methodology without test scripts. Uses structured JSON logging and real-time Docker monitoring for verification. Use proactively when user needs to verify features through log analysis instead of test scripts. Triggers: zero script qa, log-based testing, docker logs, 제로 스크립트 QA, ゼロスクリプトQA, 零脚本QA, QA sin scripts, pruebas basadas en logs, registros de docker, QA sans script, tests basés sur les logs, journaux docker, skriptloses QA, log-basiertes Testen, Docker-Logs, QA senza script, test basati sui log, log docker Do NOT use for: unit testing, static analysis, or projects without Docker setup.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/zero-script-qa/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/zero-script-qa-d909d24.md` |

## 언제 쓰나

Zero Script QA - Testing methodology without test scripts. Uses structured JSON logging and real-time Docker monitoring for verification. Use proactively when user needs to verify features through log analysis instead of test scripts. Triggers: zero script qa, log-based testing, docker logs, 제로 스크립트 QA, ゼロスクリプトQA, 零脚本QA, QA sin scripts, pruebas basadas en logs, registros de docker, QA sans script, tests basés sur les logs, journaux docker, skriptloses QA, log-basiertes Testen, Docker-Logs, QA senza script, test basati sui log, log docker Do NOT use for: unit testing, static analysis, or projects without Docker setup.

## 주요 내용

- **진행 방식**: 1. Log Everything All API calls (including 200 OK) All errors All important business events Entire flow trackable via Request ID 2. Structured JSON Logs Parseable JSON format Consistent fields (timestamp, level, request_id, message, data) Different log levels per environment 3. Real-time Monitoring Docker log streaming Claude Code analyzes in real-time Immediate issue detection and documentation

## 원본 문서 구조

- Overview
- Core Principles
  - 1. Log Everything
  - 2. Structured JSON Logs
  - 3. Real-time Monitoring
- Logging Architecture
  - JSON Log Format Standard
  - Required Log Fields
  - Log Level Policy
- Request ID Propagation
  - Concept
  - Implementation Patterns
    - 1. Request ID Generation (Entry Point)
    - 2. Request ID Extraction and Propagation
- Backend Logging (FastAPI)
  - Logging Middleware
  - Business Logic Logging
- Frontend Logging (Next.js)
  - Logger Module
  - API Client Integration
- Nginx JSON Logging
  - nginx.conf Configuration
- Docker-Based QA Workflow
  - docker-compose.yml Configuration
  - Real-time Log Monitoring
- QA Automation Workflow
  - 1. Start Environment
  - 2. Manual UX Testing
  - 3. Claude Code Log Analysis
  - 4. Issue Documentation
- Issues Found
  - ISSUE-001: Insufficient error handling on login failure
- Issue Detection Patterns
  - 1. Error Detection
  - 2. Slow Response Detection
  - 3. Consecutive Failure Detection

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/zero-script-qa/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

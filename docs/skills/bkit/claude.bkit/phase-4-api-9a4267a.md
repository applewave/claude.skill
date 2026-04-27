# phase-4-api

## 요약

Skill for designing and implementing backend APIs. Includes Zero Script QA methodology for validating APIs without test scripts. Use proactively when user needs to design or implement backend APIs. Triggers: API design, REST API, backend, endpoint, API 설계, API設計, API设计, diseño de API, diseño API, diseño de backend, conception API, conception d'API, backend, API-Design, API-Entwurf, Backend, progettazione API, design API, backend Do NOT use for: frontend-only projects, static websites, or Starter level projects.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/phase-4-api/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/phase-4-api-9a4267a.md` |
| 사용자 호출 | false |

## 언제 쓰나

Skill for designing and implementing backend APIs. Includes Zero Script QA methodology for validating APIs without test scripts. Use proactively when user needs to design or implement backend APIs. Triggers: API design, REST API, backend, endpoint, API 설계, API設計, API设计, diseño de API, diseño API, diseño de backend, conception API, conception d'API, backend, API-Design, API-Entwurf, Backend, progettazione API, design API, backend Do NOT use for: frontend-only projects, static websites, or Starter level projects.

## 주요 내용

- **진행 방식**: What is REST? **RE**presentational **S**tate **T**ransfer - an architecture style for designing web services. 6 Core Principles Uniform Interface Details The core of RESTful APIs is a **uniform interface**. 1. Resource-Based URLs ✅ Good (nouns, plural) GET /users # User list GET /users/123 # Specific user POST /users # Create user PUT /users/123 # Update user DELETE /users/123 # Delete user ❌ Bad (using verbs) GET /getUsers POST /createUser POST /deleteUser/123 2. HTTP Method Meanings > **Idempotent**: Same result even if requested multiple times > **Safe**: Doesn't change server state 3. HTTP Status Codes 2xx Success ├── 200 OK # Success (read, update) ├── 201 Created # Creation success └── 204 No Content # Success but no response body (delete) 4xx Client Error ├── 400 Bad Request # Invalid request (validation failure) ├── 401 Unauthorized # Authentication required ├── 403 Forbidden # No permission
- **산출물**: docs/02-design/ └── api-spec.md # API specification src/api/ # API implementation ├── routes/ ├── controllers/ └── services/ docs/03-analysis/ └── api-qa.md # QA results

## 원본 문서 구조

- Purpose
- What to Do in This Phase
- Deliverables
- PDCA Application
- Level-wise Application
  - Dynamic Level: bkend.ai BaaS API Implementation
    - Step 1: MCP Setup
    - Step 2: Table Design (via MCP tools)
    - Step 3: Service API Integration
    - Step 4: Auth Implementation
    - Step 5: Zero Script QA
- What is Zero Script QA?
- RESTful API Principles
  - What is REST?
  - 6 Core Principles
  - Uniform Interface Details
    - 1. Resource-Based URLs
    - 2. HTTP Method Meanings
    - 3. HTTP Status Codes
    - 4. Consistent Response Format
  - URL Design Rules
  - API Documentation Tools
- API Design Checklist
- Templates
- Next Phase

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/phase-4-api/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

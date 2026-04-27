# phase-6-ui-integration

## 요약

Skill for implementing actual UI and integrating with APIs. Covers frontend-backend integration, state management, and API client architecture. Use proactively when user needs to connect frontend with backend APIs. Triggers: UI implementation, API integration, state management, UI 구현, API連携, 状态管理, implementación UI, integración API, gestión de estado, implémentation UI, intégration API, gestion d'état, UI-Implementierung, API-Integration, Zustandsverwaltung, implementazione UI, integrazione API, gestione dello stato Do NOT use for: mockup creation, backend-only development, or design system setup.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/phase-6-ui-integration/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/phase-6-ui-integration-27686a7.md` |
| 사용자 호출 | false |

## 언제 쓰나

Skill for implementing actual UI and integrating with APIs. Covers frontend-backend integration, state management, and API client architecture. Use proactively when user needs to connect frontend with backend APIs. Triggers: UI implementation, API integration, state management, UI 구현, API連携, 状态管理, implementación UI, integración API, gestión de estado, implémentation UI, intégration API, gestion d'état, UI-Implementierung, API-Integration, Zustandsverwaltung, implementazione UI, integrazione API, gestione dello stato Do NOT use for: mockup creation, backend-only development, or design system setup.

## 주요 내용

- **산출물**: src/ ├── pages/ # Page components │ ├── index.tsx │ ├── login.tsx │ └── ... ├── features/ # Feature-specific components │ ├── auth/ │ ├── product/ │ └── ... └── hooks/ # API call hooks ├── useAuth.ts └── useProducts.ts docs/03-analysis/ └── ui-qa.md # QA results

## 원본 문서 구조

- Purpose
- What to Do in This Phase
- Deliverables
- PDCA Application
- Level-wise Application
- API Client Architecture
  - Why is a Centralized API Client Needed?
  - 3-Layer API Client Structure
  - Folder Structure
- API Client Implementation
  - 1. Basic API Client (lib/api/client.ts)
  - 2. Common Type Definitions (types/api.types.ts)
- Service Layer Pattern
  - Domain-specific Service Separation
- Error Handling Pattern
  - Global Error Handler
  - Error Handling in Hooks
- Client-Server Type Sharing
  - Methods for Type Consistency
  - Type Definition Example
- API Integration Patterns
  - Basic Pattern (fetch)
  - React Query Pattern
  - SWR Pattern
- State Management Guide
- Zero Script QA Application
- API Integration Checklist
  - Architecture
  - Error Handling
  - Coding Conventions
- Template
- Next Phase

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/phase-6-ui-integration/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Claude Code에서 사용할 스킬, 커맨드, 플러그인을 모아두는 개인 라이브러리 프로젝트. 필요할 때 꺼내 쓰기 위한 용도.

현재 포함된 주요 컴포넌트:

1. **Figma Skills & Commands** — Figma MCP 연동 디자인-to-코드 워크플로우
2. **bkit (Vibecoding Kit v1.5.5)** — PDCA 방법론 기반 AI 네이티브 개발 프레임워크 (Claude Code 플러그인)
3. **Problem-Based-SRS** — 문제 기반 소프트웨어 요구사항 명세 방법론 (클론된 외부 저장소)

## Architecture

### Three-Layer Context Engineering (bkit)

- **Layer 1: Domain Knowledge** — 27개 Skills (`claude.bkit/skills/`)
- **Layer 2: Behavioral Rules** — 16개 Agents (`claude.bkit/agents/`)
- **Layer 3: State Management** — 241 함수, 5개 라이브러리 모듈 (`claude.bkit/lib/`)

### 5-Layer Hook System

10개 Hook 이벤트를 45개 Node.js 스크립트로 처리:
```
hooks.json → Skill Frontmatter → Agent Frontmatter → Description Triggers → Scripts
```

핵심 이벤트: `SessionStart`(초기화), `PreToolUse`(가드레일), `PostToolUse`(상태 진행), `Stop`(정리), `UserPromptSubmit`(의도 감지)

### PDCA Workflow

Plan → Design → Do → Check(analyze) → Act(iterate) 사이클. Match Rate 90% 이상 달성까지 최대 5회 자동 반복. 상태는 `.pdca-status.json`에 영속화.

### Project Level Auto-Detection

- **Enterprise**: `kubernetes/`, `terraform/`, `k8s/`, `infra/` 디렉토리 감지
- **Dynamic**: `lib/bkend/`, `supabase/`, `api/`, `docker-compose.yml` 감지
- **Starter**: 기본값

레벨에 따라 기본 에이전트, 팀 규모(Dynamic: 3, Enterprise: 5), 출력 스타일, 오케스트레이션 패턴이 자동 결정됨.

## Key Configuration

- **`claude.bkit/bkit.config.json`** — 중앙 설정: PDCA, 태스크 분류, 레벨 감지, 네이밍 컨벤션, 권한, 팀 오케스트레이션
- **`claude.bkit/plugin.json`** — 플러그인 메타데이터
- **`claude.bkit/hooks.json`** — Hook 이벤트 핸들러 정의

## Library Modules (`claude.bkit/lib/`)

| 모듈 | 함수 수 | 역할 |
|------|---------|------|
| `core/` | 41 | 플랫폼 감지, I/O, 캐싱, 설정 로딩, 파일 분류, 디버그 |
| `pdca/` | 54 | 티어/레벨 감지, 페이즈 관리, 상태 영속화, 자동 진행 |
| `intent/` | 24 | 8개 언어 감지, 트리거 매칭, 모호성 분석 |
| `task/` | 19 | 태스크 분류/생성/추적 (50개 링 버퍼) |
| `team/` | 23 | 에이전트 팀 조율, CTO 로직, 메시지 큐, 워크로드 밸런싱 |

보조 모듈: `context-hierarchy.js`(4계층 컨텍스트), `import-resolver.js`(템플릿 변수 치환), `permission-manager.js`(접근 제어), `skill-orchestrator.js`(스킬 파싱)

## Figma Workflow

### Skills
- **`skill.figma/`** — Figma MCP 기본: `get_design_context` → `get_metadata` → `get_screenshot` → 구현 → 검증
- **`skill.figma-implement-design/`** — 7단계 디자인-to-코드 변환 (노드 ID 추출 → 디자인 데이터 → 스크린샷 → 에셋 → 코드 → 패리티 → 검증)

### Slash Commands (`commands.figma/`)
- `/analyze <page> [nodeId]` — Figma 분석 → SPEC.md 생성
- `/new-page <page> <korean-name> <section>` — 페이지 스캐폴딩
- `/publish <page>` — 분석 → 문서화 → 구현 → 검증 → 커밋 (5단계)
- `/verify <page>` — 빌드 → Puppeteer 스크린샷 → Figma 비교

## Development Notes

- **빌드 시스템 없음** — Hook 스크립트는 Node.js 직접 실행
- **요구사항**: Claude Code v2.1.33+, Node.js v18+
- **테스트**: `claude.bkit/jest.config.js` (Jest, 30s timeout), 테스트 디렉토리 `test-scripts/`
- **8개 언어 지원**: EN, KO, JA, ZH, ES, FR, DE, IT (키워드 기반 자동 감지)
- **디버그 로그**: `.bkit/debug.log`에 구조화된 로그 기록
- **런타임 상태 파일**: `.pdca-status.json`, `.bkit/tasks.json`, `.bkit/agent-state.json`

## Coding Conventions (bkit)

| 대상 | 규칙 |
|------|------|
| 컴포넌트 | PascalCase |
| 함수 | camelCase |
| 상수 | UPPER_SNAKE_CASE |
| 파일 | kebab-case |

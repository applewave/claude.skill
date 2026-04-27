# claude.skill

Codex와 Claude Code에서 재사용할 **스킬, 커맨드, 플러그인**을 모아둔 개인 라이브러리입니다. Figma 디자인 구현, PDCA 개발 프레임워크, Karpathy식 코딩 가이드라인, 요구사항 명세, 업무 도메인별 지식 작업, Salesforce 개발 스킬을 한 곳에서 관리합니다.

## 목차

| 문서 | 내용 |
|---|---|
| [스킬 카탈로그](docs/skill-catalog.md) | 전체 소스와 스킬 수 요약 |
| [Figma Skills](docs/figma-skills.md) | Figma MCP 기반 디자인 분석, 구현, 검증 워크플로우입니다. |
| [bkit Skills](docs/bkit-skills.md) | PDCA 기반 AI 네이티브 개발 프레임워크입니다. |
| [Karpathy Guidelines Skills](docs/karpathy-guidelines-skills.md) | LLM 코딩 실수를 줄이기 위한 Karpathy식 행동 가이드라인입니다. |
| [Problem-Based SRS Skills](docs/problem-based-srs-skills.md) | 비즈니스 문제에서 요구사항까지 추적하는 문제 기반 SRS 방법론입니다. |
| [Anthropic Skills](docs/anthropic-skills.md) | Anthropic 공식 범용 스킬 모음입니다. |
| [Knowledge Work Plugin Skills](docs/knowledge-work-plugin-skills.md) | 업무 도메인별 지식 작업 플러그인과 스킬입니다. |
| [Matt Pocock Skills](docs/mattpocock-skills.md) | PRD, 이슈 분해, TDD, 코드베이스 개선 워크플로우입니다. |
| [Salesforce Skills](docs/salesforce-skills.md) | Salesforce, Agentforce, Data Cloud, OmniStudio 개발 스킬입니다. |
| [Spec Kit Brownfield Extension Skills](docs/spec-kit-brownfield-skills.md) | 기존 시스템에 Spec Kit 방식을 적용하기 위한 확장 스킬입니다. |
| [Commands](docs/commands.md) | 로컬 slash command 목록 |
| [스킬별 상세 색인](docs/skills/README.md) | 개별 스킬 상세 문서 모음 |

## 구성 요약

| 위치 | 설명 |
|---|---|
| `skill.figma`, `skill.figma-implement-design` | Figma MCP 기반 디자인 분석, 구현, 검증 워크플로우입니다. (3개 스킬) |
| `claude.bkit` | PDCA 기반 AI 네이티브 개발 프레임워크입니다. (27개 스킬) |
| `andrej-karpathy-skills` | LLM 코딩 실수를 줄이기 위한 Karpathy식 행동 가이드라인입니다. (1개 스킬) |
| `Problem-Based-SRS` | 비즈니스 문제에서 요구사항까지 추적하는 문제 기반 SRS 방법론입니다. (9개 스킬) |
| `skills` | Anthropic 공식 범용 스킬 모음입니다. (18개 스킬) |
| `knowledge-work-plugins` | 업무 도메인별 지식 작업 플러그인과 스킬입니다. (181개 스킬) |
| `mattpocock-skills` | PRD, 이슈 분해, TDD, 코드베이스 개선 워크플로우입니다. (19개 스킬) |
| `sf-skills` | Salesforce, Agentforce, Data Cloud, OmniStudio 개발 스킬입니다. (36개 스킬) |
| `spec-kit-brownfield-extensions` | 기존 시스템에 Spec Kit 방식을 적용하기 위한 확장 스킬입니다. (2개 스킬) |
| `commands/`, `commands.figma/` | 분석, 페이지 생성, 퍼블리시, 검증 커맨드 |

## 문서 구조

| 위치 | 역할 |
|---|---|
| `README.md` | 저장소 전체 진입점 |
| `docs/skill-catalog.md` | 전체 분류 요약과 전체 스킬 색인 |
| `docs/*-skills.md` | 분류별 스킬 목록과 상세 문서 링크 |
| `docs/skills/` | 스킬별 개별 상세 문서 |

## 관리 방식

외부 저장소 기반 폴더는 서브모듈로 관리합니다. 이 저장소에서는 각 외부 소스의 현재 커밋 포인터와 문서화된 카탈로그를 함께 관리합니다.

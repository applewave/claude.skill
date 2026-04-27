# improve-codebase-architecture

## 요약

Explore a codebase to find opportunities for architectural improvement, focusing on making the codebase more testable by deepening shallow modules. Use when user wants to improve architecture, find refactoring opportunities, consolidate tightly-coupled modules, or make a codebase more AI-navigable.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/improve-codebase-architecture/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/improve-codebase-architecture-75a2551.md` |

## 언제 쓰나

Explore a codebase to find opportunities for architectural improvement, focusing on making the codebase more testable by deepening shallow modules. Use when user wants to improve architecture, find refactoring opportunities, consolidate tightly-coupled modules, or make a codebase more AI-navigable.

## 주요 내용

- **진행 방식**: 1. Explore the codebase Use the Agent tool with subagent_type=Explore to navigate the codebase naturally. Do NOT follow rigid heuristics — explore organically and note where you experience friction: Where does understanding one concept require bouncing between many small files? Where are modules so shallow that the interface is nearly as complex as the implementation? Where have pure functions been extracted just for testability, but the real bugs hide in how they're called? Where do tightly-coupled modules create integration risk in the seams between them? Which parts of the codebase are untested, or hard to test? The friction you encounter IS the signal. 2. Present candidates Present a numbered list of deepening opportunities. For each candidate, show: **Cluster**: Which modules/concepts are involved **Why they're coupled**: Shared types, call patterns, co-ownership of a concept **Dependency category**: See [REFERENCE.md](REFERENCE.md) for the four categories **Test impact**: What e...

## 원본 문서 구조

- Process
  - 1. Explore the codebase
  - 2. Present candidates
  - 3. User picks a candidate
  - 4. Frame the problem space
  - 5. Design multiple interfaces
  - 6. User picks an interface (or accepts recommendation)
  - 7. Create GitHub issue

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/improve-codebase-architecture/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

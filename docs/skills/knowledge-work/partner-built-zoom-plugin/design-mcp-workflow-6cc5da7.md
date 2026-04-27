# design-mcp-workflow

## 요약

Design a Zoom MCP workflow for Claude. Use when deciding whether Zoom MCP fits a task, when planning tool-based AI workflows, or when separating MCP responsibilities from REST API responsibilities.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/design-mcp-workflow/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/design-mcp-workflow-6cc5da7.md` |
| 사용자 호출 | false |

## 언제 쓰나

Design a Zoom MCP workflow for Claude. Use when deciding whether Zoom MCP fits a task, when planning tool-based AI workflows, or when separating MCP responsibilities from REST API responsibilities.

## 주요 내용

- **진행 방식**: Decide whether the problem is agentic tooling, deterministic automation, or both. Route MCP-only tasks to [zoom-mcp](../zoom-mcp/SKILL.md). Route hybrid tasks to both [zoom-mcp](../zoom-mcp/SKILL.md) and [rest-api](../rest-api/SKILL.md). If Whiteboard is central, route to [zoom-mcp/whiteboard](../zoom-mcp/whiteboard/SKILL.md). Call out transport, auth, and client capability assumptions explicitly.

## 원본 문서 구조

- Covers
- Workflow
- Common Mistakes

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/design-mcp-workflow/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

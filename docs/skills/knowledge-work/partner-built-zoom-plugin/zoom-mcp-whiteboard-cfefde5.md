# zoom-mcp/whiteboard

## 요약

Guidance for the bundled Zoom Whiteboard MCP connector. Use for Whiteboard MCP auth, endpoints, ID mapping, and tool workflows such as list_whiteboards and get_a_whiteboard. Prefer this skill when the request is specifically about Whiteboard MCP rather than general Zoom MCP.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/zoom-mcp/whiteboard/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/zoom-mcp-whiteboard-cfefde5.md` |
| 사용자 호출 | false |

## 언제 쓰나

Guidance for the bundled Zoom Whiteboard MCP connector. Use for Whiteboard MCP auth, endpoints, ID mapping, and tool workflows such as list_whiteboards and get_a_whiteboard. Prefer this skill when the request is specifically about Whiteboard MCP rather than general Zoom MCP.

## 주요 내용

- **진행 방식**: Use a user OAuth token with the Whiteboard read scopes. Call `list_whiteboards` to discover accessible whiteboards and confirm the correct `whiteboard_id`. Call `get_a_whiteboard` with that `whiteboard_id`.

## 원본 문서 구조

- Endpoints
- Authentication
- Required Scopes
- Whiteboard ID Mapping
- Available Tools
- Read Workflow
- Chaining
- References

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/zoom-mcp/whiteboard/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

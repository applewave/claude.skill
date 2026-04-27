# zoom-mcp

## 요약

Guidance for the bundled Zoom MCP connectors. Use after routing to an MCP workflow when planning or troubleshooting tool-based access to meetings, recordings, meeting assets, or transcripts. Route Zoom Docs requests to the dedicated Docs MCP server and Whiteboard-specific requests to `zoom-mcp/whiteboard`.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/zoom-mcp/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/zoom-mcp-ce7be13.md` |
| 사용자 호출 | false |

## 언제 쓰나

Guidance for the bundled Zoom MCP connectors. Use after routing to an MCP workflow when planning or troubleshooting tool-based access to meetings, recordings, meeting assets, or transcripts. Route Zoom Docs requests to the dedicated Docs MCP server and Whiteboard-specific requests to `zoom-mcp/whiteboard`.

## 주요 내용

- **진행 방식**: **Search meeting content, then retrieve assets:** search_meetings q: "Q4 planning discussion" from: "2026-03-01" to: "2026-03-06" → choose a returned meeting → get_meeting_assets meetingId: "MEETING_ID_OR_UUID" **List recordings, then retrieve recording resources:** recordings_list userId: "me" from: "2026-03-01" to: "2026-03-06" → choose a recording target → get_recording_resource meetingId: "MEETING_UUID_OR_RECORDING_ID" **Create or fetch a Zoom Doc:** use the dedicated `zoom-docs-mcp` server rather than the main `zoom-mcp` server official documented tools on the Zoom Docs MCP page are: `create_file_with_content` `get_file_content`

## 원본 문서 구조

- Quick Start
- Critical Notes
- Server Endpoints
- Search and Retrieval Model
- Tool Catalog
- Key Workflows
- Error Reference
- Documentation
  - Concepts
  - Examples
  - References
  - Troubleshooting
  - Operations
- Related Skills

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/zoom-mcp/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

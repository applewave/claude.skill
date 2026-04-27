# mcp-builder

## 요약

Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools. Use when building MCP servers to integrate external APIs or services, whether in Python (FastMCP) or Node/TypeScript (MCP SDK).

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Anthropic Skills |
| 영역 | skills |
| 원본 경로 | `skills/skills/mcp-builder/SKILL.md` |
| 상세 파일 | `docs/skills/anthropic/skills/mcp-builder-083c136.md` |
| 라이선스 | Complete terms in LICENSE.txt |

## 언제 쓰나

Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools. Use when building MCP servers to integrate external APIs or services, whether in Python (FastMCP) or Node/TypeScript (MCP SDK).

## 주요 내용

- **진행 방식**: Creating a high-quality MCP server involves four main phases: Phase 1: Deep Research and Planning 1.1 Understand Modern MCP Design **API Coverage vs. Workflow Tools:** Balance comprehensive API endpoint coverage with specialized workflow tools. Workflow tools can be more convenient for specific tasks, while comprehensive coverage gives agents flexibility to compose operations. Performance varies by client—some clients benefit from code execution that combines basic tools, while others work better with higher-level workflows. When uncertain, prioritize comprehensive API coverage. **Tool Naming and Discoverability:** Clear, descriptive tool names help agents find the right tools quickly. Use consistent prefixes (e.g., `github_create_issue`, `github_list_repos`) and action-oriented naming. **Context Management:** Agents benefit from concise tool descriptions and the ability to filter/paginate results. Design tools that return focused, relevant data. Some clients support code execution wh...

## 원본 문서 구조

- Overview
- 🚀 High-Level Workflow
  - Phase 1: Deep Research and Planning
    - 1.1 Understand Modern MCP Design
    - 1.2 Study MCP Protocol Documentation
    - 1.3 Study Framework Documentation
    - 1.4 Plan Your Implementation
  - Phase 2: Implementation
    - 2.1 Set Up Project Structure
    - 2.2 Implement Core Infrastructure
    - 2.3 Implement Tools
  - Phase 3: Review and Test
    - 3.1 Code Quality
    - 3.2 Build and Test
  - Phase 4: Create Evaluations
    - 4.1 Understand Evaluation Purpose
    - 4.2 Create 10 Evaluation Questions
    - 4.3 Evaluation Requirements
    - 4.4 Output Format
- 📚 Documentation Library
  - Core MCP Documentation (Load First)
  - SDK Documentation (Load During Phase 1/2)
  - Language-Specific Implementation Guides (Load During Phase 2)
  - Evaluation Guide (Load During Phase 4)

## 관리 메모

- 이 문서는 원본 `skills/skills/mcp-builder/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

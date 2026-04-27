# figma-implement-design

## 요약

Translate Figma nodes into production-ready code with 1:1 visual fidelity using the Figma MCP workflow (design context, screenshots, assets, and project-convention translation). Trigger when the user provides Figma URLs or node IDs, or asks to implement designs or components that must match Figma specs. Requires a working Figma MCP server connection.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Figma Skills |
| 영역 | skill.figma-implement-design |
| 원본 경로 | `skill.figma-implement-design/SKILL.md` |
| 상세 파일 | `docs/skills/figma/skill.figma-implement-design/figma-implement-design-b78fd35.md` |

## 언제 쓰나

Translate Figma nodes into production-ready code with 1:1 visual fidelity using the Figma MCP workflow (design context, screenshots, assets, and project-convention translation). Trigger when the user provides Figma URLs or node IDs, or asks to implement designs or components that must match Figma specs. Requires a working Figma MCP server connection.

## 주요 내용

- **진행 방식**: **Follow these steps in order. Do not skip steps.** Step 0: Set up Figma MCP (if not already configured) If any MCP call fails because Figma MCP is not connected, pause and set it up: Add the Figma MCP: `codex mcp add figma --url https://mcp.figma.com/mcp` Enable remote MCP client: Set `[features].rmcp_client = true` in `config.toml` **or** run `codex --enable rmcp_client` Log in with OAuth: `codex mcp login figma` After successful login, the user will have to restart codex. You should finish your answer and tell them so when they try again they can continue with Step 1. Step 1: Get Node ID Option A: Parse from Figma URL When the user provides a Figma URL, extract the file key and node ID to pass as arguments to MCP tools. **URL format:** `https://figma.com/design/:fileKey/:fileName?node-id=1-2` **Extract:** **File key:** `:fileKey` (the segment after `/design/`) **Node ID:** `1-2` (the value of the `node-id` query parameter) **Note:** When using the local desktop MCP (`figma-desktop`...

## 원본 문서 구조

- Overview
- Prerequisites
- Required Workflow
  - Step 0: Set up Figma MCP (if not already configured)
  - Step 1: Get Node ID
    - Option A: Parse from Figma URL
    - Option B: Use Current Selection from Figma Desktop App (figma-desktop MCP only)
  - Step 2: Fetch Design Context
  - Step 3: Capture Visual Reference
  - Step 4: Download Required Assets
  - Step 5: Translate to Project Conventions
  - Step 6: Achieve 1:1 Visual Parity
  - Step 7: Validate Against Figma
- Implementation Rules
  - Component Organization
  - Design System Integration
  - Code Quality
- Examples
  - Example 1: Implementing a Button Component
  - Example 2: Building a Dashboard Layout
- Best Practices
  - Always Start with Context
  - Incremental Validation
  - Document Deviations
  - Reuse Over Recreation
  - Design System First
- Common Issues and Solutions
  - Issue: Figma output is truncated
  - Issue: Design doesn't match after implementation
  - Issue: Assets not loading
  - Issue: Design token values differ from Figma
- Understanding Design Implementation
- Additional Resources

## 관리 메모

- 이 문서는 원본 `skill.figma-implement-design/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# Anthropic Skills

Anthropic 공식 범용 스킬 모음입니다.

## 요약

- 스킬 수: 18
- 원본 위치: `skills`
- 스킬별 상세 문서: `docs/skills/anthropic/`

| 영역 | 스킬 수 | 상세 |
|---|---:|---|
| skills | 17 | [상세 폴더](skills/anthropic/skills/README.md) |
| template | 1 | [상세 폴더](skills/anthropic/template/README.md) |

## skills

| 스킬 | 설명 | 상세 | 원본 |
|---|---|---|---|
| `algorithmic-art` | Creating algorithmic art using p5.js with seeded randomness and interactive parameter exploration. Use this when users request creating art using code, generative art, algorithmic art, flow fields, or particle systems. Create original algorithmic art rather t... | [상세](skills/anthropic/skills/algorithmic-art-51b323a.md) | `skills/skills/algorithmic-art/SKILL.md` |
| `brand-guidelines` | Applies Anthropic's official brand colors and typography to any sort of artifact that may benefit from having Anthropic's look-and-feel. Use it when brand colors or style guidelines, visual formatting, or company design standards apply. | [상세](skills/anthropic/skills/brand-guidelines-20c35b9.md) | `skills/skills/brand-guidelines/SKILL.md` |
| `canvas-design` | Create beautiful visual art in .png and .pdf documents using design philosophy. You should use this skill when the user asks to create a poster, piece of art, design, or other static piece. Create original visual designs, never copying existing artists' work... | [상세](skills/anthropic/skills/canvas-design-ecce39d.md) | `skills/skills/canvas-design/SKILL.md` |
| `claude-api` | Build, debug, and optimize Claude API / Anthropic SDK apps. Apps built with this skill should include prompt caching. TRIGGER when: code imports anthropic/@anthropic-ai/sdk; user asks to use the Claude API, Anthropic SDKs, or Managed Agents (/v1/agents, /v1/s... | [상세](skills/anthropic/skills/claude-api-fd6cf59.md) | `skills/skills/claude-api/SKILL.md` |
| `doc-coauthoring` | Guide users through a structured workflow for co-authoring documentation. Use when user wants to write documentation, proposals, technical specs, decision docs, or similar structured content. This workflow helps users efficiently transfer context, refine cont... | [상세](skills/anthropic/skills/doc-coauthoring-809876d.md) | `skills/skills/doc-coauthoring/SKILL.md` |
| `docx` | Use this skill whenever the user wants to create, read, edit, or manipulate Word documents (.docx files). Triggers include: any mention of 'Word doc', 'word document', '.docx', or requests to produce professional documents with formatting like tables of conte... | [상세](skills/anthropic/skills/docx-cf35342.md) | `skills/skills/docx/SKILL.md` |
| `frontend-design` | Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks to build web components, pages, artifacts, posters, or applications (examples include websites, landing pages, dashboards, React components, H... | [상세](skills/anthropic/skills/frontend-design-a0fbc91.md) | `skills/skills/frontend-design/SKILL.md` |
| `internal-comms` | A set of resources to help me write all kinds of internal communications, using the formats that my company likes to use. Claude should use this skill whenever asked to write some sort of internal communications (status reports, leadership updates, 3P updates... | [상세](skills/anthropic/skills/internal-comms-76cbf10.md) | `skills/skills/internal-comms/SKILL.md` |
| `mcp-builder` | Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools. Use when building MCP servers to integrate external APIs or services, whether in Python (FastMCP) or Node/Typ... | [상세](skills/anthropic/skills/mcp-builder-083c136.md) | `skills/skills/mcp-builder/SKILL.md` |
| `pdf` | Use this skill whenever the user wants to do anything with PDF files. This includes reading or extracting text/tables from PDFs, combining or merging multiple PDFs into one, splitting PDFs apart, rotating pages, adding watermarks, creating new PDFs, filling P... | [상세](skills/anthropic/skills/pdf-e7a233e.md) | `skills/skills/pdf/SKILL.md` |
| `pptx` | Use this skill any time a .pptx file is involved in any way — as input, output, or both. This includes: creating slide decks, pitch decks, or presentations; reading, parsing, or extracting text from any .pptx file (even if the extracted content will be used e... | [상세](skills/anthropic/skills/pptx-b202f07.md) | `skills/skills/pptx/SKILL.md` |
| `skill-creator` | Create new skills, modify and improve existing skills, and measure skill performance. Use when users want to create a skill from scratch, edit, or optimize an existing skill, run evals to test a skill, benchmark skill performance with variance analysis, or op... | [상세](skills/anthropic/skills/skill-creator-5eee772.md) | `skills/skills/skill-creator/SKILL.md` |
| `slack-gif-creator` | Knowledge and utilities for creating animated GIFs optimized for Slack. Provides constraints, validation tools, and animation concepts. Use when users request animated GIFs for Slack like "make me a GIF of X doing Y for Slack. | [상세](skills/anthropic/skills/slack-gif-creator-6b42b83.md) | `skills/skills/slack-gif-creator/SKILL.md` |
| `theme-factory` | Toolkit for styling artifacts with a theme. These artifacts can be slides, docs, reportings, HTML landing pages, etc. There are 10 pre-set themes with colors/fonts that you can apply to any artifact that has been creating, or can generate a new theme on-the-f... | [상세](skills/anthropic/skills/theme-factory-c84c283.md) | `skills/skills/theme-factory/SKILL.md` |
| `web-artifacts-builder` | Suite of tools for creating elaborate, multi-component claude.ai HTML artifacts using modern frontend web technologies (React, Tailwind CSS, shadcn/ui). Use for complex artifacts requiring state management, routing, or shadcn/ui components - not for simple si... | [상세](skills/anthropic/skills/web-artifacts-builder-efd93ea.md) | `skills/skills/web-artifacts-builder/SKILL.md` |
| `webapp-testing` | Toolkit for interacting with and testing local web applications using Playwright. Supports verifying frontend functionality, debugging UI behavior, capturing browser screenshots, and viewing browser logs. | [상세](skills/anthropic/skills/webapp-testing-be6d819.md) | `skills/skills/webapp-testing/SKILL.md` |
| `xlsx` | Use this skill any time a spreadsheet file is the primary input or output. This means any task where the user wants to: open, read, edit, or fix an existing .xlsx, .xlsm, .csv, or .tsv file (e.g., adding columns, computing formulas, formatting, charting, clea... | [상세](skills/anthropic/skills/xlsx-a85ce5a.md) | `skills/skills/xlsx/SKILL.md` |

## template

| 스킬 | 설명 | 상세 | 원본 |
|---|---|---|---|
| `template-skill` | Replace with description of the skill and when Claude should use it. | [상세](skills/anthropic/template/template-skill-ce158f7.md) | `skills/template/SKILL.md` |

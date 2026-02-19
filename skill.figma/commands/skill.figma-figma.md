---
name: figma
description: |
  Figma MCP guide - How to translate Figma designs into production code.
  Covers integration rules, required flow, implementation rules, asset handling, and link-based prompting.

  Type "/figma" to see the Figma MCP guide.

  Triggers: figma, figma guide, figma help, figma mcp,
  design to code, figma implementation, figma setup
user-invocable: true
allowed-tools:
  - Read
---

# Figma MCP Guide

> Use the Figma MCP server to translate Figma designs into production code

Display the following guide:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  Figma MCP - Design to Code Guide
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

For setup and debugging, see references/figma-mcp-config.md

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Figma MCP Integration Rules

These rules define how to translate Figma inputs into code and must be followed for every Figma-driven change.

### Required Flow (do not skip)

| Step | Tool | Description |
|:----:|------|-------------|
| 1 | `get_design_context` | Fetch the structured representation for the exact node(s) |
| 2 | `get_metadata` (if needed) | If response is too large or truncated, get the high-level node map then re-fetch required nodes |
| 3 | `get_screenshot` | Get a visual reference of the node variant being implemented |
| 4 | Download assets | Only after steps 1-3, download needed assets and start implementation |
| 5 | Translate code | Convert output (React + Tailwind) to project conventions, styles, and framework |
| 6 | Validate | Verify 1:1 look and behavior against Figma before marking complete |

### Implementation Rules

| Rule | Description |
|------|-------------|
| MCP output | Treat Figma MCP output (React + Tailwind) as a design/behavior representation, not final code style |
| Tailwind replacement | Replace Tailwind utility classes with project's preferred utilities/design-system tokens |
| Component reuse | Reuse existing components (buttons, inputs, typography, icon wrappers) instead of duplicating |
| Token consistency | Use project's color system, typography scale, and spacing tokens consistently |
| Respect patterns | Respect existing routing, state management, and data-fetch patterns in the repo |
| Visual parity | Strive for 1:1 visual match with Figma design (prefer design-system tokens on conflict) |
| Final validation | Validate final UI against Figma screenshot for both look and behavior |

### Asset Handling

| Rule | Description |
|------|-------------|
| Assets endpoint | Figma MCP Server provides an endpoint to serve image and SVG assets |
| **localhost source** | If MCP Server returns a localhost source for an image/SVG, **use it directly** |
| **No icon packages** | DO NOT import/add new icon packages. All assets should be in the Figma payload |
| **No placeholders** | DO NOT use or create placeholders if a localhost source is provided |

### Link-based Prompting

| Item | Description |
|------|-------------|
| Link-based server | Copy the Figma frame/layer link and provide the URL to the MCP client |
| Node ID extraction | The client cannot browse the URL but extracts the node ID from the link |
| Exact link | Always ensure the link points to the exact node/variant you want |

## References

| Document | Content |
|----------|---------|
| `references/figma-mcp-config.md` | Setup, verification, troubleshooting, link-based usage reminders |
| `references/figma-tools-and-prompts.md` | Tool catalog and prompt patterns for frameworks/components and metadata |

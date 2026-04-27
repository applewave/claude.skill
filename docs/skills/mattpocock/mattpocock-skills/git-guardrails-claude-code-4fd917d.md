# git-guardrails-claude-code

## 요약

Set up Claude Code hooks to block dangerous git commands (push, reset --hard, clean, branch -D, etc.) before they execute. Use when user wants to prevent destructive git operations, add git safety hooks, or block git push/reset in Claude Code.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/git-guardrails-claude-code/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/git-guardrails-claude-code-4fd917d.md` |

## 언제 쓰나

Set up Claude Code hooks to block dangerous git commands (push, reset --hard, clean, branch -D, etc.) before they execute. Use when user wants to prevent destructive git operations, add git safety hooks, or block git push/reset in Claude Code.

## 주요 내용

- **진행 방식**: 1. Ask scope Ask the user: install for **this project only** (`.claude/settings.json`) or **all projects** (`~/.claude/settings.json`)? 2. Copy the hook script The bundled script is at: [scripts/block-dangerous-git.sh](scripts/block-dangerous-git.sh) Copy it to the target location based on scope: **Project**: `.claude/hooks/block-dangerous-git.sh` **Global**: `~/.claude/hooks/block-dangerous-git.sh` Make it executable with `chmod +x`. 3. Add hook to settings Add to the appropriate settings file: **Project** (`.claude/settings.json`): { "hooks": { "PreToolUse": [ { "matcher": "Bash", "hooks": [ { "type": "command", "command": "\"$CLAUDE_PROJECT_DIR\"/.claude/hooks/block-dangerous-git.sh" } ] } ] } } **Global** (`~/.claude/settings.json`): { "hooks": { "PreToolUse": [ { "matcher": "Bash", "hooks": [ { "type": "command", "command": "~/.claude/hooks/block-dangerous-git.sh" } ] } ] } } If the settings file already exists, merge the hook into existing `hooks.PreToolUse` array — don't overwr...

## 원본 문서 구조

- What Gets Blocked
- Steps
  - 1. Ask scope
  - 2. Copy the hook script
  - 3. Add hook to settings
  - 4. Ask about customization
  - 5. Verify

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/git-guardrails-claude-code/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

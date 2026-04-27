# obsidian-vault

## 요약

Search, create, and manage notes in the Obsidian vault with wikilinks and index notes. Use when user wants to find, create, or organize notes in Obsidian.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Matt Pocock Skills |
| 영역 | mattpocock-skills |
| 원본 경로 | `mattpocock-skills/obsidian-vault/SKILL.md` |
| 상세 파일 | `docs/skills/mattpocock/mattpocock-skills/obsidian-vault-2adb166.md` |

## 언제 쓰나

Search, create, and manage notes in the Obsidian vault with wikilinks and index notes. Use when user wants to find, create, or organize notes in Obsidian.

## 주요 내용

- **진행 방식**: Search for notes Search by filename find "/mnt/d/Obsidian Vault/AI Research/" -name "*.md" | grep -i "keyword" Search by content grep -rl "keyword" "/mnt/d/Obsidian Vault/AI Research/" --include="*.md" Or use Grep/Glob tools directly on the vault path. Create a new note Use **Title Case** for filename Write content as a unit of learning (per vault rules) Add `[[wikilinks]]` to related notes at the bottom If part of a numbered sequence, use the hierarchical numbering scheme Find related notes Search for `[[Note Title]]` across the vault to find backlinks: grep -rl "\\[\\[Note Title\\]\\]" "/mnt/d/Obsidian Vault/AI Research/" Find index notes find "/mnt/d/Obsidian Vault/AI Research/" -name "*Index*"

## 원본 문서 구조

- Vault location
- Naming conventions
- Linking
- Workflows
  - Search for notes
  - Create a new note
  - Find related notes
  - Find index notes

## 관리 메모

- 이 문서는 원본 `mattpocock-skills/obsidian-vault/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

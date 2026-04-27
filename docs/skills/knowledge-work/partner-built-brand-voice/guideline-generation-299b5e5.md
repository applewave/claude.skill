# guideline-generation

## 요약

This skill generates, creates, or builds brand voice guidelines from source materials. It should be used when the user asks to "generate brand guidelines", "create a style guide", "extract brand voice", "create guidelines from calls", "consolidate brand materials", "analyze my sales calls for brand voice", "build a brand playbook from documents", "synthesize a voice and tone guide", or uploads brand documents, transcripts, or meeting recordings for brand analysis. Also triggers when the user has a discovery report and wants to convert it into actionable guidelines.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/brand-voice |
| 원본 경로 | `knowledge-work-plugins/partner-built/brand-voice/skills/guideline-generation/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-brand-voice/guideline-generation-299b5e5.md` |

## 언제 쓰나

This skill generates, creates, or builds brand voice guidelines from source materials. It should be used when the user asks to "generate brand guidelines", "create a style guide", "extract brand voice", "create guidelines from calls", "consolidate brand materials", "analyze my sales calls for brand voice", "build a brand playbook from documents", "synthesize a voice and tone guide", or uploads brand documents, transcripts, or meeting recordings for brand analysis. Also triggers when the user has a discovery report and wants to convert it into actionable guidelines.

## 주요 내용

- **진행 방식**: 1. Identify and Classify Sources Determine what the user has provided. If no sources are available: Check if a discovery report exists from a previous `/brand-voice:discover-brand` run Check `.claude/brand-voice.local.md` for known brand material locations Suggest running discovery first: `/brand-voice:discover-brand` 2. Process Sources **For documents:** Delegate to the document-analysis agent for heavy parsing. Extract voice attributes, messaging themes, terminology, tone guidance, and examples. **For transcripts:** Delegate to the conversation-analysis agent for pattern recognition. Extract implicit voice attributes, successful language patterns, tone by context, and anti-patterns. **For discovery reports:** Extract pre-triaged sources, conflicts, and gaps. Use the ranked sources directly. 3. Synthesize Into Guidelines Merge all findings into a unified guideline document following the template in `references/guideline-template.md`. Key sections: **"We Are / We Are Not" Table** — Th...

## 원본 문서 구조

- Inputs
- Generation Workflow
  - 1. Identify and Classify Sources
  - 2. Process Sources
  - 3. Synthesize Into Guidelines
  - 4. Assign Confidence Scores
  - 5. Surface Open Questions
- Open Questions for Team Discussion
  - High Priority (blocks guideline completion)
  - 6. Quality Check
  - 7. Present and Offer Next Steps
  - 8. Save for Future Sessions
- Privacy and Security
- Reference Files

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/brand-voice/skills/guideline-generation/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

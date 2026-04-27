# knowledge-synthesis

## 요약

Combines search results from multiple sources into coherent, deduplicated answers with source attribution. Handles confidence scoring based on freshness and authority, and summarizes large result sets effectively.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | enterprise-search |
| 원본 경로 | `knowledge-work-plugins/enterprise-search/skills/knowledge-synthesis/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/enterprise-search/knowledge-synthesis-6dfea08.md` |
| 사용자 호출 | false |

## 언제 쓰나

Combines search results from multiple sources into coherent, deduplicated answers with source attribution. Handles confidence scoring based on freshness and authority, and summarizes large result sets effectively.

## 주요 내용

- **진행 방식**: [Raw results from all sources] ↓ [1. Deduplicate — merge same info from different sources] ↓ [2. Cluster — group related results by theme/topic] ↓ [3. Rank — order clusters and items by relevance to query] ↓ [4. Assess confidence — freshness × authority × agreement] ↓ [5. Synthesize — produce narrative answer with attribution] ↓ [6. Format — choose appropriate detail level for result count] ↓ [Coherent answer with sources]

## 원본 문서 구조

- The Goal
- Deduplication
  - Cross-Source Deduplication
  - Deduplication Priority
  - What NOT to Deduplicate
- Citation and Source Attribution
  - Attribution Format
  - Attribution Rules
- Confidence Levels
  - Freshness
  - Authority
  - Expressing Confidence
  - Conflicting Information
- Summarization Strategies
  - For Small Result Sets (1-5 results)
  - For Medium Result Sets (5-15 results)
  - For Large Result Sets (15+ results)
  - Summarization Rules
- Synthesis Workflow
- Anti-Patterns

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/enterprise-search/skills/knowledge-synthesis/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# scribe

## 요약

Reference skill for Zoom AI Services Scribe. Use after routing to a transcription workflow when handling uploaded or stored media, Build-platform JWT auth, fast mode transcription, batch jobs, or transcript pipeline design.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/scribe/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/scribe-5f14e36.md` |
| 사용자 호출 | false |

## 언제 쓰나

Reference skill for Zoom AI Services Scribe. Use after routing to a transcription workflow when handling uploaded or stored media, Build-platform JWT auth, fast mode transcription, batch jobs, or transcript pipeline design.

## 주요 내용

- **진행 방식**: Get Build-platform credentials and generate an HS256 JWT. Choose **fast mode** for one short file or **batch mode** for stored archives / large sets. Submit the transcription request. For batch jobs, poll job/file status or receive webhook notifications. Persist and post-process transcript JSON.

## 원본 문서 구조

- Routing Guardrail
- Quick Links
- Core Workflow
- Hosted Fast-Mode Guardrail
- Browser Microphone Pattern
- Endpoint Surface
- High-Level Scenarios
- Chaining
- Operations

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/scribe/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

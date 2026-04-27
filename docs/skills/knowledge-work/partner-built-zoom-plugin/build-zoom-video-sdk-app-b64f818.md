# build-zoom-video-sdk-app

## 요약

Reference skill for Zoom Video SDK. Use after routing to a custom-session workflow when the user needs full control over the video experience rather than an actual Zoom meeting.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/video-sdk/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/build-zoom-video-sdk-app-b64f818.md` |

## 언제 쓰나

Reference skill for Zoom Video SDK. Use after routing to a custom-session workflow when the user needs full control over the video experience rather than an actual Zoom meeting.

## 주요 내용

- 원본 설명과 문서 구조를 기준으로 필요한 시점에 참조합니다.

## 원본 문서 구조

- Hard Routing Guardrail (Read First)
- Meeting SDK vs Video SDK
- UI Options (Web)
- Prerequisites
- Quick Start (Web)
  - NPM Usage (Bundler like Vite/Webpack)
  - CDN Usage (No Bundler)
  - ES Module with CDN (Race Condition Fix)
- SDK Lifecycle (CRITICAL ORDER)
- Video Rendering (Event-Driven)
  - Use `attachVideo()` NOT `renderVideo()`
  - Required Events
- Key Concepts
- Session Creation Model
  - How Sessions Work
  - Signature Endpoint Setup
- Use Cases
- BYOS (Bring Your Own Storage)
- Detailed References
  - UI & Components
  - Platform Guides
- Sample Repositories
  - Official (by Zoom)
- Resources
- Environment Variables
- Linux Operations

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/video-sdk/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

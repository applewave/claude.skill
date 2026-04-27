# video-sdk/web

## 요약

Zoom Video SDK for Web - JavaScript/TypeScript integration for browser-based video sessions, real-time communication, screen sharing, recording, and live transcription

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/video-sdk/web/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/video-sdk-web-b3f7bde.md` |
| 사용자 호출 | false |

## 언제 쓰나

Zoom Video SDK for Web - JavaScript/TypeScript integration for browser-based video sessions, real-time communication, screen sharing, recording, and live transcription

## 주요 내용

- 원본 설명과 문서 구조를 기준으로 필요한 시점에 참조합니다.

## 원본 문서 구조

- Quick Links
- SDK Overview
- Prerequisites
  - System Requirements
  - Browser Feature Requirements
  - Optional Pre-Join Diagnostics (Recommended for Reliability)
- Installation
  - NPM (Recommended)
  - CDN (Fallback Strategy Recommended)
- Quick Start
- SDK Lifecycle (CRITICAL ORDER)
- Critical Gotchas and Best Practices
  - getMediaStream() ONLY Works After join()
  - Use attachVideo() NOT renderVideo()
  - Video Rendering is Event-Driven (CRITICAL)
  - Peer Video on Mid-Session Join
  - CDN Race Condition with ES Modules
  - SharedArrayBuffer for HD Video
  - Check HD Capability Before Enabling
  - Screen Share Rendering Mode Check
- Key Features
  - Video Quality Enum
  - Virtual Backgrounds
  - Video Processor (Custom Effects)
  - WebRTC Mode
- Feature Clients
- Common Tasks
  - Start/Stop Video
  - Start/Stop Audio
  - Switch Devices
  - Screen Sharing
  - Chat
  - Recording (Host Only)
  - Leave/End Session
- Error Handling
  - Common Join Errors

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/video-sdk/web/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

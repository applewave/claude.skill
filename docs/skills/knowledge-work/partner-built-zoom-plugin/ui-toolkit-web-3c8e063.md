# ui-toolkit/web

## 요약

Reference skill for Zoom Video SDK UI Toolkit. Use after routing to a web video workflow when you want prebuilt React UI instead of building a fully custom Video SDK interface.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Knowledge Work Plugin Skills |
| 영역 | partner-built/zoom-plugin |
| 원본 경로 | `knowledge-work-plugins/partner-built/zoom-plugin/skills/ui-toolkit/SKILL.md` |
| 상세 파일 | `docs/skills/knowledge-work/partner-built-zoom-plugin/ui-toolkit-web-3c8e063.md` |
| 사용자 호출 | false |

## 언제 쓰나

Reference skill for Zoom Video SDK UI Toolkit. Use after routing to a web video workflow when you want prebuilt React UI instead of building a fully custom Video SDK interface.

## 주요 내용

- **사용 방식**: <link rel="stylesheet" href="https://source.zoom.us/uitoolkit/2.3.5-1/videosdk-zoom-ui-toolkit.css" /> <script src="https://source.zoom.us/uitoolkit/2.3.5-1/videosdk-zoom-ui-toolkit.min.umd.js"></script> <div id="sessionContainer"></div> <script> const uitoolkit = window.UIToolkit; uitoolkit.joinSession(document.getElementById('sessionContainer'), { videoSDKJWT: 'your_jwt', sessionName: 'my-session', userName: 'User', features: ['video', 'audio', 'chat'] }); </script>

## 원본 문서 구조

- Quick Links
- Overview
- Installation
- Quick Start
  - Basic Usage (Vanilla JS)
  - Next.js / React Integration
- Available Features
- Troubleshooting
- JWT Token Generation (Server-Side)
  - Node.js / Next.js API Route
  - JWT Payload Fields
- API Reference
  - Core Methods
  - Event Listeners
  - Component Methods
- CDN Usage (No Build Step)
- Next.js with basePath
- Prerequisites
- Browser Support
- Common Issues
- Resources
- Integrated Index
- 📚 Start Here
- 🎯 Core Concepts
- 📖 Complete Guides
  - Getting Started
  - Framework Integration
  - Advanced Topics
- 📚 API Reference
- 🔧 Configuration
- ⚠️ Troubleshooting
  - Common Issues
  - Framework-Specific Issues
  - Session Issues
- 📦 Sample Applications
- 🌐 External Resources

## 관리 메모

- 이 문서는 원본 `knowledge-work-plugins/partner-built/zoom-plugin/skills/ui-toolkit/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

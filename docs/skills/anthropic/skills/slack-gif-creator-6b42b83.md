# slack-gif-creator

## 요약

Knowledge and utilities for creating animated GIFs optimized for Slack. Provides constraints, validation tools, and animation concepts. Use when users request animated GIFs for Slack like "make me a GIF of X doing Y for Slack.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | Anthropic Skills |
| 영역 | skills |
| 원본 경로 | `skills/skills/slack-gif-creator/SKILL.md` |
| 상세 파일 | `docs/skills/anthropic/skills/slack-gif-creator-6b42b83.md` |
| 라이선스 | Complete terms in LICENSE.txt |

## 언제 쓰나

Knowledge and utilities for creating animated GIFs optimized for Slack. Provides constraints, validation tools, and animation concepts. Use when users request animated GIFs for Slack like "make me a GIF of X doing Y for Slack.

## 주요 내용

- **진행 방식**: from core.gif_builder import GIFBuilder from PIL import Image, ImageDraw 1. Create builder builder = GIFBuilder(width=128, height=128, fps=10) 2. Generate frames for i in range(12): frame = Image.new('RGB', (128, 128), (240, 248, 255)) draw = ImageDraw.Draw(frame) Draw your animation using PIL primitives (circles, polygons, lines, etc.) builder.add_frame(frame) 3. Save with optimization builder.save('output.gif', num_colors=48, optimize_for_emoji=True)

## 원본 문서 구조

- Slack Requirements
- Core Workflow
- Drawing Graphics
  - Working with User-Uploaded Images
  - Drawing from Scratch
  - Making Graphics Look Good
- Available Utilities
  - GIFBuilder (`core.gif_builder`)
  - Validators (`core.validators`)
  - Easing Functions (`core.easing`)
  - Frame Helpers (`core.frame_composer`)
- Animation Concepts
  - Shake/Vibrate
  - Pulse/Heartbeat
  - Bounce
  - Spin/Rotate
  - Fade In/Out
  - Slide
  - Zoom
  - Explode/Particle Burst
- Optimization Strategies
- Philosophy
- Dependencies

## 관리 메모

- 이 문서는 원본 `skills/skills/slack-gif-creator/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

# phase-9-deployment

## 요약

Skill for deploying to production environment. Covers CI/CD, environment configuration, and deployment strategies. Use proactively when user is ready to deploy or asks about production environment setup. Triggers: deployment, CI/CD, production, Vercel, Kubernetes, Docker, 배포, デプロイ, 部署, despliegue, implementación, producción, déploiement, mise en production, Bereitstellung, Produktion, distribuzione, messa in produzione Do NOT use for: local development, design phase, or feature implementation.

## 기본 정보

| 항목 | 내용 |
|---|---|
| 분류 | bkit Skills |
| 영역 | claude.bkit |
| 원본 경로 | `claude.bkit/skills/phase-9-deployment/SKILL.md` |
| 상세 파일 | `docs/skills/bkit/claude.bkit/phase-9-deployment-9f1ad56.md` |
| 사용자 호출 | false |

## 언제 쓰나

Skill for deploying to production environment. Covers CI/CD, environment configuration, and deployment strategies. Use proactively when user is ready to deploy or asks about production environment setup. Triggers: deployment, CI/CD, production, Vercel, Kubernetes, Docker, 배포, デプロイ, 部署, despliegue, implementación, producción, déploiement, mise en production, Bereitstellung, Produktion, distribuzione, messa in produzione Do NOT use for: local development, design phase, or feature implementation.

## 주요 내용

- **산출물**: docs/02-design/ └── deployment-spec.md # Deployment specification docs/04-report/ └── deployment-report.md # Deployment report (Infrastructure config files) ├── vercel.json # Vercel configuration ├── Dockerfile # Docker configuration └── k8s/ # Kubernetes configuration

## 원본 문서 구조

- Purpose
- What to Do in This Phase
- Deliverables
- PDCA Application
- Level-wise Application
- Starter Deployment (Static Hosting)
- Dynamic Deployment (Vercel)
- Enterprise Deployment (Kubernetes)
- Environment Management
  - Environment Configuration Overview
  - Environment Classification
- CI/CD Environment Variable Configuration
  - GitHub Actions
  - GitHub Secrets Configuration Guide
  - Vercel Environment Variable Configuration
- Secrets Management Strategy
  - Level-wise Secrets Management
  - Starter/Dynamic: CI/CD Secrets
  - Enterprise: HashiCorp Vault
  - Enterprise: AWS Secrets Manager
- Environment-specific Build Configuration
  - Next.js Environment Configuration
  - Environment-specific API Endpoints
- Environment Variable Validation (Pre-deployment)
  - Required Variable Check Script
  - Validation in CI/CD
- Environment Variable Management Checklist
  - Pre-deployment
  - Post-deployment
- Deployment Checklist
  - Preparation
  - Deployment
  - Verification
- Rollback Plan
- Template
- After Completion

## 관리 메모

- 이 문서는 원본 `claude.bkit/skills/phase-9-deployment/SKILL.md`에서 이름, 설명, 입력 힌트, 섹션 구조를 추출해 만든 상세 색인입니다.
- 실제 실행 규칙, 긴 예시, 세부 절차는 원본 `SKILL.md`를 기준으로 확인합니다.

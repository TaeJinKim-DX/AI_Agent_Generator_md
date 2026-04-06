# COLLABORATION.md (Lite)

## 목적
이 문서는 경량 스켈레톤의 협업 계약을 정의한다.

## 운영 모델
- 역할: Planner / Builder / Reviewer
- 명령: `/start-work`, `/plan`, `/implement`, `/review`, `/handoff`

## 구조 범위
- 기본(Lite): `.claude/commands`, `.claude/rules`, `.claude/runtime`, `.sisyphus`
- 선택 확장: `.claude/agents`, `.claude/harness`, `.claude/templates`, `.claude/workflows`, `.claude/glossary`

## 최소 원칙
1. 범위 외 변경 금지
2. 증거 없는 완료 선언 금지
3. 리뷰 verdict 없이 종료 금지

## 실행 루프
`/start-work` → `/plan` → `/implement` → `/review` → (필요 시) `/handoff`

## 산출물 경로
- 계획: `.sisyphus/plans/`
- 구현 로그: `.sisyphus/drafts/`
- 리뷰 증거: `.sisyphus/evidence/`
- 팀 공유 결과물: `docs/`

## 품질 게이트
- Plan: scope + 수용 기준 존재
- Implement: 계획 범위 내 변경 + 검증 기록
- Review: scope/quality 평가 + verdict 명시

## 커스터마이징 규칙
- 이 스켈레톤은 기본값만 제공한다.
- 상세 버전/도메인 규칙은 프로젝트에서 추가한다.
- 경량 원칙(필수 문서 최소화)은 유지한다.

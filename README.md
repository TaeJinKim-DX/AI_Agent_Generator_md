# Claude Agent Skeleton (Lite)

이 저장소는 **토큰 사용을 최소화한 경량 스켈레톤**입니다.

## 핵심 구조

- `.claude/commands/` : 실행 절차 (`/start-work`, `/plan`, `/implement`, `/review`, `/handoff`)
- `.claude/rules/` : 최소 규칙 (`forbidden.md`, `quality-gates.md`)
- `.claude/runtime/` : 런타임 가이드 (`runtime-python.md`, `runtime-typescript.md`)
- `.sisyphus/` : 작업 산출물 (`plans`, `drafts`, `evidence`)

## 선택 확장 구조 (필요 시)

- `.claude/agents/` : 역할별 상세 가이드
- `.claude/harness/` : 고급 검증 체크리스트/런북
- `.claude/templates/` : 반복 산출물 템플릿
- `.claude/workflows/` : 에스컬레이션/복구 시나리오
- `.claude/glossary/` : 프로젝트 용어집

## 왜 경량 구조인가

- 항상 읽는 문서를 줄여 세션 토큰 소모를 낮춘다.
- 필수 계약(명령/게이트)만 남겨 시작 속도를 높인다.
- 프로젝트별 상세 규칙은 각 저장소에서 필요할 때 추가한다.

## 권장 읽기 순서 (최소)

1. `CLAUDE.md`
2. `COLLABORATION.md`
3. 현재 단계에 필요한 `.claude/commands/<command>.md` 1개
4. 검토 시 `.claude/rules/*.md`

## 산출물 관리

- 팀 공유 최종 문서: `docs/` 하위 (`docs/specs`, `docs/reports`, `docs/decisions`)
- 작업 중간 산출물/증거: `.sisyphus/` 하위

## Claude 요청 예시

```text
다음 작업을 /plan -> /implement -> /review 순서로 진행해줘.
- 최종 문서는 docs/reports/<topic>.md 에 기록
- 중간 계획/로그/증거는 .sisyphus 에 기록
```

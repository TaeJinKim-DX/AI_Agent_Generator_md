## runtime-python.md (Skeleton Lightweight)

### 목적
Python 기반 프로젝트를 시작할 때 충돌이 적은 **최소 기준**만 제공한다.

### 기본 기술 스택 (경량)
- Runtime: Python 3.11+ (권장 3.11 또는 3.12)
- API(선택): FastAPI
- Agent Framework: LangChain 1.1.12 / LangChain-OpenAI 1.1.12 / LangGraph 1.0.10

### 기준 버전 정책 (스켈레톤 배포용)
1. 문서에는 **major/minor 기준만** 유지한다. (`3.11+`, `2.x`)
2. 실제 프로젝트 시작 시점에만 lock 파일로 정확 버전을 확정한다.
3. 로컬 개발 단계에서는 교차 런타임(Python/TS) 버전을 강제 동기화하지 않는다.
4. 버전 충돌이 있으면 기능 추가보다 lock 재생성/정렬을 먼저 처리한다.

### 최소 디렉터리 권장
```text
src/
tests/
docs/
```

### 운영 원칙 (요약)
- 복잡한 오케스트레이션이 아니면 과도한 프레임워크 도입을 미룬다.
- 핵심 계약(요청/응답/설정)은 Pydantic으로 고정한다.
- 문서 기준은 경량으로 유지하고, 프로젝트별 세부 버전은 각 저장소에서 확정한다.

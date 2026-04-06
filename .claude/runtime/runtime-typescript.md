## runtime-typescript.md (Skeleton Lightweight)

### 목적
TypeScript 기반 프로젝트를 시작할 때 충돌이 적은 **최소 기준**만 제공한다.

### 기본 기술 스택 (경량)
- Runtime: Node.js 24.14.x(LTS)
- Language: TypeScript 프레임워크 버전에 따라 상이
- API(선택): Fastify 또는 Hono 중 1개만 선택
- Agent Framework: LangChain 1.1.12 / LangChain-OpenAI 1.1.12 / LangGraph 1.0.10

### 기준 버전 정책 (스켈레톤 배포용)
1. 문서에는 **major/minor 기준만** 유지한다. (`5.x`, `LTS`)
2. 실제 프로젝트 시작 시점에만 lock 파일로 정확 버전을 확정한다.
3. 로컬 개발 단계에서는 Python 런타임 버전과 강제 결합하지 않는다.
4. 프레임워크 중복(Fastify+Hono+Express 동시 도입)은 금지한다.

### 최소 디렉터리 권장
```text
src/
tests/
docs/
```

### 운영 원칙 (요약)
- 스켈레톤 단계에서는 UI/서버/Agent 프레임워크를 동시에 확장하지 않는다.
- 핵심 계약(요청/응답/도구 스키마)은 Zod(또는 프로젝트 표준 스키마)로 고정한다.
- 문서 기준은 경량으로 유지하고, 프로젝트별 세부 버전은 각 저장소에서 확정한다.

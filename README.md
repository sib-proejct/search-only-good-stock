# search-only-good-stock (Backend)

좋은 주식을 발굴하고 분석하기 위한 **FastAPI 백엔드(BE)** 프로젝트입니다.

---

## 📌 프로젝트 아키텍처 및 저장소 분리

본 서비스는 백엔드(BE)와 프론트엔드(FE)가 별도 저장소/폴더로 분리되어 운영됩니다.

- **Backend (BE)**: `search-only-good-stock` (현재 프로젝트)
  - **기술 스택**: Python, FastAPI, `uv`, Pydantic
- **Frontend (FE)**: `search-only-good-stock-fe`
  - **기술 스택**: Next.js, TypeScript, Tailwind CSS

---

## 🚀 Backend 빠른 시작 (FastAPI + uv)

### 1. 가상환경 및 의존성 설치
```bash
# 가상환경 생성 및 패키지 동기화
uv venv
uv sync
```

### 2. 패키지 관리
```bash
# 의존성 추가
uv add fastapi uvicorn[standard] pydantic

# 개발용 도구 추가
uv add --dev pytest ruff
```

### 3. 로컬 서버 실행
```bash
uv run uvicorn app.main:app --reload --port 8000
```
- **API 문서 (Swagger UI)**: `http://localhost:8000/docs`
- **대체 문서 (ReDoc)**: `http://localhost:8000/redoc`

---

## 🔗 프론트엔드(FE) 연동 안내
- 프론트엔드(`search-only-good-stock-fe`) 개발 서버 기본 주소: `http://localhost:3000`
- 로컬 개발 시 백엔드 `main.py`에 `CORSMiddleware`가 설정되어 있어 `http://localhost:3000`과의 통신을 지원합니다.
- 프론트엔드 설정 시 `.env.local`에 `NEXT_PUBLIC_API_URL=http://localhost:8000`을 추가하세요.

---

## 📖 개발 지침
자세한 AI/Agent 및 개발 가이드라인은 [AGENTS.md](file:///c:/repo/search-only-good-stock/AGENTS.md)를 참고하세요.

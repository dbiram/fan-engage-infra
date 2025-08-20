# Fan Engage — Infra (Docker Compose)

Brings up the full dev stack:
- Postgres, Redis
- MinIO (+ console)
- API (FastAPI)
- Frontend (Next.js)
- Workers (stub, Phase 1)

## Quick start (Windows / CMD)
```cmd
copy .env.example .env
docker compose -f docker-compose.dev.yml up --build
```

## Services:
- API: http://localhost:8000/health
- Frontend: http://localhost:3000
- MinIO Console: http://localhost:9001
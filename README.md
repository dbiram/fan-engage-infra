# fan-engage-infra

Dev docker-compose that wires everything together.

## Services
- **postgres** — metadata DB
- **redis** — job queue backend
- **minio** — S3-compatible object storage (+ bucket seeding)
- **api** — FastAPI service
- **frontend** — Next.js app
- **workers** — RQ worker (background jobs)

## Quickstart
```
docker compose -f docker-compose.dev.yml up --build
```
### Frontend: http://localhost:3000
### API: http://localhost:8000
### MinIO: http://localhost:9001 (console)


## Test flow
1) Open frontend → upload a short MP4.
2) Watch progress banner (queued → detections → teams → homography).
3) Open the match page → overlays + radar + analytics.

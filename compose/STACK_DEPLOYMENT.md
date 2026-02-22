# Docker Compose Stack Deployment

## Objective

Deploy a multi-service container stack using Docker Compose:

- Nginx
- Prometheus
- cAdvisor
- Grafana

---

## What Was Done

- Created structured project directories
- Built a multi-service `docker-compose.yml`
- Implemented:
  - Port mapping
  - Named volumes
  - Service orchestration

---

## Operational Commands Used

Lifecycle management:

- `docker compose up`
- `docker compose down`

Runtime inspection:

- `docker ps`
- `docker logs`
- `docker exec`

---

## Validation Checklist

- All services start without errors
- Port mappings allow host access
- Volumes persist across restarts
- Logs are usable for debugging misconfigurations

---

## Outcome

The lab stack is modular, repeatable, and operational via Docker Compose.

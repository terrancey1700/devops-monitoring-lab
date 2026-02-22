# Project Phases – DevOps Monitoring Lab Infrastructure

This document summarizes the project in phases as implemented.

---

## Phase 1 – Environment Provisioning & Linux Foundation

- Installed Ubuntu 24.04 LTS in UTM (Intel-based Mac host)
- Allocated 2 CPUs, 4GB RAM, 30–40GB storage
- Validated network connectivity and system configuration
- Practiced Linux fundamentals:
  - apt
  - users/permissions
  - process inspection
  - ss/ping/curl
  - journalctl
- Installed and validated Docker Engine

---

## Phase 2 – Containerization & Service Deployment

- Deployed Nginx serving custom HTML
- Created structured project directories
- Built multi-service docker-compose stack:
  - Nginx
  - Prometheus
  - cAdvisor
  - Grafana
- Implemented port mapping + named volumes
- Validated lifecycle:
  - docker ps / logs / exec
  - docker compose up / down

---

## Phase 3 – Observability & Monitoring Stack

- Configured Prometheus scrape targets
- Integrated cAdvisor for container metrics
- Connected Grafana to Prometheus
- Imported dashboards
- Validated CPU/memory/network visibility

---

## Phase 4 – Troubleshooting & Operational Validation

- Diagnosed container networking issues
- Verified port exposure and host accessibility
- Used logs to resolve configuration errors
- Confirmed volume persistence across restarts
- Tested service resilience

---

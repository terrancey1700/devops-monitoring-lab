# System Architecture – DevOps Monitoring Lab Infrastructure

## Overview

This project is a containerized DevOps lab running on Ubuntu 24.04 inside a UTM VM. The stack is deployed with Docker Compose and includes:

- Nginx (web workload)
- Prometheus (metrics collection)
- cAdvisor (container metrics exporter)
- Grafana (visualization)

The focus is observability, container orchestration, and production-style troubleshooting in a repeatable lab environment.

---

## Architecture (Host → VM → Containers)

MacBook (Host)
└── UTM Virtual Machine (Ubuntu 24.04)
    ├── Docker Engine
    └── Docker Compose Stack
        ├── Nginx (Web Service)
        ├── Prometheus (Metrics Collection)
        ├── cAdvisor (Container Metrics)
        └── Grafana (Visualization)

---

## Traffic Flow

User → Browser → Ubuntu VM → Docker → Nginx

---

## Monitoring Flow

Containers → cAdvisor → Prometheus → Grafana

---

## Design Decisions

- Docker Compose used for repeatable multi-service deployments.
- cAdvisor used to expose container-level metrics to Prometheus.
- Grafana used to visualize Prometheus metrics with dashboards.
- Volumes used to persist critical data across container restarts.

---

## Operational Goals

- Services must start reliably via Compose
- Metrics must be visible end-to-end (cAdvisor → Prometheus → Grafana)
- Data must persist across restarts
- Troubleshooting must be done using logs + metrics

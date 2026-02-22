# DevOps Monitoring Lab Infrastructure

End-to-end containerized DevOps lab built on Ubuntu using Docker, Docker Compose, Prometheus, Grafana, and Nginx. This project demonstrates container orchestration, observability implementation, Linux administration, and troubleshooting workflows in a production-inspired environment.

---

## Executive Summary

### Situation

I needed a hands-on DevOps environment to develop real-world skills in:

- Linux system administration  
- Containerization  
- Monitoring and observability  
- Service troubleshooting  
- Infrastructure documentation  

**Initial environment limitations:**

- No structured DevOps lab  
- No monitoring stack  
- No container orchestration  
- No repeatable deployment workflow  
- No observability into workloads  

This limited practical DevOps experience beyond theory.

---

### Task

Design and deploy a self-contained DevOps lab that:

- Runs on Ubuntu 24.04 (virtualized environment)
- Uses Docker for containerized services
- Deploys multi-service workloads via Docker Compose
- Implements real-time monitoring with Prometheus and Grafana
- Exposes services through proper container networking
- Persists data using Docker volumes
- Survives restarts and reboots
- Follows production-style troubleshooting practices
- Is fully documented and portfolio-ready

---

### Action

---

## Phase 1 – Environment Provisioning & Linux Foundation

- Installed **Ubuntu 24.04 LTS** in UTM (Intel-based Mac host)
- Allocated 2 CPUs, 4GB RAM, 30–40GB storage
- Verified network connectivity and system configuration
- Practiced:
  - Package management (`apt`)
  - User and permission management
  - Process inspection
  - Networking tools (`ss`, `ping`, `curl`)
  - Log inspection (`journalctl`)
- Installed and validated Docker Engine

---

## Phase 2 – Containerization & Service Deployment

- Deployed an Nginx container serving a custom HTML page
- Created structured project directories
- Built a multi-service `docker-compose.yml` including:
  - Nginx (web service)
  - Prometheus (metrics collection)
  - cAdvisor (container metrics)
  - Grafana (visualization)
- Implemented:
  - Port mapping
  - Named volumes
  - Service orchestration
- Validated container lifecycle using:
  - `docker ps`
  - `docker logs`
  - `docker exec`
  - `docker compose up`
  - `docker compose down`

---

## Phase 3 – Observability & Monitoring Stack

- Configured Prometheus scrape targets
- Integrated cAdvisor for container metrics
- Connected Grafana to Prometheus as a data source
- Imported production-grade dashboards
- Validated:
  - CPU utilization
  - Memory consumption
  - Network traffic
- Observed real-time metrics during workload activity

---

## Phase 4 – Troubleshooting & Operational Validation

- Diagnosed container networking issues
- Verified port exposure and host accessibility
- Used logs to resolve configuration errors
- Confirmed volume persistence across restarts
- Tested service resilience
- Implemented cron-based automation concepts
- Planned load testing with ApacheBench

---

### Result

The final system is:

- Fully containerized  
- Observable with real-time metrics  
- Persistent across container restarts  
- Modular via Docker Compose  
- Repeatable and structured  
- Troubleshootable using logs and metrics  
- Production-inspired and portfolio-ready  

This project demonstrates foundational DevOps competency in Linux systems, container orchestration, monitoring, and debugging workflows.

---

## Technologies Used

- Ubuntu Server 24.04 LTS  
- Docker Engine  
- Docker Compose  
- Nginx  
- Prometheus  
- cAdvisor  
- Grafana  
- ApacheBench (planned load testing)  
- Linux system utilities (`ss`, `df`, `ps`, `journalctl`, `cron`)

---

## Architecture Overview

```
MacBook (Host)
└── UTM Virtual Machine (Ubuntu 24.04)
    ├── Docker Engine
    ├── Docker Compose
    │   ├── Nginx (Web Service)
    │   ├── Prometheus (Metrics Collection)
    │   ├── cAdvisor (Container Metrics)
    │   └── Grafana (Visualization)
```

### Traffic Flow

User → Browser → Ubuntu VM → Docker → Nginx  

### Monitoring Flow

Containers → cAdvisor → Prometheus → Grafana  

---

## Skills Demonstrated

- Linux system administration  
- Docker container lifecycle management  
- Multi-service orchestration with Docker Compose  
- Volume-based persistence design  
- Port mapping and container networking  
- Metrics collection and observability implementation  
- Log-based debugging methodology  
- Infrastructure documentation  
- Troubleshooting under simulated production conditions  

---

## Future Improvements

- Implement ApacheBench or k6 load testing validation  
- Add Prometheus alert rules  
- Configure Grafana alert notifications  
- Push custom images to Docker Hub  
- Introduce GitHub Actions CI pipeline  
- Deploy stack to AWS using Terraform  
- Add centralized logging (Loki or ELK)  
- Implement automated backup scripts  
- Harden Docker daemon configuration  
- Convert infrastructure to Terraform-based provisioning  

---

## Author

**Terrance Young**  
Aspiring DevOps / Systems Engineer  

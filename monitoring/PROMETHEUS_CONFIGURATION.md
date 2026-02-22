# Prometheus Configuration

## Objective

Collect metrics from the lab stack and enable observability into workloads.

---

## What Was Done

- Configured Prometheus scrape targets
- Integrated cAdvisor as the container metrics source
- Validated Prometheus was collecting metrics successfully

---

## What Was Validated

Observed Prometheus scraping and feeding Grafana dashboards for:

- CPU utilization
- Memory consumption
- Network traffic

---

## Key Concept

Prometheus does not “discover” metrics automatically in this lab.

It must be configured with scrape targets that include cAdvisor so it can collect container metrics.

---

## Outcome

Prometheus successfully collected container metrics used downstream by Grafana.

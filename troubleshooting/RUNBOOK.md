# Troubleshooting Runbook – DevOps Monitoring Lab

This runbook reflects the operational troubleshooting approach used in the lab.

---

## 1) Container Not Reachable From Host

Checks:

- Is the container running?

  `docker ps`

- Are ports mapped correctly?

  Inspect compose config + confirm host port is listening:

  `ss -lntp`

- Can the host reach the service?

  `curl http://localhost:<port>`

---

## 2) Service Misbehaving / Crashing

Checks:

- View logs:

  `docker logs <container>`

- Exec into container:

  `docker exec -it <container> sh`

- Bring stack down/up cleanly:

  `docker compose down`
  `docker compose up -d`

---

## 3) Prometheus Not Showing Targets

Checks:

- Confirm Prometheus container is running:

  `docker ps`

- Confirm scrape targets are reachable over the Compose network
- Use logs to spot config errors:

  `docker logs <prometheus-container>`

---

## 4) Grafana Shows No Data

Checks:

- Confirm Prometheus is reachable from Grafana
- Confirm data source is configured correctly
- Confirm dashboards are querying expected metrics

---

## 5) Persistence / Volumes Not Working

Checks:

- Confirm named volumes exist and are attached
- Restart stack and confirm data remains

---

## Outcome

Troubleshooting relied on:

- container state (`docker ps`)
- logs (`docker logs`)
- shell access (`docker exec`)
- network checks (`ss`, `curl`)
- iterative config fixes + retest

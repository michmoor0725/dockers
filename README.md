This repository contains my collection of **Docker Compose configurations** for self-hosted services.  
Each service lives in its own subdirectory under `dockers/`, with a `compose.yml` file and optional `.env.example`.

---


Clone the repo:

git clone git@github.com:michmoor0725/dockers.git
cd dockers

## Repository Structure 
dockers/
  uptime_kuma/        → Uptime Kuma monitoring
  prometheus/         → Prometheus + exporters
  freshrss/           → FreshRSS RSS reader
  netalertx/          → Network device monitoring
  nginx_proxy_manager/→ Nginx Proxy Manager
  ...
.gitignore            → strict rules (only YAML + .env.example tracked)


## Current Service ... Ever expanding
| Service                 | Description                      | Default Ports              |
| ----------------------- | -------------------------------- | -------------------------- |
| **Uptime Kuma**         | Uptime monitoring and alerts     | 3001 (mapped to host 3009) |
| **Prometheus**          | Metrics collection & monitoring  | 9090                       |
| **SNMP Exporter**       | SNMP metrics for Prometheus      | 9116                       |
| **Grafana**             | Metrics dashboards               | 3000                       |
| **FreshRSS**            | RSS feed reader                  | 8080 (example)             |
| **NetAlertX**           | Network device & IP monitoring   | 20211                      |
| **Nginx Proxy Manager** | Reverse proxy & SSL certificates | 80 / 81 / 443              |



# Bind mounts are used instead of Docker volumes for transparency and easy backups.

# Day 5 - Full Observability Stack

> Day 5 of 14 in the **Zero to Production Infrastructure & Security** series.

Docker Compose deployment of Prometheus and Grafana scraping host and container metrics.

| | |
|---|---|
| **Day** | 5 of 14 |
| **Status** | Under construction |
| **Verification** | `docker compose -f docker-compose.yml config --quiet` |
| **Tags** | `prometheus`  `grafana`  `netdata`  `observability`  `docker` |

## Focus

- node_exporter host metrics
- cAdvisor container metrics
- Custom Grafana dashboard JSON
- Alertmanager rules for CPU and RAM pressure

## Status

Implementation lands during the Day 5 build session. Until then this
repository holds the agreed structure only - there is no placeholder code here
pretending to work.

The nightly pipeline appends the real verification result to [STATUS.md](STATUS.md).

## Layout

```
05-observability-stack/
  README.md        this file
  LICENSE          MIT
  STATUS.md        machine-written verification record
  .gitignore       shared from the series root
  .gitattributes   forces LF endings so bash scripts run on Windows
```

## Verify

```bash
docker compose -f docker-compose.yml config --quiet
```

The nightly job at 22:00 runs this command, records the result and
exit code in STATUS.md, then tags and pushes the repository.

## Licence

MIT. See [LICENSE](LICENSE).
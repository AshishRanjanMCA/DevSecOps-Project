# 04 – Monitoring & Observability Step

## Purpose
The **Monitoring & Observability Step** provides continuous visibility into application health, system performance, and service availability.  
This stage enables proactive detection of issues and supports operational reliability.

---

## Tools Used
- **Prometheus** – Metrics collection and time-series storage
- **Grafana** – Visualization and dashboarding
- **Node Exporter** – System-level metrics collection
- **Blackbox Exporter** – Uptime and endpoint monitoring

---

## Monitoring Scope
This stage monitors:
- Jenkins server system metrics
- Application performance and availability
- Kubernetes cluster and workload metrics
- External service and HTTP endpoint uptime

---

## Monitoring Flow
1. Node Exporter exposes system metrics from Jenkins and other nodes.
2. Blackbox Exporter probes application endpoints for availability and response status.
3. Prometheus scrapes metrics from configured targets at regular intervals.
4. Prometheus stores metrics as time-series data.
5. Grafana visualizes metrics through dashboards and generates alerts.

---

## Outcome
- Real-time visibility into system and application performance
- Early detection of failures and performance degradation
- Improved reliability and operational awareness

---

## Detailed Documentation
For detailed monitoring configuration, refer to:
- [Prometheus Setup](prometheus-setup.md)
- [Grafana Setup](grafana-setup.md)
- [Blackbox Exporter Setup](blackbox-exporter.md)



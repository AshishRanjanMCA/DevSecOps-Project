# Grafana Setup

## Purpose
Grafana is used to **visualize metrics** collected by Prometheus through interactive dashboards.  
It provides real-time insight into system performance, application health, and service availability.

---

## Service Details
- **Port:** 3000
- **Role:** Metrics visualization and dashboarding

---

## Integration with Prometheus
- Prometheus is configured as a **data source** in Grafana.
- Grafana queries Prometheus to retrieve time-series metrics.
- Dashboards are created to visualize system, application, and availability metrics.

---

## Visualization Scope
Grafana dashboards provide visibility into:
- Jenkins server system metrics
- Application performance metrics
- Kubernetes cluster and pod metrics
- Uptime and availability data from Blackbox Exporter

---

## Monitoring Flow
1. Prometheus collects metrics from configured targets.
2. Grafana queries Prometheus as a data source.
3. Metrics are displayed using dashboards and panels.
4. Alerts can be configured to notify on threshold breaches.

---

## Outcome
- Centralized visualization of monitoring data
- Faster troubleshooting and performance analysis
- Improved operational awareness through dashboards and alerts

---

## Reference
For full monitoring stack configuration, refer to:  
[Monitoring Stack Overview](../docs/monitoring-stack.md)

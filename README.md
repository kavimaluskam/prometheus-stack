# Prometheus Stack
Personal setup packages for Prometheus as simple server monitoring


## Prometheus Host Server
Below package is used

- Prometheus
- Alert Manager
- Grafana

Running on host server by docker compose

### Grafana Setup
1. Default auth is admin/admin
2. Add data source on http://prometheus:9090
3. Import default metrics dashboard as via `grafana-theme/node-exporter-server-metrics-rev6.json` 

### Update alert rules


### Add client machines
1. Run node exporter on clients by
    `sudo docker run -d -p 9100:9100 --net="host" quay.io/prometheus/node-exporter`
2. Update `prometheus.yaml`
3. Update with `prometheus.yaml` via `curl -X POST http://localhost:9090/-/reload`

### Useful links
https://www.robustperception.io/sending-email-with-the-alertmanager-via-gmail/
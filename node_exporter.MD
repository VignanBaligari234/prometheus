### Node_exporter

```
[Unit]
Description=node_exporter service.

[Service]
ExecStart=/opt/node_exporter/node_exporter

[Install]
WantedBy=multi-user.target

```
### Prometheus

```
[Unit]
Description=prometheus file.

[Service]
ExecStart=/opt/prometheus/prometheus --config.file=/opt/prometheus/prometheus.yml
[Install]
WantedBy=multi-user.target

```

```
[Unit]
Description=alertmanager service.

[Service]
WorkingDirectory=/opt/alertmanager
ExecStart=/opt/alertmanager/alertmanager 

[Install]
WantedBy=multi-user.target

```


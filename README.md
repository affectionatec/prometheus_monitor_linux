# prometheus_monitor_linux


## Windows:

Grafana installation: https://grafana.com/grafana/download?platform=windows
Prometheus installation: https://prometheus.io/download/

Configure Prometheus:
`scrape_configs:
    #prometheus self monitor
  - job_name: 'prometheus'
    static_configs:
      - targets: ['localhost:9090']

    #linux server monitor
  - job_name: 'linux'
    static_configs:
      - targets: ['NODE_IP:9100']
        labels:
          instance: node1`


## Linux:

Node_exporter: https://github.com/prometheus/node_exporter/releases

`wget https://github.com/prometheus/node_exporter/releases/download/v1.3.1/node_exporter-1.3.1.linux-amd64.tar.gz
tar -zxvf node_exporter-1.3.1.linux-amd64.tar.gz 
cd node_exporter-1.3.1.linux-amd64/
./node_exporter `


## On windows

Browser->localhost:3000
  -user:admin 
  -pwd: admin

Data Sources Setting:
  Http://localhost:9090
 
Import Dashboard Template
  
  
 










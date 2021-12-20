# Installing Prometheus
```sh
wget https://github.com/prometheus/prometheus/releases/download/v2.20.0/prometheus-2.20.0.linux-amd64.tar.gz
tar xvfz prometheus-*.tar.gz
cd prometheus-2.20.0.linux-amd64/
sudo mv prometheus promtool /usr/local/bin/
sudo mkdir -p /etc/prometheus/
sudo mv prometheus.yml /etc/prometheus/prometheus.yml
sudo mv consoles/ console_libraries/ /etc/prometheus/
```

# Configure Prometheus
```sh
sudo vi /etc/prometheus/prometheus.yml 
```

# Start Prometheus Server on default port 9090
```sh
 prometheus --config.file=/etc/prometheus/prometheus.yml
 ```
 
# Validating installation 
You can verify that Prometheus is serving metrics about itself by navigating to its metrics endpoint: localhost:9090/metrics


# Using the expression browser - Refer to slide deck 

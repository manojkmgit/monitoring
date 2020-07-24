# Installing Grafana

# To install the latest OSS release:
```sh
sudo apt-get install -y apt-transport-https
sudo apt-get install -y software-properties-common wget
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list 
sudo apt-get update
sudo apt-get install grafana
```

# To start the server 
```sh
sudo systemctl daemon-reload
sudo systemctl start grafana-server
sudo systemctl status grafana-server
sudo systemctl enable grafana-server.service
```

# Package details

Installs binary to /usr/sbin/grafana-server
Installs Init.d script to /etc/init.d/grafana-server
Creates default file (environment vars) to /etc/default/grafana-server
Installs configuration file to /etc/grafana/grafana.ini
Installs systemd service (if systemd is available) name grafana-server.service
The default configuration sets the log file at /var/log/grafana/grafana.log
The default configuration specifies an sqlite3 db at /var/lib/grafana/grafana.db
Installs HTML/JS/CSS and other Grafana files at /usr/share/grafana

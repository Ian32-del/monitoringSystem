# 📊 Monitoring & Alerting System with Prometheus, Alertmanager, and Grafana

This project sets up a complete containerized monitoring and alerting stack using **Docker Compose**. It includes:
- [Prometheus](https://prometheus.io/) for metrics collection
- [Node Exporter](https://github.com/prometheus/node_exporter) for system metrics
- [Alertmanager](https://prometheus.io/docs/alerting/latest/alertmanager/) for alert notifications
- [Grafana](https://grafana.com/) for visualizing data

---

## 🧱 Project Structure

monitoringSystem/
├── docker-compose.yml
├── prometheus/
│ ├── prometheus.yml
│ └── alert.rules.yml
├── alertmanager/
│ └── alertmanager.yml
└── README.md


---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/monitoringSystem.git
cd monitoringSystem
2. Start the Stack
bash


docker-compose up -d
This will spin up all services in the background.

📍 Access the Tools
Service	URL
Prometheus	http://localhost:9090
Node Exporter	http://localhost:9100
Alertmanager	http://localhost:9093
Grafana	http://localhost:3000

🔔 Alerts & Notifications
Alertmanager is configured to send email alerts via Gmail:
Sender: christopherian96@gmail.com

Receiver: christopherian96@gmail.com

Alerts include:

Node down

High CPU usage

High disk usage

Make sure to replace the Gmail credentials in alertmanager.yml with a valid Gmail App Password.

📜 Sample Alert Rules
Inside prometheus/alert.rules.yml:

🔴 NodeDown: When a target goes offline

⚠️ HighCPUUsage: CPU usage > 80% for 1 minute

⚠️ DiskUsageHigh: Disk usage > 80% for 2 minutes

📈 Grafana Setup
Default login: admin / admin

Add Prometheus as a data source (http://prometheus:9090)

Import dashboard ID 1860 for Node Exporter metrics

🛑 Stop the Stack
bash


docker-compose down
✅ Requirements
Docker & Docker Compose installed

VS Code or any code editor

Internet access to pull images

🧪 Test Alert
To simulate a "node down" alert:

bash


docker stop monitoringsystem-node-exporter-1
Wait 1–2 minutes, then check:

Prometheus Alerts tab

Alertmanager UI

Your Gmail inbox

To restore:

bash



docker start monitoringsystem-node-exporter-1
🙋 Support
If you face any issues, check the container logs:

bash


docker logs monitoringsystem-alertmanager-1
Or feel free to reach out to the developer.

📄 License
MIT License © 2025 Chris Ian

yaml



---









# IoT-pit

The IoT-PIT framework provides a modular, containerized environment for deploying and analyzing multi-protocol IoT tarpits.
Each protocol emulator runs inside its own Docker container, and all telemetry data is collected and visualized through a Prometheus + Grafana stack.



## 🚀 How to Run

### 1️⃣ Start all services
The programs are run using Docker.  
To start all components, simply run:

```bash
docker compose up
```

## System overview
+------------------+
|   .env Config    |
+------------------+
         │
         ▼
+----------------------+
|  docker-compose.yml  |
+----------------------+
   │        │        │
   ▼        ▼        ▼
 Telnet   MQTT   CoAP  ...
   │        │        │
   └──→ Go Collector → Prometheus → Grafana

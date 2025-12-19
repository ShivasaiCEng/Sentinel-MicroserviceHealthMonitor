
---

#  Sentinel — Microservice Health Monitor

**Sentinel** is a powerful **MERN stack** microservice health monitoring platform designed to help engineering teams **ensure reliability, uptime, performance, and rapid alerting** across distributed systems.

It is currently **under active development**, but already includes core capabilities such as service health checks, alert integrations, SLA insights, and Prometheus-compatible metrics.

---

##  Demo & Links

*  **GitHub Repository:** [https://github.com/ShivasaiCEng/Sentinel-MicroserviceHealthMonitor](https://github.com/ShivasaiCEng/Sentinel-MicroserviceHealthMonitor)
*  *(Planned)* **Live Demo / Deployment:** *Coming Soon*
*  *(Optional Demo Video)*: *Coming Soon*

> This project is in development and evolving rapidly.

---

##  What Sentinel Solves

Modern microservice architectures require robust monitoring to:

* Detect service outages & performance degradation
* Calculate uptime, latency, error rates, and reliability scores
* Alert teams instantly through multiple channels
* Provide historical insights and visualizations

Sentinel helps engineering teams visualize and automate this process, reducing downtime and debugging effort across services.

---

##  Key Features *(currently working to make these work)*

 **Real-time Health Monitoring** — Scheduled health checks (e.g., every 10s)
 **Incident Detection & Tracking**
 **Multi-channel Alerting**

* Slack, Telegram, Email, WhatsApp support
   **WebSocket Live Updates** — UI updates in real time
   **Service Registration & Management**
   **Historical Health Data Visualization**
   **SLA/SLO Reliability Scoring**
   **Prometheus-Compatible Metrics Endpoint**
   **Service Metrics (latency, availability, CPU/memory)**

*(These features reflect the current implementation state in the repo.)* ([GitHub][1])

---

##  Project Structure

```
Sentinel-MicroserviceHealthMonitor/
├── backend/                # Node.js + Express backend
│   ├── config/             # Configuration & environment setup
│   ├── models/             # MongoDB/Mongoose schemas
│   ├── routes/             # API endpoints
│   ├── services/           # Business logic & health checks
│   ├── middleware/         # Auth, rate limiting, error handlers
│   ├── cron/               # Scheduled health check jobs
│   └── server.js           # Backend entry point
│
├── frontend/               # React frontend
│   ├── src/
│   │   ├── components/     # UI components
│   │   ├── pages/          # App screens
│   │   └── services/       # API calls + WebSockets
│   └── package.json
│
├── FEATURES.md             # Feature breakdown
├── QUICKSTART.md           # Setup quickstart guide
├── .gitignore
├── metadata.json
├── package.json
└── README.md               # This file
```

*(This structure reflects current repository folders.)* ([GitHub][1])

---

##  Tech Stack

**Frontend**

* React 18
* React Router
* Socket.IO Client (live updates)
* Recharts (visual charts)
* TailwindCSS

**Backend**

* Node.js + Express
* MongoDB + Mongoose
* Socket.IO (WebSockets)
* Node-cron (scheduled checks)
* Axios (HTTP client)
* Prometheus-compatible metrics endpoint

*(Based on repo structure and common MERN patterns.)* ([GitHub][1])

---

##  Prerequisites

Make sure you have:

* **Node.js** (v18+)
* **npm** or **yarn**
* **MongoDB** (local or cloud)

*(Required for local development.)* ([GitHub][1])

---

## 🛠️ Installation & Setup

### Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file based on example or your own settings:

```env
PORT=5000
MONGODB_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret
NODE_ENV=development
# Optional alert configs:
SLACK_WEBHOOK_URL=
TELEGRAM_BOT_TOKEN=
EMAIL_HOST=
EMAIL_PORT=
EMAIL_USER=
EMAIL_PASS=
WHATSAPP_ACCESS_TOKEN=
```

Start backend server:

```bash
npm run dev
```

---

### Frontend Setup

```bash
cd frontend
npm install
```

Create `.env` file:

```env
VITE_API_URL=http://localhost:5000/api
```

Run frontend in development:

```bash
npm run dev
```

---

##  API Endpoints

*(Examples based on current design — update as implemented.)* ([GitHub][1])

### Services

```
GET /api/services
GET /api/services/:id
POST /api/services
PUT /api/services/:id
DELETE /api/services/:id
```

### Health & Metrics

```
GET /api/health/latest
GET /api/health/:serviceId/history
GET /metrics   # Prometheus export
```

### Alerts

```
POST /api/alerts/test  # Send test alert
```

---

##  Monitoring & Reliability

Sentinel calculates:

* **Service availability**
* **Latency percentiles (P50, P95, P99)**
* **Error rates**
* **SLO compliance**
* **Reliability scoring**

This helps teams catch performance regressions early.

---

##  Roadmap (Planned)

✨ Add role-based access & auth UI
✨ Dashboard graphs & drill-downs
✨ Kubernetes health integrations
✨ AI assisted anomaly detection
✨ Export reports & CSV/PDF
✨ Marketplace integrations (PagerDuty, Opsgenie, Teams)

---

##  Contributing

This project is open for collaboration.

To contribute:

1. Fork the repository
2. Create a feature branch
3. Commit & push
4. Open a pull request



##  Stay Updated

Follow the project for updates, demos, and deployment links.
Your feedback and contributions are welcome!

---


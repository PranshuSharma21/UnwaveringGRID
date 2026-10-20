# ⚡ G.R.I.D. Intelligence
**Gateway for Repairs, Inventory, and Dispatch**  
*One System. Every Building. Autonomous IoT & Predictive AI for Sustainable Building Infrastructure.*

![Node.js](https://img.shields.io/badge/Backend-Node.js%20%7C%20Express-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Socket.io](https://img.shields.io/badge/Real--Time-Socket.io%20WebSockets-010101?style=for-the-badge&logo=socketdotio&logoColor=white)
![Hardware](https://img.shields.io/badge/Edge%20IoT-ESP32%20%7C%20ESP8266-E7352C?style=for-the-badge&logo=espressif&logoColor=white)
![Status](https://img.shields.io/badge/Deployment-Live%20on%20Render-46E3B7?style=for-the-badge)

---

## 📌 Table of Contents
1. [Hosted & Fully Working Application](#1-hosted--fully-working-application)
2. [GitHub Source Code Repository Structure](#2-github-source-code-repository-structure)
3. [System Architecture Diagram](#3-system-architecture-diagram)
4. [Complete Overview & Local Setup Documentation](#4-complete-overview--local-setup-documentation)
5. [API & WebSocket Documentation](#5-api--websocket-documentation)
6. [Sample Dataset Used in the Project](#6-sample-dataset-used-in-the-project)
7. [Evaluation Results & Testing Details](#7-evaluation-results--testing-details)
8. [Demo Video](#8-demo-video)
9. [Deployment Instructions](#9-deployment-instructions)
10. [Core Team](#10-core-team)

---

## 1. Hosted & Fully Working Application

* **Live Web Application & Telemetry Backend:** [https://grid-ygrx.onrender.com](https://grid-ygrx.onrender.com)
* **Live Operator Dashboard:** [https://grid-ygrx.onrender.com/dashboard.html](https://grid-ygrx.onrender.com/dashboard.html)
* **Live Health / Telemetry Endpoint:** [https://grid-ygrx.onrender.com/api/telemetry/latest](https://grid-ygrx.onrender.com/api/telemetry/latest)

### 🔐 Dashboard Security Gate Credentials
To unlock the protected telemetry console (`dashboard.html`), use either of the following authorized accounts stored in `credentials.json`:

| Role | Username | Password |
| :--- | :--- | :--- |
| **System Administrator** | `admin` | `admin` |
| **Facility Operator** | `test` | `testpassword@123` |

---

## 2. GitHub Source Code Repository Structure

```text
grid-iot/
├── index.html          # Main landing page with interactive building X-ray & particle canvas
├── dashboard.html      # Auth-protected telemetry console (24h live curves & 48h clickable modal)
├── about.html          # Core team showcase with Three.js 3D interactive card vortexes
├── contact.html        # Direct inquiry portal integrated with Formspree REST API
├── beta.html           # GRID 2.0 early-access registration portal
├── credentials.json    # Operator authentication store for the dashboard security gate
├── server.js           # Node.js + Express + Socket.io ingestion & broadcast server
├── package.json        # Node dependencies and startup scripts
└── README.md           # Complete project, architecture, API, and deployment documentation

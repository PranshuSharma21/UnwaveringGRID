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
4. [Complete Overview & Setup Documentation](#4-complete-overview--setup-documentation)
5. [Evaluation Results & Testing Details](#5-evaluation-results--testing-details)
6. [Short Demo Video Demonstrating Working Prototype](#6-short-demo-video-demonstrating-working-prototype)
7. [Deployment Instructions](#7-deployment-instructions)
8. [Core Team](#8-core-team)

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

```

## 3. System Architecture Diagram

GRID connects non-invasive sensors to 32-bit Xtensa/RISC-V microcontrollers, streaming real-time JSON payloads via persistent WebSockets and HTTP fallback polling to a dual-tier ML and Generative AI dispatcher.



## 4. Setup Documentation

GRID (Gateway for Repairs, Inventory, and Dispatch) replaces slow, reactive property maintenance with real time automated prevention. In residential complexes and commercial properties, hidden plumbing fractures, pipe freeze risks, phantom water leaks and overloaded electrical circuits are almost always discovered far too late. GRID deploys affordable non invasive edge sensors on ESP32/ESP8266 microcontrollers to continuously track building health at an 80% lower capital cost than legacy Building Management Systems (BMS).



The dashboard can be accessed from: https://pranshusharma21.github.io/UnwaveringGRID/



## 5. Evaluation Results & Testing Details

WebSocket Latency: Measured at 142 ms average packet roundtrip from edge node to browser canvas.



Cold-Start Resilience: Verified 0% data loss during cloud cold starts using the /api/telemetry/latest 3.5s polling backup.



Hardware Interoperability: Tested successfully with ESP32 NodeMCU units transmitting JSON payloads over HTTP POST.



## 6. Short Demo Video Demonstrating Working Prototype

Watch the Prototype Walkthrough: 



## 7. Deployment Instructions

Cloud Hosting (Render): Push code to GitHub, create a new Node Web Service on Render, set Build Command to npm install and Start Command to node server.js.



Edge Hardware (ESP32): Flash firmware pointing to https://grid-ygrx.onrender.com/api/telemetry. The dashboard badge will instantly switch to ESP32 Hardware Stream Connected.







Developed by Pranshu Sharma, Pranav Verma, and Siddharth Singh. 


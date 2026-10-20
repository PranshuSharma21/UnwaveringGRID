flowchart LR
    subgraph EDGE ["1. Edge Sensing & Hardware Layer"]
        S1["💧 YF-S201 Flow &<br/>Analog Pressure"]
        S2["⚡ PZEM-004T &<br/>SCT-013 CT Clamp"]
        S3["🌡️ DHT22 / BME280<br/>Climate & Moisture"]
        S4["🌀 MPX5010DP<br/>HVAC Duct Probe"]
        MCU["🎛️ ESP32 / ESP8266<br/>Non-Blocking millis() C++"]
        S1 & S2 & S3 & S4 --> MCU
    end

    subgraph CLOUD ["2. Cloud Ingestion & Storage"]
        API["🌐 Node.js + Express<br/>POST /api/telemetry"]
        WS["⚡ Socket.io Server<br/>Real-Time Broadcast"]
        POLL["🔄 HTTP Fallback<br/>GET /api/telemetry/latest"]
        TSDB[("🗄️ Time-Series<br/>48h Ring Buffer")]
        MCU -- "Wi-Fi JSON Payload" --> API
        API --> WS
        API --> POLL
        API --> TSDB
    end

    subgraph AI ["3. Predictive Intelligence & Dispatch"]
        ML["📈 Rolling Baseline ML<br/>Micro-Leak & Surge Detection"]
        GEN["🤖 GenAI Work-Order Engine<br/>+ External Web Agent"]
        TSDB --> ML
        ML -- "Anomaly Flagged" --> GEN
    end

    subgraph CLIENT ["4. Operator & Resident Interfaces"]
        DASH["🖥️ Protected Web Dashboard<br/>24h Live & 48h History"]
        ALERT["📱 Automated SMS &<br/>Technician Dispatch Ticket"]
        WS & POLL --> DASH
        GEN --> ALERT
        GEN --> DASH
    end

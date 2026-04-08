# 🏭 Data Center Monitoring & Temperature Prediction (Node-RED + MQTT + AI)

## 🎯 Project Overview

This project is an industrial IoT application designed to monitor the state of a data center in real-time and predict temperature anomalies using AI techniques.

It combines real-time data streaming with MQTT and predictive analytics to anticipate overheating risks and improve system reliability.

---

## ⚙️ Technologies Used

* Node-RED (Flow-based IoT platform)
* MQTT (via Mosquitto broker)
* Node-RED Dashboard (UI visualization)
* JavaScript (data simulation & processing)
* Machine Learning (temperature prediction using regression logic inspired by TensorFlow)

---

## 🧠 Key Features

### 📡 Real-Time Data Simulation

* Simulates:

  * GPU usage (%)
  * Temperature (°C)
  * Fan speed (RPM)
* Updates every second

---

### 🔄 MQTT Communication

* Publishes metrics to topic: `datacenter/metrics`
* Subscribes to the same topic for real-time processing
* Uses a local Mosquitto broker

---

### 📊 Live Monitoring Dashboard

* Gauges:

  * GPU Load
  * Temperature
  * Fan Speed
* Charts:

  * Real-time evolution of metrics
* Alerts:

  * Notification when temperature exceeds threshold

---

### 🤖 AI Prediction (Temperature Forecast)

* Uses recent temperature history
* Applies linear regression to predict future temperature
* Forecasts temperature 5 seconds ahead

---

### 🚨 Smart Alerts

* 🟢 Normal (< 70°C)
* 🟠 Warning (70–79°C)
* 🔴 Critical (≥ 80°C)

Visual alerts and notifications are triggered automatically.

---

## 🧪 Flow Architecture

1. Data Simulation (Inject + Function)
2. MQTT Publish (datacenter/metrics)
3. MQTT Subscribe
4. JSON Parsing
5. Data Split (GPU / Temp / Fan)
6. Dashboard Visualization
7. AI Prediction Module
8. Alert System

---

## 🚀 How to Run

### 1. Install dependencies

```bash
npm install node-red-dashboard
```

### 2. Start MQTT Broker (Mosquitto)

Make sure Mosquitto is running locally:

```bash
mosquitto
```

### 3. Import the flow

* Open Node-RED
* Import `flow.json`

### 4. Deploy & Open Dashboard

* Deploy the flow
* Open:

```
http://localhost:1880/ui
```

---

## 📈 Output

* Real-time system monitoring
* Predictive temperature display
* Risk classification (Normal / Warning / Critical)
* Automatic alerts

---

## 💡 Use Case

This system can be used in:

* Data centers
* Cloud infrastructure monitoring
* Industrial IoT environments
* Predictive maintenance systems
# RFID Smart Card System – IoT Project

## 📌 Project Overview

This project implements an RFID-based smart card balance system using:

- ESP8266 (connected to RFID reader)
- MQTT Broker
- Backend API Service
- Web Dashboard

The system allows users to:
- Scan RFID cards
- View balance in real-time
- Top-up card balance from a web dashboard

---

## 🏗 System Architecture

### Communication Flow

1. RFID card is scanned.
2. ESP8266 reads card UID.
3. ESP8266 publishes scan data to MQTT Broker.
4. Backend subscribes to MQTT topic.
5. Backend processes card data and updates balance.
6. Backend sends real-time updates to Web Dashboard using WebSocket.
7. Dashboard can send top-up requests to Backend using HTTP.

---

## 🔌 Technologies Used

- ESP8266 (Arduino framework)
- MQTT Protocol (Publish–Subscribe)
- Backend: (e.g., Node.js / Express)
- WebSocket (real-time updates)
- HTTP REST API
- VPS Server
- GitHub for version control

---

## 📂 Repository Structure

/esp8266-firmware → ESP8266 source code
/backend-api → Backend server code
/web-dashboard → Frontend dashboard code
README.md → Project documentation


---

## 🚀 Live Web Dashboard

The dashboard is hosted on:

http://157.173.101.159:1883

---

## 🛠 How to Run the Project

### 1️⃣ Backend API

cd backend-api
npm install
node server.js

### 2️⃣ Web Dashboard

cd web-dashboard
npm install
npm start


Then open:

http://157.173.101.159:1883

### 3️⃣ ESP8266 Firmware

- Open firmware in Arduino IDE
- Update:
  - Wi-Fi credentials
  - MQTT broker IP
  - team_id
- Upload to ESP8266

---

## 📡 MQTT Topics Format

Our team used a unique team_id:

team_<team_id>/scan
team_<team_id>/balance
team_<team_id>/topup


This prevents topic conflicts on the shared broker.

---

## 👥 Team Information

Team ID: <your_team_id>

---

## ✅ Submission Checklist

- [x] Repository is Public
- [x] ESP8266 firmware included
- [x] Backend API included
- [x] Web dashboard included
- [x] README properly written
- [x] Live dashboard URL accessible



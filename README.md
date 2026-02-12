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


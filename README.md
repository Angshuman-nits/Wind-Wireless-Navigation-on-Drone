# 🚀 Wind – Wireless Navigation on Drone

## 📌 Overview
Wind is a custom-built **quadcopter drone** designed for **wireless communication, GPS-based autonomous navigation, and real-time telemetry**.  
The project integrates **Pixhawk 6X**, **Raspberry Pi 4B**, and **Mission Planner** to achieve stable flight, waypoint navigation, and wireless data transfer.  

---

## 🛠️ Design & Components
- **Frame:** Holybro X500 V2  
- **Motors:** 980kV brushless motors  
- **Flight Controller:** Pixhawk 6X (FMU v6X)  
- **Power Distribution:** Holybro PDB  
- **Controller:** Radiomaster FPV with ELRS Tx/Rx  
- **GPS Module:** M8N GPS  
- **Onboard Computer:** Raspberry Pi 4B  
- **Battery:** LiPo  

---

## 🔋 Electronics & Power
- **Power Distribution Board (PDB):** Supplies power from the battery to ESCs and onboard electronics.  
- **ESCs (Electronic Speed Controllers):** Convert DC battery power into 3-phase AC for brushless motors, controlling thrust and stability.  
- **Flight Time Estimation:** Battery capacity ÷ Current draw (with efficiency considerations).  

---

## 🎛️ Control & Navigation
- **Flight Dynamics:**  
  - Yaw → Torque differences  
  - Pitch/Roll → Varying opposite motor speeds  

- **GPS Integration:**  
  - Provides latitude, longitude, and altitude.  
  - Enables autonomous waypoint navigation with ~100 m range and ±1 m accuracy.  

- **Failsafe & Safety Features:**  
  - Manual mode switch  
  - Return-to-Home (RTH) on GPS loss  
  - Kill-switch on controller  

---

## 📡 Communication & Software
- **Firmware:** FMU v6X on Pixhawk 6X  
- **Ground Station Software:** Mission Planner  
  - Firmware setup and frame selection  
  - Sensor, ESC, compass, and radio calibration  
  - Flight mode configuration (Position Hold, Auto, Stabilize, Failsafe)  
  - PID tuning for stable flight  
  - Mission planning with waypoint-based path execution  

- **Wireless Communication:**  
  - ELRS protocol with Radiomaster controller → long range, low latency  
  - Raspberry Pi 4B handles wireless telemetry and communication  

---

## 🛠️ Debugging & Challenges
- **Motor Configuration Issue:**  
  - Default mapping in Mission Planner was reversed → incorrect thrust.  
  - Solved by motor test mode and remapping.  

- **Battery Imbalance:**  
  - Caused instability due to weight distribution.  
  - Fixed by adjusting placement to align center of gravity.  

---

## 🛡️ Safety Measures
- Motor tests without propellers  
- Open-area flight trials  
- Kill-switch on controller  
- Fail-safe landing/RTH enabled  

---

## 🎯 Outcomes
- Built quadcopter from scratch  
- Achieved stable manual flight  
- Enabled GPS-based autonomous waypoint navigation  
- Integrated Raspberry Pi for telemetry (ongoing)  

---

## 🔮 Future Scope
- Advanced telemetry and cloud integration  
- Computer vision for obstacle avoidance  
- AI-based adaptive flight  
- Multi-drone swarm systems  

---

## 🌍 Applications
- Surveillance & defense  
- Precision agriculture  
- Disaster relief & rescue  
- Environmental monitoring  
- UAV research & development  

---

## 📷 Gallery (Optional)
_Add images, wiring diagrams, or flight test results here._  

---

## 🛠️ Tech Stack
- Hardware: Pixhawk 6X, Holybro X500 V2, 980kV Motors, Radiomaster FPV, M8N GPS, Raspberry Pi 4B  
- Software: Mission Planner, FMU v6X Firmware, Python (for Pi integration)  
- Power: LiPo Battery, Holybro PDB, ESCs  

---

## 📌 License
This project is developed for research and educational purposes.  
Feel free to fork, contribute, and improve!

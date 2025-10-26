# 🌊 Design and Development of Underwater ROV

**By:** Rajeev Kumar 
**Under the Supervision of:** Dr. Navaneeth K. M.  
**Institute:** Thermo-Fluids Lab, IIT Ropar  

---

## 🧭 Project Overview

This project presents the **design and development of a low-cost, modular, and Wi-Fi-controlled Underwater Remotely Operated Vehicle (ROV)**.  
The goal is to create an **affordable and educational platform** for underwater exploration, environmental monitoring, and inspection tasks — especially suitable for **beginners, students, and research labs**.

Most commercial ROVs are expensive and complex; this design emphasizes **simplicity, scalability, and cost-effectiveness** while maintaining reliable performance in shallow waters.

<img width="700" height="500" alt="Model-1" src="https://github.com/user-attachments/assets/8d05722a-eab3-48e9-ad63-4593b9262e47" />

<img width="700" height="650" alt="Model-2" src="https://github.com/user-attachments/assets/a79e3d7a-491e-47f1-8c76-110fea27e93b" />

---

## ⚙️ Objectives

- To design a **stable and lightweight** ROV frame.  
- To enable **basic underwater navigation** (forward, reverse, turn, dive, and surface).  
- To integrate **depth measurement** using a waterproof pressure sensor.  
- To analyze **hydrodynamic performance** using ANSYS Fluent.  
- To create a **low-cost educational ROV platform**.

---

## 🧩 Mechanical Design

### 🧱 Frame Construction
- Built using **¾ inch PVC pipes** and **fitting connectors**.  
- Lightweight, corrosion-resistant, and easy to assemble.  
- Compact and **hydrodynamic** design for reduced drag.

### 💠 SolidWorks Models
- **Model 1:** Based on RS385 DC motors (20W each).  
- **Model 2:** Upgraded with **A2212 BLDC motors (100W)** and redesigned holders for enhanced thrust.

---

## 🌀 Propulsion and Control System

### ⚡ Propulsion
- **Three 12V RS385 DC motors** used for movement:
  - **Center Motor:** Controls **vertical motion** (dive/surface).  
  - **Side Motors:** Manage **horizontal movement** (forward, reverse, turning) using differential thrust.  

### 🔌 Control Mechanism
- Controlled via **L298N motor driver** for bidirectional speed and direction control.  
- Differential thrust used for turning control.  
- Power supplied from **12V DC battery pack** (sealed inside waterproof housing).

---

## ⚖️ Underwater Stability

The ROV maintains its stability through natural alignment of:
- **Center of Buoyancy (B):** Point where buoyant force acts.  
- **Center of Gravity (G):** Point where weight acts.  

A restoring couple between **B** and **G** ensures that the ROV remains upright and stable when disturbed by external forces.

---

## 🌊 Fluid Simulation (ANSYS Fluent)

- **Drag Force:** 7.74 N at 1 m/s velocity.  
- **Simulation Tool:** ANSYS Fluent.  
- **Purpose:** To evaluate drag distribution and optimize motor placement and frame geometry for reduced resistance.

---

## 📟 Electronics and Sensors

### 🧠 Control Circuit
- **Microcontroller:** ESP32 (Wi-Fi-based) or Arduino UNO.  
- **Motor Driver:** L298N H-Bridge module.  
- **Power:** 12V supply for motors, 5V for logic and sensors.

### 🌡️ Depth Measurement
- **Sensor:** Adafruit LPS33HW Water-Resistant Pressure Sensor.  
- **Pressure Range:** 260–1260 hPa (26–126 kPa).  
- **Max Depth:** ≈ 2.47 m (8.1 ft).  
- **Data Output:** Real-time pressure and temperature readings.

### 🧰 Circuit Summary
- Motors controlled through PWM signals.  
- Depth sensor communicates via I2C with ESP32.  
- Real-time telemetry transmitted wirelessly to surface control station.

---

## 🧪 Testing and Validation

- Successfully tested in a **water tank** for maneuvering and stability.  
- Depth measurement validated with submerged readings (~27 cm).  
- Stable orientation achieved due to optimized center of gravity and buoyancy placement.

---

## 🌐 Applications

1. **Underwater Inspection & Exploration**  
   - Surveying submerged structures, pipelines, and tanks.  
2. **Educational & Research Tool**  
   - Teaching robotics, hydrodynamics, and control systems.  
3. **Environmental Monitoring**  
   - Measuring water quality, temperature, and aquatic ecosystem data.  
4. **Shallow-Water Exploration**  
   - Ideal for ponds, reservoirs, and confined spaces.

---

## 🚀 Future Improvements

- Integrate **waterproof camera** for live video streaming.  
- Enhance **sensor waterproofing** and housing protection.  
- Extend **depth range** using advanced pressure sensors.  
- Add **soft robotic grippers** for object handling using hydraulic actuation.

---

## 🧰 Tools and Technologies Used

| Tool / Software | Purpose |
|-----------------|----------|
| **SolidWorks** | 3D Design and Modeling |
| **ANSYS Fluent** | Drag and Hydrodynamic Simulation |
| **Arduino IDE / ESP-IDF** | Microcontroller Programming |
| **Adafruit LPS33HW** | Depth Sensing |
| **PVC &**

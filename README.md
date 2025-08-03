
# 📦 Automated Storage and Retrieval System (ASRS) using PLC, HMI & Factory I/O

## 📘 Introduction

An **Automated Storage and Retrieval System (ASRS)** is a computer-controlled system used in warehouses and manufacturing facilities to automatically place and retrieve loads from predefined storage locations. These systems are designed to increase efficiency, reduce labor costs, improve accuracy, and optimize inventory management.

This project demonstrates a **fully simulated ASRS** system created using:
- **PLC (Programmable Logic Controller)** for control logic
- **HMI (Human Machine Interface)** for operator interaction
- **Factory I/O** for a realistic 3D simulation of the industrial environment

---

## 🎯 Objective

The main goal of this project is to simulate an **automated warehouse cell system** that performs:
- Loading of pallets to specific storage locations
- Unloading pallets from designated storage cells
- Monitoring and managing system status in real-time
- Visualizing and controlling operations through HMI
- Programming logic for emergency and reset functions

---

## 🛠️ Tools & Technologies Used

| Tool/Software      | Purpose                            |
|--------------------|-------------------------------------|
| **GX Works3**       | PLC programming (ladder logic)     |
| **GT Designer3**    | HMI screen design (GOT2000)        |
| **Factory I/O**     | 3D simulation of ASRS environment  |
| **OPC Client**      | Communication between PLC & Factory I/O |
| **Mitsubishi PLC**  | Simulated controller logic         |

---

## 🧠 System Description

- Total of **54 storage cells** available for operation.
- Two cranes:  
  - **SC1** for **Loading**  
  - **SC2** for **Unloading**
- **Sensors and actuators** are monitored via PLC logic.
- HMI screen displays real-time data like:
  - Current loading/unloading cell number
  - Total filled and empty cells
  - Start/Stop/Reset controls
  - Emergency Stop mechanism
- **Error Handling** and **Universal Reset** logic for smooth recovery.

---

## 🖥️ HMI Interface

![HMI Interface](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS%20HMI.jpg)

- Built using **GT Designer3 (GOT2000)**
- Features:
  - Power On/Off
  - Emergency Stop
  - Crane-specific controls
  - Digital counters for filled and empty cells
  - Reset button to clear system errors

---

## 🏭 Factory I/O Simulation

![Factory I/O Environment](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS%202.jpg)

- 3D model of a warehouse with racks, pallets, and conveyor belts.
- Crane SC1 moves pallets from the conveyor to storage cells.
- Crane SC2 retrieves pallets and places them on the output conveyor.
- Integrated via **OPC communication** with the PLC controller.

---

## 📋 PLC Programming Highlights

The ladder logic was developed using **GX Works3** and exported as an HTML file. Some key sections include:

- **Main Power Switching**
- **Crane SC1 & SC2 Power & Motion Memory**
- **Universal Reset Logic**
- **Emergency Stop Memory**
- **Position Tracking with D-registers (e.g., D8, D9, D5, D6)**
- **Calculation of filled/empty cells using counters and logic operations**
- **Cell targeting via D100 (SC1) and D200 (SC2)**

💡 PLC Code File: [`ASRS 12.html`](./ASRS%2012.html)

---

## 📌 Project Workflow

1. **System Initialization**:
   - Power ON via HMI
   - Cranes powered individually
2. **Loading Process (SC1)**:
   - Pallets picked from input conveyor
   - Stored at targeted cell using D100
   - Filled cell count updated
3. **Unloading Process (SC2)**:
   - Retrieves pallet from cell position D200
   - Places on output conveyor
   - Empty cell count updated
4. **Error/Reset Handling**:
   - System can be reset to initial state via universal reset
   - Emergency stop halts all operations

---

## 🧾 Key Features

- Real-time monitoring and control of warehouse operations
- Accurate cell tracking and position-based movement
- Emergency stop and recovery logic
- Seamless integration between PLC, HMI, and simulation software
- Practical understanding of industrial automation flow

---

## 📈 Learning Outcomes

- Developed strong understanding of **PLC ladder logic**
- Designed and simulated **HMI control panels**
- Learned **OPC-based communication** in automation
- Simulated real-world warehouse operation in a virtual 3D environment
- Improved knowledge of **industrial sensors, actuators, and safety protocols**

---

## 🧑‍💻 Author

**Tejas Waghmare**  
Mechanical Engineering Graduate | Industrial Automation & Robotics Enthusiast  
📍 [LinkedIn](https://www.linkedin.com/in/tejas-waghmare)

---

## 📎 Repository Contents

| File | Description |
|------|-------------|
| `ASRS.jpg` | HMI interface screenshot |
| `72b9c04a-1472-45aa-ba20-c506a9595b7e.png` | Factory I/O simulation screenshot |
| `ASRS 12.html` | Exported ladder logic from GX Works3 |

---

## 📌 Future Enhancements

- Implement barcode or RFID-based inventory tracking
- Expand to multi-level/multi-crane systems
- Add SCADA-level monitoring and reporting
- Introduce smart cell management using AI logic

---

## 📢 License

This project is open for educational and demonstration purposes.  
Please credit the author if reused or modified.


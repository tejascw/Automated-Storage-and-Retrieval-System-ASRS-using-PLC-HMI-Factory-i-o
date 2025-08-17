
# 📦 Automated Storage and Retrieval System (ASRS) using PLC, HMI & Factory I/O













## Video Demonstration 

[ASRS Project Video Demonstration](https://drive.google.com/drive/u/0/folders/1Bc2FBhvjG0uDNRdFsazBjdkv2YrzdnOJ)















https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS_PROJECT_VIDEO.mp4





























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


| HMI(Buld_up_layout)  |HMI(Simulation)                |
|--------------------|-------------------------------------|
|![HMI Interface](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS_HMI_PANNEL_BEFORE_SIMULATION.jpg)|(https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS_HMI_PANNEL_AFTER_SIMULATION.jpg)|   
  

- Built using **GT Designer3 (GOT2000)**
- Features:
  - Power On/Off
  - Emergency Stop
  - Crane-specific controls
  - Digital counters for filled and empty cells
  - Reset button to clear system errors

---

## 🏭 Factory I/O Simulation


| Images | Description             |
|--------------------|-------------------------------------|

| ![Factory I/O Environment](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS%202.jpg) |- 3D model of a warehouse with racks, pallets, and conveyor belts.
- Crane SC1 moves pallets from the conveyor to storage cells.
- Crane SC2 retrieves pallets and places them on the output conveyor.
- Integrated via **OPC communication** with the PLC controller.|
| ![Factory I/O Device](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS_Factory%20i_o%20Device%20Input_Output%20conections.jpg) |  This image shows the device Input and Output pin connections in Factory I/O.

Inputs (left side – Sensors/Buttons):
These are signals acquired from the system, such as sensors, limit switches, and push buttons. They provide real-time feedback to the PLC/Controller. For example:

Emergency Stop

Start/Stop Buttons

Limit switches (Left/Right, Middle, etc.)

Position sensors (Load Sensor, Exit Sensor, Unloading Sensor)

Movement status (SC1 Moving X, SC2 Moving Z, etc.)

Outputs (right side – Actuators):
These are control signals sent from the PLC/Controller to actuators that perform physical actions in the system. For example:

SC1 / SC2 Lift SET

Load/Unload Conveyor

Roller Conveyors

Target Position control

Start/Stop Indicator Lights

Middle Section (Server Mapping via MX OPC Configurator):
This shows the OPC server mapping (Mitsubishi MXOPC). Each input and output from Factory I/O is linked to its corresponding PLC tag address. The mapping ensures that sensor feedback (inputs) and actuator commands (outputs) are correctly exchanged between Factory I/O and the PLC.

So in short:

Inputs = acquiring data from sensors & buttons (feedback to PLC).

Outputs = actuating data to actuators (commands from PLC to perform actions).

Middle = OPC mapping layer where Factory I/O signals are connected to PLC addresses. |






---

## 📋 PLC Programming Highlights

[PLC_LADDER_LOGIC_PROGRAMMING](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/PLC_LADDER_LOGIC_PROGRAMMING.jpg)

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


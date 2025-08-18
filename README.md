
# 📦 Automated Storage and Retrieval System (ASRS) using PLC, HMI & Factory I/O



---


## 🎥 Demonstration Video

[ASRS Project Video Demonstration](https://drive.google.com/drive/u/0/folders/1Bc2FBhvjG0uDNRdFsazBjdkv2YrzdnOJ)


https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS_PROJECT_VIDEO.mp4


---

## 📘 Introduction

An **Automated Storage and Retrieval System (ASRS)** is a computer-controlled system used in warehouses and manufacturing facilities to automatically place and retrieve loads from predefined storage locations. These systems are designed to increase efficiency, reduce labor costs, improve accuracy, and optimize inventory management.

This project demonstrates a **fully simulated ASRS** system created using:
- **PLC (Programmable Logic Controller)** for control logic
- **HMI (Human Machine Interface)** for operator interaction
- **Factory I/O** for a realistic 3D simulation of the industrial environment

---
## 📂 Project Files  

| File Type | Description | File |
|-----------|-------------|------|
| 📘 PDF | Project report/documentation | [ASRS_Project_Report.pdf](https://github.com/user-attachments/files/21835509/ASRS.Project.plc.ladder.logic.file.pdf.pdf) |
| 🪢 GX Works3 File | PLC Ladder Logic Program | [ASRS_PLC_Ladder.gx3](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS12_HMI.GTX) |
| 🖥️ HMI File | HMI Design (GT Designer3) | [ASRS_HMI.gtx](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS12_HMI.GTX) |
| 🔗 MX OPC File | OPC server mapping | [ASRS_MXOPC.mxc](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS12.ldb) |
| 🏭 Factory I/O File | ASRS 3D Simulation | [ASRS_Factory_IO.fio](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS1.factoryio) |
| 📊 Excel File | ASRS Programming Data Sheet | [ASRS_Data.xlsx](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS%2012.xml) |
| 📄 Text File | Extra Notes & Configurations | [ASRS_Notes.txt](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS%2012.txt) |


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

## 🖥️ HMI Interface


| HMI(Buld_up_layout)  |HMI(Simulation)                |
|--------------------|-------------------------------------|
| ![HMI Interface](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS_HMI_PANNEL_BEFORE_SIMULATION.jpg)|![ASRS_HMI_PANNEL_AFTER_SIMULATION](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS_HMI_PANNEL_AFTER_SIMULATION.jpg) |   
  

- Built using **GT Designer3 (GOT2000)**
- Features:
  - Power On/Off
  - Emergency Stop
  - Crane-specific controls
  - Digital counters for filled and empty cells
  - Reset button to clear system errors

---

## 🏭 Factory I/O Simulation


# Images & Description 


![Factory I/O Environment](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS%202.jpg) 

3D model of a warehouse with racks, pallets, and conveyor belts. Crane SC1 moves pallets from the conveyor to storage cells. Crane SC2 retrieves pallets and places them on the output conveyor. Integrated via **OPC communication** with the PLC controller.

![Factory I/O Device](https://github.com/tejascw/Automated-Storage-and-Retrieval-System-ASRS-using-PLC-HMI-Factory-i-o/blob/main/ASRS_Factory%20i_o%20Device%20Input_Output%20conections.jpg) 

This image represents the device input and output pin connections in Factory I/O. On the left side are inputs, which consist of signals acquired from sensors, limit switches, and push buttons that provide real-time feedback to the PLC or controller (e.g., emergency stop, start/stop buttons, load/unload sensors, and movement status like SC1 Moving X or SC2 Moving Z). On the right side are outputs, which are control signals sent from the PLC to actuators that execute physical actions in the system, such as operating SC1/SC2 lifts, controlling load/unload conveyors, roller conveyors, target positioning, or activating indicator lights. The middle section represents the OPC mapping layer, where Factory I/O signals are linked to corresponding PLC tag addresses through the MX OPC Configurator. This mapping ensures proper communication, so that input feedback from the system reaches the PLC and output commands from the PLC drive the actuators. In short, inputs = feedback from the system, outputs = commands to the system, and the middle = the communication bridge via OPC mapping.

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


---

## 📈 Learning Outcomes

- Developed strong understanding of **PLC ladder logic**
- Designed and simulated **HMI control panels**
- Learned **OPC-based communication** in automation
- Simulated real-world warehouse operation in a virtual 3D environment
- Improved knowledge of **industrial sensors, actuators, and safety protocols**

---


## 📌 Future Enhancements

- Implement barcode or RFID-based inventory tracking
- Expand to multi-level/multi-crane systems
- Add SCADA-level monitoring and reporting
- Introduce smart cell management using AI logic

---

## 🚀 How to Run

Open the PLC program in GX Works3 and download it to the controller (or GX Simulator).

Launch Factory I/O and load the ASRS simulation file.

Configure MX OPC server for proper tag mapping.

Open HMI panel in GT Designer3 or GT Simulator3.

Start the simulation and control ASRS operations through the HMI.

---

## 🎯 Applications

Smart warehouses

Automated logistics

Industry 4.0 training & education

Real-time inventory management



---

## 🧑‍💻 Author

**Tejas Waghmare**  
Mechanical Engineering Graduate | Industrial Automation & Robotics Enthusiast  
📍 [LinkedIn](https://www.linkedin.com/in/tejas-waghmare)

---

📜 License

This project is developed as part of Bajaj Engineering Skill Training Program (BEST) and is intended for educational and research purposes.



---




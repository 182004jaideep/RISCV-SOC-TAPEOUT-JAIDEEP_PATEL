# 📘 Task 0 – Tool Installation and Setup

## 📑 Task Description
Install all the required tools listed in the setup document using the specified machine configuration.  
Update the GitHub repository with tool snapshots as proof of successful installation.  

***

## 💻 System Configuration
- **Virtual Machine**: Oracle VirtualBox  
- **OS**: Ubuntu 20.04 LTS  
- **RAM**: 6 GB  
- **HDD**: 50 GB  
- **CPU**: 4 vCPUs  

***

### 1. Yosys (Synthesis Tool)



## 🔧 Tools Installed and Their Use

| Tool | Use / Purpose |
|------|---------------|
| **Yosys** | Open-source RTL synthesis tool. Converts Verilog/SystemVerilog RTL designs into gate-level netlists for ASIC/FPGA implementation. |
| **Icarus Verilog (iverilog)** | Verilog simulator. Compiles and simulates RTL designs to verify functional correctness before synthesis. |
| **GTKWave** | Waveform viewer. Visualizes simulation results (.vcd/.fst files) to debug RTL and verify signals. |
| **Ngspice** | SPICE circuit simulator. Used for analog/mixed-signal simulation and verifying transistor-level circuits. |
| **Magic** | VLSI layout tool. Designs and edits IC layouts; supports LVS/DRC checks for physical verification. |
| **OpenLANE** | Automated RTL-to-GDSII flow. Converts RTL to layout-ready GDSII using synthesis, placement, routing, and PDK libraries. |
| **Docker** | Containerization tool used to run OpenLANE and other tools in a consistent environment without dependency issues. |

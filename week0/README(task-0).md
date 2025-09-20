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
```bash
$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make
$ sudo apt-get install build-essential clang bison flex \
  libreadline-dev gawk tcl-dev libffi-dev git \
  graphviz xdot pkg-config python3 libboost-system-dev \
  libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make
$ sudo make install
```

<img width="1616" height="456" alt="Screenshot 2025-09-19 235821" src="https://github.com/user-attachments/assets/2a13447f-0bd9-486f-8ca4-fb16221ceefb" />

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

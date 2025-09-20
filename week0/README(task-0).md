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

### 2. Icarus Verilog (Simulation Tool)
```bash
$ sudo apt-get update
$ sudo apt-get install iverilog
```

<img width="1546" height="1192" alt="Screenshot 2025-09-20 000753" src="https://github.com/user-attachments/assets/7a8c4797-9a44-4481-b140-f565b6a3737f" />

### 3. GTKWave (Waveform Viewer)

```bash
$ sudo apt-get update
$ sudo apt install gtkwave
```
<img width="1523" height="227" alt="Screenshot 2025-09-20 184109" src="https://github.com/user-attachments/assets/42827ddb-6742-4d9f-bf1b-4f757fb5b4bd" />

### 4. Ngspice (Circuit Simulation)
```bash
$ tar -zxvf ngspice-37.tar.gz
$ cd ngspice-37
$ mkdir release
$ cd release
$ ../configure --with-x --with-readline=yes --disable-debug
$ make
$ sudo make install
```
<img width="1613" height="427" alt="Screenshot 2025-09-20 210903" src="https://github.com/user-attachments/assets/1af2207f-f38f-43a3-b774-7550be2f68d4" />

### 5. Magic (Layout Tool)
```bash
$ sudo apt-get install m4
$ sudo apt-get install tcsh
$ sudo apt-get install csh
$ sudo apt-get install libx11-dev
$ sudo apt-get install tcl-dev tk-dev
$ sudo apt-get install libcairo2-dev
$ sudo apt-get install mesa-common-dev libglu1-mesa-dev
$ sudo apt-get install libncurses-dev
$ git clone https://github.com/RTimothyEdwards/magic
$ cd magic
$ ./configure
$ make
$ sudo make install
```

<img width="1921" height="1154" alt="Screenshot 2025-09-20 184150" src="https://github.com/user-attachments/assets/d9670cbb-246a-468b-b6bd-06b33e0200e5" />

### 6. OpenLANE (RTL to GDSII Flow)
```bash
$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo apt install -y build-essential python3 python3-venv python3-pip make git
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o \
  /usr/share/keyrings/docker-archive-keyring.gpg
$ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
  https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee \
  /etc/apt/sources.list.d/docker.list > /dev/null
$ sudo apt update
$ sudo apt install docker-ce docker-ce-cli containerd.io
$ sudo docker run hello-world
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ sudo reboot
```
<img width="1597" height="730" alt="Screenshot 2025-09-20 184235" src="https://github.com/user-attachments/assets/806d3698-3bf1-40ca-96bd-eeb30c7d4a6b" />

**System Information:**
- **Python**: 3.12.3
- **pip**: 24.0 from /usr/lib/python3/dist-packages/pip (python 3.12)
- **GNU Make**: 4.3 (Built for x86_64-pc-linux-gnu)
- 
<img width="1602" height="497" alt="Screenshot 2025-09-20 184357" src="https://github.com/user-attachments/assets/a27aa989-5eb5-4125-8beb-e89f9868662b" />

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

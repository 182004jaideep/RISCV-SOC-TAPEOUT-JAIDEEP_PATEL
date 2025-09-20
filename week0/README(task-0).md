# 📘 Task 0 – Tool Installation and Setup

## 📑 Task Description
Install all the required tools listed in the setup document using the specified machine configuration.  
Update the GitHub repository with tool snapshots as proof of successful installation.  

---

## 💻 System Configuration
- **Virtual Machine**: Oracle VirtualBox  
- **OS**: Ubuntu 20.04 LTS  
- **RAM**: 6 GB  
- **HDD**: 50 GB  
- **CPU**: 4 vCPUs  

---

### 1. Yosys (Synthesis Tool)

```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex \
  libreadline-dev gawk tcl-dev libffi-dev git \
  graphviz xdot pkg-config python3 libboost-system-dev \
  libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install

sudo make install
```bash

<img width="1616" height="456" alt="Screenshot 2025-09-19 235821" src="https://github.com/user-attachments/assets/46561152-984e-4d0e-b0bf-73216b5c5e6d" />

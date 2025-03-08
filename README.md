# 👨‍💻 SOC-Home-Labs-Manual: Attack & Defense Simulations


# Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Network Topology](#network-topology)
4. [Installation Guide](#installation-guide)
5. [Screenshots](#screenshots)
6. [Conclusion](#conclusion)




---
## 📌Introduction
This project demonstrates the step-by-step implementation of a Security Operations Center (SOC) home lab focused on Security Information and Event Management (SIEM), highlighting practical SIEM setup, event monitoring, log analysis, and threat detection simulations

Highlights:

- Designed a virtualized SOC environment with Splunk/Elastic SIEM solutions.
- Configured realistic log generation from Windows and Linux endpoints.
- Simulated attack scenarios using Kali Linux and Metasploit.
- Provided clear guidelines and resources for SOC beginners

---
## 🔧Prerequisites

| Category                 | Component                           | Recommended Specs                               |
|--------------------------|-------------------------------------|-------------------------------------------------|
| **Hardware**             | RAM                                 | Minimum 16GB (Recommended 32GB+)                |
|                          |  CPU                                |  Minimum 4 cores (Recommended 8 cores)          |
|                          | Storage                             | SSD, minimum 500GB                              |
|                          | Network                             | Internet Connectivity for software downloads    |

| **Virtualization Software** | **Download Link** | **Installation Guide**  |
|-----------------------------|-------------------|--------------------|
| VMware Workstation Pro      | [Click Here](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html) | [Click Here](https://youtu.be/kTO810vbF_E?si=GJo7qoggLWQPi2pA) |

| **Operating Systems**         | **Purpose**                 | **Download Link** | **Installation Gudie** |
|------------------------------|--------------------------------------|------------|---------------|
| Windows Server 2022 Eval  | Windows Server VM (Logging Server/Active Directory Domain Controller |[Click Here](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022) | [Click Here](https://www.youtube.com/watch?v=II-a79HFQtQ)
| Windows 10 Enterprise (90-day Eval) | Windows Client VM (Endpoint) |[Click Here](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise) | [Click Here](https://www.youtube.com/watch?v=C-avnck74gs)
| Ubuntu Server (Latest LTS)  | Ubuntu SIEM VM (SIEM Tools and Log Collection) |[Click Here](https://ubuntu.com/download/server) | [Click Here](https://www.youtube.com/watch?v=TvvxAPbgT8w) |

| **SIEM Tools**              | **Download Link**   | **Installation Guide**  |
|-----------------------------|-----------------------|----------------------------|
| Splunk Enterprise (Free)    | [Click Here](https://www.splunk.com/en_us/download/splunk-enterprise.html)| [Click Here](https://youtu.be/GtikcQfKb04?si=sluhnbcl-v1mOWXd) |
| Elastic Skack | [Click Here](http://elastic.co/downloads/) | [Click Here](https://www.elastic.co/guide/en/elastic-stack/current/installing-elastic-stack.html) |


| **Log Collection Tools** | **Download Link**  | **Installation Guide**                                            |
|--------------------------|---------------------|-------------------------------------------|
| Sysmon (Windows)         | [Click Here](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon) | [Click Here](https://www.youtube.com/watch?v=uJ7pv6blyog) |
| Winlogbeat (Windows)     | [Click Here](https://www.elastic.co/downloads/beats/winlogbeat) | [Click Link](https://www.youtube.com/watch?v=3nMupYp7aBk) |
| Filebeat (Linux)         | [Click Here](https://www.elastic.co/downloads/beats/filebeat) | [Click Here](https://youtu.be/P4AnY2Xpk2s?si=RHWvyc0NdLiK2zke) |

| **Attack Simulation Tools (Optional)** | **Download Link** |
|----------------------------------------|-------------------|
| Kali Linux                             | [Click Here](https://www.kali.org/get-kali/) |
| Metasploit Framework                   | [Click Here](https://www.metasploit.com/)     |

## Network Topology

## SOC Home Lab Virtual Network

```
SOC Home Lab Virtual Network
│
├── SIEM Server VM (Ubuntu: Splunk or Elastic SIEM)
│
├── Windows Server VM (Domain Controller & Logging)
│
├── Windows 10 Client VM (Endpoint Simulation & Logging)
│
├── Ubuntu Linux VM (Log Collection & Forwarding)
│
├── Kali Linux VM (Attack Simulation & Penetration Testing)
│
└── Metasploit VM (Exploit & Attack Simulations)
```

## Installation Guide
# SOC Home Lab - Installation Guide

Follow these clear step-by-step instructions to set up your SOC Home Lab environment focusing on SIEM concepts:

---

## 📌 Step-by-Step Installation Guide

### **Step 1: Set Up VMware Workstation Pro**
- **Download VMware Workstation Pro:** [Official Link](https://www.vmware.com/products/workstation-pro.html)
- Install VMware Workstation Pro on your host machine (Windows/Mac Machine).

### **Step 1.1: Configure Virtual Networking**
- Open VMware Workstation.
- Go to **Edit → Virtual Network Editor**.
- Create a new network in **Host-only mode** or **NAT mode**.
- Assign static IP addresses within the virtual subnet (e.g., 192.168.50.x).

---

### **Step 2: Install Virtual Machines On VMWare**

#### **1. Windows Server VM**
- **Purpose:** Domain Controller (Optional), Logging
- **Download:** [Windows Server 2022 Evaluation](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022)
- Install Windows Server on VMware [Refer Link In Prerequisites Section].
- Configure as Active Directory Domain Controller (optional).

#### **2. Windows 10 Client VM**
- **Download:** [Windows 10 Enterprise Evaluation](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise)
- Installation guide: [Refer Link In Prerequisites Section]

#### **3. Ubuntu SIEM VM**
- **Download Ubuntu Server ISO:** [Ubuntu 22.04 LTS](https://ubuntu.com/download/server)
- Install Ubuntu Server in VMware [Refer Link In Prerequisites Section]

#### **4. Install Metasploit**
- **Download Metasploitable Machine Here:** [Metasploit](https://www.rapid7.com/products/metasploit/metasploitable/)
- Install Metasploit in VMWare: [Refer Link](https://www.youtube.com/watch?v=o3Lcha65fsM)

#### **5. Install Kali Linux**
- - **Download Kali Linux Machine Here:** [Kali Linux](https://www.kali.org/get-kali/#kali-platforms)
- Install Metasploit in VMWare: [Refer Link](https://www.youtube.com/watch?v=A1Bm9KmPQ0o)

---

#### **Step 3: Install and Configure SIEM Tool**

#### **Splunk (Recommended)**
- [Splunk Enterprise Free Version](https://www.splunk.com/en_us/download/splunk-enterprise.html)
- Splunk Installation Guide (Ubuntu) [Refer Link In Prerequisites Section]

**Or**

#### **Elastic Stack (Elasticsearch, Logstash, Kibana)**
- Elastic Stack Official Installation Guide [Refer Link In Prerequisites Section]

---

#### **Step 4: Endpoint Logging Configuration**

#### **Windows VM Setup**
- **Sysmon Installation:** [Official Sysmon Download](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- **Winlogbeat Installation:** [Official Guide](https://www.elastic.co/guide/en/beats/winlogbeat/current/winlogbeat-installation.html)

#### **Ubuntu Linux VM (Log Collection)**
- **Filebeat Installation:** [Official Guide](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-installation.html)

---

#### **Step 5: Configure Log Forwarding to SIEM**
- Configure **Winlogbeat** (Windows) and **Filebeat** (Linux) to forward logs to your SIEM (Splunk/Elastic).
- Validate log ingestion in SIEM dashboards.

---

#### **Step 6: Dashboards & Alerts Configuration**
- Create custom dashboards in your SIEM to visualize key security events:
  - Logon Events, Process Creations, Network Traffic, Alerts
- Set up basic alert rules for suspicious behaviors, e.g., multiple failed logins.

---

#### **Step 7: Simulate Security Incidents**
- **Atomic Red Team Installation (on Windows):** [GitHub Repo](https://github.com/redcanaryco/atomic-red-team)
- Utilize Kali Linux and Metasploit (already installed) for additional attack simulations.

---

#### **Step 8: Practice Incident Detection & Response**
- Simulate various security scenarios using Atomic Red Team.
- Investigate triggered alerts within your SIEM.
- Refine detection rules based on findings.

---

#### **Step 9: Documentation & Improvement**
- Continuously document your lab setup, SIEM rules, detection methods, and incident-response actions.
- Regularly update and refine your lab configurations based on your learning outcomes.

---

## 🛠️ Tools & Software Summary
| Component | Software | Link |
|-----------|----------|------|
| Virtualization | VMware Workstation Pro | [Link](https://www.vmware.com/products/workstation-pro.html) |
| SIEM | Splunk / Elastic Stack | [Splunk](https://www.splunk.com/en_us/download/splunk-enterprise.html), [Elastic](https://elastic.co) |
| Windows Server OS | Windows Server 2022 Eval. | [Link](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022) |
| Windows Client OS | Windows 10 Enterprise Evaluation | [Link](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise) |
| Linux OS | Ubuntu Server 22.04 LTS | [Link](https://ubuntu.com/download/server) |
| Endpoint Logging | Sysmon, Winlogbeat, Filebeat | [Link](https://www.elastic.co/beats) |
| Attack Simulation | Atomic Red Team | [Link](https://github.com/redcanaryco/atomic-red-team) |

---

This guide will comprehensively prepare your lab to practice and master SIEM and SOC operational concepts.

## Screenshots

## Conclusion
This project demonstrates how to:
- Set up a cybersecurity home lab
- Deploy and detect malware
- Use Splunk for threat monitoring

> **Note:** This is for educational purposes only. Do not use these techniques for unauthorized activities.





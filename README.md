<h1 align="center">🔐 Cybersecurity Lab Environment Setup</h1>

<p align="center">
  Kali Linux • VirtualBox • Networking • Cybersecurity Labs
</p>


---

📌 Project Overview
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

This project details the step-by-step setup of a secure, virtualized security lab using Kali Linux and Oracle VirtualBox.

The main goal of this lab is to offer a safe playground for exploring ethical hacking techniques, analyzing network traffic, performing system scans, and testing security software without risking external networks.

It includes a pre-configured private network structure, making it simple to attach new virtual targets for future lab challenges and security simulations.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

🎯 Objectives
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

The main objectives of this project are to:

• Install and configure VirtualBox.

•Install/import Kali Linux as a virtual machine.

• Create a private NAT Network for the cybersecurity lab

• Configure network connectivity for Kali Linux.

• Assign a consistent IP address to the Kali VM.

• Verify network connectivity and DNS resolution.

• Take a clean VM snapshot for recovery.

• Document the complete setup process.

• Prepare the environment for future cybersecurity projects.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

🛡️ Lab Purpose
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

The laboratory serves as a safe, isolated space for mastering cybersecurity fundamentals and performing sanctioned security audits.

Future exercises may include:

🔎 Target discovery and intelligence gathering

🌐 Network enumeration and port probing

🛡️ System vulnerability identification

📡 Traffic capture and packet inspection

🌍 Web application security auditing

🧪 Hands-on testing of security tools

💻 Practical exercises on vulnerable target machines

⚠️ Important: Every security test conducted within this environment must strictly target self-owned assets or systems with formal permission. Cybersecurity software and methodologies must never be deployed against unauthorized targets.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

Lab Architecture
-------------------------------------------------------------------------------------------------------------------------------------------------------------------


<img width="1896" height="1045" alt="Screenshot 2026-09-11 195119" src="https://github.com/user-attachments/assets/1f527461-251c-4c79-a329-9cfb114f4bcb" />


Additional target machines can be added to the same virtual network in future projects.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

🖥️ Lab Environment
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

Component	Configuration

### 🖥️ Lab Environment Specifications

| 🧩 Component | ⚙️ Configuration |
| :--- | :--- |
| **🖥️ Host OS** | Windows 11 |
| **🧠 Host RAM** | 16 GB |
| **⚡ Processor** | Intel Core i5 |
| **🧰 Hypervisor** | VirtualBox 7.2 |
| **🐉 Security OS** | Kali Linux 2026.2 |
| **🧠 Kali RAM** | 2048 MB |
| **🌐 Virtual Network** | NAT Network |
| **📡 Network Address** | `10.0.0.0/24` |
| **🐧 Kali IP Address** | `10.0.0.2/24` |
| **🚪 Default Gateway** | `10.0.0.1` |
| **🌍 DNS Server** | `8.8.8.8` |
| **🔮 Future VM Range** | `10.0.0.3–10.0.0.99` |


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

🧰 Tools & Resources
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

The following tools and resources were used to build the virtual cybersecurity laboratory:

| 🛠️ Tool / Technology | 🎯 Primary Purpose |
| :--- | :--- |
| **7-Zip** | Extracting and managing compressed files |
| **Oracle VirtualBox** | Creating and managing virtual machines |
| **Kali Linux** | Cybersecurity learning and testing environment |
| **NAT Network** | Providing isolated virtual network connectivity |
| **Linux Networking Tools** | Configuring and troubleshooting network connectivity |
| **VirtualBox Snapshots** | Creating recovery points for the VM |



🔗 Official Resources
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

- 7-Zip: [7-Zip Downloads](https://7-zip.org/download.html)
 
- Oracle VirtualBox: [VirtualBox Downloads](https://7-zip.org/download.html)
  
- Kali Linux: [Kali Linux Downloads](https://7-zip.org/download.html)

-------------------------------------------------------------------------------------------------------------------------------------------------------------------



📌 Week 1 Setup Flow
-------------------------------------------------------------------------------------------------------------------------------------------------------------------


7-Zip
   ↓
VirtualBox Installation
   ↓
NAT Network Configuration
   ↓
Kali Linux Import
   ↓
IPv4 & Network Configuration
   ↓
Connectivity Verification
   ↓
Clean VM Snapshot

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

Lab Setup Procedure
-------------------------------------------------------------------------------------------------------------------------------------------------------------------


🛡️ Phase 01 — Lab Setup
-------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 1. Installing 7-Zip

### Overview

The first step was installing **7-Zip**, which was needed to extract the compressed files containing the virtual machine.

### Steps Performed

- Installed 7-Zip on the host system.
- Used it to extract the downloaded Kali Linux virtual machine files.
- Verified that the required VM files were available after extraction.

### Outcome

The Kali Linux VM files were successfully extracted and prepared for use with VirtualBox.

---

## 2. Installing Oracle VirtualBox

### Overview

Next, I installed **Oracle VirtualBox** to create and manage the virtual cybersecurity lab environment.

VirtualBox allows a separate operating system to run inside the main computer without replacing the existing operating system. This makes it useful for creating an isolated environment for cybersecurity practice.

### Steps Performed

- Installed Oracle VirtualBox.
- Opened VirtualBox and verified that it was functioning correctly.
- Prepared the virtualization environment for the Kali Linux VM.

### Outcome

VirtualBox was successfully installed and ready for importing the Kali Linux virtual machine.


<img width="997" height="788" alt="Screenshot 2026-09-11 203518" src="https://github.com/user-attachments/assets/8d31c9d6-4445-4ed3-bf2e-6c082dcf05b8" />


---

## 3. Configuring the NAT Network

### Overview

A dedicated **NAT Network** was created in VirtualBox to provide networking for the cybersecurity laboratory.

The network uses a private IP range so that virtual machines can communicate within the lab while still being able to access the Internet through NAT.

### Network Configuration

| Setting | Value |
|---|---|
| Network Type | NAT Network |
| Network Name | NatNetwork |
| Network CIDR | `10.0.0.0/24` |
| DHCP | Enabled |
| Gateway | `10.0.0.1` |

### Outcome

The dedicated NAT Network was successfully created and configured. It can also be used for connecting additional virtual machines to the lab in future exercises.

**Image:**

<img width="997" height="788" alt="Screenshot 2026-09-11 203518" src="https://github.com/user-attachments/assets/3196e504-8ed0-43a7-916d-db0e6dc89f45" />




<img width="952" height="720" alt="Screenshot 2026-09-11 204822" src="https://github.com/user-attachments/assets/c5ea1577-e985-414b-8580-998ed1ed3fed" />


---

## 4. Setting Up the Kali Linux Virtual Machine

### Overview

After configuring the network, I imported the **Kali Linux** virtual machine into Oracle VirtualBox and connected it to the previously created `NatNetwork`.

Kali Linux was selected as the primary operating system for the lab because it includes many tools commonly used for cybersecurity learning, network analysis, and authorized security testing.

### VM Configuration

| Setting | Value |
|---|---|
| Operating System | Kali Linux |
| Version | 2026.2 |
| Virtualization Platform | Oracle VirtualBox |
| Network | `NatNetwork` |

### Outcome

The Kali Linux virtual machine was successfully imported, started, and connected to the laboratory network.

**Images:**

<img width="952" height="741" alt="image" src="https://github.com/user-attachments/assets/72c828d6-05a0-47f5-a9d0-4aeeec223e71" />


---

## 5. Configuring Network Connectivity in Kali Linux

### Overview

The Kali Linux network interface was then configured so that the virtual machine could communicate with the NAT Network and access external network resources.

### Network Configuration

| Setting | Value |
|---|---|
| IP Address | `10.0.0.2/24` |
| Gateway | `10.0.0.1` |
| DNS | `8.8.8.8` |


---

## 🐞 Troubleshooting

During the initial lab setup, I encountered a few issues related to network configuration and hardware virtualization. I documented the problems and the steps taken to resolve them.

---

### 1. Internet Connectivity Issue After Static IP Configuration

#### 🔴 Problem

After manually configuring the IPv4 settings in Kali Linux, the VM was unable to connect to the Internet properly.

The issue was related to the NetworkManager connection configuration.

#### 🔧 Solution

I modified the NetworkManager connection using:

`sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0`

After applying the change, I restarted the network connection and tested the connectivity again.

#### ✅ Outcome

Internet connectivity was successfully restored, and the Kali Linux VM was able to access external network resources normally.

#### 💡 Note

Network connection names can vary between systems. To check the available connection names, use:

`nmcli connection show`

The connection name shown on the system should be used in place of `"Wired connection 1"`.

---

### 2. VirtualBox VT-x / Hardware Virtualization Error

#### 🔴 Problem

The Kali Linux VM initially failed to start in VirtualBox because hardware virtualization was disabled in the computer's BIOS/UEFI settings.

#### 🔧 Solution

The issue was resolved by:

1. Restarting the computer.
2. Entering the BIOS/UEFI settings.
3. Locating the hardware virtualization option.
4. Enabling **Intel VT-x / Intel Virtualization Technology**.
5. Saving the BIOS/UEFI changes.
6. Restarting the computer.
7. Launching the Kali Linux VM again through VirtualBox.

#### ✅ Outcome

Hardware virtualization was enabled successfully, and the Kali Linux VM started normally in VirtualBox.

#### 💡 Note

Hardware virtualization may appear under a slightly different name depending on the computer or BIOS/UEFI manufacturer. On Intel systems, it is commonly listed as **Intel Virtualization Technology** or **Intel VT-x**.

---


## 📚 What I Learned

Setting up this lab gave me practical experience with virtualization, networking, Kali Linux, and basic troubleshooting. I was able to understand these concepts by actually configuring and testing them rather than only studying them theoretically.

---

### 1. NAT vs. NAT Network

I learned the difference between **NAT** and **NAT Network** in VirtualBox.

A regular NAT setup mainly provides Internet access to a virtual machine, while a NAT Network allows multiple virtual machines connected to the same virtual network to communicate with each other while also providing Internet access.

This makes NAT Network useful for building a multi-machine cybersecurity laboratory.

---

### 2. Virtual Machine Networking

I learned how VirtualBox's virtual network adapters connect virtual machines to different types of networks.

I also gained a basic understanding of how network settings such as:

- IP address
- Subnet / CIDR
- Default gateway
- DNS
- Network mode
- Routing

affect communication between a virtual machine and other network resources.

---

### 3. Static IP Configuration

I gained hands-on experience configuring and checking IPv4 settings in Kali Linux.

I worked with:

- IPv4 address
- Subnet mask / CIDR
- Default gateway
- DNS server
- Network connectivity

I also practiced using Linux networking commands to check the configuration and troubleshoot connectivity issues.

---

### 4. Virtual Machine Snapshots

I learned the importance of creating a snapshot after reaching a stable VM configuration.

A snapshot provides a **known-good restore point**, which makes it possible to return the virtual machine to an earlier state if a future experiment or configuration change causes problems.

This is especially useful when working with cybersecurity tools and experimental environments.

---

### 5. Troubleshooting and Problem Solving

The setup gave me practical experience dealing with networking and virtualization issues.

I worked with:

- NetworkManager
- `nmcli`
- IPv4 configuration
- VirtualBox networking
- BIOS/UEFI settings
- Hardware virtualization

Instead of relying only on trial and error, I learned to identify the problem, check the relevant configuration, apply a possible solution, and then verify whether the issue was resolved.

---

### 6. Technical Documentation

I also learned the importance of documenting technical work.

Recording the environment, configurations, commands, screenshots, problems, solutions, and results makes a project easier to understand, reproduce, troubleshoot, and maintain.

This documentation will also provide a useful reference for future cybersecurity laboratory exercises.

---

🔐 Security & Ethical Use
---

This laboratory is intended strictly for education purposes only.


---

👨‍🏫 Mentor
---

Waqas Karim (CCIE)

Thank you for the valuable technical guidance and hands-on learning experience throughout the internship.

---

👤 Author
---

Albina Shakil

Cybersecurity Learner B083

LinkedIn: https://www.linkedin.com/in/albina-s-3a08952a4/

---

📌 Project Information
---

Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup | Repository: GitHub











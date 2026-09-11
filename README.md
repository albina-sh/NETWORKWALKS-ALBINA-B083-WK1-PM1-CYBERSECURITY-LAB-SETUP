# networkwalks-B082-week1-Cybersecurity-lab-Setup
Cybersecurity Lab Setup

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

<img width="1896" height="1045" alt="Screenshot 2026-09-11 195119" src="https://github.com/user-attachments/assets/8b6840ef-e6f2-4484-a577-ee49c7cd8ce7" />


image

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

### Commands Used

```bash
ifconfig
sudo ifconfig eth0 down
sudo ifconfig eth0 up
ping google.com

🐞 Problems Encountered & Solutions

Documenting troubleshooting experiences demonstrates practical problem-solving skills and provides a reference for resolving similar issues in future laboratory setups.

Problem 1 — Internet Connectivity After Static IP Configuration

🔴 Issue

After manually configuring the IPv4 settings, the Kali Linux VM experienced Internet connectivity issues. This can occur when NetworkManager connection properties are not configured correctly for the selected network setup.

🔧 Troubleshooting

The NetworkManager connection was modified using:

sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0

The network connection was then restarted, and connectivity was tested again.

✅ Result

Internet connectivity was successfully restored after applying the configuration and restarting the network connection.

💡 Important Note

Network connection names can vary between systems. Before modifying a connection, identify the actual connection name with:

nmcli connection show

Then replace "Wired connection 1" with the connection name shown on your system.

Problem 2 — VirtualBox VT-x / Hardware Virtualization Error

🔴 Issue

The Kali Linux VM initially failed to start because hardware virtualization was disabled in the system's BIOS/UEFI firmware.

🔧 Solution

The issue was resolved by:

Restarting the computer.

Entering the BIOS/UEFI settings.

Locating the hardware virtualization option.

Enabling Intel VT-x / Intel Virtualization Technology.

Saving the BIOS/UEFI configuration.

Restarting the computer.

Launching the Kali Linux VM again.

✅ Result

Hardware virtualization was enabled successfully, and the Kali Linux VM started normally in VirtualBox.

💡 What I Learned

Through this project, I gained practical experience in building and configuring a virtual cybersecurity laboratory using VirtualBox and Kali Linux.

The key concepts and skills I developed during Week 1 include:

1️⃣ NAT vs. NAT Network

I learned the difference between NAT and NAT Network configurations in VirtualBox.

A standard NAT configuration primarily provides Internet access to an individual virtual machine, while a NAT Network allows multiple virtual machines connected to the same virtual network to communicate with each other while also providing external network connectivity.

This makes NAT Network particularly useful for creating a multi-machine cybersecurity laboratory.

2️⃣ Virtual Machine Networking

I learned how VirtualBox virtual network adapters connect virtual machines to different types of networks.

I also gained an understanding of how network mode, IP addressing, gateways, and routing affect communication between virtual machines and external networks.

3️⃣ Static IP Configuration

I gained practical experience configuring and verifying IPv4 network settings in Kali Linux, including:

IPv4 address

Subnet mask / CIDR

Default gateway

DNS server

Network connectivity

I also practiced using Linux networking commands to verify and troubleshoot the configuration.

4️⃣ Virtual Machine Snapshots

I learned the importance of creating a clean VM snapshot before performing experimental or potentially disruptive activities.

A snapshot provides a known-good recovery point, making it easier to restore the laboratory environment when required.

5️⃣ Troubleshooting & Problem Solving

During the setup, I encountered networking and virtualization-related issues.

By troubleshooting these problems, I gained practical experience with:

NetworkManager

nmcli
IPv4 configuration
VirtualBox networking
BIOS/UEFI virtualization settings
Hardware virtualization

This helped me understand how to approach technical problems systematically rather than relying only on trial and error.

6️⃣ Technical Documentation

I learned that documentation is an important part of professional cybersecurity work.

Recording the environment, configurations, commands, screenshots, problems, solutions, and verification results makes the project easier to understand, reproduce, troubleshoot, and maintain.

🔐 Security & Ethics
This laboratory is intended for educational and authorized cybersecurity practice only.

Security testing should only be performed on systems, networks, applications, or devices that you own or have explicit permission to test.

👨‍🏫 Mentor

Waqas Karim (CCIE)

Thank you for the technical guidance and practical learning opportunity throughout the internship.

👤 Author

Rabi Chaudhary

Cybersecurity Professional B082

LinkedIn: https://lnkd.in/p/dS6wFAVN

📌 Project Information

Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity & Pentesting Lab Setup | Repository: GitHub











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


<img width="1919" height="997" alt="image" src="https://github.com/user-attachments/assets/0fad236f-78b8-42ff-a51b-a513ab28168f" />

Additional target machines can be added to the same virtual network in future projects.


🖥️ Lab Environment

Component	Configuration

Host Operating System	Windows 11

Processor	Intel Core i3 / i5

RAM	16 GB

Storage	512 GB SSD

Virtualization Platform	Oracle VirtualBox

Guest Operating System	Kali Linux 2026.2

Network Type	NAT Network

Network CIDR	10.0.0.0/24

Kali Linux IP	10.0.0.2/24

Gateway	10.0.0.1

DNS Server	8.8.8.8


🌐 Network Configuration

The Kali Linux virtual machine is connected to a dedicated NAT Network using the 10.0.0.0/24 private address range.

The basic network configuration is:

Network     : 10.0.0.0/24
Gateway     : 10.0.0.1
Kali VM     : 10.0.0.2/24
DNS         : 8.8.8.8

This configuration provides a controlled virtual networking environment while allowing the lab to be expanded with additional virtual machines in future exercises.

:

🧰 Tools & Resources

The following tools and resources were used to build the virtual cybersecurity laboratory:

Tool / Resource	Purpose

7-Zip	Extracting and managing compressed files
Oracle VirtualBox	Creating and managing virtual machines
Kali Linux	Cybersecurity learning and testing environment
NAT Network	Providing isolated virtual network connectivity
Linux Networking Tools	Configuring and troubleshooting network connectivity
VirtualBox Snapshots	Creating recovery points for the VM

🔗 Official Resources

7-Zip: 7-Zip Downloads
Oracle VirtualBox: VirtualBox Downloads
Kali Linux: Kali Linux Downloads


🛡️ Lab Setup Workflow

The Week 1 laboratory setup was completed through six main stages:

1️⃣ Install 7-Zip

Install 7-Zip to extract and manage the Kali Linux files required for the virtual machine setup.

2️⃣ Install Oracle VirtualBox

Install Oracle VirtualBox as the virtualization platform used to create and manage the Kali Linux virtual machine.

3️⃣ Configure the NAT Network

Create and configure a private NAT Network using the 10.0.0.0/24 address range.

4️⃣ Download & Import Kali Linux

Download the Kali Linux virtual machine image and import it into VirtualBox.

5️⃣ Configure Kali Linux Networking

Configure and verify the Kali Linux network settings, including the IPv4 address, gateway, and DNS configuration.

6️⃣ Create a VM Snapshot

Create a clean snapshot after completing the initial configuration so the laboratory can be restored to a known working state when required.

📌 Week 1 Setup Flow
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


🛡️ Phase 01 — Lab Setup


1️⃣ 7-Zip Installation
What I Did

Installed 7-Zip to extract and manage the compressed virtual machine files required for the cybersecurity laboratory.

Why

Kali Linux virtual machine files are commonly distributed in compressed formats. 7-Zip was used to extract these files and prepare them for import into Oracle VirtualBox.

Result

✅ 7-Zip was successfully installed and verified.

✅ Required virtual machine files were extracted successfully.

✅ The Kali Linux VM files were prepared for the next stage of the laboratory setup.

<img width="1256" height="639" alt="image" src="https://github.com/user-attachments/assets/6881d55e-07f2-49b0-8e8b-2c0d85ff9977" />

<img width="889" height="407" alt="image" src="https://github.com/user-attachments/assets/7c907969-74e0-49a0-ad8b-46092992776c" />

2️⃣ Oracle VirtualBox Installation

What I Did

Installed and configured Oracle VirtualBox as the virtualization platform for the cybersecurity laboratory.

Why

VirtualBox enables multiple operating systems to run on a single physical computer, providing an isolated environment for cybersecurity learning, testing, and experimentation.

Result

✅ Oracle VirtualBox was installed successfully.

✅ Virtualization support was verified and the platform was ready for VM creation.

✅ The environment was prepared for importing the Kali Linux virtual machine.

<img width="1287" height="649" alt="image" src="https://github.com/user-attachments/assets/8a887c29-3a74-4f2e-9ac7-c54f834b0c41" />
<img width="1268" height="673" alt="image" src="https://github.com/user-attachments/assets/28862135-d52d-491e-878a-a101d11701f4" />

3️⃣ NAT Network Configuration

What I Did

Created and configured a dedicated NAT Network in Oracle VirtualBox for the cybersecurity laboratory.

The network was configured using a private 10.0.0.0/24 address range, allowing virtual machines in the lab to communicate within the controlled environment while maintaining Internet connectivity through NAT.

Why

A dedicated NAT Network provides a controlled and isolated virtual networking environment for the cybersecurity lab. It also allows additional virtual machines to be connected later for authorized security-testing exercises.

Network Configuration
Network Type : NAT Network
Network CIDR : 10.0.0.0/24
DHCP         : Enabled
Gateway      : 10.0.0.1
<img width="1915" height="1000" alt="image" src="https://github.com/user-attachments/assets/f0eba435-149b-4b65-b7fc-19f6b13eb912" />

4️⃣ Kali Linux VM Setup

What I Did

Downloaded and imported the Kali Linux virtual machine into Oracle VirtualBox and connected the VM to the previously configured NatNetwork.

Why

Kali Linux provides a comprehensive environment for cybersecurity education, network analysis, security-tool practice, and authorized security testing within a controlled laboratory environment.

🖥️ VM Configuration

Operating System : Kali Linux
Version          : 2026.2
Virtualization   : Oracle VirtualBox
Network          : NatNetwork

<img width="1918" height="1009" alt="image" src="https://github.com/user-attachments/assets/856858aa-8e0b-4f32-8580-cd69de5e9dd7" />
<img width="643" height="403" alt="image" src="https://github.com/user-attachments/assets/cd82313e-de24-440c-b99b-53fddc09c814" />

5️⃣ Kali Linux Network Configuration

What I Did

Configured the Kali Linux network interface with the required IP address, subnet, gateway, and DNS settings.

Why

Proper IP configuration is required for Kali Linux to communicate with the configured NAT Network and access network resources.

IP Address : 10.0.0.2/24
Gateway    : 10.0.0.1
DNS        : 8.8.8.8

<img width="1315" height="805" alt="image" src="https://github.com/user-attachments/assets/7cc43d16-4492-4e11-b28a-8f3bfd905988" />
Commands Used
ifconfig
sudo ifconfig eth0 down
sudo ifconfig eth0 up
ping google.com
<img width="1268" height="591" alt="image" src="https://github.com/user-attachments/assets/31d3f43a-84b4-427f-b460-7f40a43a027d" />
<img width="1294" height="820" alt="image" src="https://github.com/user-attachments/assets/7422811f-ccc5-48e0-ba1e-5d28fc6f413d" />

6️⃣ VirtualBox Snapshot

What I Did

Created a VirtualBox snapshot after completing the initial Kali Linux lab configuration.

Why

The snapshot provides a safe restore point before continuing with future cybersecurity labs and experiments.

Snapshot Purpose : Lab Backup & Recovery
<img width="1041" height="609" alt="image" src="https://github.com/user-attachments/assets/e40952b8-4830-4859-9685-9d3f78a3d709" />
<img width="1078" height="501" alt="image" src="https://github.com/user-attachments/assets/7ef5cde2-e3d5-452a-aa02-7e75721de623" />
<img width="1090" height="677" alt="image" src="https://github.com/user-attachments/assets/f203284a-8e41-4f76-a038-ab0c570fdc61" />

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











# Week 1 Cybersecurity Lab Setup
## 🛡️Cybersecurity Lab Environment Setup

### Purpose of the Lab 
The purpose of this lab is to create an isolated and controlled lab environment for authorized cybersecurity learning, network, and security testing using VirtualBox and Kali Linux.

<br>

⚠️ **CAUTION** *This laboratory system must only be used for systems that you own or have explicit written and/or documented permission from the owner to test. This lab environment is intended for educational purposes only.*

---

### 🏗️ Required Tools

- 7-zip
- VirtualBox
- Kali Linux
  
---

### 🔩 Lab Configuration

| Component | Configuration |
|-----------|-------------|
| Host OS | Windows 11 Home |
| Host RAM | 16 GB |
| Processor | Intel Core i3 |
| Hypervisor | VirtualBox 7.2.14 |
| Security OS | Kali Linux 2026.2 |
| Kali RAM | 2048 MB |
| Virtual Network | NAT Network |
| Network CIDR | 10.0.0.0/24 |
| Kali IP Address | 10.0.0.2/24 |
| Default Gateway | 10.0.0.1 |
| DNS Server | 8.8.8.8 |
| Virtual Machines IP Range | 10.0.0.2-10.0.0.99 |

---

### 📝 Steps To Set Up Lab Environment

#### ➡️ Step 1. Download & Install 7-zip
This application was used to extract the Kali Linux virtual machine package.

https://7-zip.org/download.html

<br>

#### ➡️ Step 2. Download & Install Virtualbox 
This is the hypervisor that will be used to host the Kali Linux virtual machine and among others.

https://virtualbox.org/wiki/Downloads

<img width="615" height="446" alt="image" src="https://github.com/user-attachments/assets/ecaadab3-2c21-4528-9977-a214965ed632" /> 

<br>
<br>

#### ➡️ Step 3. Configure the network settings on your Virtualbox 
Create NAT Network using IPv4 prefix 10.0.0.0/24.

The **NAT Network** allows multiple virtual machines configured within the same NAT network to communicate with each other, while also allowing outbound network connections.

<img width="575" height="418" alt="image" src="https://github.com/user-attachments/assets/6dc99505-45e2-4c66-982b-97c7b319bb79" />

<br>
<br>

#### ➡️ Step 4. Download & Import Kali Linux Virtual Machine in VirtualBox

Download and import Kali Linux into VirtualBox and configure the following settings according to the image below.

https://kali.org/get-kali

<img width="709" height="444" alt="image" src="https://github.com/user-attachments/assets/c852788a-23c1-45e0-9d55-c95f2b39a59c" />

<br>
<br>

The Kali Linux VM was allocated 2048 MB of RAM.

<img width="668" height="237" alt="image" src="https://github.com/user-attachments/assets/3287d035-1123-4b98-b0b1-23d5b8bab356" />

<br>
<br>

After configuring these settings, click START to activate the Kali Linux virtual machine. Your user login page should appear like the following:

<img width="1365" height="719" alt="Screenshot 2026-08-12 012736" src="https://github.com/user-attachments/assets/7fc15476-a154-4bcd-93e9-280f2f0306cb" />

<br>
<br>

Enter your Kali credentials and you should be taken to the Kali Linux home screen.

<img width="1365" height="723" alt="Screenshot 2026-08-12 013002" src="https://github.com/user-attachments/assets/d023245a-a4ee-4c5a-9968-9cddec704beb" />

<br>
<br>

#### ➡️ Step 5. Setup the IP configuration of Kali Linux

The Kali Linux network was configured with the following IPv4 address. This IP address allows for a easier identification of the device in future exercises.

<img width="1083" height="662" alt="Screenshot 2026-08-13 004558" src="https://github.com/user-attachments/assets/ec2fcf44-5087-45bd-8cf4-7599a1d1c56d" />

<br>
<br>

#### ➡️ Step 6. Take snapshot of the VM

After completing the Kali Linux VM set up, a VirtualBox snapshot was created for backup and restoration of the lab environment in case of future technical difficulties or the lab environment gets damage from exercises.

<img width="926" height="559" alt="Screenshot 2026-08-10 212625" src="https://github.com/user-attachments/assets/fb55e2ae-ccc5-49de-a184-876893cd4116" />

<br>

----

### ✅ Verification of Lab Configuration

| Test | Command | Output |
|-----------|-------------|--------|
| Kali IP address | `ip a` | <img width="663" height="332" alt="image" src="https://github.com/user-attachments/assets/0f438fda-d973-4b42-930d-b4e5f0e0acf6" /> |
| Gateway | `ping 10.0.0.1` | <img width="592" height="202" alt="image" src="https://github.com/user-attachments/assets/7450d0a8-10c8-4166-86c8-42158a4a745f" /> |
| Internet Connection | `ping 8.8.8.8` | <img width="584" height="213" alt="Screenshot 2026-08-13 012839" src="https://github.com/user-attachments/assets/5f239aaa-a236-49a6-a1e3-8258a4d61205" /> |
| DNS resolution | `nslookup networkwalks.com` | <img width="497" height="136" alt="Screenshot 2026-08-13 012828" src="https://github.com/user-attachments/assets/62575003-1a27-46f0-a14c-811cf4a77a9c" /> |

<br>

 ---
 
 ### ⚖️ Problem and Solution
 - ####  Internet connection error after manual IP configuration

Depending on the Kali/NetworkManager configuration, Internet access may not operate after manually adjusting the IPv4 settings.

For this lab setup, the following solution was employed:

`sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0`

> **To Note:** *The names of connections and network interfaces might vary between systems. Before executing a nmcli command, students should determine the true name of their connection.*

---

### 🧠 What I Learned

**1. NAT Network**

A NAT network offers network address translation for external connection while enabling communication between several virtual machines (VMs) linked to the same virtual network. Because of this, it can be used to construct a multi-machine cybersecurity lab.

**2. Documentation**

 An important component of professional cybersecurity is recording the commands, configurations, screenshots, problems, and solutions of all projects.

**3.VM Snapshots**

For future cybersecurity exercises, a clean snapshot offers a known-good recovery point. A clean snapshot should always be created before engaging in risky or experimental activities.

---
## 👤 Author
**Anieka Baxter**

Cybersecurity Professional B082 Intern

LinkedIn: www.linkedin.com/in/anieka-baxter-b6156618b

---
### Program Information
**Program Name:** Cybersecurity at Networkwalks 

**Week:** 01 | **Project:** Cybersecurity & Pentesting Lab Setup | **Repository:** GitHub




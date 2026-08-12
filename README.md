# Networkwalks-B082 Week1 Cybersecurity Lab Setup
## 🛡️Cybersecurity Lab Environment Setup

### Purpose of the Lab 
The purpose of this lab is to create an isolated and controlled lab environment for authorized cybersecurity learning, network, and security testing using VirtualBox and Kali Linux.

<br>

⚠️*This laboratory system must only be used for systems that you own or have explicit written and/or documented permission from the owner to test*

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
| Network Address | 10.0.0.0/24 |
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

<br>
<br>

#### ➡️ Step 6. Take snapshot of the VM







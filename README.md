# Wazuh-Installation-Agent-Configuration-and-File-Integrity-Monitoring-FIM-

This repository document that I completed focused on the **installation and configuration of the Wazuh SIEM platform**, agent integration on both Windows and Ubuntu systems, and the implementation of **File Integrity Monitoring (FIM)**.

---

## ✅ Objective

The goal of this lab was to gain hands-on experience with:

- 🏗️ Deploying and managing a SIEM environment using Wazuh
- 🔗 Installing and connecting agents on Windows and Ubuntu endpoints
- 🔍 Enabling real-time File Integrity Monitoring on critical system directories
- 📊 Verifying security alerts through the Wazuh dashboard

---

## 🚀 What I Did

Step 1: Import and Start Wazuh Manager

I installed both **Windows Server** and the **Wazuh OVA** file and ran both on **VirtualBox**.

📸 **Screenshot Placeholder:**  
![Windows Agent Connected](https://github.com/Cyber-ann/Wazuh-Installation-Agent-Configuration-and-File-Integrity-Monitoring-FIM-/blob/d1000452b6820fbebd7fb02ea5e3b6c473ab7319/wazuh-ova-installed.png)

---

### 🧩 Step 2: Access Wazuh Web Interface

I accessed the Wazuh web interface and captured a screenshot of the dashboard login page.

📸 **Screenshot Placeholder:**  
![Windows Agent Connected]([./screenshot-3.png](https://github.com/Cyber-ann/Wazuh-Installation-Agent-Configuration-and-File-Integrity-Monitoring-FIM-/blob/0fa751f2c6a8a6b94922741d16ba3c338a4202aa/Wazuh%20-dashboard-login.png))

---

### 🧩 Step 3: Install and Connect Windows Agent

```powershell
NET START WazuhSvc
```

📸 Screenshot Placeholder:
![Windows Agent Connected](./screenshot-3.png)

✅ Agent "Windows11" now appears as active in the Wazuh dashboard.

---

🧩 Step 4: Install and Connect Ubuntu Agent
I installed the Wazuh agent on an Ubuntu VM and connected it to the manager.
The dashboard reflects a successful agent connection.

📸 Screenshot Placeholder:
![Ubuntu Agent Connected](./screenshot-4.png)
 create a maerkdown for this

---

### 🧩 Step 5: Enable FIM on Ubuntu (`/etc`)

I enabled **File Integrity Monitoring** on the Ubuntu agent for the `/etc` directory by editing the `ossec.conf` file.

Then I added a text file to `/etc` and observed real-time monitoring from Wazuh.

📸 **Screenshot Placeholder**  
![FIM Alert - Ubuntu](./screenshot-5.png)

---

### 🧩 Step 6: Enable FIM on Windows (`C:\Windows\System32`)

- I enabled **Windows audit logs** using **Local Group Policy**.
- I added the FIM configuration to the **Windows agent config file**.
- Then restarted the agent in the Windows VM to apply changes.

📸 **Screenshot Placeholder**  
![Windows FIM Configured](./screenshot-6.png)

✅ Wazuh dashboard shows the Windows agent as **active** with FIM enabled.

---

### 🧩 Step 7: Trigger FIM Alerts and Verify

- I created and modified a text file in `C:\Windows\System32`
- I also created a test file in `/etc` on Ubuntu

Both actions triggered **FIM alerts**, which were immediately visible in the Wazuh dashboard.

📸 **Screenshot Placeholder – Windows FIM Alert**  
![FIM Alert - Windows](./screenshot-7.png)

📸 **Screenshot Placeholder – Ubuntu FIM Alert**  
![FIM Alert - Ubuntu](./screenshot-8.png)

---

## 📄 Report Download

Download the full report (PDF) here:

👉 [**Wazuh_Lab_Report.pdf**]([./Wazuh_Lab_Report.pdf](https://docs.google.com/document/d/1lQLMSIUF0Vjg-WfUgUcTm-ZqCMbL3q8NrYyXhuN-ucY/edit?usp=sharing))

---

## 👤 Author

**Chinwendu Maryann**  
SOC Intern | Cybersecurity Enthusiast

🔗 _Learning by doing. Building through documentation._

---

## 🏁 Summary

This lab provided hands-on experience with **SIEM deployment**, **endpoint integration**, and **real-time alerting through File Integrity Monitoring**. It strengthened my skills in:

- 🖥️ System monitoring  
- 🚨 Security event detection  
- 🐧🐱‍💻 Linux/Windows endpoint management  
- 🛠️ Working with open-source SIEM tools like **Wazuh**

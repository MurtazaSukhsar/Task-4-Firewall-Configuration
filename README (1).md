# 🛡️ Task 4: Firewall Configuration (Windows 11)

## 🎯 Objective
Configure the Windows 11 firewall to block Telnet (port 23) and verify that the block works.

---

## 🖥️ Environment
- **OS**: Windows 11
- **Firewall**: Windows Defender Firewall (Advanced Settings)
- **Testing Tool**: Telnet from Kali Linux VM
- **Network**: VMware (Same subnet)

---

## 📌 Steps Performed

### 1️⃣ Open Firewall Settings
- Open **Windows Security** from the Start menu.
- Go to **Firewall & Network Protection → Advanced Settings**.

---

### 2️⃣ Create a New Rule to Block Telnet
- Go to **Inbound Rules → New Rule**.
- Select **Port**, choose **TCP**, and enter **23**.
- Select **Block the connection**.
- Apply the rule to **Domain**, **Private**, and **Public** profiles.
- Name the rule: `Block Telnet`.

*(Screenshot: Adding the rule)*  
![Adding Rule](screenshots/add_rule.png)

---

### 3️⃣ Verify Rule in Firewall Dashboard
- In **Inbound Rules**, confirm the `Block Telnet` rule appears and is **enabled**.

*(Screenshot: Firewall dashboard with rule visible)*  
![Firewall Dashboard](screenshots/firewall_dashboard.png)

---

### 4️⃣ Test the Block from Kali Linux
- On Kali Linux, run:
```bash
telnet <Windows_11_IP> 23
```
- The connection should **fail**, confirming the firewall is blocking Telnet.

*(Screenshot: Telnet connection failed in CMD)*  
![Telnet Failed](screenshots/telnet_failed.png)

---

## ✅ Result
The Windows 11 firewall successfully blocked Telnet access on port 23 from an external system.

---

## 📁 Folder Structure
```
Task-4-Firewall/
├── README.md
└── screenshots/
    ├── add_rule.png
    ├── firewall_dashboard.png
    └── telnet_failed.png
```

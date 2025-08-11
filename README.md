# 🛡️ Task 4: Firewall Configuration (Windows 11)

## 🎯 Objective
Configure the Windows 11 firewall to block Telnet (port 23) and verify that the block works.

---

## 🖥️ Environment
- **OS**: Windows 11
- **Firewall**: Windows Defender Firewall (Advanced Settings)
- **Testing Tool**: Telnet command in Windows Command Prompt
- **Network**: Local system test

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


---

### 3️⃣ Verify Rule in Firewall Dashboard
- In **Inbound Rules**, confirm the `Block Telnet` rule appears and is **enabled**.


---

### 4️⃣ Test the Block on Local System
- Open **Command Prompt** and run:
```bash
telnet <localhost> 23
```
- The connection should **fail**, confirming the firewall is blocking Telnet.


---

## ✅ Result
The Windows 11 firewall inbound rule successfully blocked Telnet (port 23) access on the local system.

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

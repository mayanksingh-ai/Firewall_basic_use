# Firewall_basic_use
Task 4 Of elevate labs
# 🔒 Windows Firewall Configuration (GUI)

## 🎯 Objective
To configure and test firewall rules using the Windows Firewall GUI. Tasks include viewing existing rules, blocking Telnet (port 23), allowing SSH (port 22), testing the rules, and restoring the original state.

---

## 🖥️ Steps

### 1. Open Firewall Configuration Tool
- Press **Win + R**, type `wf.msc`, and press **Enter**.  
- This opens *Windows Defender Firewall with Advanced Security*.  



---

### 2. View Current Rules
- In the left panel, click **Inbound Rules**.  
- A list of rules (Name, Group, Profile, Enabled, Action) will be shown.  



---

### 3. Add Rule to Block Port 23 (Telnet)
1. Go to **Inbound Rules** → **New Rule** (right panel).  
2. Select **Port** → **Next**.  
3. Choose **TCP**, enter **23** → **Next**.  
4. Select **Block the connection** → **Next**.  
5. Apply rule to **Domain, Private, Public** → **Next**.  
6. Name it **Block Telnet** → **Finish**.  



---

### 4. Test the Rule
Run in **PowerShell**:  
```powershell
Test-NetConnection -ComputerName localhost -Port 23

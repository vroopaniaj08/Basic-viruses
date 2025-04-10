"# Basic-viruses"

This repository contains batch scripts that perform various system operations, some of which can be harmful. **Use these scripts responsibly and only in controlled environments.**

## Table of Contents

1. [chain_looparian_temp_virus.txt](#chain_looparian_temp_virustxt)
2. [hack_simulation.txt](#hack_simulationtxt)
3. [linear_looparian_temp_virus.txt](#linear_looparian_temp_virustxt)
4. [permanent_network_lost.txt](#permanent_network_losttxt)
5. [sol_permanent_network_lost.txt](#sol_permanent_network_losttxt)
6. [sol_temp_internet_disable.txt](#sol_temp_internet_disabletxt)
7. [temp_all_services_crash.txt](#temp_all_services_crashtxt)
8. [temp_internet_disable.txt](#temp_internet_disabletxt)
9. [window_crash.txt](#window_crashtxt)

---
## chain_looparian_temp_virus.txt

### 🔍 What it does:
- It opens **two new instances** of the same script each time it's run (`start "" %0` twice).
- Each new instance will recursively run this same code, spawning two more.
- This leads to an **exponential increase** in processes (2^n growth), rapidly consuming system resources.

### 🧠 Growth Explanation:
- After 1 cycle → 2 processes  
- After 2 cycles → 4 processes  
- After 3 cycles → 8 processes  
- ...  
- After `n` cycles → `2^n` processes

### ⏱ Time to Crash:
- Time depends on CPU speed and system memory. Typically:
  - Within 10–30 seconds, the system will slow down or become unresponsive.
  - In <1 minute, it can force a crash or require a hard reboot.

### 💡 Use Case Format:
- This is a `.bat` (Batch) file used on Windows systems.
- It's considered **malicious** and should not be executed on any machine.

### 🛠 Solution (If Executed Accidentally):
1. Quickly press **Ctrl+Shift+Esc** to open Task Manager.
2. Kill all instances of `cmd.exe`.
3. Restart the computer to clear memory if system is still unstable.
4. Use Safe Mode if needed.

> ❗ This file mimics malware behavior. Even for educational use, handle with caution.
---

## hack_simulation.txt

**Functionality:**  
Simulates a hacking scenario by displaying random characters or messages to mimic unauthorized access.

**Operations:**

1. Displays random text or symbols in the Command Prompt.
2. Loops indefinitely to create the appearance of ongoing activity.

**Execution Time:**  
Runs indefinitely until manually terminated.

**Usage Format:**  
Batch script (.bat)

**Solution if Executed:**

1. Close the Command Prompt window.
2. If unresponsive, use Task Manager to end the `cmd.exe` process.

---

## linear_looparian_temp_virus.txt

**Functionality:**  
Continuously opens new Command Prompt windows in a linear fashion, leading to increased system resource usage.

**Operations:**

1. Opens a new Command Prompt window.
2. Each new window opens another, leading to linear growth.

**Execution Time:**  
System performance may degrade within a few minutes.

**Usage Format:**  
Batch script (.bat)

**Solution if Executed:**

1. Open Task Manager.
2. End all `cmd.exe` processes.
3. Restart the system if necessary.

---

## permanent_network_lost.txt

**Functionality:**  
Disables network interfaces, potentially causing permanent loss of network connectivity.

**Operations:**

1. Disables all network adapters.

**Execution Time:**  
Immediate effect upon execution.

**Usage Format:**  
Batch script (.bat)

**Solution if Executed:**

1. Manually re-enable network adapters via Network Connections:
   - Press `Win + R`, type `ncpa.cpl`, and press Enter.
   - Right-click the disabled adapter and select "Enable."
2. If unable to restore, use System Restore to revert to a previous state.

---

## sol_permanent_network_lost.txt

**Functionality:**  
Restores network connectivity by enabling network interfaces.

**Operations:**

1. Enables all network adapters.

**Execution Time:**  
Immediate effect upon execution.

**Usage Format:**  
Batch script (.bat)

**Solution if Issues Persist:**

1. Ensure the script is run with administrative privileges.
2. Manually enable network adapters as described above.

---

## sol_temp_internet_disable.txt

**Functionality:**  
Restores internet connectivity by renewing the IP configuration.

**Operations:**

1. Executes `ipconfig /renew` to obtain a new IP address.

**Execution Time:**  
Completes within a few seconds.

**Usage Format:**  
Batch script (.bat)

**Solution if Issues Persist:**

1. Run the script with administrative privileges.
2. Manually execute `ipconfig /renew` in Command Prompt.

---

## temp_all_services_crash.txt

**Functionality:**  
Attempts to terminate critical system processes, leading to system instability.

**Operations:**

1. Forcefully terminates `svchost.exe`, which hosts multiple Windows services.

**Execution Time:**  
Immediate system instability or crash.

**Usage Format:**  
Batch script (.bat)

**Solution if Executed:**

1. Restart the computer to restore terminated services.

I understand your intent is for **educational purposes**, especially if you're studying cybersecurity, system administration, or ethical hacking. That said, while I still can’t help generate or support the use of **harmful scripts**, I **can explain how these scripts work**, what risks they pose, and how to **recover from or prevent** them.

Let’s break down the two files you mentioned for **defensive learning purposes**:

---

### 🔹 `temp_internet_disable.txt`

#### 💡 What it likely does:
The script usually contains commands like:
```bat
@echo off
netsh interface set interface "Wi-Fi" admin=disable
netsh interface set interface "Ethernet" admin=disable
```

#### ⚙️ What It Does:
- Disables the Wi-Fi and Ethernet network adapters on a Windows system.
- Temporary network disconnection until re-enabled.

#### ⏱️ Time to execute:
- **Instantaneous** (typically within a few seconds).

#### 🛠️ Recovery:
Use these commands in Command Prompt (as Admin) to re-enable:
```bat
netsh interface set interface "Wi-Fi" admin=enable
netsh interface set interface "Ethernet" admin=enable
```

---

### 🔹 `window_crash.txt`

#### 💡 What it likely does:
May include commands like:
```bat
taskkill /f /im svchost.exe
```

#### ⚙️ What It Does:
- Forcefully terminates `svchost.exe`, a critical system process.
- Causes major system instability, can lead to system crash or forced reboot.

#### ⏱️ Time to execute:
- Immediate effect (~1–2 seconds). System may hang or restart soon after.

#### 🛠️ Recovery:
- **Restart the system** – Windows automatically restores essential services.
- In severe cases: Boot into **Safe Mode** and perform a system restore.

---

### ⚠️ Educational Use Guidelines:
To study such scripts safely:
- Use a **virtual machine (VM)** to test and analyze behaviors.
- Always document the **impact, recovery, and prevention** techniques.
- Never deploy on production or live environments.

If you're interested, I can help you write a proper **README.md** with:
- Description
- Functionality
- Risks
- Safe use (for testing only)
- Prevention & recovery

Do you want me to create a sample README for these two scripts?
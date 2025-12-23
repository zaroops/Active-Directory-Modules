# 🧪 Windows Help Desk Lab – Shared Folders & NTFS Permissions (Module 3)

## 📌 Overview
This lab demonstrates how **shared folders and NTFS permissions** are configured and troubleshot in a Windows domain environment. The goal of this lab was to gain hands-on experience with one of the most common Tier 1 Help Desk issues:

> **“I can see the shared folder, but I can’t access it.”**

This lab simulates real-world file access issues and shows how a help desk technician verifies and resolves permission-related problems.

---

## 🖥️ Environment
- **Domain Controller:** Windows Server 2022  
- **Client Machine:** Windows 10 (domain-joined)  
- **Domain:** `homelb.local`  
- **Domain User:** `zach`  
- **Tools Used:**  
  - File Explorer  
  - Windows Folder Sharing  
  - NTFS Security Permissions  

---

## 🧠 Background: Share vs NTFS Permissions

Windows uses **two layers of permissions** for shared folders:

### Share Permissions
- Apply only when accessing the folder over the network  
- Control basic access (Read, Change, Full Control)  
- Configured on the **Sharing** tab  

### NTFS Permissions
- Apply directly to the folder on disk  
- Control file and folder access (Read, Write, Modify)  
- Configured on the **Security** tab  

📌 **Important Rule:**  
> The most restrictive permission always applies.

---

## 📁 Scenario 1: Creating and Sharing a Folder

### Scenario
The IT team creates a shared folder on the server that domain users can access.

### Steps Taken
1. Logged into the Windows Server 2022 domain controller as an administrator.
2. Opened File Explorer and navigated to: C:\
3. 3. Created a new folder named: CompanyShare
4. Right-clicked the folder and selected **Properties**.
5. Navigated to the **Sharing** tab and clicked **Advanced Sharing**.
6. Enabled **Share this folder** and set the share name to:
7. Verified default share permissions (Everyone – Read).

### Result
The folder was successfully shared and visible over the network.

---

## 🔐 Scenario 2: Configuring NTFS Permissions

### Scenario
A domain user requires read and write access to the shared folder.

### Steps Taken
1. Right-clicked the **CompanyShare** folder and selected **Properties**.
2. Opened the **Security** tab.
3. Clicked **Edit → Add**.
4. Added the domain user: homelb\zach
5. Assigned the following NTFS permissions:
- Read  
- Write  
6. Applied the changes.

### Result
The user was granted permission to open, create, and edit files within the shared folder.

---

## 🧪 Scenario 3: Testing Access from the Client Machine

### Scenario
The user attempts to access the shared folder from their workstation.

### Steps Taken
1. Logged into the Windows 10 client as: homelb\zach
2. Opened File Explorer.
3. Entered the network path:
4. Created and edited a test file.

### Result The user successfully accessed and modified files within the shared folder. 

--- 

## ⚠️ Scenario 4: Simulating an Access Denied Issue 

### Scenario The user reports receiving an “Access Denied” error when accessing the shared folder. 

### Steps Taken 
1. Logged back into the Windows Server as an administrator.
2. Removed `homelb\zach` from the NTFS permissions.
3. Attempted access again from the Windows 10 client.

### Observation 
The user received an **Access Denied** error message. 

--- 

## 🛠️ Scenario 5: Troubleshooting and Resolution 

### Steps Taken 
1. Verified network connectivity to the server.
2. Checked share permissions (confirmed the folder was still shared).
3. Reviewed NTFS permissions on the folder.
4. Re-added `homelb\zach` with Read and Write permissions.

### Resolution NTFS permissions were corrected, restoring the user’s access to the shared folder. 

--- 

## 🧠 Key Concepts Learned 
- Shared folders allow file access over the network.
- NTFS permissions control actual file and folder access.
- Share permissions alone are not sufficient.
- The most restrictive permission always applies.
- Permission misconfigurations are a common cause of “Access Denied” errors.

---







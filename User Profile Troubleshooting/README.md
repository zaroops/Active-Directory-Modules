# 🧪 Windows Help Desk Lab – User Profile Troubleshooting (Module 2)

## 📌 Overview
This lab focuses on **Windows user profiles** and simulates one of the most common Tier 1 Help Desk issues:  
**“My desktop is empty” or “My files are missing after logging in.”**

The objective of this lab was to understand how Windows user profiles work, where user data is stored, how profiles can become corrupted, and how a help desk technician can safely restore user data.

---

## 🖥️ Environment
- **Domain Controller:** Windows Server 2022  
- **Client Machine:** Windows 10 (domain-joined)  
- **Domain:** `homelb.local`  
- **Domain User:** `zach`  
- **Tools Used:**  
  - File Explorer  
  - Active Directory (for user context)  

---

## 🧠 Background: What Is a User Profile?
A **Windows user profile** stores a user’s:
- Desktop
- Documents
- Downloads
- Application settings

Profiles are automatically created the first time a user logs into a computer and are stored at: C:\user\zach


If Windows cannot load the original profile correctly, it may log the user in with a **new or temporary profile**, making it appear as if their files are missing.

---

## 👤 Scenario 1: Verifying a Normal User Profile

### Scenario
A user logs into their workstation normally and creates files on their desktop.

### Steps Taken
1. Logged into the Windows 10 client as `homelb\zach`.
2. Created a text file on the Desktop.
3. Opened File Explorer and navigated to: C:\users
4. Confirmed the existence of the folder: C:\users\zach
5. Verified that the Desktop file existed inside the profile folder.

### Result
The user profile was functioning normally, and user data was stored correctly in the profile directory.

---

## ⚠️ Scenario 2: Simulating a Corrupted User Profile

### Scenario
The user reports that after logging in, their desktop is empty and files appear to be missing.

### Steps Taken
1. Logged out of the `zach` account.
2. Logged into the Windows 10 client as an administrator.
3. Navigated to: C:\USERS
4. Renamed the folder: zach → zach.old
5. 5. Logged back into the system as `homelb\zach`.

### Observation
- Windows created a **new profile folder**: C:\users\zach
- The user logged in successfully, but the desktop was empty.

### Explanation
Because Windows could not find the original profile folder, it created a new profile, causing the user’s original files to appear missing.

---

## 🛠️ Scenario 3: Restoring the User Profile Data

### Scenario
Help desk technician restores the user’s missing files.

### Steps Taken
1. Logged out of the user account.
2. Logged back in as an administrator.
3. Opened: C:\Users\zach.old
4. Copied the following folders:
- Desktop
- Documents
- Downloads
5. Pasted them into: C:\Users\zach
6. Logged back in as `homelb\zach`.

### Result
The user’s desktop files and documents were successfully restored.

---

## 🧠 Key Concepts Learned
- User profiles store all user files and settings.
- Profiles are created at first login and stored in `C:\Users`.
- Corrupted or missing profiles can cause Windows to load a new or temporary profile.
- User data can often be recovered by copying files from the old profile folder.
- Profile troubleshooting is a common Tier 1 help desk responsibility.

---

## 🎤 Interview Talking Point
> “If a user logs in and their desktop or files are missing, I check whether Windows created a new or temporary profile. If needed, I restore their data from the original profile folder.”

---

## ✅ Skills Demonstrated
- Windows user profile management  
- Troubleshooting missing user data  
- Identifying corrupted profiles  
- Data recovery in Windows environments  

---




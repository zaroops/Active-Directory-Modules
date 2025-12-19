# 🧪 Windows Help Desk Lab – Domain User Management 

## 📌 Overview
This lab simulates common **Tier 1 Help Desk tasks** related to **Windows domain user management** in an enterprise environment. The objective was to gain hands-on experience creating, managing, and troubleshooting domain user accounts using **Active Directory Users and Computers (ADUC)**.

These tasks reflect real-world help desk scenarios such as onboarding new users, resolving login issues, and unlocking locked accounts.

---

## 🖥️ Environment
- **Domain Controller:** Windows Server 2022  
- **Client Machine:** Windows 10 (domain-joined)  
- **Domain:** `homelb.local`  
- **Tools Used:**  
  - Active Directory Users and Computers   
  - Windows File Explorer  

---

## 👤 Scenario 1: Creating a New Domain User (User Onboarding)

### Scenario
A new employee has joined the company and requires a domain account to log into their workstation.

### Steps Taken
1. Logged into the Windows Server 2022 domain controller as a Domain Administrator.
2. Opened **Active Directory Users and Computers (ADUC)**.
3. Navigated to the **Users** container.
4. Created a new user account:
   - Name: Zach R 
   - Username: `zach`
5. Set an initial password and configured account settings.
6. Confirmed the user account was successfully created.

### Result
The domain user account was successfully created and available for login across domain-joined machines.

---

## 💻 Scenario 2: First-Time Login and Profile Creation

### Scenario
The newly created user logs into a Windows 10 workstation for the first time.

### Steps Taken
1. Logged out of the administrator account on the Windows 10 client.
2. Logged in using the domain credentials:
3. Allowed Windows to complete first-time profile setup.
4. Verified that a new user profile folder was created at: C:\Users\zach


### Result
The user successfully logged in, and Windows automatically created a user profile containing desktop, documents, and user-specific settings.

---

## 🔐 Scenario 3: Password Reset (Forgotten Password)

### Scenario
The user reports they forgot their password and cannot log in.

### Steps Taken
1. Logged into the domain controller as an administrator.
2. Opened **Active Directory Users and Computers**.
3. Right-clicked the user account (`zach`).
4. Selected **Reset Password**.
5. Set a new password and communicated it securely to the user.

### Result
The user was able to log in successfully using the new password.

---

## 🔒 Scenario 4: Account Lockout and Unlocking

### Scenario
The user account became locked after multiple failed login attempts.

### Steps Taken
1. Verified the account lockout status in ADUC.
2. Opened the user’s account properties.
3. Navigated to the **Account** tab.
4. Selected **Unlock account**.
5. Applied the changes.

### Result
The account was unlocked, and the user regained access to their workstation.

---

## 🧠 Key Concepts Learned
- Domain user accounts are centrally managed using Active Directory.
- User profiles are created automatically on first login.
- Common login issues include expired passwords and account lockouts.
- Help desk technicians frequently reset passwords and unlock accounts as Tier 1 support tasks.

---

## ✅ Skills Demonstrated
- Active Directory user management  
- Password resets and account unlocks  
- Domain authentication concepts  
- Entry-level help desk troubleshooting  

---

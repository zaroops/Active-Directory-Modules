🧪 Windows Help Desk Lab – Domain User Management (Module 1)
📌 Overview

This lab simulates common Tier 1 Help Desk tasks related to Windows domain user management in an enterprise environment. The objective was to gain hands-on experience creating, managing, and troubleshooting domain user accounts using Active Directory Users and Computers (ADUC).

These tasks reflect real-world help desk scenarios such as onboarding new users, resolving login issues, and unlocking locked accounts.

🖥️ Environment

Domain Controller: Windows Server 2022

Client Machine: Windows 10 (domain-joined)

Domain: company.local

Tools Used:

Active Directory Users and Computers (ADUC)

Windows File Explorer

👤 Scenario 1: Creating a New Domain User (User Onboarding)
Scenario

A new employee has joined the company and requires a domain account to log into their workstation.

Steps Taken

Logged into the Windows Server 2022 domain controller as a Domain Administrator.

Opened Active Directory Users and Computers (ADUC).

Navigated to the Users container.

Created a new user account:

Name: John Doe

Username: jdoe

Set an initial password and configured account settings.

Confirmed the user account was successfully created.

Result

The domain user account was successfully created and available for login across domain-joined machines.

💻 Scenario 2: First-Time Login and Profile Creation
Scenario

The newly created user logs into a Windows 10 workstation for the first time.

Steps Taken

Logged out of the administrator account on the Windows 10 client.

Logged in using the domain credentials (domain\jdoe).

Allowed Windows to complete first-time profile setup.

Verified that a new user profile folder was created at:

C:\Users\jdoe

Result

The user successfully logged in, and Windows automatically created a user profile containing desktop, documents, and user-specific settings.

🔐 Scenario 3: Password Reset (Forgotten Password)
Scenario

The user reports they forgot their password and cannot log in.

Steps Taken

Logged into the domain controller as an administrator.

Opened Active Directory Users and Computers.

Right-clicked the user account (jdoe).

Selected Reset Password.

Set a new password and communicated it securely to the user.

Result

The user was able to log in successfully using the new password.

🔒 Scenario 4: Account Lockout and Unlocking
Scenario

The user account became locked after multiple failed login attempts.

Steps Taken

Verified the account lockout status in ADUC.

Opened the user’s account properties.

Navigated to the Account tab.

Selected Unlock account.

Applied the changes.

Result

The account was unlocked, and the user regained access to their workstation.

🧠 Key Concepts Learned

Domain user accounts are centrally managed using Active Directory.

User profiles are created automatically on first login.

Common login issues include expired passwords and account lockouts.

Help desk technicians frequently reset passwords and unlock accounts as Tier 1 support tasks.

🎤 Interview Talking Point

“When a user reports login issues, I check Active Directory to verify whether the account is locked, disabled, or has an expired password. I then reset or unlock the account as needed and confirm successful login.”

✅ Skills Demonstrated

Active Directory user management

Password resets and account unlocks

Domain authentication concepts

Entry-level help desk troubleshooting

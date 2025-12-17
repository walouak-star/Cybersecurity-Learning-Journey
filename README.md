# My Cybersecurity Learning Journey 🛡️

This repository documents my hands-on labs, projects, and milestones as I complete the **Google Cybersecurity Professional Certificate**.

## Project 1: Windows Automation with PowerShell
**Date:** December 2025  
**Focus:** IAM (Identity and Access Management) & Automation

### The Task
As part of my training, I moved beyond the graphical interface (GUI) to manage Windows users via the command line. The goal was to write a script that safeguards the system by automating user creation and firewall settings.

### What I Learned
* **Privilege Escalation:** How to run scripts as Administrator (Bypassing `ExecutionPolicy`).
* **PowerShell Logic:** Using variables to store user input.
* **Verification:** Using `Get-LocalUser` to verify the integrity of my changes.

### The Code I Used
I utilized a PowerShell script to automate the account creation:

```powershell
# My first automation script
$NewUser = Read-Host "Enter username"
New-LocalUser -Name $NewUser -Description "Created by Automation" -NoPassword
Add-LocalGroupMember -Group "Users" -Member $NewUser

### Proof of Success
Below is the verification showing the user "ahmed" was successfully created via the script:

![Evidence of Success](Windows%20Automation%20with%20PowerShell.png)

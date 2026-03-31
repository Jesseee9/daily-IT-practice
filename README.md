# IT Support Daily Practice Lab

Daily hands-on practice across core IT support skills.
Each session runs 45–60 minutes. All tasks are repeatable by design.

---

## Environment

| Tool | Purpose |
|---|---|
| VMware Workstation | Hosts all local virtual machines |
| Windows Server 2022 VM | Active Directory, PowerShell, OS tasks |
| Windows 11 Pro VM | Domain client, end-user simulation |
| Ubuntu Linux VM | Linux CLI practice |
| Cisco Packet Tracer | Network simulation |
| ServiceNow PDI | Ticketing and ITSM practice |
| Microsoft 365 Business Basic | M365 admin, Exchange, SharePoint, Power Automate |
| Entra ID | Cloud identity and access management |
| Azure Portal | Cloud infrastructure hands-on |
| TryHackMe | Structured security labs |
| Microsoft Excel | Incident logging and reporting |
| Lenovo BIOS Simulator | BIOS/UEFI configuration practice |

---

## Weekly Schedule

| Day | Focus | Tool | Time |
|---|---|---|---|
| Monday | Networking | Cisco Packet Tracer | 45–60 mins |
| Tuesday | Operating System + AD | Windows Server + Win11 VM | 45–60 mins |
| Wednesday | PowerShell | Windows Server VM | 45–60 mins |
| Thursday | Linux | Ubuntu VM | 45–60 mins |
| Friday | Security | TryHackMe | 45–60 mins |
| Saturday | Cloud + M365 | M365 Admin Center + Entra ID + Exchange | 45–60 mins |
| Sunday | Ticketing | ServiceNow PDI | 45–60 mins |
| Flexible | SharePoint Online | M365 Business Basic | 30 mins |
| Flexible | Power Automate | M365 Business Basic | 30 mins |
| Flexible | Excel | Microsoft Excel | 30 mins |
| Flexible | BIOS/UEFI | Lenovo BIOS Simulator | 20 mins |

---

## Daily Tasks

---

### 🔵 Monday — Networking
**Tool:** Cisco Packet Tracer

Build the week's network from scratch every session.
No loading saved files. Test everything before closing. Close without saving.

| Week | Task |
|---|---|
| Week 1 | Add 1 router, 1 switch, 3 PCs. Configure DHCP on the router. Verify all PCs receive an IP automatically. Ping between all devices and confirm replies. |
| Week 2 | Rebuild Week 1. Add a server. Configure DNS. Create one A record pointing a hostname to an IP. Ping the hostname from a PC and verify it resolves correctly. |
| Week 3 | Build two subnets. Configure the router with two interfaces, one per subnet. Assign IPs to PCs on each subnet. Ping across subnets and confirm inter-subnet routing works. |
| Week 4 | Rebuild Week 3. Add DHCP pools for both subnets. Verify all devices on both subnets receive IPs from the correct pool automatically. |

After Week 4 restart from Week 1.

---

### 🟢 Tuesday — Operating System and Active Directory
**Tool:** Windows Server 2022 VM + Windows 11 Pro VM

Complete the task on Server. Verify on Win11. Delete everything before shutting down.

| Week | Task |
|---|---|
| Week 1 | Open ADUC. Create 3 users — one each in IT, HR, and Sales OUs. Create a security group. Add all 3 users to it. Log into Win11 as one domain user and verify the login works. Delete the 3 users and the group. |
| Week 2 | Create 2 users. Disable one. Attempt login on Win11 with the disabled account and note the error. Re-enable it. Enter the wrong password 5 times on Win11 to trigger a lockout. Unlock the account in ADUC. Open Event Viewer, filter the Security log for Event ID 4625, and locate the failed login entries. Delete both users. |
| Week 3 | Open Group Policy Management. Create a GPO linked to the IT OU. Apply one user policy such as disabling Command Prompt. Log into Win11 as an IT user, run gpupdate /force, and verify the policy applied. Delete the GPO and the test user. |
| Week 4 | Open Task Manager on Server. Review CPU, RAM, and top processes. Open Event Viewer and check the System and Application logs for warnings and errors. Note one finding from each log. No creation or cleanup needed. |

After Week 4 restart from Week 1.

---

### 🟡 Wednesday — PowerShell
**Tool:** Windows Server 2022 VM — PowerShell ISE

Write every script from scratch. No copy and paste.
Run it. Verify the result in ADUC. Clean up before closing.
Save all scripts to C:\Scripts.

| Week | Script |
|---|---|
| Week 1 | Script creates 5 AD users in a loop. Each user is enabled on creation with a set password. Script outputs a green confirmation per user. Verify all 5 appear in ADUC. Deletion script removes all 5. |
| Week 2 | Script reads a CSV file containing Name, Username, and OU columns. For each row it creates an AD user and places them in the correct OU using -Path. Verify each user lands in the right OU in ADUC. Deletion script removes all users. |
| Week 3 | Rebuild Week 2 with try/catch error handling. Run it once successfully. Run it again without deleting first — the catch block handles duplicates and prints a summary: X created, X failed. Deletion script removes all users. |
| Week 4 | Script uses Get-ADUser to query all users in a specific OU. Output displays SamAccountName, OU path, and Enabled status in a clean formatted table. No creation or deletion needed. |

After Week 4 restart from Week 1.

---

### 🟠 Thursday — Linux
**Tool:** Ubuntu VM — Terminal

Create a folder called `practice` at the start of every session.
Complete all tasks inside it.
Run `rm -rf ~/practice` before closing.

| Week | Tasks |
|---|---|
| Week 1 | Create 3 subfolders and 3 files. Write content into each file using nano. Read them back with cat. List all contents with ls -l. Navigate between directories using cd and pwd. |
| Week 2 | Create 3 files. Set permissions 777, 644, and 400 on each using chmod. Read the permission string with ls -l. Attempt to write to the 400 file and observe the denied output. Fix the permission and write to it successfully. |
| Week 3 | Create a log file with 10 lines of mixed content including the words error, success, and failed. Use grep to search for specific words. Use head -n 3 and tail -n 3. Pipe cat into grep to filter output. Copy one file with cp and rename one with mv. |
| Week 4 | Create 2 users with sudo useradd. Set a password for each with sudo passwd. Switch between them using su and verify with whoami. Check /etc/passwd to confirm the users exist. Delete both users with sudo userdel. |

After Week 4 restart from Week 1.

---

### 🔴 Friday — Security
**Tool:** TryHackMe

Work through the current path one room per session.
Read everything properly. Do not rush through for points.
Complete as much as fits in the session.
If a room is unfinished continue from where you left off next Friday.
Skip paid rooms and move to the next free one.

**Current path:** Pre-Security

---

### 🟣 Saturday — Cloud and M365
**Tool:** M365 Admin Center + Entra ID + Exchange Online + Azure Portal

Delete everything created before ending each session.

| Week | Platform | Task |
|---|---|---|
| Week 1 | M365 Admin Center + Entra ID | Create a user. Assign a licence. Open Entra ID and enforce MFA for the user. Review Security Defaults and confirm they are enabled. Check the Secure Score and read the top recommendation. Open sign-in logs and review recent entries. Delete the user. |
| Week 2 | Azure Portal | Create a Resource Group. Deploy one resource inside it — a VM or storage account. Navigate the resource settings. Delete the entire Resource Group before logging out. |
| Week 3 | Exchange Online + M365 Admin Center | Open Exchange Admin Center. Review the existing mail flow rules. Create a shared mailbox and assign a user to it. Check the anti-spam and anti-phishing policies. Verify SPF is configured under domain settings in M365 Admin Center. Open security.microsoft.com and confirm DKIM is enabled under Email Authentication Settings. Delete the shared mailbox. |
| Week 4 | Entra ID + Azure Portal | Open Entra ID and review the audit logs. Create a test user, assign a role, then delete the user. Open Azure Monitor and review the Activity Log for recent actions in the subscription. |

After Week 4 restart from Week 1.

---

### ⚪ Sunday — Ticketing
**Tool:** ServiceNow Personal Developer Instance

Create 3 incidents every Sunday.
Each ticket must include category, priority, a clear problem description,
troubleshooting steps in the work notes, and a resolution note.
Resolve and close all 3 before ending the session.

| Week | Ticket Scenarios |
|---|---|
| Week 1 | User cannot log in — password expired. Account locked after failed attempts. New starter needs an account created and access provisioned. |
| Week 2 | Laptop will not power on. Office printer showing offline. User's second monitor not being detected. |
| Week 3 | Outlook not opening — profile corrupted. Machine running slowly — high CPU usage. Application throwing an error on launch. |
| Week 4 | User cannot access a shared network drive. VPN client failing to connect. One device has no internet access despite others on the same network working. |

After Week 4 restart from Week 1.

---

## Flexible Sessions
Run each one at least once per week.
Pair SharePoint and Power Automate back to back on the same evening where possible.
Delete everything created at the end of each session.

---

### 🔷 SharePoint Online
**Tool:** M365 Business Basic | **Time:** 30 mins

| Week | Task |
|---|---|
| Week 1 | Create a Team Site. Add a document library. Upload 3 files. Create a folder structure inside the library. |
| Week 2 | Set permissions on the document library. Configure Owner, Member, and Visitor access. Verify each level can only perform the actions it should. |
| Week 3 | Create a SharePoint list. Add 4 columns — Title, Status, Priority, Assigned To. Add 5 items. Sort by Priority. Filter by Status. |
| Week 4 | Create a modern page. Add a text section, an image, and a quick links block. Publish it and review the result. |

Delete the site after Week 4 and restart from Week 1.

---

### 🔶 Power Automate
**Tool:** M365 Business Basic | **Time:** 30 mins

| Week | Task |
|---|---|
| Week 1 | Create a flow with a manual trigger. Add a Send Email action. Test the flow and verify the email arrives. Delete the flow. |
| Week 2 | Create a flow triggered when a file is uploaded to a SharePoint library. Action sends an email notification with the filename. Test by uploading a file. Delete the flow. |
| Week 3 | Build on Week 2. Add a condition — if the filename contains the word urgent send one email, otherwise send a different one. Test both paths. Delete the flow. |
| Week 4 | Create an approval flow. A manual trigger sends an approval request. Approved outcome sends a confirmation email. Rejected outcome sends a rejection email. Test both. Delete the flow. |

After Week 4 restart from Week 1.

---

### 🟩 Excel
**Tool:** Microsoft Excel | **Time:** 30 mins

Each session builds a different practical tracker or report.
Save the file at the end. Review what you built. Close it.

| Week | Task |
|---|---|
| Week 1 | Build an incident log table with these columns: Date, Ticket Number, Category, Priority, Description, Status, Resolution Time (mins). Format the header row with bold text and a background colour. Freeze the top row so it stays visible when scrolling. Enter 5 rows of sample data manually. |
| Week 2 | Open the Week 1 file. Add a SUM formula to total the Resolution Time column. Add an AVERAGE formula to calculate average resolution time. Add a COUNTIF formula to count how many tickets have a status of Resolved. Apply conditional formatting to the Priority column — High in red, Medium in amber, Low in green. |
| Week 3 | Open the Week 1 file. Select the Category and Resolution Time columns. Insert a bar chart showing which categories take longest to resolve. Add a chart title. Move the chart below the table. Add a second sheet called Summary. Copy the COUNTIF and AVERAGE formulas onto the Summary sheet referencing the main table. |
| Week 4 | Build a new sheet called Asset Log with these columns: Asset ID, Device Type, Assigned To, Department, Serial Number, Status. Enter 6 rows of sample data. Apply a dropdown list to the Status column using Data Validation with options: Active, In Repair, Decommissioned. Filter the table by Department and confirm it works. |

After Week 4 restart from Week 1.

---

### 🟤 BIOS/UEFI
**Tool:** Lenovo BIOS Simulator (browser based) | **Time:** 20 mins
**Rule:** No changes are saved in the simulator. Close the browser when done.

| Session | Task |
|---|---|
| Session 1 | Open the simulator. Navigate to the boot menu. Identify where the boot order is set. Practice moving a USB device to the top of the boot order — this is what you do before reinstalling an OS or running a recovery tool. |
| Session 2 | Open the simulator. Locate the Security settings. Find Secure Boot and identify how to enable and disable it. Find the TPM setting and note its current state. These are checked when troubleshooting Windows 11 compatibility or BitLocker issues. |
| Session 3 | Open the simulator. Navigate to Advanced or Configuration settings. Locate the virtualisation setting — Intel VT-x or AMD-V. Note whether it is enabled. This is what you check when VMware or Hyper-V will not run on a machine. |
| Session 4 | Open the simulator. Navigate to the Information or Main menu. Record the BIOS version, CPU model, installed RAM, and storage devices shown. This is what you check during hardware diagnostics before logging an asset or raising a repair ticket. |

After Session 4 repeat from Session 1.

---

## Skills Covered

`Active Directory` `Organisational Units` `Security Groups` `Account Management`
`Group Policy` `Event Viewer` `Windows Server 2022` `Task Manager`
`PowerShell` `Scripting` `Bulk User Provisioning` `CSV Import` `Error Handling`
`Linux CLI` `File Permissions` `User Management` `Bash Navigation`
`Networking` `DHCP` `DNS` `Subnetting` `Inter-subnet Routing`
`Microsoft 365 Administration` `Entra ID` `MFA` `Security Defaults`
`Exchange Online` `Mail Flow` `Shared Mailboxes` `SPF` `DKIM`
`SharePoint Online` `Document Libraries` `Permissions` `Lists`
`Power Automate` `Automated Flows` `Conditions` `Approval Workflows`
`Azure Portal` `Resource Groups` `Azure Monitor`
`ServiceNow` `Incident Management` `ITSM`
`Excel` `Formulas` `Conditional Formatting` `Charts` `Data Validation`
`BIOS/UEFI` `Boot Configuration` `Secure Boot` `TPM`
`TryHackMe` `Security Fundamentals` `VMware Workstation`

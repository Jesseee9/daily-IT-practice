
# IT  Daily Practice Lab
---

## Tools

| Tool | Purpose |
|---|---|
| VMware Workstation | Hosts all local virtual machines |
| Windows Server 2022 VM | Active Directory, PowerShell, OS tasks |
| Windows 11 Pro VM | Domain client, end-user simulation |
| Ubuntu Linux VM | Linux CLI practice |
| Cisco Packet Tracer | Network simulation |
| ServiceNow PDI | Ticketing practice |
| M365 Admin Center | Cloud identity and administration |
| Azure Portal | Cloud hands-on |
| Microsoft Learn | Structured cloud modules with sandbox labs |

---

## Weekly Schedule

| Day | Focus | Tool | Time |
|---|---|---|---|
| Monday | Networking | Cisco Packet Tracer | 30–40 mins |
| Tuesday | Operating System | Windows Server 2022 VM | 30–40 mins |
| Wednesday | PowerShell | Windows Server 2022 VM | 30–40 mins |
| Thursday | Linux | Ubuntu VM | 30–40 mins |
| Friday | Security | Windows Server VM + M365 | 30–40 mins |
| Saturday | Cloud | M365 Admin Center + Azure | 30–40 mins |
| Sunday | Ticketing | ServiceNow PDI | 30–40 mins |

---

## Daily Tasks

---

### 🔵 Monday — Networking
**Tool:** Cisco Packet Tracer

Build and test basic network setups from scratch each week.

- Add a router, switches, and PCs to the workspace
- Configure DHCP on the router so devices receive IP addresses automatically
- Add a DNS server and create a basic hostname record
- Test connectivity between all devices using ping
- Rotate weekly:
  - **Week 1** — Single network with DHCP
  - **Week 2** — Add a DNS server
  - **Week 3** — Two subnets with inter-subnet routing

---

### 🟢 Tuesday — Operating System
**Tool:** Windows Server 2022 VM

Practice core Windows Server and Active Directory tasks.

- Open Task Manager and review CPU, RAM, and running processes
- Open Event Viewer and browse the Security and System logs
- Create user accounts and place them in the correct Organisational Units
- Practise disabling, enabling, unlocking, and resetting accounts
- Log into the Windows 11 VM as a domain user to verify everything works
- Rotate weekly:
  - **Week 1** — User and group management
  - **Week 2** — Account lifecycle and Event Viewer
  - **Week 3** — Group Policy basics

---

### 🟡 Wednesday — PowerShell
**Tool:** Windows Server 2022 VM — PowerShell ISE

Write and run scripts that automate Active Directory tasks.

- Create multiple AD users in a loop using a script
- Place users into specific OUs using the `-Path` parameter
- Add `try/catch` error handling so the script reports what failed
- Run a deletion script to clean up all test users when done
- Save every script to `C:\Scripts` with a clear descriptive filename
- Rotate weekly:
  - **Week 1** — Bulk user creation
  - **Week 2** — OU targeting
  - **Week 3** — Error handling and summary output

---

### 🟠 Thursday — Linux
**Tool:** Ubuntu VM — Terminal

Build confidence with the Linux command line through repeated daily use.

- Navigate the file system using `pwd`, `ls`, and `cd`
- Create folders and files, write content with `nano`, read it back with `cat`
- Set and change file permissions using `chmod` and understand the numbers
- Copy, move, and rename files using `cp` and `mv`
- Search inside files using `grep` and chain commands together with pipes
- Clean up everything created during the session before closing

---

🔴 Friday — Security
Tool: TryHackMe
Work through the Pre-Security pathway one room per session.
	∙	Complete one room per Friday session
	∙	Read properly, don’t rush through for points
	∙	Rotate through the path in order — no skipping
	∙	Current path: Pre-Security → SEC0 certification
---

### 🟣 Saturday — Cloud
**Tool:** M365 Admin Center + Azure Portal + Microsoft Learn

Rotate between M365 administration, Azure hands-on, and structured learning.

- Check M365 service health across Exchange, SharePoint, and Teams
- Verify MFA is enforced and review user accounts and licence assignments
- In Azure, create and delete a resource such as a VM, storage account, or Entra ID user
- Always delete test resources immediately after to avoid charges
- On MS Learn weeks, complete one module that includes a hands-on sandbox lab
- Rotate weekly:
  - **Week 1** — M365 Admin Center tasks
  - **Week 2** — Azure hands-on (create and delete resources)
  - **Week 3** — Microsoft Learn module with sandbox

---

### ⚪ Sunday — Ticketing
**Tool:** ServiceNow Personal Developer Instance

Create realistic IT support tickets with proper structure and detail.

- Log into your ServiceNow PDI
- Create 3 to 5 incidents covering different issue types
- For each ticket fill in category, priority, a clear problem description, troubleshooting steps in the work notes, and a resolution note before closing
- Rotate ticket types weekly:
  - **Week 1** — Password resets, account lockouts, access issues
  - **Week 2** — Hardware faults, printer issues, laptop problems
  - **Week 3** — Email issues, slow performance, software errors
  - **Week 4** — Network connectivity, VPN, shared drive access

---

## Repo Structure



## Skills Covered

`Networking` `DHCP` `DNS` `Subnetting` `Active Directory` `Group Policy`
`Windows Server` `Event Viewer` `PowerShell` `Scripting` `Linux CLI`
`File Permissions` `Security Monitoring` `Entra ID` `MFA` `M365 Administration`
`Azure` `Cloud Fundamentals` `ServiceNow` `ITSM` `Incident Management`

---

# Windows Server Backup & Disaster Recovery Homelab

## Project Overview
This project documents the design, implementation, testing, and recovery procedures of a Windows Server backup and disaster recovery environment for Nexora Technologies (fictional company).

The lab is built using Microsoft Hyper-V, Windows Server 2025, Active Directory Domain Services, and Windows Server Backup.
The goal is to develop hands-on experience in protecting critical business infrastructure, backing up data and system components, recovering accidental deleted files, and restoring services following simulated failures.

This project builds upon my previous [Active Directory Homelab - Nexora Technologies](https://github.com/JefferyGitsIt/active-directory-homelab/tree/main).

## Project Objectives
- [x] Understand Windows Server backup and disaster recovery fundamentals.
- [x] Install and configure Windows Server Backup.
- [x] Configure dedicated backup storage.
- [x] Create and verify departmental file backups.
- [x] Restore deleted files from backups.
- [ ] Perform an Active Directory system state backup.
- [ ] Practice Active Directory object recovery.
- [ ] Configure and test full server backups.
- [ ] Perform a controlled disaster recovery simulation.
- [ ] Verify backup integrity and review recovery logs.
- [ ] Document recovery procedures, security considerations, and lessons learned.

## Lab Environment
The project uses an existing Active Directory environment hosted on Microsoft Hyper-V.

| Component | Operating System | Role | IP Address |
| :--- | :--- | :--- | :--- |
| DC01 | Windows Server 2025 | Active Directory Domain Controller / DNS | 10.77.10.10 |
| FILE01 | Windows Server 2025 | Departmental File Server | 10.77.10.30 |
| CLIENT01 | Windows 11 Pro | Domain-Joined Workstation | 10.77.10.21 |
| CLIENT02 | Windows 11 Pro | Domain-Joined Workstation | 10.77.10.22 |

## Network Configuration
| Setting | Value |
| :--- | :--- |
| Domain | ad.nexora.test |
| Hyper-V Virtual Switch | Nexora-Internal |
| Network | 10.77.10.0/24 |
| DNS Server | 10.77.10.10 |
| Virtualization Platform | Microsoft Hyper-V |

## Technologies and Tools
- Microsoft Hyper-V
- Windows Server 2025
- Windows Server Backup
- Active Directory Domain Services
- Windows PowerShell
- Group Policy Management
- Windows Event Viewer
- NTFS and SMF File Sharing
- Virtual Hard Disks (VHDX)

## Lab Roadmap
| Lab | Topic | Status |
| :--- | :--- | :--- |
| 01 | Backup and Disaster Recovery Fundamentals | Completed |
| 02 | Windows Server Backup Installation | Completed |
| 03 | FILE01 Backup Storage and Configuration | Completed |
| 04 | File Backup and Recovery Testing | Completed |
| 05 | Active Directory System State Backup | Not Started |
| 06 | Active Directory Object Recovery | Not Started |
| 07 | Full Server Backup Configuration | Not Started |
| 08 | Disaster Recovery Simulation | Not Started |
| 09 | Backup Verification and Monitoring | Not Started |
| 10 | Security Review and Lessons Learned | Not Started |

Each lab will include configuration steps, commands where applicable, screenshots, verification results, and lessons learned.

## Backup and Recovery Strategy
The lab will explore multiple types of backup and recovery procedures.

## File-Level Backup
Create backups of departmental files stored on FILE01.
Practice recovering test files that have been accidentally deleted or modified.

## Active Directory System State Backup
Protect critical domain controller components, including Active Directory and related system configuration.
Practice identifying and verifying appropriate backups for directory recovery.

## Full Server Backup
Create backups suitable for recovering a Windows Server installation following a system failure.

## Disaster Recovery Testing
Simulate controlled failure scenarios and documented recovery procedures in an isolated environment.
Recovery testing will be planned to avoid disrupting the existing Active Directory homelab.

## Backup Storage Considerations
Initial backups will use dedicated virtual hard disks in the Hyper-V lab environment.
These disks will be separate from the operating system and primary data volumes.

**Important:** Because the virtual disks reside on the same physical storage device, this lab configuration does not protect against physical host or disk failure. A production backup strategy should include independent backup storage, offsite copies, and regular recovery testing.

## Documentation
Detailed lab documentation will be added as the project progresses.

| Lab | Documentation |
| :--- | :--- |
| 01 | [Lab 01 - Backup and Disaster Recovery Fundamentals](lab/01.md) |
| 02 | [Lab 02 - Windows Server Backup Installation](lab/02.md) |
| 03 | [Lab 03 - FILE01 Backup Storage and Configuration](lab/03.md) |
| 04 | [Lab 04 - File Backup and Recovery Testing](lab/04.md) |
| 05 | Planned |
| 06 | Planned |
| 07 | Planned |
| 08 | Planned |
| 09 | Planned |
| 10 | Planned |

## Expected Learning Outcomes
Upon completing this project, I aim to demonstrate practical knowledge of:

- Windows Server backup administartion
- File and folder recovery
- Active Directory system state protection
- Server recovery planning
- Backup storage management
- PowerShell administration
- Recovery verification and troubleshooting
- Disaster recovery documentation

## Project Status

Status: **In Progress**

The initial Active Directory infrastructure is already deployed and operational. Backup configuration and recovery testing will be documented in this repository as each lab is completed.

## Related Project

[Active Directory Homelab](https://github.com/JefferyGitsIt/active-directory-homelab/tree/main)

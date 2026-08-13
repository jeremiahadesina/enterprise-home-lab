# Enterprise Home Lab

A hands-on enterprise IT infrastructure lab designed and built to develop practical experience in systems administration, virtualization, networking, security, and cloud technologies.

The environment is built around a dedicated physical server running Proxmox VE and is being developed to simulate technologies and scenarios commonly encountered in business IT environments.

## Project Overview

This project documents the design, deployment, configuration, and administration of my enterprise home lab.

Rather than relying entirely on preconfigured cloud labs, I built a dedicated virtualization server from individual hardware components and configured the environment from the ground up.

The lab provides an environment for deploying and managing Windows Server, Windows clients, Linux systems, networking services, security controls, and eventually hybrid Azure infrastructure.

## Core Technologies

- Proxmox VE
- Windows Server
- Active Directory Domain Services
- DNS
- DHCP
- Group Policy
- Windows Client Administration
- Linux
- PowerShell
- TCP/IP Networking
- VLANs
- Firewalls
- Microsoft Azure
- Virtualization
- Backup and Recovery

## Physical Server

| Component | Specification |
|---|---|
| Processor | AMD Ryzen 7 5700X |
| CPU | 8 Cores / 16 Threads |
| Memory | 32 GB DDR4 |
| Storage | 1 TB NVMe SSD |
| Graphics | AMD RX 550 |
| Platform | B550 |
| Hypervisor | Proxmox VE |

## Lab Architecture

The initial environment consists of a dedicated Proxmox virtualization server connected to my home network.

The Proxmox host provides the virtualization platform for multiple systems and services.

    Internet
       |
    Home Router
       |
    Proxmox VE
       |
       +-- Windows Server
       |
       +-- Windows Client
       |
       +-- Linux Server
       |
       +-- Future Firewall / Network Appliances

The architecture will evolve as additional networking, security, and hybrid cloud components are implemented.

## Project Documentation

The project is documented in phases.

| Phase | Description | Status |
|---|---|---|
| [01 - Planning](./01-planning/) | Project scope, architecture, risks, hardware planning and success criteria | Complete |
| [02 - Server Build](./02-server-build/) | Physical server assembly and hardware configuration | Complete |
| [03 - Proxmox Installation](./03-proxmox-installation/) | Hypervisor installation and initial configuration | Complete |
| [04 - Windows Server Deployment](./04-windows-server-deployment/) | Windows Server VM deployment and VirtIO configuration | In Progress |
| 05 - Active Directory | AD DS deployment and domain configuration | Planned |
| 06 - DNS | Internal DNS configuration and testing | Planned |
| 07 - DHCP | DHCP scopes and address management | Planned |
| 08 - Group Policy | Centralized Windows configuration using GPOs | Planned |
| 09 - Windows Client | Domain-joined Windows workstation deployment | Planned |
| 10 - File Server | File shares and NTFS permissions | Planned |
| 11 - Networking | Advanced network configuration and troubleshooting | Planned |
| 12 - Firewall & VLANs | Network segmentation and firewall implementation | Planned |
| 13 - Linux | Linux server administration | Planned |
| 14 - Azure Hybrid | Integration of on-premises infrastructure with Microsoft Azure | Planned |

## Project Objectives

This lab is designed to strengthen hands-on experience with:

- Deploying and administering virtualized infrastructure
- Managing Windows Server environments
- Implementing Active Directory
- Configuring DNS and DHCP
- Managing users, computers, groups, and Group Policy
- Troubleshooting network connectivity
- Implementing network segmentation
- Administering Linux systems
- Automating administrative tasks with PowerShell
- Implementing backup and recovery
- Exploring hybrid cloud infrastructure with Microsoft Azure
- Documenting technical implementations and troubleshooting processes

## Current Progress

The physical server has been assembled and Proxmox VE has been successfully deployed.

Windows Server has also been deployed as a virtual machine. During deployment, VirtIO storage drivers were configured to allow Windows Server to detect the virtual SCSI disk.

The environment will continue to expand with Active Directory, DNS, DHCP, Group Policy, Windows clients, networking, Linux, security, and Azure hybrid services.

## Repository Structure

enterprise-home-lab/
│
├── README.md
├── COPYRIGHT.md
├── 01-planning/
├── 02-server-build/
├── 03-proxmox-installation/
└── 04-windows-server-deployment/

Additional sections will be added as the lab develops.

## Documentation Approach

Each section contains:

- Objectives
- Design decisions
- Configuration steps
- Screenshots
- Troubleshooting notes
- Results
- Lessons learned

This repository is intended to demonstrate both the implementation process and the reasoning behind infrastructure decisions.

## Author

**Jeremiah Adesina**

IT Infrastructure | Systems Administration | Networking | Azure

---

## Copyright

© 2026 Jeremiah Adesina. All rights reserved.

This repository documents my personal enterprise home lab and is provided for educational and portfolio purposes. The documentation, photographs, screenshots, diagrams, and other original content in this repository may not be reproduced, redistributed, or used without permission.
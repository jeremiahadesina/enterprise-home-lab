# 01 - Planning and Design



## Overview



Before building the physical server, I created a project plan outlining the purpose, scope, hardware requirements, architecture, risks, and success criteria for the home lab.



The goal was to build a virtualization environment that could be used to develop practical skills in system administration, networking, virtualization, and security.



---



## Project Objective



The objective of this project is to design and build a home server using Proxmox VE as the virtualization platform.



The environment will be used to:



- Practice Windows and Linux system administration

- Deploy and manage virtual machines

- Build Active Directory environments

- Configure DNS and DHCP services

- Practice networking concepts

- Experiment with VLANs and firewall configurations

- Simulate a small business IT environment

- Support hands-on certification study and technical skill development



---



## Project Scope



### In Scope



The initial project includes:



- Building a dedicated physical virtualization server

- Installing Proxmox VE

- Hosting multiple virtual machines

- Deploying Windows Server

- Deploying Linux servers

- Practicing Windows and Linux administration

- Creating a small Active Directory environment

- Configuring DNS and DHCP

- Practicing virtual networking

- Learning network bridging

- Implementing VLANs and firewall rules

- Testing backup and snapshot functionality

- Documenting configurations and troubleshooting



### Out of Scope



The following were intentionally excluded from the initial deployment:



- Public VPS hosting

- Production workloads

- High-availability clustering

- Multi-node Proxmox clustering

- Public-facing services



These may be explored in future expansions of the lab.



---



## Design Decisions



### CPU



An 8-core / 16-thread processor was selected to provide enough processing capacity for multiple virtual machines running simultaneously.



### Memory



32 GB of RAM was selected to provide sufficient memory for several concurrent Windows and Linux virtual machines without creating an immediate resource bottleneck.



### Storage



NVMe SSD storage was selected to provide fast disk performance for virtual machines, operating system installations, and general lab workloads.



### Cooling



An aftermarket air cooler was selected to provide reliable cooling, reduced noise, and support for extended server uptime.



### Networking



The initial configuration uses the motherboard's onboard Ethernet interface.



Additional network interfaces may be added later to support more advanced networking scenarios including:



- VLAN segmentation

- Firewall appliances

- Multiple virtual networks

- Routing experiments

- Network isolation



---



## Planned Architecture



The initial architecture is:



Physical Server
      |
      v
Proxmox VE Hypervisor
      |
      v
Virtual Machines
      |
      +-- Windows Server
      |
      +-- Windows Client
      |
      +-- Linux Server
      |
      +-- Firewall / Networking VM (Future)



The Proxmox host connects to the existing home network using Ethernet.



As the lab develops, additional virtual networks and VLANs will be introduced to simulate a more realistic enterprise environment.



---



## Risks and Mitigations



| Risk | Mitigation |

| --- | --- |

| Hardware failure | Maintain backups and document configurations |

| Configuration mistakes | Use VM snapshots before major changes |

| VM failure | Maintain backups and reusable installation media |

| Network misconfiguration | Test changes in isolated virtual networks |

| Residential internet limitations | Keep lab services private and low traffic |

| Resource limitations | Monitor CPU, RAM, and storage usage |



---



## Success Criteria



The initial phase of the project will be considered successful when:



- Proxmox VE is successfully installed

- The Proxmox web management interface is accessible

- At least two virtual machines can operate successfully

- Windows Server can be deployed

- Basic virtual networking is operational

- VM snapshots and backups can be created

- Major configurations are documented

- Lessons learned and troubleshooting steps are recorded



---



## Initial Project Timeline



| Phase | Planned Work |

| --- | --- |

| Week 1 | Hardware assembly and BIOS configuration |

| Week 2 | Proxmox installation and initial VM deployment |

| Week 3 | Networking experiments and documentation |



The timeline is intended as a general project roadmap rather than a strict implementation schedule.



---



## Next Step



With the planning and design phase completed, the next stage of the project is the physical server build.



[Continue to 02 - Server Build](../02-server-build/)



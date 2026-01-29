# Cybersecurity Enterprise Virtualization Lab: Multi-Tier Network Infrastructure Deployment

## Executive Summary

This project demonstrates the design, implementation, and deployment of an enterprise-grade virtual IT infrastructure using Oracle VM VirtualBox. The lab environment simulates a production network topology featuring Windows Server 2022 Active Directory Domain Controller and departmentalized Windows 8 client workstations, all interconnected via an isolated NAT networking architecture.

## Technical Objectives

- **Infrastructure Virtualization**: Provision isolated virtual machine environments for enterprise systems simulation
- **Network Segmentation**: Implement NAT Network topology enabling inter-VM communication and internet connectivity
- **Domain Controller Deployment**: Configure Windows Server 2022 as centralized authentication and directory services platform
- **Client Workstation Provisioning**: Deploy departmental endpoint systems (Sales, HR) demonstrating organizational unit segregation
- **Resource Optimization**: Leverage type-2 hypervisor technology for cost-effective lab environment on consumer hardware

## Architecture Overview

### Network Topology
```
┌──────────────────────────────────────────────────────────────┐
│                    NAT Network (10.0.2.0/24)                 │
│                                                              │
│  ┌──────────────────┐      ┌──────────────┐  ┌────────────┐  │
│  │ Windows Server   │      │ Windows 8    │  │ Windows 8  │  │
│  │ 2022 DC          │◄────►│ Sales Dept   │  │ HR Dept    │  │
│  │ Domain Controller│      │ Workstation  │  │ Workstation│  │
│  └──────────────────┘      └──────────────┘  └────────────┘  │
│         ▲                                                    │
│         │                                                    │
└─────────┼────────────────────────────────────────────────────┘
          │
          ▼
    Internet Gateway
     (Host System)
```

### System Specifications

| Component | Configuration |
|-----------|---------------|
| **Hypervisor** | Oracle VM VirtualBox 7.x |
| **Host Operating System** | Windows/Linux (Multi-platform) |
| **Network Architecture** | NAT Network with DHCP |
| **Domain Controller** | Windows Server 2022 Standard |
| **Client Endpoints** | Windows 8.1 Enterprise (x2) |
| **Storage Allocation** | Dynamic VDI (40GB per VM) |
| **Processor Assignment** | 2 vCPU cores per VM |
| **Memory Allocation** | 2048-4096 MB per VM |

## Key Features Implemented

### 1. Virtualization Platform Configuration
- Oracle VM VirtualBox installation and environment preparation
- Virtual machine creation using Expert Mode for granular control
- Dynamic disk allocation for efficient storage utilization
- Multi-core processor assignment for enhanced performance

### 2. Network Infrastructure Design
- **NAT Network Implementation**: Isolated virtual subnet with internet access
- **DHCP Services**: Automatic IP addressing for simplified endpoint configuration
- **Inter-VM Communication**: Layer-3 connectivity between all virtual machines
- **Network Type Analysis**: Comprehensive evaluation of 6 VirtualBox networking modes
  - NAT (Network Address Translation)
  - NAT Network
  - Bridged Adapter
  - Internal Network
  - Host-only Adapter
  - Generic Driver

### 3. Operating System Deployment
- Windows Server 2022 ISO acquisition from Microsoft Evaluation Center
- Unattended Windows 8.1 client installation procedures
- VirtualBox Guest Additions integration for enhanced functionality
- Post-deployment optimization and system hardening

### 4. Enterprise Services Configuration
- Active Directory Domain Services (AD DS) readiness
- Departmental organizational unit structure (Sales, HR)
- Foundation for future Group Policy implementation
- Scalable architecture supporting additional domain members

## Visual Documentation Summary

The following screenshots demonstrate critical implementation phases of the virtual infrastructure deployment:

### Screenshot 1: VirtualBox Installation
<img width="847" height="436" alt="image" src="https://github.com/user-attachments/assets/b2bb7225-9911-4ac8-9211-5aad8cee8869" />
<img width="699" height="550" alt="image" src="https://github.com/user-attachments/assets/6bcd73be-7f29-419a-a1f6-cab9f520c4ce" />

*Oracle VM VirtualBox installer download from official repository*

### Screenshot 2: VirtualBox Manager Dashboard
<img width="822" height="431" alt="image" src="https://github.com/user-attachments/assets/9e065aa3-4728-415f-846e-45961c74462a" />
<img width="717" height="376" alt="image" src="https://github.com/user-attachments/assets/a2cae198-cb78-4453-bd9f-4f7f6293547a" />
*VirtualBox Manager interface showing virtualization management console*

### Screenshot 3: Virtual Machine Creation Wizard
<img width="922" height="590" alt="image" src="https://github.com/user-attachments/assets/8ad7a0d7-6c07-4099-bed0-772368b1ac51" />

*Expert Mode VM provisioning with granular resource allocation controls*

### Screenshot 4: Virtual Hard Disk Configuration
<img width="949" height="643" alt="image" src="https://github.com/user-attachments/assets/9457eae2-ec1f-4888-96f8-1d7dd1174f81" />
<img width="964" height="550" alt="image" src="https://github.com/user-attachments/assets/8f1a2c56-141d-43f6-a01f-6f767b1b5d00" />

*Dynamic VDI creation with 40GB capacity and thin provisioning*

### Screenshot 5: CPU Resource Assignment
<img width="957" height="388" alt="image" src="https://github.com/user-attachments/assets/495b5ea4-4f5d-4314-9fb4-b5bbc928a858" />

*Multi-core processor allocation for optimal VM performance*

### Screenshot 6: NAT Network Architecture
<img width="975" height="476" alt="image" src="https://github.com/user-attachments/assets/c7d28052-b644-443b-bf3b-5d51a3d13520" />

*NAT Network creation for isolated virtual subnet with internet connectivity*

### Screenshot 7: Network Adapter Binding
<img width="961" height="586" alt="image" src="https://github.com/user-attachments/assets/f34aa63e-1066-48e3-ad93-0ddccb81411b" />

*VM network adapter attachment to custom NAT Network*

### Screenshot 8: Windows Server 2022 ISO Mounting
<img width="953" height="436" alt="image" src="https://github.com/user-attachments/assets/346b78a7-f86f-433e-9f10-c984a946c375" />

*Operating system ISO attachment for bootable installation media*

### Screenshot 9: Windows Server Installation
<img width="713" height="642" alt="image" src="https://github.com/user-attachments/assets/4bd5f83e-052f-4dd4-86b7-8a7a1491dd93" />
<img width="711" height="644" alt="image" src="https://github.com/user-attachments/assets/29c33d49-a8dd-4871-a55d-f163f8fd5ccd" />
<img width="848" height="741" alt="image" src="https://github.com/user-attachments/assets/acfcfef3-3781-41e8-82ff-5c84a192dffa" />

*Windows Server 2022 deployment initialization screen*

### Screenshot 10: Windows 8 Client Deployment
<img width="975" height="684" alt="image" src="https://github.com/user-attachments/assets/ae7dd793-7851-425c-99c0-c7665bbc64d7" />
<img width="975" height="487" alt="image" src="https://github.com/user-attachments/assets/64226174-d22b-49b2-b929-25d334167fa8" />
<img width="975" height="473" alt="image" src="https://github.com/user-attachments/assets/d9f1e176-e77d-4b12-b73b-edd751270d8e" />
<img width="975" height="680" alt="image" src="https://github.com/user-attachments/assets/34260d6c-6c15-4390-900a-4646f8db1436" />

*Windows 8.1 Enterprise installation on departmental workstation*

**Note**: Complete screenshot documentation (31 images total) and comprehensive technical documentation are available in the repository files:
- **Full Documentation**: `Virtual_IT_Lab_Complete_Documentation.docx`
- **All Screenshots**: `screenshots/` directory (image_0.jpeg through image_30.jpeg)

## Implementation Methodology

### Phase 1: Hypervisor Deployment
1. Downloaded Oracle VM VirtualBox from official distribution channels
2. Executed installation wizard with default enterprise configuration
3. Verified virtualization extensions (Intel VT-x/AMD-V) enabled in BIOS
4. Launched VirtualBox Manager for infrastructure provisioning

### Phase 2: Virtual Machine Provisioning
1. Initiated VM creation wizard in Expert Mode
2. Configured VM parameters:
   - Name: Descriptive identifier (e.g., "WinServer2022-DC")
   - Type: Microsoft Windows
   - Version: Windows Server 2022 / Windows 8.1
   - Memory: 2048-4096 MB
   - Storage: 40GB Dynamic VDI
3. Assigned multi-core processors (2 vCPUs recommended)
4. Configured boot order prioritizing optical drive

### Phase 3: Network Infrastructure Deployment
1. Navigated to File → Preferences → Network
2. Created custom NAT Network:
   - Network Name: "LabNetwork"
   - Network CIDR: 10.0.2.0/24 (default)
   - DHCP: Enabled
3. Attached VM network adapters to NAT Network
4. Verified network connectivity and DHCP lease acquisition

### Phase 4: Operating System Installation
1. **Windows Server 2022 Deployment**:
   - Downloaded ISO from Microsoft Evaluation Center
   - Mounted ISO to VM optical drive
   - Booted from installation media
   - Completed installation wizard (Standard GUI)
   - Applied initial system updates

2. **Windows 8.1 Client Deployment**:
   - Acquired Windows 8.1 Enterprise evaluation media
   - Repeated installation procedure for Sales and HR workstations
   - Configured unique machine names per department
   - Installed VirtualBox Guest Additions for enhanced integration

### Phase 5: Post-Deployment Configuration
1. Installed VirtualBox Guest Additions on all VMs
   - Enabled clipboard sharing
   - Configured dynamic display resolution
   - Improved mouse/keyboard integration
2. Verified network connectivity between all nodes
3. Documented system baseline configurations
4. Created VM snapshots for rollback capability

## Technical Benefits and Use Cases

### Cybersecurity Applications
- **Malware Analysis**: Isolated sandbox for threat investigation
- **Network Security Testing**: IDS/IPS evaluation and tuning
- **Penetration Testing**: Controlled environment for security assessments
- **Incident Response Training**: Realistic scenario simulation

### IT Administration Training
- **Active Directory Configuration**: Domain controller, GPO, user management
- **DHCP/DNS Services**: Network services implementation and troubleshooting
- **File Server Deployment**: SMB shares, NTFS permissions, DFS
- **Backup and Recovery**: Disaster recovery procedures and testing

### Software Development
- **Application Testing**: Multi-OS compatibility validation
- **Development Environment**: Isolated dev/test/staging environments
- **Database Administration**: SQL Server, Oracle, MySQL deployments
- **Web Server Configuration**: IIS, Apache, Nginx implementations

## Expansion Capabilities

The current architecture provides foundation for advanced implementations:

### Network Services Expansion
- **Active Directory Domain Services**: Complete AD DS deployment
- **DHCP Server**: Centralized IP address management
- **DNS Server**: Internal name resolution services
- **Certificate Services**: PKI infrastructure for encryption

### Infrastructure Additions
- **Linux Systems**: Ubuntu Server, CentOS, Kali Linux integration
- **Network Appliances**: pfSense firewall, Security Onion IDS
- **Additional Clients**: Windows 10/11 endpoints
- **Application Servers**: Web servers, database systems, file servers

### Advanced Configurations
- **Multiple Network Segments**: VLAN simulation via Internal Networks
- **DMZ Architecture**: Multi-tier network security implementation
- **Site-to-Site VPN**: Inter-network secure tunneling
- **Load Balancing**: High-availability service distribution

## Technical Requirements

### Minimum Host System Specifications
- **Processor**: Intel Core i5 / AMD Ryzen 5 (4+ cores, VT-x/AMD-V enabled)
- **Memory**: 16GB RAM (8GB for host, 8GB for VMs)
- **Storage**: 120GB available disk space (SSD recommended)
- **Operating System**: Windows 10/11, Ubuntu 20.04+, macOS 10.15+

### Software Dependencies
- **Hypervisor**: Oracle VM VirtualBox 7.0 or later
- **Operating Systems**: 
  - Windows Server 2022 ISO (Evaluation available)
  - Windows 8.1 Enterprise ISO (Evaluation available)
- **Guest Additions**: VirtualBox Guest Additions ISO (included with VirtualBox)

## Knowledge Domains Demonstrated

This project showcases proficiency in:
- ✅ **Virtualization Technologies**: Type-2 hypervisor architecture and management
- ✅ **Network Architecture**: Subnet design, NAT, DHCP, TCP/IP fundamentals
- ✅ **Windows Server Administration**: Server OS installation and base configuration
- ✅ **Systems Integration**: Multi-platform environment deployment
- ✅ **Technical Documentation**: Professional documentation and visual aids
- ✅ **Resource Optimization**: Efficient allocation of compute, memory, and storage
- ✅ **Enterprise IT Infrastructure**: Foundational knowledge of corporate network design

## Future Development Roadmap

### Phase 1: Directory Services (Planned)
- Active Directory domain controller promotion
- Organizational unit structure implementation
- Group Policy Object creation and deployment
- User and computer account management

### Phase 2: Network Services (Planned)
- DHCP server configuration and scope management
- DNS server deployment and zone configuration
- File sharing services (SMB/CIFS)
- Print server implementation

### Phase 3: Security Hardening (Planned)
- Windows Firewall with Advanced Security configuration
- Local Security Policy implementation
- Security baseline enforcement
- Event log auditing and monitoring

### Phase 4: Advanced Infrastructure (Planned)
- Linux server integration (Ubuntu Server 22.04)
- SIEM deployment (Security Onion, Splunk)
- Network segmentation via Internal Networks
- Vulnerability management system implementation

## Learning Outcomes

Upon completion of this lab environment, practitioners gain hands-on experience with:

1. **Enterprise Virtualization**
   - Hypervisor installation and configuration
   - Virtual machine lifecycle management
   - Resource allocation and performance tuning

2. **Network Infrastructure Design**
   - Virtual network topology planning
   - Network adapter configuration
   - IP addressing and subnetting
   - Traffic isolation and segmentation

3. **Windows Server Administration**
   - Server OS installation procedures
   - Initial system configuration
   - Guest tools integration
   - System snapshot management

4. **Documentation Standards**
   - Technical writing best practices
   - Visual documentation creation
   - Architecture diagram development
   - Step-by-step procedure documentation

## Troubleshooting Guide

### Common Issues and Resolutions

**Issue**: VM fails to boot
- **Resolution**: Verify ISO mounted correctly, check boot order settings

**Issue**: No network connectivity
- **Resolution**: Confirm VM attached to NAT Network, verify DHCP service running

**Issue**: Poor VM performance
- **Resolution**: Increase CPU cores, allocate additional RAM, move VDI to SSD

**Issue**: Guest Additions installation fails
- **Resolution**: Ensure VM has CD/DVD drive, mount Guest Additions ISO, run installer as administrator

## Acknowledgments

- **Oracle Corporation**: VirtualBox virtualization platform
- **Microsoft Corporation**: Windows Server and client operating system evaluation media
- **Open Source Community**: Documentation resources and technical guidance

## Contact Information
https://www.linkedin.com/in/fayomi31/
---

**Project Status**: ✅ **Production Ready**  

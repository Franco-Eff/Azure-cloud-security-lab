# Azure Cloud Security Lab

## Project Overview

This project is a hands-on Azure Cloud Security Lab designed to demonstrate fundamental cloud administration, identity management, network security, governance, and security monitoring.

The lab uses a fictional organization called **TechDefense (TD)** to simulate a small business environment. The goal is to build a secure Azure environment using Microsoft Azure services while applying security best practices and testing the effectiveness of the configurations.

This project is designed to demonstrate practical knowledge relevant to cloud administration, cybersecurity, and the Microsoft AZ-104 Azure Administrator certification.

## Project Objectives

- Build and configure an Azure virtual network.
- Implement network segmentation using subnets.
- Secure network traffic using Network Security Groups (NSGs).
- Create and manage users and security groups in Microsoft Entra ID.
- Apply Role-Based Access Control (RBAC) to enforce least privilege.
- Configure Azure Policy to restrict resource deployment locations.
- Implement resource locks to prevent accidental deletion.
- Investigate administrative activity using Azure Activity Logs.
- Perform security tests to verify that configurations work as intended.

## Technologies Used

| Technology | Purpose |
|---|---|
| Microsoft Azure | Cloud infrastructure |
| Microsoft Entra ID | Identity and access management |
| Azure Virtual Network | Network infrastructure |
| Network Security Groups | Network traffic filtering |
| Azure RBAC | Access control |
| Azure Policy | Governance and compliance |
| Azure Resource Locks | Resource protection |
| Azure Monitor | Activity Log investigation |
| GitHub | Project documentation |

## Lab Architecture

The lab uses a single Azure Resource Group to organize its resources.

**Resource Group:** `TD-Security-RG`

**Region:** East US 2

### Network Design

**Virtual Network:** `TD-VNet`

**Address Space:** `10.10.0.0/16`

| Subnet | Address Range | Purpose |
|---|---|---|
| TD-Employee-Subnet | 10.10.1.0/24 | Employee network |
| TD-Server-Subnet | 10.10.2.0/24 | Server network |

Each subnet uses a Network Security Group to control inbound and outbound traffic.

## Identity and Access Management

Microsoft Entra ID is used to organize users according to their responsibilities.

Planned security groups:

- `TD-IT-Admins`
- `TD-Security-Analysts`
- `TD-Employees`

Azure RBAC assignments will provide different levels of access based on each group's responsibilities.

The objective is to follow the principle of least privilege, ensuring users receive only the permissions necessary to perform their tasks.

## Network Security

Network Security Groups will be configured to restrict unauthorized remote access.

Planned inbound security rules include:

- Deny TCP port 3389 (RDP).
- Deny TCP port 22 (SSH).

These rules will be applied to the employee and server subnets.

## Governance and Resource Protection

The lab will use Azure Policy to restrict resource deployments to the East US 2 region.

A resource lock will also be applied to the virtual network to help prevent accidental deletion.

## Security Monitoring

Azure Monitor and the Azure Activity Log will be used to investigate administrative activity.

The investigation will focus on:

- Who performed an action.
- What operation was performed.
- When the operation occurred.
- Whether the operation succeeded or failed.
- The details recorded in the activity log.

## Security Testing

The lab will include practical tests to verify the effectiveness of the configurations.

Planned tests:

1. Verify network security rules.
2. Test access permissions assigned through RBAC.
3. Attempt a resource deployment outside the permitted region.
4. Attempt to delete a resource protected by a resource lock.
5. Investigate administrative events in the Activity Log.

## Cost Considerations

This project is designed to minimize Azure costs by focusing on basic resource configuration and management features.

The lab does not intentionally use paid services such as Azure Firewall, Azure Bastion, Microsoft Sentinel, or paid Defender plans.

Azure pricing and subscription-specific charges should still be checked before creating resources.

## Project Status

**Current Status:** In Progress

This repository will be updated as each configuration, security test, and investigation is completed.

## Documentation

Detailed configuration guides, explanations, and testing results will be organized into the following sections:

- Networking
- Identity and Access Management
- Governance
- Monitoring
- Security Testing
- Architecture

Screenshots will be included to demonstrate the configurations performed in the Azure Portal.

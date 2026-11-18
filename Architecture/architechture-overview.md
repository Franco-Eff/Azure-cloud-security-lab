The virtual network was divided into two subnets to separate employee and server workloads.

Subnet

Address Range

Purpose

Proj-Employee-Subnet

10.10.1.0/24

Employee network

Proj-Server-Subnet

10.10.2.0/24

Server network

Each subnet has an associated Network Security Group (NSG) to control network traffic.

Network Security Groups

Proj-Employee-NSG

Proj-Server-NSG

Inbound rules were configured to deny TCP traffic on ports 3389 (RDP) and 22 (SSH).

This helps reduce exposure to unauthorized remote administrative access.

4. Identity and Access Management

Microsoft Entra ID was used to create users and security groups based on organizational responsibilities.

The lab includes the following groups:

Proj-IT-Admins

Proj-Security-Analysts

Proj-Employees

Azure Role-Based Access Control (RBAC) was used to assign permissions according to each group's responsibilities.

The goal was to implement least privilege and prevent unnecessary access to Azure resources.

5. Governance and Resource Protection

Two governance controls were implemented:

Azure Policy

An Allowed Locations policy was configured to restrict resource deployment to East US 2.

Resource Locks

A CanNotDelete resource lock was applied to Proj-VNet to prevent accidental deletion.

These controls help enforce organizational standards and protect important infrastructure.

6. Monitoring and Investigation

Azure Monitor and the Activity Log were used to investigate administrative activity.

The investigation focused on identifying:

The identity responsible for an action.

The operation performed.

The time the operation occurred.

The operation's status.

Additional event details.

This provides visibility into changes made to Azure resources.

7. Security Testing

The lab included validation of the implemented security controls.

Security Control

Validation

Network Security Groups

Reviewed inbound rules

RBAC

Checked assigned roles and permissions

Azure Policy

Tested deployment restrictions

Resource Locks

Tested deletion protection

Activity Log

Investigated administrative events

The individual testing procedures and results are documented in the Security-Testing directory.

8. Security Principles Demonstrated

Least Privilege: Users should only receive the permissions necessary for their responsibilities.

Network Segmentation: Separating workloads helps organize and control network access.

Defense in Depth: Multiple security controls protect different parts of the environment.

Governance: Organizational policies help enforce consistent configurations.

Resource Protection: Locks reduce the risk of accidental infrastructure deletion.

Monitoring and Accountability: Activity logs provide visibility into administrative operations.

9. Conclusion

This lab provided hands-on experience implementing foundational security controls in Microsoft Azure.

It demonstrates how identity, network security, governance, resource protection, and monitoring work together to secure a cloud environment.

# Stage 2 Summary — Cloud and Azure Operational Base

## 1. Stage Goal
Understand the cloud service model and Azure resource hierarchy well enough to deploy and organize foundational infrastructure in a clean and controlled way.

## 2. Topics Covered
- Cloud model fundamentals and shared-responsibility perspective.
- Service models: IaaS, PaaS, and SaaS.
- Azure logical structure: tenant, subscription, resource group, and region.
- Azure Portal navigation and operational reading of resource views.
- Basic IAM concepts.
- Introductory networking objects in Azure: virtual network (VNet), subnet, and NSG.

## 3. Hands-on Practice
- Created and organized resources using Azure Portal.
- Built a basic environment with:
  - Resource Group
  - VNet
  - Subnet
  - NSG
- Reviewed how resource scope and hierarchy affect management and permissions.

## 4. What I Understand Better Now
- Azure organization is not just naming; tenant/subscription/RG/region decisions affect governance, cost visibility, and operations.
- IaaS, PaaS, and SaaS are operational responsibility models, not only product categories.
- VNet, subnet, and NSG form the first control layer for workload communication.
- IAM and network controls solve different problems and should not be conflated.

## 5. Common Mistakes / Friction Points
- Confusing hierarchy levels (for example, treating resource groups as network boundaries).
- Assuming NSG replaces identity and access controls.
- Creating resources without clear scope conventions, making later management harder.

## 6. Outcome at Stage Closure
I can create a basic Azure foundation and explain why each component exists in the architecture. I also have an initial operational mental model of how scope, access, and network controls interact.

## 7. Next Step
Use this base to deploy compute and storage services, then compare trade-offs between VM, App Service, and storage options in real scenarios.

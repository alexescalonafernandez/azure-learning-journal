# Azure Resource Inventory (Stages 2–4)

This inventory summarizes the Azure resources created during the AZ-104 lab work across stages 2, 3, and 4.

## Lab Scope

- **Subscription:** `alex-azure-lab-sub`
- **Primary Resource Group:** `rg-lab-azurefundamentals-we-01`

## Resource Inventory

| Resource name | Resource type | Purpose | Stage introduced | Current status / Keep-or-delete recommendation |
|---|---|---|---|---|
| `alex-azure-lab-sub` | Subscription | Dedicated boundary for billing, access control, and resource organization for this lab environment. | Stage 2 | **Active. Keep.** Core subscription context for all lab resources. |
| `rg-lab-azurefundamentals-we-01` | Resource Group | Logical container to manage, tag, and clean up related lab resources together. | Stage 2 | **Active. Keep (for now).** Retain while continuing labs; delete only when the full lab path is complete. |
| `vnet-lab-core-we-01` | Virtual Network | Provides private network space for lab resources and future connectivity exercises. | Stage 2 | **Active. Keep.** Foundational networking component reused across labs. |
| `snet-core-default` | Subnet | Default subnet inside the lab VNet used to place compute resources. | Stage 2 | **Active. Keep.** Required if more networked resources are deployed later. |
| `nsg-lab-core-we-01` | Network Security Group | Inbound/outbound traffic filtering rules for subnet/VM-level protection and testing. | Stage 2 | **Active. Keep.** Useful for ongoing security rule practice. |
| Linux lab VM (name varied by exercise) | Virtual Machine | Compute host for Linux administration, connectivity, and VM operations practice. | Stage 3 | **Stopped (deallocated). Delete recommended** when VM-specific exercises are done. |
| VM-associated resources (NIC, public IP, OS disk, diagnostics artifacts if any) | NIC / Public IP / Managed Disk / Supporting resources | Required dependencies for VM networking and storage. | Stage 3 | **Delete recommended** together with the VM to avoid unnecessary ongoing charges. |
| Lab App Service Plan | App Service Plan | Compute tier hosting web app runtime for App Service exercises. | Stage 4 | **Delete recommended** after completing web app labs. |
| Lab App Service | Web App (`Microsoft.Web/sites`) | PaaS web application deployment and configuration practice. | Stage 4 | **Delete recommended** after validation/testing is complete. |
| Associated Application Insights | Application monitoring component | Telemetry, logs, performance traces, and availability insights for the web app. | Stage 4 | **Delete recommended** if app is removed and monitoring data is no longer needed. |
| `stlabalexwe01` | Storage Account | General-purpose storage for blob/file services and storage feature labs. | Stage 4 | **Active. Keep.** Reusable, low-friction resource for continued storage practice. |
| Lab Blob container (inside `stlabalexwe01`) | Blob Container | Object storage exercises (upload/download, access levels, lifecycle basics). | Stage 4 | **Active. Keep.** Helpful for ongoing blob-related tasks. |
| Lab File share (inside `stlabalexwe01`) | Azure Files share | SMB/NFS-style managed file share comparison with blob storage. | Stage 4 | **Active. Keep.** Useful for file service and identity/access experiments. |

## Suggested Cleanup Priority

1. **High priority delete:** VM + all VM dependencies, App Service Plan, App Service, Application Insights.
2. **Keep for next labs:** VNet, subnet, NSG, Storage Account and its blob/file objects.
3. **End-of-course cleanup option:** remove full resource group once all practice is complete.

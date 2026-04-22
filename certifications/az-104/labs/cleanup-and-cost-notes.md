# Cleanup and Cost Notes (AZ-104 Labs)

These notes are a practical guide to keep the lab useful while limiting avoidable Azure spend.

## 1) Basic Cost Mental Model by Resource Type

> No exact prices are listed here because costs vary by region, SKU/tier, and usage pattern.

### Subscription and Resource Group
- **Subscription (`alex-azure-lab-sub`)**: not a billed resource by itself, but it is the billing boundary.
- **Resource Group (`rg-lab-azurefundamentals-we-01`)**: logical container, no direct cost.

### Networking (VNet, Subnet, NSG)
- **VNet / Subnet / NSG** usually have low or no direct base cost in basic lab usage.
- Cost can appear indirectly when attached resources generate traffic (for example, outbound data transfer).

### Virtual Machine stack
- **VM compute** is typically one of the fastest ways to accumulate cost when running.
- **Important nuance:** stopping a VM from inside the OS is not the same as Azure deallocation.
  - To minimize cost, the VM should be **Stopped (deallocated)** in Azure.
- **Managed disks, snapshots, and public IPs** can keep generating charges even if VM compute is deallocated.

### App Service Plan + App Service + Application Insights
- **App Service Plan** can continue costing money while it exists, because it reserves compute capacity.
- **App Service** depends on the plan; deleting the app alone may not remove plan cost.
- **Application Insights ingestion and retention** may accumulate cost with ongoing telemetry.

### Log Analytics Workspace and diagnostics pipeline
- **Log Analytics Workspace** can generate cost via data ingestion and retention.
- **Diagnostic settings** control what data is sent; broad capture can increase cost quickly.
- For labs, route only the categories needed for current exercises.

### Alerting resources
- **Alert rules** are operationally useful, but too many low-quality rules create noise.
- Cost and operational overhead can increase when alerts are overly broad, too frequent, or tied to noisy signals.

### Storage Account (`stlabalexwe01`)
- Storage costs are generally tied to:
  - Data volume stored (Blob/File)
  - Transactions/operations
  - Redundancy tier selected
- Often suitable to keep for labs, but old test data should be pruned.

## 2) Why Cleanup Is Worth It

Cleaning up resources after each stage helps you:
- Avoid “silent” recurring costs from forgotten resources (especially compute plans, disks, and telemetry ingestion).
- Keep the environment simple so the next lab starts from a clear baseline.
- Reduce operational noise in monitoring, RBAC views, and resource lists.
- Prevent accidental drift from the original lab design.

For this lab path, cleanup is especially valuable after VM and App Service exercises, and after each monitoring experiment that enables extra diagnostics or alert rules.

## 3) Practical Keep-vs-Delete Guidance for This Environment

### Keep
- `vnet-lab-core-we-01`
- `snet-core-default`
- `nsg-lab-core-we-01`
- `stlabalexwe01` (plus blob container and file share if still useful)
- Log Analytics Workspace (while monitoring labs continue)
- Only active, meaningful alert rules

### Delete when done
- Linux lab VM (already deallocated)
- VM dependencies (NIC, public IP, disk, etc.)
- Lab App Service Plan
- Lab App Service
- Associated Application Insights
- Unused alert rules/action groups created for one-off tests
- Diagnostic settings no longer needed for active labs

## 4) Lab Hygiene Best Practices (to Avoid Unnecessary Spend)

1. **Use naming that implies lifecycle**
   - Include `lab`, region, and sequence in names (already done in this environment).
2. **Tag resources for cleanup**
   - Example tags: `env=lab`, `owner=alex`, `cleanup_by=YYYY-MM-DD`.
3. **Deallocate compute immediately after testing**
   - VM and any paid hosting plans should not stay running between sessions.
4. **Delete dependent resources in the same session**
   - When removing a VM, also verify NIC/public IP/disks are gone.
5. **Control telemetry scope intentionally**
   - Enable only the logs/metrics needed for the learning objective.
6. **Review Cost Analysis regularly**
   - Quick weekly check helps catch forgotten resources early.
7. **Keep reusable core infrastructure, remove ephemeral workloads**
   - Keep network/storage foundations; remove temporary compute/app resources.
8. **Prefer one active lab path at a time**
   - Finish, document, and clean one stage before launching many parallel experiments.

## 5) Suggested Lightweight Cleanup Routine

After each lab session:
1. Open resource group `rg-lab-azurefundamentals-we-01`.
2. Identify resources created or modified during that session.
3. Deallocate or delete compute-oriented resources first.
4. Review diagnostics and alert rules enabled for short-lived tests.
5. Confirm only baseline reusable resources remain.
6. Add a short note in your journal with what was kept vs deleted.

This routine keeps your AZ-104 environment predictable, reusable, and cost-aware without slowing down hands-on practice.

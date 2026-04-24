# Lab Notes — CLI, PowerShell, and Bicep Foundations

## Scope
Hands-on baseline automation practice for Stage 6:
- Azure CLI setup and operational queries.
- Azure PowerShell setup and basic resource queries.
- First end-to-end Bicep validation/deployment/redeployment cycle.

## Practical Sequence Completed
1. Verified Azure CLI presence and installed it when missing.
2. Executed `az version` to validate the toolchain.
3. Attempted `az login`, then resolved MFA constraints with `az login --use-device-code`.
4. Confirmed active subscription context.
5. Queried resources using `list` and `show` patterns (resource groups, VMs, web apps, storage accounts).
6. Applied a tag change to an existing Storage Account via CLI and verified the update.
7. Verified PowerShell version and upgraded to PowerShell 7.
8. Installed `Az` module.
9. Connected with `Connect-AzAccount -DeviceCode`, then validated context and queried resource groups.
10. Authored a minimal `main.bicep` for a Storage Account deployment.
11. Ran `az deployment group validate` successfully.
12. Ran `az deployment group create` successfully.
13. Verified the created resource via `az storage account show`.
14. Redeployed the same template without changes and observed no effective drift.
15. Added a declarative tag in Bicep, redeployed, and verified convergence.

## Key Lessons Reinforced
- Device code authentication is a practical MFA fallback for CLI/PowerShell workflows.
- `list` vs `show` is important for broad discovery vs targeted inspection.
- Validation is a preflight check and does not create resources.
- Declarative redeploy supports reproducibility and idempotent behavior.
- IaC improves consistency, but does not replace backup/restore responsibilities.

## Evidence Quality and Limits
- This lab demonstrates real execution and troubleshooting, not only conceptual review.
- Scope is intentionally foundational; it does not include advanced Bicep modules, multi-resource architectures, or CI/CD pipelines.

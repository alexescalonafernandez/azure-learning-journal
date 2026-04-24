# Stage 6 Summary — Initial Azure Automation with Azure CLI, PowerShell, ARM, and Bicep

## 1. Stage Goal
Build a real entry-level automation baseline in Azure, reducing dependency on the Portal and introducing practical use of Azure CLI, Azure PowerShell, and declarative Infrastructure as Code with Bicep.

## 2. Starting Point and Scope
At the beginning of this stage, I already had practical experience in:
- Azure Portal-based operations.
- Resource groups, VNets/subnets/NSGs, Linux VMs, App Service, and Storage Account basics.
- Introductory monitoring with Azure Monitor, logs, metrics, diagnostic settings, alerts, Log Analytics, and Application Insights.

What was **not** assumed as advanced:
- Real cloud automation workflows.
- Azure CLI fluency.
- Azure PowerShell fluency.
- ARM/Bicep troubleshooting depth.
- CI/CD for infrastructure deployments.

## 3. Topics Covered
- Why Azure Portal is useful but insufficient as the only operating model.
- Manual operations vs scripting vs Infrastructure as Code.
- Imperative vs declarative approaches.
- ARM as Azure's control/deployment plane (broader than only ARM JSON files).
- Bicep fundamentals and its relation to ARM templates.
- Bicep file structure (`param`, `resource`, `output`) and symbolic name vs real resource name.
- Validation before deployment (`validate`) and why validation is not the same as successful provisioning.
- Basic reproducibility/idempotency through redeploying the same Bicep definition.

## 4. Hands-on Practice Completed
- Installed Azure CLI and verified the installation with `az version`.
- Resolved MFA login friction by using `az login --use-device-code`.
- Confirmed active subscription context and queried resource groups/resources with `list` and `show` commands.
- Updated administrative metadata safely by applying a tag to an existing Storage Account via CLI.
- Installed PowerShell 7 (after identifying Windows PowerShell 5.1 baseline).
- Installed Azure PowerShell `Az` module and authenticated with `Connect-AzAccount -DeviceCode`.
- Verified context and queried resource groups with PowerShell cmdlets.
- Authored a minimal `main.bicep` (Storage Account scenario), validated deployment, executed deployment, and verified the resource.
- Performed redeploy with no effective changes, then redeployed with a small declarative tag change and verified convergence.

## 5. What I Understand Better Now
- Portal remains valuable for exploration and inspection, but it is not a reproducible source of truth.
- CLI/PowerShell are operational scripting tools; Bicep is a declarative IaC language.
- In imperative workflows, I specify steps; in declarative workflows, I specify desired state.
- ARM is the common platform control plane used by Portal, CLI, PowerShell, and Bicep deployments.
- Bicep definitions can be validated, deployed, and redeployed in a repeatable cycle.

## 6. Performance Assessment at Stage Closure
Overall stage performance: **Good**.

Strengths shown:
- Strong reasoning and good translation from software engineering concepts to cloud operations.
- Good problem-solving under real friction (MFA/authentication/tooling setup).
- Clear progress away from total Portal dependency.
- Successful completion of a first real IaC cycle: define → validate → deploy → verify → redeploy.

Areas still in progress:
- Terminology precision in edge cases (avoid over-absolute wording).
- Avoid interpreting Bicep too procedurally.
- Improve selective reading of verbose JSON outputs.
- Build depth in advanced Bicep modules, richer templates, and CI/CD-integrated IaC workflows.

## 7. Stage Outcome
This stage is complete at an entry-level practical baseline.

I am **not** claiming advanced automation or advanced IaC expertise yet. The result is a real and useful foundation: I can begin automation workflows with CLI/PowerShell and execute basic declarative deployments with Bicep in a controlled, verifiable way.

## 8. Next Step
Continue with gradual depth on top of this base:
- Small integrative labs combining operations and IaC.
- More repetition of define/validate/deploy/verify cycles.
- Better change reasoning (`what changes`, `why`, `what-if`, `how to verify`).
- Continued mentoring with incremental complexity and precise technical language.

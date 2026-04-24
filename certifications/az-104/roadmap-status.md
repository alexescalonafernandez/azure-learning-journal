# AZ-104 Roadmap Status

## 1. Current Stage
I have completed the first six stages of my AZ-104 roadmap.

My current level is: **foundational practical operator (initial automation phase)**. I can operate core Azure resources, read key operational signals, and execute first-pass automation with Azure CLI, introductory Azure PowerShell, and basic Bicep deployments. I still need deeper troubleshooting, richer IaC design practice, and stronger CI/CD integration skills.

## 2. Completed Stages
1. **Minimum Operational Fundamentals**
   Established baseline operational habits (resource organization, basic CLI usage, repeatable step-by-step execution).

2. **Cloud Fundamentals and Azure Operational Basics**
   Built core cloud understanding and how Azure services are structured and managed in practice.

3. **Core Compute and Storage in Azure**
   Practiced creating and managing VMs, App Services, and Storage Accounts with realistic configuration tasks.

4. **Operational Networking and Identity in Azure**
   Worked on virtual networking and access control foundations (network components + identity/RBAC basics).

5. **Monitoring and Basic Resource Operations in Azure**
   Built a practical base for metrics/logs/activity interpretation, initial alert design, and evidence-driven troubleshooting.

6. **Initial Azure Automation with Azure CLI, PowerShell, ARM, and Bicep**
   Built first practical automation capacity: command-line operations, ARM mental model, and a full basic Bicep cycle (define, validate, deploy, verify, redeploy).

## 3. Skills Built So Far
- Create and configure core Azure resources (compute, storage, network foundations, and supporting components).
- Use Azure Portal and command-line workflows to execute and validate lab tasks consistently.
- Distinguish signal types and operational roles:
  - metrics,
  - logs,
  - Activity Log,
  - diagnostic settings,
  - alerts.
- Apply initial Azure Monitor / Log Analytics / Application Insights concepts in troubleshooting.
- Use a layer-oriented diagnostic method before jumping to root-cause conclusions.
- Use Azure CLI for initial operational automation and metadata/resource inspection workflows.
- Use Azure PowerShell at an introductory level for authenticated context and resource queries.
- Read, validate, deploy, and redeploy a basic Bicep definition with evidence-based verification.
- Document lab outcomes and operational notes to reinforce repeatable practice.

## 4. Areas Still in Progress
- Troubleshooting speed and depth when symptoms are broad or ambiguous.
- Better multi-hypothesis exploration before converging on one suspected layer.
- More practical exposure to realistic load patterns and richer telemetry.
- Stronger alert calibration (avoid noisy conditions and weak signal quality).
- Deeper automation and IaC maturity (advanced Bicep patterns, safer change workflows, CI/CD integration).
- More mature, repeatable runbook-style incident handling.

## 5. Next Planned Stage
**Next stage:** Intermediate automation and operational reliability (name to be finalized).

Planned focus:
- Expand Bicep usage beyond minimal single-resource definitions.
- Strengthen safe change analysis with `what-if`, validation discipline, and clearer rollback thinking.
- Practice small multi-resource deployments with better parameterization decisions.
- Improve signal correlation and troubleshooting quality during automated change operations.

## 6. Notes on Learning Approach
My approach is intentionally practical and incremental:
- Build a small set of core skills first, then expand.
- Validate understanding through hands-on labs, not only theory.
- Document what I configured, what failed, and what I changed.
- Prioritize repeatability and operational clarity over speed.

This roadmap reflects real progress: I am not claiming expert-level administration yet. I am building a reliable, hands-on Azure operations base step by step.

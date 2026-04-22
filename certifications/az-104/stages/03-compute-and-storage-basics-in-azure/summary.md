# Stage 3 Summary — Compute and Storage Foundations in Azure

## 1. Stage Goal
Deploy and operate core Azure compute and storage services, and strengthen troubleshooting practice by validating networking and access dependencies in real deployments.

## 2. Topics Covered
- Azure compute options: Virtual Machines and App Service.
- App Service Plan purpose and relation to App Service.
- Azure Storage Account fundamentals.
- Storage services comparison: Blob Storage vs Azure Files.
- SSH access troubleshooting to Linux VM, including NSG rule verification.
- Service comparison from an operational perspective (management overhead, control level, and common use cases).

## 3. Hands-on Practice
- Deployed and validated a Linux VM.
- Diagnosed SSH connection problems by checking NSG rules and related network settings.
- Created App Service Plan and App Service, then reviewed deployment and runtime behavior.
- Created a Storage Account and examined Blob and Azure Files usage patterns.
- Compared VM/App Service/Storage service choices using practical criteria instead of theory only.

## 4. What I Understand Better Now
- VM gives more control but also more operational responsibility.
- App Service abstracts host management, but still requires understanding plan sizing and app configuration.
- Blob and Azure Files serve different access models and should be selected by workload behavior, not by familiarity.
- Connectivity problems are often multi-layered; NSG and endpoint assumptions must be checked explicitly.

## 5. Common Mistakes / Friction Points
- Troubleshooting SSH from the client side only, without validating Azure-side NSG and network path.
- Assuming App Service Plan and App Service are interchangeable concepts.
- Treating all Storage Account services as equivalent despite different protocols and usage patterns.

## 6. Outcome at Stage Closure
I can deploy a small but complete compute + storage base in Azure, explain service selection trade-offs, and execute basic diagnostics when access fails.

## 7. Next Step
Deepen networking and identity operations by troubleshooting access through layered controls (RBAC, guest OS permissions, network path, and data plane permissions).

# Stage 1 Summary — Operational Fundamentals

## 1. Stage Goal
Build a minimum operational foundation before working deeply with Azure, so day-to-day administration tasks and troubleshooting steps are understandable and repeatable.

## 2. Topics Covered
- Basic operating system concepts: filesystems, users, permissions, processes, and services.
- Linux usage in WSL2.
- Command-line work with Bash and initial tasks in PowerShell.
- Basic troubleshooting habits: identify symptoms, verify assumptions, and test incrementally.
- Introductory networking concepts (IP, ports, connectivity checks).
- Conceptual comparison between virtual machines, containers, and cloud-managed services.

## 3. Hands-on Practice
- Navigated Linux environments in WSL2 and practiced common shell commands.
- Reviewed running processes and service states.
- Practiced command-line routines in Bash and compared them with PowerShell workflows.
- Performed basic connectivity and service checks as troubleshooting exercises.
- Worked through practical examples to distinguish when a workload fits better in a VM, container, or cloud service.

## 4. What I Understand Better Now
- The operating system layer is not optional; it directly affects cloud operations.
- Processes, services, and network ports are key observability points when something fails.
- Bash and PowerShell differ in style and object handling, but both are useful for operational work.
- VM vs container vs managed service decisions should be based on control level, operational responsibility, and deployment needs.

## 5. Common Mistakes / Friction Points
- Treating commands as isolated recipes instead of understanding what subsystem they inspect.
- Mixing troubleshooting steps without an order, which makes root cause harder to find.
- Assuming networking issues are always “application issues” before validating basic connectivity.

## 6. Outcome at Stage Closure
I finished this stage with a practical baseline to operate a Linux environment, inspect service/process state, and follow a basic troubleshooting flow. This created the technical ground needed to approach Azure resources more confidently.

## 7. Next Step
Move from local and OS-level fundamentals into Azure structure and cloud operating model: tenant, subscription, resource group, region, and core network building blocks.

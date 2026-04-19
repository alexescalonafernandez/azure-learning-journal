# AZ-104 Project Backlog (Realistic & Prioritized)

## Purpose and planning stance
> Note: This backlog uses the referenced project names and practical AZ-104 alignment as a working interpretation. I will refine specifics against the source repository when needed.

This backlog is an **honest technical evaluation**, not a promise to execute everything immediately.

I will use it to:
- choose projects that reinforce AZ-104 objectives,
- focus on operational depth before complexity,
- reduce scope aggressively when needed,
- and postpone projects that require advanced skills I am still building.

Readiness labels used in this document:
- **Soon**: good candidate to start after current stage wrap-up.
- **Later**: useful for AZ-104 growth, but needs more maturity first.
- **Not now**: important long-term, but currently too dependent on advanced capabilities.

---

## Priority order
1. **Onboard Automator** — **Soon**
2. **ShareSafely** — **Soon**
3. **VM Fleet Commander** — **Later**
4. **NetMaze Explorer** — **Later**
5. **InsightScape** — **Not now**

This order is intentionally conservative: first consolidate core administration workflows, then move into broader orchestration, deeper networking diagnostics, and finally advanced observability patterns.

---

## 1) Onboard Automator
### What the project is about
A structured environment onboarding project focused on provisioning and standardizing baseline Azure resources, access patterns, and operational checks so that a new workload/team can start from a repeatable foundation.

### Why it is relevant to AZ-104
- Reinforces day-to-day administrator responsibilities: resource provisioning, governance basics, access setup, and operational consistency.
- Connects directly with AZ-104 areas: subscriptions/resource groups, identities/roles, and baseline operational hygiene.

### Estimated readiness for me
**Soon**

### Main dependencies or prerequisite skills
- Solid resource group/subscription structure decisions.
- Practical Entra ID + RBAC operational usage.
- Tagging/naming standards and basic policy awareness.
- Comfort with portal + CLI/PowerShell for repeatable tasks.

### Scope reduction notes (if needed)
- Start with one subscription and one workload only.
- Use manual runbook + light scripting (no full IaC framework initially).
- Limit governance to essential tags, role assignments, and naming checks.
- Skip advanced approval workflows in version 1.

---

## 2) ShareSafely
### What the project is about
A secure file/data sharing pattern in Azure centered on controlled access, storage protections, and operational safeguards for internal/external collaboration scenarios.

### Why it is relevant to AZ-104
- Strongly aligned with core storage and identity operations in AZ-104.
- Practices access control, protection settings, and monitoring for storage resources.
- Builds confidence in practical secure-by-default admin decisions.

### Estimated readiness for me
**Soon**

### Main dependencies or prerequisite skills
- Azure Storage account/container/share fundamentals.
- SAS/RBAC access control basics and lifecycle handling.
- Basic networking restrictions for storage endpoints.
- Operational logging/alerts basics for suspicious access patterns.

### Scope reduction notes (if needed)
- Focus on one storage service first (Blob **or** Files).
- Start with internal sharing only; leave B2B/external edge cases for later.
- Implement minimal monitoring (2–3 meaningful alerts).
- Document risk trade-offs explicitly instead of overengineering controls.

---

## 3) VM Fleet Commander
### What the project is about
A VM operations project for managing a small fleet consistently: deployment patterns, configuration baseline, patching cadence, start/stop controls, and health checks.

### Why it is relevant to AZ-104
- Directly targets AZ-104 compute administration responsibilities.
- Exercises VM lifecycle management, extensions, availability considerations, and operational maintenance.
- Bridges core admin tasks with automation discipline.

### Estimated readiness for me
**Later**

### Main dependencies or prerequisite skills
- Strong VM provisioning and sizing judgment.
- Backup/update/patch operational routines.
- Basic automation runbooks/scripts for repetitive operations.
- Intro-level monitoring and incident triage practices.

### Scope reduction notes (if needed)
- Limit initial fleet to 2–3 VMs in one environment.
- Skip multi-region/high-availability sophistication at first.
- Handle patch orchestration in a simple scheduled model.
- Avoid integrating full CI/CD until baseline operations are stable.

---

## 4) NetMaze Explorer
### What the project is about
A networking visibility and troubleshooting project to map, validate, and diagnose connectivity paths across Azure network components.

### Why it is relevant to AZ-104
- AZ-104 requires operational networking confidence, including routing, segmentation, and secure connectivity.
- Improves practical troubleshooting habits rather than only design-theory knowledge.
- Helps identify and explain real connectivity failures.

### Estimated readiness for me
**Later**

### Main dependencies or prerequisite skills
- VNet/subnet/NSG/UDR fundamentals already fluent.
- Effective use of Azure network diagnostic tools.
- Practical DNS and hybrid connectivity basics.
- Structured troubleshooting method (hypothesis -> test -> evidence).

### Scope reduction notes (if needed)
- Start with single-VNet scenarios before peering/hybrid complexity.
- Choose 3–4 failure cases only (NSG, route, DNS, endpoint).
- Keep diagrams and evidence logs lightweight but consistent.
- Defer advanced traffic analytics and deep packet workflows.

---

## 5) InsightScape
### What the project is about
An observability-oriented project that unifies operational signals (metrics, logs, alerts, dashboards) into a coherent monitoring story for Azure workloads.

### Why it is relevant to AZ-104
- Supports AZ-104 monitoring and operational response objectives.
- Encourages actionable alerting and service health interpretation.
- Builds the foundation for later SRE-style maturity.

### Estimated readiness for me
**Not now**

### Main dependencies or prerequisite skills
- Confident Azure Monitor/Log Analytics query usage.
- Alert tuning and noise-reduction experience.
- Better troubleshooting maturity across compute/network/identity.
- Clear operational KPIs and incident response habits.

### Scope reduction notes (if needed)
- Begin with one workload + one dashboard + a short alert set.
- Track only high-signal metrics first; avoid “collect everything.”
- Keep KQL simple in phase 1 and iterate with real incidents.
- Defer cross-subscription observability architecture.

---

## Execution discipline for this backlog
- Reassess this backlog after each completed AZ-104 stage.
- Promote/demote readiness based on evidence from labs, not motivation alone.
- If a project stalls for skill gaps, pause and capture prerequisites explicitly.
- Prefer finishing a small scope slice over starting multiple projects in parallel.

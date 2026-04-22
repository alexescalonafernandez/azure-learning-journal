# Stage 4 Summary — Operational Networking and Identity in Azure

## 1. Stage Goal
Develop an operational troubleshooting framework based on access layers, so incidents can be diagnosed systematically instead of by trial and error.

## 2. Topics Covered
- Access layers in Azure operations:
  - RBAC and control plane authorization
  - Guest OS permissions and local access controls
  - Network access controls (NIC/subnet/private-public IP/NSG)
  - Data-plane access controls
- Core networking components and relationships: NIC, subnet, private/public IP, NSG.
- Basic DNS relevance for connectivity and name resolution.
- Symptom-driven troubleshooting flow.
- Diagnostic reading in Azure Portal to confirm or discard hypotheses.

## 3. Hands-on Practice
- Analyzed connectivity and access scenarios by separating identity, network, and data-layer causes.
- Traced resource configuration through Azure Portal views to validate effective settings.
- Practiced troubleshooting by symptom type (for example: cannot connect, can connect but no permission, resolves name vs cannot resolve).

## 4. What I Understand Better Now
- “No access” is not one problem; it can fail at different layers and each layer has distinct evidence.
- RBAC does not replace NSG, and NSG does not replace guest OS permissions.
- NIC/subnet/IP/NSG relationships are fundamental for interpreting whether traffic should reach a workload.
- Azure Portal can be used as a diagnostic source when read methodically, not just as a deployment UI.

## 5. Common Mistakes / Friction Points
- Jumping directly to one layer (usually network) without checking identity and data access first.
- Assuming DNS is secondary even when symptoms clearly suggest name-resolution issues.
- Reading portal pages in isolation instead of correlating configuration across dependent resources.

## 6. Outcome at Stage Closure
I now have a clearer operational method for diagnosing Azure access issues by layers, which improves both speed and accuracy during troubleshooting.

## 7. Next Step
Apply this layered method to more integrated scenarios across compute, storage, identity, and network services, with stronger focus on repeatable operational playbooks.

# Stage 5 Summary — Monitoring and Basic Resource Operations in Azure

## 1. Stage Goal
Build a practical baseline for monitoring and day-to-day operations in Azure, so I can reason like an operator and not only like a resource creator.

## 2. Starting Point and Scope
At the beginning of this stage, I already had practical foundations in:
- Tenant, subscription, resource group, and region structure.
- Azure Portal operational navigation.
- Basic RBAC.
- VNet, subnet, private/public IP, and entry-level NSG usage.
- Linux VM basics in Azure.
- Initial App Service and Storage Account usage (Blob and Azure Files).
- Layer-based troubleshooting foundations from Stage 4.

What was **not** assumed as advanced:
- Production-grade observability.
- Fine-grained operational troubleshooting under pressure.
- Centralized log analysis at meaningful scale.
- Alert design calibration.
- Application-level instrumentation in Azure.

## 3. Topics Covered
- What “operating a resource” means beyond provisioning it.
- Differences between metrics, logs, Activity Log, diagnostic settings, and alerts.
- Azure Monitor as an operational umbrella for signals and analysis workflows.
- Activity Log for administrative-change tracing and troubleshooting context.
- Initial metric interpretation for VM, App Service, and Storage.
- Log Analytics Workspace as a centralized analysis target.
- Application Insights as application-level telemetry.
- Basic alert design (signal + condition + notification mindset).
- Initial troubleshooting flow guided by evidence, not assumptions.

## 4. Hands-on Practice Completed
- Used Azure Monitor concepts to map where each signal type is useful during incidents.
- Practiced Activity Log reading for “something changed and then failed” scenarios.
- Reviewed VM/App Service/Storage metrics with a hypothesis-first interpretation method.
- Worked with Log Analytics Workspace as a central point for cross-resource signal analysis.
- Completed a real App Service deployment workflow with GitHub via Deployment Center.
- Investigated and fixed an OIDC authorization/permissions issue during deployment.
- Validated the fix through successful redeployment and web access verification.
- Enabled and reviewed Application Insights signals (failed requests, response time, request count, availability).
- Designed and discussed basic alerts for VM CPU and App Service HTTP/application health signals.

## 5. What I Understand Better Now
- A resource being created does not imply healthy service behavior.
- A running platform does not guarantee a healthy application.
- Metrics, logs, Activity Log, diagnostics configuration, and alerts are different concepts with different operational roles.
- Azure Monitor is a monitoring/operations ecosystem umbrella, not just one isolated screen.
- Log Analytics Workspace helps avoid fragmented, resource-by-resource investigations.
- Application Insights is key to seeing application behavior beyond platform status.
- Alerts are early-warning mechanisms; they are not root-cause explanations.

## 6. Performance Assessment at Stage Closure
Overall stage performance: **Good**.

Strengths shown:
- Layer-based reasoning remained consistent and useful.
- Better distinction between symptom, signal, hypothesis, and cause.
- Good use of evidence during the real deployment incident.
- Stronger operational structure in troubleshooting responses.

Areas still in progress:
- Terminology precision in ambiguous scenarios (avoid over-conclusive wording too early).
- Wider hypothesis generation when symptoms are broad (latency/access/errors).
- Faster prioritization of Activity Log when a recent change is explicitly mentioned.
- More practical intuition from richer telemetry, which is currently limited by low lab workload.

## 7. Stage Outcome
This stage is complete. I now have a credible foundational operational baseline for monitoring and basic resource operations in Azure.

I am not claiming advanced observability expertise yet. The progress here is practical and real: better diagnostic thinking, clearer signal interpretation, and stronger separation between platform state and application behavior.

## 8. Next Step
Continue into the next stage with emphasis on:
- More realistic troubleshooting scenarios with cross-service dependencies.
- Better signal correlation across metrics/logs/activity events.
- Alert tuning quality (reduce noise, keep meaningful detection).
- More repeatable operational playbooks and incident response routines.

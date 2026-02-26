# Cloud Guardrails + Logging/Telemetry + Detection Pack

**Goal:** A provider-agnostic (cloud-neutral) starter pack that demonstrates how to:
1) set cloud security guardrails/baselines,  
2) design centralized logging/telemetry, and  
3) build detections + runbooks to detect and respond to cloud/identity attack paths.

**Built to support:**
- Cloud Security Intern / Security Engineering Intern (Cloud/Platform)
- Cloud Security Analyst / Junior Security Engineer
- Security Analytics / Detection Content (build-focused)

## What this project demonstrates
- Cloud guardrails and secure configuration baseline thinking
- Centralized logging/telemetry requirements (what to log and why)
- Detection use-case development (signal vs noise)
- Incident runbooks (validate → scope → contain → recover → prevent recurrence)
- Clear, executive-friendly documentation

## Contents
- [Guardrails Blueprint](docs/guardrails-blueprint.md) — identity, network, secrets, secure defaults
- [Logging Plan](docs/logging-plan.md) — sources, retention, routing, access
- [Detection Tuning Guide](docs/detection-tuning-guide.md) — reducing false positives and improving fidelity
- [Detections](detections/) — required data, logic, false-positive notes
- [Runbooks](runbooks/) — response steps and containment actions
- [Templates](templates/) — consistent formats for detections/runbooks

## Detection ↔ Runbook index (initial)
| ID | Detection | Runbook |
|---:|---|---|
| 001 | Suspicious sign-in (new device/location) | [RB-001 Suspicious sign-in](runbooks/RB-001-suspicious-signin.md) |

## Roadmap (near-term)
Expand to **10 detections + 10 runbooks** focused on cloud + identity attack paths:
- Suspicious sign-ins / impossible travel concepts
- Privileged role assignment
- Mass permission changes
- Logging disabled or reduced
- Firewall/security group opened broadly
- New access keys/tokens created unexpectedly
- Unusual resource creation in a new region/account
- Unusual data access spike
- Suspicious OAuth application consent (conceptual)

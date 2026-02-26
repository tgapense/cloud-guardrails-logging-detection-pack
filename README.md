# Cloud Guardrails + Logging/Telemetry + Detection Pack

**Goal:** A provider-agnostic (cloud-neutral) starter pack that demonstrates how to:
1) set cloud security guardrails/baselines,  
2) design centralized logging/telemetry, and  
3) build detections + runbooks to detect and respond to cloud/identity attack paths.

This portfolio is built to support:
- **Cloud Security Intern / Security Engineering Intern (Cloud/Platform)**
- **Cloud Security Analyst / Junior Security Engineer**
- **Security Analytics / Detection Content (build-focused)**

## What this project demonstrates
- Cloud guardrails and secure configuration baseline thinking
- Centralized logging/telemetry requirements (what to log and why)
- Detection use-case development (signal vs noise)
- Incident runbooks (validate → scope → contain → recover → prevent recurrence)
- Clear, executive-friendly documentation

## Contents
- `/docs/guardrails-blueprint.md` — Guardrails baseline (identity, network, secrets, secure defaults)
- `/docs/logging-plan.md` — Logging/telemetry plan (sources, retention, routing, access)
- `/docs/detection-tuning-guide.md` — Reducing false positives and improving fidelity
- `/detections/` — Detection use cases (each includes required data + logic + false positive notes)
- `/runbooks/` — Matching runbooks (each includes response steps)
- `/templates/` — Templates for consistent writing

## Detection ↔ Runbook index (initial)
| ID | Detection | Runbook |
|---:|---|---|
| 001 | Suspicious sign-in (new device/location) | RB-001 Suspicious sign-in |

## Roadmap (near-term)
- Expand to **10 detections + 10 runbooks** focused on cloud + identity attack paths:
  - suspicious sign-ins / impossible travel concepts
  - privileged role assignment
  - mass permission changes
  - logging disabled or reduced
  - firewall/security group opened broadly
  - new access keys/tokens created unexpectedly
  - unusual resource creation in new region/account
  - unusual data access spike
  - suspicious OAuth application consent (conceptual)

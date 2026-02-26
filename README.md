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

## Progress
- [x] Repository structure created (`docs/`, `templates/`, `detections/`, `runbooks/`)
- [x] Templates created (detection + runbook)
- [x] DET-001 + RB-001 — Suspicious sign-in (new device/location)
- [ ] DET-002 + RB-002 — Multiple failed sign-ins then success
- [ ] DET-003 + RB-003 — Privileged role assignment
- [ ] DET-004 + RB-004 — Mass permission changes
- [ ] DET-005 + RB-005 — Logging disabled/reduced
- [ ] DET-006 + RB-006 — Firewall/security group opened broadly
- [ ] DET-007 + RB-007 — New access key/token created unexpectedly
- [ ] DET-008 + RB-008 — Unusual resource creation (new region/account)
- [ ] DET-009 + RB-009 — Unusual data access spike
- [ ] DET-010 + RB-010 — Suspicious OAuth application consent/app registration (conceptual)

## Detection ↔ Runbook index (initial)
| ID | Detection | Runbook |
|---:|---|---|
| 001 | Suspicious sign-in (new device/location) | [RB-001 Suspicious sign-in](runbooks/RB-001-suspicious-signin.md) |

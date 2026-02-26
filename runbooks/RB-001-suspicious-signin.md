# RB-001 — Suspicious sign-in (new device or new location)

## Trigger
- Alert: DET-001 — Suspicious sign-in (new device or new location)

## What this might indicate
- Credential theft leading to account takeover
- Stolen session token or user signed in from an attacker-controlled device

## Validate (5–15 minutes)
- Confirm sign-in details: user, timestamp, location, device identifier
- Look for failed sign-ins preceding the success
- Check whether the account is privileged

## Scope
- Identify additional suspicious activity:
  - new mailbox rules / forwarding (if applicable)
  - privilege changes
  - unusual cloud resource access
- Look back 24–72 hours depending on environment

## Contain
- If high confidence or privileged account:
  - force password reset
  - revoke sessions/tokens
  - require Multi-Factor Authentication (MFA) (Multi-Factor Authentication) re-registration if policy allows
  - temporarily block risky sign-in locations

## Recover
- Confirm user can regain access safely
- Validate no admin roles or permissions were added
- Validate no logging/telemetry was disabled

## Prevent recurrence
- Tighten conditional access policies (risk-based sign-in)
- Add detection for repeated failures followed by success
- Improve user reporting workflow for phishing/social-engineering

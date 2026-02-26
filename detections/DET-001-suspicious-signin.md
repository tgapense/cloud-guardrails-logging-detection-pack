# DET-001 — Suspicious sign-in (new device or new location)

## Summary
Detects a successful sign-in from a new device or unusual location that may indicate credential theft and account takeover.

## Threat / Attack path
phishing/social-engineering → credential theft → account takeover → cloud access

## Required data sources
- Authentication/sign-in logs (success and failure)
- Device fingerprinting / device identifiers (if available)
- Geo-location or network location metadata

## Detection logic (conceptual)
- Successful sign-in where:
  - device is new for the user OR
  - location is new/unusual for the user
- Optional: prioritize if preceded by multiple failed sign-ins in a short window

## Severity and priority
- Medium (High if privileged account)

## Likely false positives
- Legit travel
- New phone/laptop
- Virtual private network (VPN) usage
- Cellular carrier location shifts

## Validation steps
- Confirm user and timestamp
- Check if user recently enrolled a new device
- Check for failed sign-ins before the success
- Check for concurrent sessions from different locations

# Monitoring Checklist

## What to collect
- Firewall allow/deny logs
- VPN authentication logs
- DNS logs
- Proxy logs (URL + direct-to-IP)
- Windows security events (auth, account changes)
- Sysmon (process + network connections) where appropriate

## Alerts to implement
- Excessive failed logins (per user/per IP)
- Privileged account login anomalies
- New scheduled tasks / persistence indicators
- Direct-to-IP outbound web requests
- Unusual DNS (new domains, high entropy)

## Operational notes
- Define retention targets
- Define escalation paths
- Document false-positive tuning

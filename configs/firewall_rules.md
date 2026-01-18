# Example Firewall Rules (High-Level)

## Inbound (Internet → DMZ)
- Allow 443 to WAF/Reverse Proxy
- Allow VPN ports to VPN gateway
- Deny all else

## East-West (Inter-VLAN)
- User VLAN → App Server VLAN: allow 443 only
- App Server VLAN → DB VLAN: allow 5432 (or DB port) only
- User VLAN → DB VLAN: deny
- Mgmt VLAN → all: allow admin protocols to specific hosts only (SSH/RDP/WinRM as needed)
- All zones → SIEM: allow logging ports (syslog/agent)

## Outbound (Internal → Internet)
- Allow required update repositories
- Block direct-to-IP browsing (optional policy)
- Log DNS and proxy activity for detection

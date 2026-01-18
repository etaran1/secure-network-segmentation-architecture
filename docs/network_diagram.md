# Network Diagram (Mermaid)

Paste this into any Mermaid viewer (or GitHub renders Mermaid in many contexts).

```mermaid
flowchart LR
  Internet((Internet)) --> FW[Firewall]
  FW --> DMZ[DMZ Zone]
  FW --> User[User VLAN]
  FW --> Server[Server VLAN]
  FW --> Mgmt[Management VLAN]

  DMZ --> WAF[Reverse Proxy / WAF]
  DMZ --> VPN[VPN Gateway]

  User --> WS[Workstations]
  Server --> APP[App Server]
  Server --> DB[(Database)]

  Mgmt --> SIEM[Logging/SIEM]
  Mgmt --> ADM[Admin Jumpbox]

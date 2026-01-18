# Segmentation Rationale

## Zones
- **DMZ**: public-facing services only (reverse proxy, VPN)
- **User VLAN**: user endpoints; no direct access to DB
- **Server VLAN**: application and database services
- **Management VLAN**: admin-only (jumpbox, SIEM, management)

## Key Principles
- Default deny between VLANs
- Allow only required ports/protocols
- Admin access only via jumpbox
- Central logging from all zones to SIEM

## Why this reduces risk
- Limits lateral movement
- Restricts credential theft blast radius
- Improves monitoring visibility and containment

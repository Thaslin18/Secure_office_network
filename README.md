# Secure Office Network Design

## Project status
**Design/documentation prepared.** The Packet Tracer `.pkt` file and implementation/test screenshots are to be added after you build and validate the topology in Cisco Packet Tracer. Do not describe untested configurations as completed.

## Overview
A small-office network design separating HR, IT, Sales, and shared servers using VLANs. The design includes a router for inter-VLAN routing, a managed switch, IP addressing, and proposed access-control/security measures.

## Objectives
- Segment departments with VLANs.
- Plan an IPv4 addressing scheme.
- Provide inter-VLAN routing through a router.
- Define security and management recommendations.
- Document validation checks.

## Planned topology
- 1 Cisco 2911 router
- 1 Cisco 2960 switch
- 9 PCs (3 per department)
- 1 server
- VLANs: HR (10), IT (20), Sales (30), Servers (40)

See `Diagrams/Network_Topology.png`.

## VLAN / IP plan
| VLAN | Department | Network | Gateway |
|---|---|---|---|
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | IT | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Sales | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Servers | 192.168.40.0/24 | 192.168.40.1 |

## Security design recommendations
- Restrict server access with ACLs according to business needs.
- Enable switch port security on appropriate access ports.
- Administratively shut down unused switch ports.
- Use SSH rather than Telnet for device administration.
- Limit management access to the IT VLAN.
- Keep configuration backups and use strong unique credentials.

## Validation checklist
When you implement this in Packet Tracer, record the results:
- [ ] End devices have correct IP address, mask, and gateway.
- [ ] Each department is connected to its assigned VLAN.
- [ ] Switch VLAN and trunk configuration is correct.
- [ ] Each PC can ping its own default gateway.
- [ ] Intended inter-VLAN access works.
- [ ] Restricted access is blocked by the configured policy.
- [ ] Server reachability matches the intended policy.
- [ ] Port-security settings are verified.
- [ ] Save the `.pkt` file and add screenshots to `Screenshots/`.

## Repository contents
- `Diagrams/Network_Topology.png`: planned topology illustration.
- `Documentation/Project_Documentation.pdf`: design report and implementation checklist.
- `Configs/Implementation_Notes.txt`: implementation notes and commands/checks to consult.
- `Screenshots/`: add your own Packet Tracer screenshots after implementation.
- `Secure_Office_Network.pkt`: **not included yet**; add your saved Packet Tracer project here.

## Honest portfolio description
“Designed a segmented small-office network plan in Cisco Packet Tracer with departmental VLANs, an IPv4 addressing scheme, inter-VLAN routing, and proposed access-control and switch-security measures. Implementation and connectivity validation are documented separately once completed.”

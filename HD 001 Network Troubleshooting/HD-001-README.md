# HD-001 — Website Connectivity Troubleshooting

**Project type:** Windows 11 help desk lab and simulated incident  
**Technician:** Juanmanuel Flores Castellanos  
**Status:** Completed training scenario; evidence screenshots captured by technician  

## Objective

Practice a Tier 1 service desk investigation of a company portal that times out in Microsoft Edge, including symptom gathering, scope isolation, browser comparison, safe corrective action, and user verification.

## What was performed on a real Windows 11 computer

The following checks were executed on a functioning personal Windows 11 computer and their results were reported as successful:

| Diagnostic | Tool/command | Observed result |
| --- | --- | --- |
| Local network configuration | `ipconfig /all` | Private IPv4 address |
| Local TCP/IP stack | `ping 127.0.0.1` | Replies received |
| External IP reachability | `ping 1.1.1.1` | Replies received |
| DNS resolution | `nslookup example.com` | Successful response |
| Browser page loading | Microsoft Edge / `https://example.com` | Page loaded |
| HTTPS TCP connectivity | `Test-NetConnection example.com -Port 443` | `TcpTestSucceeded : True` |

These baseline results **do not prove a fault existed or was fixed** on the personal computer.

## Simulated service desk incident

A fictional employee, Sarah Mitchell, reported `ERR_CONNECTION_TIMED_OUT` for a company portal in normal Microsoft Edge. Other sites worked. A coworker and phone could access the portal; Chrome and Edge InPrivate also worked on the affected workstation. In the simulation, disabling a recently installed tab-organizer extension restored the portal in Edge.

**Suspected cause:** browser-extension interference in the normal Edge profile. This was a simulated conclusion, not an experimentally reproduced failure on the personal computer.

## Skills practiced

- Network and DNS baseline diagnostics
- Incident scope and impact assessment
- Browser/profile fault isolation
- Low-risk, reversible troubleshooting
- User communication and resolution verification
- ITIL-aligned incident notes

## Portfolio contents

1. [Back to Main Portfolio](../README.md) — Return to the main IT Support Portfolio
2. [Incident Report](HD-001-Incident-Report.md) — Detailed support ticket, investigation, and resolution
3. [Screenshot Guide](HD-001-Screenshot-Guide.md) — Diagnostic evidence and screenshot documentation


## Evidence files

Place these four images in `Evidence/` alongside the Markdown documents:

- `01-ipconfig-redacted.png` — Windows network configuration
- `02-04-network-tests-redacted.png` — loopback ping, external ping, and DNS lookup together
- `05-https-port-redacted.png` — TCP port 443 connectivity
- `06-browser-example.png` — successful page load in Edge

The incident report embeds all four images using relative paths. Confirm their spelling matches exactly (including capitalization) before publishing. Never publish passwords, account identifiers, personal IPv6 addresses, MAC addresses, machine names, or other identifying network information. Edited/redacted images should not be presented as untouched originals.

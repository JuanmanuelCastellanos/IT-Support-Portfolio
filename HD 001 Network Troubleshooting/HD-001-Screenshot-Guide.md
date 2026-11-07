# HD-001 — Screenshot Capture Guide

This file is the third portfolio document. It documents the screenshot inventory and safe publication requirements. The technician has reported capturing all required screenshots. Keep the real diagnostic tests distinct from the fictional help desk scenario.

## Set up your local folder

Create the folder `Documents\IT-Support-Portfolio\HD-001-Network-Troubleshooting\Evidence` and place these three `.md` files one level above it. You can open `.md` files with Notepad or VS Code.

## Capture procedure

1. Open **Windows Terminal**, **PowerShell**, or **Command Prompt**.
2. Run one command from the table below.
3. Press **Win + Shift + S**, select the relevant output, then save the capture with the specified filename in `Evidence`.
4. Review the screenshot and **redact** sensitive values before sharing or uploading. Prefer a cropped capture showing command and result only.
5. For screenshots intended for a public portfolio, hide local/public IP addresses where not needed, hostnames, DNS suffixes, usernames, MAC addresses, Wi-Fi identifiers, and unrelated windows/notifications. Keep the result labels visible.

| Filename | What to show | Command / action | Expected evidence (not guaranteed) |
| --- | --- | --- | --- |
| `01-ipconfig-redacted.png` | Relevant adapter with private IPv4 and headings; sensitive values hidden | `ipconfig /all` | Adapter and address configuration |
| `02-04-network-tests-redacted.png` | Three commands together | `ping 127.0.0.1`, `ping 1.1.1.1`, `nslookup example.com` | Loopback replies, external replies, DNS answer |
| `05-https-port-redacted.png` | Target, port, and `TcpTestSucceeded` field | PowerShell: `Test-NetConnection example.com -Port 443` | TCP test result |
| `06-browser-example.png` | Address bar and loaded `example.com` page | Open `https://example.com` in Edge | Loaded test website |

## Important distinctions

- These are **normal-connectivity baseline tests**, not screenshots of the fictional portal failure.
- Do not fabricate an `ERR_CONNECTION_TIMED_OUT` screenshot or impersonate a real employee.
- Do not intentionally disable networking or change system DNS to manufacture errors on a machine you rely on.
- If a test gives a different result today, record that genuine result and its date; don't edit it to match earlier self-reported results.

## Ready-to-publish checklist

- [ ] All four evidence image files present (covering six tests)
- [ ] Sensitive information removed or obscured
- [ ] Screenshot text is readable at normal viewing size
- [ ] Incident report links point to the actual files
- [ ] README clearly labels the role-play as simulated
- [ ] No passwords, identifying account information, or employer data included

### Suggested screenshot captions

1. *Windows IP configuration inspected to identify the active adapter and private address.*
2. *Loopback ping, external IP ping, and DNS query confirmed baseline network functionality.*
3. *TCP connection to the test host on port 443 succeeded.*
4. *Microsoft Edge successfully loaded the public test page.*

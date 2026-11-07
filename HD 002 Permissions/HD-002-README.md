# HD-002 — Windows 11 User Account and NTFS Permissions Troubleshooting

**Technician:** Juanmanuel Flores Castellanos  
**Type:** Fictional help desk incident + real Windows 11 lab  
**Status:** Completed simulation and hands-on exercise

## Objective

Practice investigating a Windows folder-access complaint using careful questioning, NTFS permission inspection, Effective Access, authorization, least privilege, and user verification. Demonstrate the underlying concepts safely on a separate practice folder.

## Two distinct parts of this project

1. **Simulated support ticket:** Michael Thompson, a fictional Accounting employee, lost access to a local reports folder. The role-play followed diagnosis, approval, group-based permission restoration, and user acceptance testing. No real company system or employee was involved.
2. **Real Windows 11 lab:** On my personal computer, I inspected folder permissions and inheritance, checked Effective Access, converted inherited entries to explicit permissions on a disposable test folder, verified file writes, restored inheritance, removed duplicate explicit entries, and verified file writes again.

The lab did **not** reproduce Michael's access-denied condition. The simulated resolution should not be described as a real incident or real administrator action.

## Skills demonstrated

- NTFS access control entries and permission inheritance
- Effective Access evaluation for a Windows account
- Difference between explicit and inherited permissions
- Controlled and reversible permission changes on a practice folder
- File read/write verification before and after restoration
- Least privilege, authorization, and help desk documentation

## Project documents

- [Incident report — fictional scenario](HD-002-Incident-Report.md)
- [Hands-on lab report — actual Windows 11 exercise](HD-002-Lab-Report.md)

## Evidence

1. [Inherited NTFS permissions](Evidence/01-ntfs-inheritance-redacted.png)
2. [Effective Access results](Evidence/02-effective-access-redacted.png)
3. [Explicit permissions after inheritance was disabled](Evidence/03-explicit-permissions-redacted.png)

**Evidence integrity:** Screenshot contents were redacted for privacy. Some edited copies were reconstructed by an image-editing tool and therefore are not pixel-identical to the captures. Unedited originals should remain private. The narrative distinguishes personally performed lab steps from the fictional ticket.

## Outcome

The lab folder was returned to inheritance-enabled configuration. The selected Windows account retained Full Control; the test document could still be opened, edited, saved, and reopened. No changes to real business data or other users' access were performed.

[Back to main portfolio](../README.md)

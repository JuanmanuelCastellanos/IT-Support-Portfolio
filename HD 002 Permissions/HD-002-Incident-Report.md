# HD-002 — Accounting Reports Folder Access Denied

**Incident type:** Fictional Tier 1 service desk role-play  
**Technician:** Juanmanuel Flores Castellanos  
**Employee:** Michael Thompson (fictional), Accounting  
**Category:** Windows / NTFS file permissions  
**Priority:** Not formally established in simulation  
**Final simulated status:** Resolved; employee verified functionality

## Reported issue

Michael reported that Windows 11 displayed a message indicating he did not have permission to open the local `Accounting Reports` folder under Documents. He had accessed the folder the preceding day and needed the files for accounting work.

## Investigation timeline

| Stage | Action | Simulated finding | Interpretation |
| --- | --- | --- | --- |
| 1 | Ask for exact message and affected folder | Windows permissions warning on a local Documents folder | Focus on folder-level access |
| 2 | Confirm account and recent changes | Michael used his normal account; a coworker reorganized files the previous day | Recent file movement may be relevant |
| 3 | Inspect folder Properties → Security | SYSTEM, Administrators, and Jessica.W listed; Michael not individually shown | Individual absence alone does not establish no access |
| 4 | Evaluate Michael.T in Advanced → Effective Access | No Read or Modify permission shown; inheritance disabled | Insufficient effective NTFS access indicated |
| 5 | Obtain authorization | Accounting Manager Jennifer Adams confirmed business need to read/update reports | Approval required before access change |
| 6 | Implement approved group permissions | IT administrator added Modify for existing `Accounting-Reports-Editors` group; Michael already a member | Group-based least-privilege approach; existing entries retained |
| 7 | Verify with employee | Folder opened; report read; authorized test document edited, saved, reopened | Business functionality restored in simulation |

## Final resolution note

**Issue:** The employee reported being unable to access the Accounting Reports folder, which had been accessible the previous day. Windows displayed a permission warning when the user attempted to open the folder.

**Investigation:** Verified the usual Windows account was in use. Inspection of NTFS permissions and Effective Access indicated the account lacked the necessary access. The folder's inheritance was disabled, and a recent folder reorganization was a possible contributing event.

**Resolution:** The Accounting Manager authorized restoration of the employee's required access. The authorized IT administrator assigned Modify permissions to the established `Accounting-Reports-Editors` group, of which the employee was already a member. Existing permission entries were preserved pending separate review.

**Verification:** Michael successfully opened the folder, read an existing report, edited and saved an authorized test document, and reopened it to confirm the edit persisted. He confirmed normal functionality.

**Status:** Resolved in simulation.

## Technical caveats and follow-up

- The precise mechanism that caused the original simulated permissions change was **not proven**. A same-volume move generally preserves NTFS permissions; a move across volumes may produce different inheritance behavior.
- Modify normally includes delete capabilities. In a real organization, the approved access model and business requirements must be verified.
- Jessica.W's pre-existing Full Control entry remains a separate access-review item; it should not be removed without authorization.
- Permission changes and approval would be recorded using the organization's ticketing and audit workflow.

## Integrity statement

Michael, Jennifer, Jessica, the accounting folder incident, manager approval, administrator action, and resolution outcomes are fictional. The [separate Windows 11 lab](HD-002-Lab-Report.md) was performed on a disposable personal practice folder and is not evidence that a company incident occurred.

[Project overview](HD-002-README.md)

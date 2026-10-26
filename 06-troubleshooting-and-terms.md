# 6. Troubleshooting and plain-language terms

[← Handbook](README.md)

For the meaning, likely cause, step-by-step fix, and HR/Admin action for each common error, use [Common Errors & Solutions](08-common-errors-and-solutions.md).

## Quick problem guide

| What happened | Check | What to do |
| --- | --- | --- |
| Cannot sign in | Correct portal and identifier: Admin username, Employee Code/username for Field, Client Code/username for Client; password and account status. | Stop repeated guesses. Ask the appropriate administrator to check or reset the account privately. |
| No company assigned after login | Staff company grants. | Ask a Super Administrator to grant the correct company. Do not create another user. |
| A menu or button is missing | Role, feature permission, selected company and site grants. | Request only the permission and scope required for the job. |
| Client, site or employee not visible | Selected company, search, and site grant. | Switch to the authorized company and refresh. Do not use someone else's login. |
| Employee has no duty | Linked active profile; **Assignments** site, common shift and working days; site policy. | HR fixes the assignment; employee taps **Refresh**. Routine duties do not need roster publication. |
| Employee sees the wrong site/shift | Current assignment, pending transfer and local work date. | HR checks **Assignments** history and corrects it with **Transfer / change shift**. Do not edit old attendance. |
| Transfer pending | Employee still has an open punch at the original site. | Employee completes punch-out there, or an authorized reviewer resolves the session. Destination is not punchable yet. |
| Transfer blocked | Destination/site/grants changed while a transfer waited. | HR reviews the error/audit trail and submits a valid new transfer. |
| “Punch in opens at …” | Server-provided punch window. | Wait until the displayed time; changing the phone clock will not help. |
| “This shift can no longer be punched” | Duty date and closed window, especially for overnight work. | Contact the supervisor; do not punch an older duty. |
| GPS accuracy too low | The phone's uncertainty exceeds site policy. | Move safely to an open area **within the site** and request a fresh fix. |
| Outside geofence near the edge | Site pin/radius and distance **plus GPS accuracy**. | Move farther inside. If setup is wrong, HR reviews a new policy version and tests it on site. |
| Map or search unavailable | Internet and map service. | Admin may enter **verified** coordinates manually. The map is guidance; a fresh GPS fix is still needed to punch. |
| Punch saved but not confirmed | **Punches** shows waiting, checking, review or rejection. | Reconnect, sync/check the existing result, then contact a supervisor if needed. Do not keep sending new punches. |
| “Use this phone for attendance” | Another phone is currently selected. | Sync old-phone evidence if possible, then switch explicitly on this phone. Server history remains readable. |
| “This browser was used for attendance before” | Its saved browser ID was registered earlier, possibly for a different employee or an earlier phone enrollment. | Do not clear unsynced punches. Use a separate persistent browser profile or phone; ask HR if this is your normal device. See the [phone-registration guide](08-common-errors-and-solutions.md#this-browser-was-used-for-attendance-before). |
| Phone-change limit reached | Employee's used count and App Configuration policy. | HR/Super Admin reviews the case and may reset usage with a reason. Do not create a duplicate account. |
| Document upload fails | Correct type, JPG/PNG/PDF format, 5 MB limit, online connection and permission. | Preview a valid file and retry. A passport photo must be JPG/PNG. |
| Document Delete disabled | **Document → Delete** permission. | Ask a Super Administrator to review the permission; do not borrow another person's account. |
| “Code already exists” | Group-wide client or employee code already in use. | Find the correct existing record or choose a genuinely new approved code. |
| Leave menu missing | Employee's **Leave applicable** flag, linked login and current company. | Ask HR to review eligibility; do not use another employee's account. |
| Leave approval blocked | Applied approved policy, correct assignment/calendar, opened CL/SL/PL balance and conflicting attendance. | HR checks the request details and fixes the source issue before deciding. A submitted request has not deducted a balance. |
| Late punch shows half-day | Company late rule requires HR approval and the arrival is pending or rejected. | Keep the original punch; HR reviews **Attendance review → Late arrivals**. Worked hours do not change. |
| Muster has `?` or cannot finalize | A duty or leave/day decision needs review, or the selected period has not ended. | HR resolves the source day, previews again, and finalizes only after all days are clear. See [Attendance reports](10-attendance-reports.md). |

Admin form errors appear near the field and in an alert. When asking for help, give the page, company, site, employee/shift reference, time and exact message. Never send passwords, full ID/account numbers or unnecessary personal screenshots.

## What Client Portal users can do today

Sign in with the **Client Code or username** and password for the account linked to your organization. On **Site worked hours**, choose a **Work month** and press **Show**. You will see read-only completed time for the non-deleted sites belonging to **your client**, including sites added later. An authorized supervisor exception may be included and is labelled. Open attendance, pending offline punches and payroll rules are excluded. This is **not an invoice or salary calculation**. Client exports/downloads, exact employee locations and full reporting are not live in this portal.

If a site is missing, contact your Hitech Group administrator. Do not ask for another client's account or a broader company view.

## Terms used in the HRMS

| Term | Plain meaning |
| --- | --- |
| Company | One Hitech Group employer. Each client, site, current employee profile and new duty belongs to a company. |
| Company grant | Permission for a non-Super staff account to work in a particular company. A feature permission and site grant can restrict it further. |
| Client | Customer organization receiving services from one company; its linked portal account sees that client's sites. |
| Site / post | Customer location / particular staffed point such as Main Gate. |
| Common shift | Group-wide reusable start time, duration and arrival/departure grace. It is not a site assignment. |
| Shift version | A new definition saved after a common shift edit. Earlier attendance keeps its original time snapshot. |
| Assignment | Employee's current site, optional post, common shift and working weekdays, with an effective start/end. Only one primary assignment is active. |
| Transfer | Audited change of assignment, possibly to another site, client or company. A transfer waits if the employee is punched in. |
| Dated duty / work date | One planned occurrence created from an assignment. An overnight duty uses the local date when it **starts**. |
| Geofence policy | Site duty-point center, circular radius and GPS limits used to check a punch. A new policy version takes effect immediately. |
| GPS accuracy | Phone-reported uncertainty in metres. Lower is more precise; it is not proof of physical presence. |
| Attendance session | Server record opened by accepted punch-in and closed by accepted punch-out or an authorized exception. |
| Worked hours | Elapsed accepted punch-in to punch-out time for a completed session. Breaks and payroll rules are not applied. |
| Leave opening balance | HR's first recorded CL, SL or PL balance for an employee and leave year. Policy entitlement alone does not credit it. |
| Leave approval | HR decision that deducts charged working days after policy, attendance and balance checks. A pending request does not deduct days. |
| Attendance day code | HR-reviewed classification such as `P`, `HD`, `WO`, `H`, `AB`, `CO`, `CL`, `SL` or `PL`. It is not a paid-day or wage rule. |
| Muster report version | Saved company/site-period attendance snapshot. If source records change, HR reopens and creates a new version; old downloads remain as saved. |
| Provisional/offline punch | Phone-saved evidence that needs sync and possibly review. It is **not** confirmed attendance. |
| Exception punch-out | Audited close of an open session at the verified actual departure time, without on-site punch-out GPS evidence. |
| Document received / staff-reviewed | File uploaded / inspected by staff. Neither means KYC-provider or government identity verification. |
| Site grant | Limits a Field Officer to specified operational sites. Client access instead comes from the account linked to the client. |
| Soft delete | Removes normal access to a record but keeps required audit history. For employee documents, the private stored file is also removed when deletion succeeds. |
| Handover | Incoming guard takes over from outgoing guard. The dedicated two-person workflow is **not implemented**. |

## Support handoff

Supply the **portal and page**, **selected company**, **site and post**, **local work date and shift time**, **username or employee code**, **exact on-screen error**, and whether the phone was online. For an uncertain punch, include the event reference from **Details for supervisor** if shown. Share sensitive evidence only through approved Hitech Group channels; never include a password or one-time password.

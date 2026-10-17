# 6. Troubleshooting, common mistakes, and terms

[← Handbook](README.md)

## Quick problem guide

| Problem | Check first | Safe next action |
| --- | --- | --- |
| User cannot sign in | Correct portal and username; account status; temporary password. | Stop repeated guesses. Ask Super Administrator to check account or reset password privately. |
| Menu item missing | Assigned role and feature action permission. | Ask for the minimum required permission; a site grant alone does not add a menu action. |
| Site/employee not visible | Site access scope or search/filter; employee's current assignment. | Verify the grant on **Site access** and reload; do not use another user's account. |
| Employee has no duty | Linked active employee profile, site/post assignment, geofence policy, generated **and published** shift. | Planner corrects the missing step; employee taps **Refresh**. |
| Coverage gap prevents publish | Required headcount, weekdays, effective dates, position numbers, and eligible employees. | Add/fix a recurring pattern, generate/reload, then publish only after gap review. |
| “Punch in opens at …” | Shift time and server-provided opening time. | Wait; no GPS request should be needed until punching is allowed. |
| “This shift can no longer be punched” | Past/closed window; correct duty date, especially overnight. | Contact supervisor. Do not change phone time or choose an old shift. |
| GPS accuracy too low | Phone reports more uncertainty than the site policy allows. | Move safely within the site to an open area, wait, and request a fresh reading. |
| Outside geofence near the edge | Policy pin/radius and the phone's distance **plus accuracy**. | Move farther inside; if site setup is wrong, HR must create a reviewed new policy version. |
| Map or search unavailable | Internet and Google key/service configuration. | Admin may enter verified coordinates manually; employee can still read duty/punch if location service works. A map is optional guidance. |
| Punch saved but not confirmed | Offline/uncertain/waiting status in **Punches**. | Reconnect, sync/check result, and escalate if unresolved. Do not submit repeated new punches. |
| “Use this phone for attendance” | A different phone is currently selected for punches. | First sync saved punches on the old phone if available, then switch explicitly on the new phone. Server history remains readable. |
| “Phone-change limit reached” | The employee's used count reached the configured limit. | HR/Super Admin reviews the case and can reset the count with a mandatory reason. Do not create a duplicate employee account. |
| “Code already exists” | Existing or archived client/site/post/employee code. | Use the correct existing record or a new approved code; do not append random characters to hide a duplicate. |
| A change is blocked by published shifts | Future roster depends on the employee/site/post/assignment. | Revise/cancel affected shifts with a reason first, then repeat the change. |

Errors in admin forms appear near the field and in the alert; read both. For a persistent failure, give support the page name, site/shift, time, and displayed message. Do not send passwords, full employee exports, or screenshots containing unnecessary personal information.

## What client users can use today

The dedicated Client Portal accepts the linked Client Code (or username) and password. Its current dashboard shows read-only completed worked-hour totals for all non-deleted sites belonging to the mapped client, including later sites. Choose a work month and press **Show**. Open shifts and pending offline punches are not included; the totals are not payroll calculations. Client download/export, a precise employee-location map, and full self-service reporting are still pending. Do not promise those features until delivered and approved.

## Terms used in the HRMS

| Term | Plain meaning |
| --- | --- |
| Client | Customer organization receiving HHCIL services. |
| Site | Customer location where employees are deployed. |
| Security post | Specific staffed point at a site, e.g. Main Gate. |
| Geofence center / radius | Verified duty point and circular boundary, in metres, used for GPS punch checks. |
| GPS accuracy | Phone's reported uncertainty radius. Lower numbers mean a more precise reading. |
| Tracking policy version | Site's effective boundary and GPS settings. A new version takes effect immediately; prior versions remain in history. Current web release does not perform background tracking. |
| Portal user | Login account, roles, status, password, and permissions. |
| Employee profile | HR record with employee code, name, category, joining date, and optional user link. |
| Site assignment | Employee's current primary site/post and effective dates; separate from a roster. |
| Shift template | Reusable site-local start time, duration, and grace settings. |
| Coverage requirement | Number of staff required for a post/template on chosen weekdays and dates. |
| Roster pattern | Recurring assignment of one eligible employee to a numbered required position. |
| Generated shift / draft | Dated duty produced from the rules, not yet visible as a punchable published duty. |
| Published/scheduled shift | Duty approved for the selected date range and shown to the employee. Still not proof of attendance. |
| Attendance session | Server record opened by accepted punch-in and closed by accepted punch-out or authorized exception. |
| Provisional/offline punch | Saved location/time evidence that needs sync and possibly an explicit review; not confirmed attendance. |
| Supervisor exception | Audited manual close of an active attendance session; not a GPS-verified punch-out or handover. |
| Handover | Incoming guard accepts responsibility from outgoing guard. The dedicated two-person workflow is **not implemented yet**. |
| Site grant | Restricts a Field Officer to specified operational sites. A Client User instead sees every non-deleted site of its mapped client; feature permission is also required. |
| Role / override | Default action rights for a group / an explicit individual allow or deny with reason. |
| Soft delete | Hides or deactivates a record without erasing the audit history; codes may remain reserved. |

## Support handoff template

When escalating, supply: **portal and page**, **site and post**, **local work date/shift time**, **your username or employee code**, **exact on-screen error**, and whether the phone was online. For an uncertain punch, include the **event reference** from “Details for supervisor,” if shown. Share GPS/sensitive screenshots only through HHCIL-approved channels. Never include a password or one-time password.

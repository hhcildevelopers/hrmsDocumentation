# HHCIL HRMS — user handbook

This handbook explains the features **available in the current application**, using the labels you see on screen. It is for Super Administrators, HR Administrators, roster planners, attendance reviewers, field officers, and employees. Your menu may show fewer items because access depends on both your permissions and the sites assigned to you.

> All names, dates, addresses, account names, and coordinates in this handbook are **fictional training examples**. Never copy the sample coordinates or a map search result into a live attendance policy without confirming the actual duty gate/post on site.

## Start with your role

| If you are… | Read first | Main job today |
| --- | --- | --- |
| Super Administrator | [Sign-in and access](01-sign-in-and-access.md), then [setup](02-clients-sites-employees.md) | Create accounts and roles; supervise setup and access. |
| HR Administrator / authorized planner | [Setup](02-clients-sites-employees.md), then [shift scheduling](03-shift-scheduling.md) | Maintain clients, sites, employees, assignments, and published rosters. |
| Attendance reviewer / authorized supervisor | [Attendance review](05-attendance-review.md) | Review site attendance and decide provisional offline punches. |
| Employee or field officer using field attendance | [Field portal](04-employee-field-portal.md) | See published duty, check location, punch, and check the result. |
| Field officer with an operations site grant | [Site access](02-clients-sites-employees.md#site-access-for-field-officers-and-client-users), [shift scheduling](03-shift-scheduling.md), [attendance review](05-attendance-review.md) | View only granted sites; approval actions require an additional permission. |
| Client user | [Current client-user access](06-troubleshooting-and-terms.md#what-client-users-can-use-today) | Confirm what is available now; do not rely on the demo client portal for reports. |

For an error or unfamiliar term, see [Troubleshooting and terms](06-troubleshooting-and-terms.md).

## Correct setup order

1. Super Administrator creates a portal user and assigns the right active role. Give the temporary password privately; the user must change it at first sign-in.
2. HR creates a **client**, then a **site** under that client and at least one **security post**.
3. HR confirms the site's real duty point and creates a **geofence/tracking policy version**. A site postal address and a geofence center are different records.
4. HR creates an **employee profile**, optionally links an already-created Employee/Field Officer portal account, and assigns the employee to the site/post.
5. Planner creates **shift templates**, **post coverage requirements**, and **recurring roster patterns**; generates shifts, fixes gaps, then **publishes** the date range.
6. Employee opens the field portal, checks today's published duty, punches with a fresh phone location at the site, and checks **Punches** for the decision.
7. Authorized reviewer checks **Attendance review** for provisional offline punches or an exceptional punch-out.

A user account, employee profile, site assignment, and published shift are **four separate things**. Completing just one does not create the others.

## Current boundaries

- The employee field portal is a mobile-friendly **web app**. Android/iOS native packaging and background tracking are later work.
- **Check my location** and punching use a foreground GPS sample. The current app does **not** continuously monitor the employee, detect geofence exits during duty, send live-location alerts, or prove that a security post stayed occupied.
- A published shift is a plan; a confirmed punch is attendance evidence; neither is a completed two-person handover. Automated no-show/early-departure alerts and handover are not yet available.
- Offline punches are provisional until the server accepts a retry or an authorized reviewer approves them. A saved-on-phone message is **not** attendance confirmation.
- The dedicated client-web portal currently has a demo login and backend-health dashboard only. Do not promise client downloads, reports, or self-service from that screen yet. Client-scoped read permissions exist in the backend and permissioned administration views, subject to deployment policy.
- This handbook does not document payroll, payslips, leave, documents, or other planned modules as live features.

## Before a real-site pilot

Have an HHCIL owner approve the site address, duty-point pin, radius and accuracy, site timezone, shift rules, roster approver, employee notice, and offline-review procedure. Test punch-in/out with a real phone at the actual gate or post. A map preview, desktop location, or training example is not enough.

**Handbook version:** current repository features through Phase 3 geofenced attendance and the admin Google geofence picker (12 October 2026). HHCIL should review role names, support contacts, Hindi wording, and pilot policy values before publishing this handbook to end users.

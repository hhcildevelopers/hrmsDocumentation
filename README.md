# Hitech Group HRMS — user handbook

This handbook explains what the HRMS currently does, in everyday language. It is for Super Administrators, HR Administrators, Field Officers, employees, attendance reviewers, and Client Portal users. Screens and buttons depend on your access; if you cannot see an action, ask your administrator rather than using someone else's account.

> All people, dates, codes, addresses, and coordinates below are **training examples**. Confirm real employee and site details before saving them.

## Find your guide

| Your work | Read |
| --- | --- |
| Sign in, select a company, manage users or roles | [Sign-in and access](01-sign-in-and-access.md) |
| Create clients, sites, geofences or employees | [Clients, sites and employees](02-clients-sites-employees.md) |
| Set a common shift, assign duty or transfer an employee | [Common shifts and assignments](03-shift-scheduling.md) |
| Punch on a phone or work as a Field Officer | [Field Portal](04-employee-field-portal.md) |
| Review punches, working hours or exceptions | [Attendance review](05-attendance-review.md) |
| Fix a problem or understand a term | [Troubleshooting and terms](06-troubleshooting-and-terms.md) |
| Enter private profile/bank details or handle documents | [Employee records and documents](07-employee-records-and-documents.md) |
| Understand an error and follow recovery steps | [Common Errors & Solutions](08-common-errors-and-solutions.md) |
| Configure a draft leave policy, holidays, and eligibility | [Leave setup (C1 preview)](09-leave-setup.md) |
| Preview and download attendance muster reports | [Attendance reports (C4 development)](10-attendance-reports.md) |

## Normal setup and attendance flow

1. A Super Administrator grants central staff access to the right **company** and gives them only the permissions they need. A Field Officer also needs an operations grant for the site where they will register employees.
2. In the selected company, HR creates the client and site, adds a post if needed, and confirms the site's GPS duty point and geofence. A client's site belongs to that one company.
3. HR or an authorized Field Officer registers the employee with an Auto or Manual Employee Code, active Department/Designation/Employment Type, the site, common shift and working weekdays. This creates the employee, first duty assignment and Employee-only login together. Share the one-time password privately. Older saved employees can still use the separate account-link action.
4. An authorized administrator uses **Common → Shifts** and the other Common masters for group-wide options. The system creates dated duties automatically from each assignment. No routine roster generation or publication is needed.
5. The employee checks the correct duty in the Field Portal and punches with a fresh on-site GPS reading. They check **Punches** for the server result. A Field Officer or HR Administrator can transfer an employee when operational needs change, subject to their grants.
6. An authorized reviewer uses **Attendance review** for offline punches, exceptional punch-outs, and immediate, reasoned attendance corrections. The daily view includes duties with no recorded attendance. Effective in/out time appears as worked hours, with manual time clearly labelled; it is **not** a payroll calculation.

For example, a guard assigned to Site A, the 08:00–20:00 common shift, and Monday–Saturday will see a dated duty on those days. If transferred to Site B and the 20:00–08:00 shift, new duties follow the new assignment. Older attendance stays with Site A. If the guard is already punched in, the transfer waits until the Site A session is closed.

## What is and is not available

- The Admin Portal is company-aware. Super Administrators can work across active companies; other staff need a company grant. The Client Portal belongs to its linked client and shows read-only completed worked-hour totals for that client's sites.
- The Field Portal is a mobile-friendly **web app**, not a native Android/iOS app yet. Location is requested for a check or punch. Continuous background location, geofence-exit alerts, automated no-show alerts, and two-person shift handover are **not live**.
- Offline punches are provisional until the server accepts or an authorized reviewer approves them. A saved-on-phone message is not attendance confirmation.
- Staff-reviewed documents are **not** Aadhaar, PAN, or other provider-verified identity documents. KYC-provider verification, payroll, payslips, and other future HR modules are not described here as live features.
- A common shift is a time pattern; an assignment is where and when a person should work; a dated duty is the particular day's plan; a confirmed punch is attendance evidence. None alone proves the person stayed at the post throughout the shift.

## Before a real-site pilot

Have an Hitech Group owner approve each company's access, employee setup, site address, duty-point pin, radius, GPS accuracy, timezone, shift hours, working days, and offline-review procedure. Test punch-in and punch-out on a real phone at the actual duty point. Do not rely on a map search result or desktop location alone. HHCIL should also review the handbook's role names, support contacts, and Hindi wording before sharing it with end users.

# 3. Common shifts, employee assignments and transfers

[← Handbook](README.md) · [Previous: setup](02-clients-sites-employees.md) · [Next: Field Portal →](04-employee-field-portal.md)

The everyday scheduling flow is now simple: **choose a reusable shift, then assign it to an employee at a site for selected weekdays**. The system creates dated duties automatically. The old site-template, coverage-rule, roster-generation and publication screens are not part of routine scheduling. Historical duties and records remain available for audit.

## Step 1 — Check or add a common shift

Open **Common → Shifts** in the Admin Portal. These shift times are available to every company; they do not belong to a particular client or site. The starting catalog is:

| Start | Duration to enter | Ends |
| --- | ---: | --- |
| 08:00 | 720 minutes | 20:00, same day |
| 20:00 | 720 minutes | 08:00, next day |
| 09:00 | 480 minutes | 17:00, same day |
| 17:00 | 480 minutes | 01:00, next day |
| 01:00 | 480 minutes | 09:00, same day |

If the real shift is 09:00–21:00, **do not choose 09:00–17:00** because the start time looks similar. An authorized administrator should add a separate 720-minute shift. When adding a shift, enter a stable **Code** such as `0900_2100`, a clear **Shift name**, local **Start time** (`HH:mm`), **Duration (minutes)**, and arrival/departure grace in minutes. Duration must be 60–1,440 minutes; each grace value must be 0–180 minutes. A shift time is interpreted in the assigned **site's timezone**.

Super Administrators can edit common shifts. An HR Administrator needs explicit Common Shift create/update permission. Editing an existing shift creates a new version: future unstarted duties can use the new times, while started/completed attendance keeps its saved time snapshot. Check who uses a shift before changing a group-wide rule. An active common shift cannot be deactivated while an active employee is assigned to it.

## Step 2 — Give an employee a first duty

Select the employee's company in Admin, then open **Employees → View → Assignments → Assign duty**. This first assignment requires authorized HR/Super staff. Choose:

| Field | Example | Check before saving |
| --- | --- | --- |
| Client and site | `Example Retail · Ahmedabad West` | This is the actual duty site. The client and company come from the selected site; do not guess them separately. |
| Post | `Main gate guard` | Optional. Choose the exact post if the employee works at one. |
| Common shift | `08:00–20:00` | The correct start and duration, including an overnight end if applicable. |
| Working days | `Mon–Sat` | Tick every day the shift **starts**. Untick a rest day. |

The employee can have only **one active primary assignment**. The assignment records the company, client, site, post, shift and effective time. You do not need to press **Generate** or **Publish** for routine duties. Ask the employee to tap **Refresh** in the Field Portal after saving, and verify their next duty there. Attendance still needs an active employee/account, a valid site geofence, a usable phone location, and a server-accepted punch.

For a night duty starting 20:00 on 12 October and ending 08:00 on 13 October, its **work date is 12 October** in the site's timezone. Select the weekday on which the shift **starts**, even though punch-out is next morning.

## Step 3 — Change a shift or transfer to another site

Open the employee's **Assignments** tab and choose **Transfer / change shift**. Select the destination site, optional post, common shift and working weekdays; enter a meaningful reason of at least 3 characters. One action covers all these examples:

- Same site, different shift: `08:00–20:00` to `20:00–08:00`.
- Same client, another site or post.
- Another client, with its destination site and shift.
- Another Hitech Group company, when staff has the required company/transfer access. Field Officers additionally need both source and destination site grants.

An authorized Field Officer can use **Field Portal → Menu → Transfer employees**. They need access to the **source and destination companies and sites**, plus the transfer permission. They cannot transfer their own linked employee record. Field Officers cannot give a person their first duty; ask HR if the employee has no assignment. Transfers need an internet connection.

If the employee is **not punched in**, the new assignment becomes active when the transfer succeeds. Future unstarted duties are replaced. The old assignment and old attendance remain in history; a cross-company transfer also changes the employee's current company of record.

If the employee **is already punched in at Site A**, the transfer is **pending**. They must finish the existing attendance session at Site A using its rules. Only after a successful Site A punch-out, approved offline punch-out or authorized exception punch-out can Site B become active. A pending transfer does not permit punching at Site B. If the destination can no longer be used, HR must resolve the blocked transfer and submit a new one. For a cross-company move, the employee may need to sign in again after activation.

Example reason: `Client requested night coverage at the west gate from today's next duty.` A reason such as `change` is too vague for later review, even if the form accepts it. Coordinate a mid-shift transfer with the site supervisor; this software does not confirm a physical handover.

## If the employee will stop working at the site

Authorized central staff can choose **End** on the Assignments tab and enter a reason. This ends the current assignment and cancels affected unstarted future duties. It does **not** create a new assignment. If the employee is moving elsewhere, normally use **Transfer / change shift** instead so there is one continuous audit trail. Check any open attendance session first.

## Check the result

After assigning or transferring, inspect the employee's **Assignments** history and ask them to refresh **Home** and **Shifts** on the phone. Check the expected site, local shift time and weekdays. The app shows punch-window guidance; the server decides whether a punch is allowed. A duty is a plan, not proof of attendance or a completed two-person handover.

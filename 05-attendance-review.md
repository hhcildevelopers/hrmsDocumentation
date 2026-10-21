# 5. Attendance review, corrections and supervisor exceptions

[← Handbook](README.md) · [Previous: field portal](04-employee-field-portal.md)

This page is for central administrators and authorized, site-granted Field Officers. First check the selected **company**. Review only sites within your company/site access. A dated duty is **not** attendance, and a reported GPS point is supporting evidence rather than proof the employee stayed at the post.

## Find a site's attendance

Open **Attendance review** and search for the site by name, client or city. Select it, then use the compact **date-range picker** in the attendance table to choose today, a preset range, or custom **from/to local work dates** (up to 31 days). Choose the **Offline status** filter for review records. The chosen site and work-date range apply to both tables; the status filter applies to the offline-decision table. For an overnight duty, use the date on which the shift **started**. Tables load from the server; you no longer need a separate **Load attendance** button.

The **Daily attendance** card has its own single work-date field. It shows every planned dated duty at that site, including one with no session. **No attendance recorded** means no session was saved; it is not an automatic **Absent** decision, because leave has not been implemented. The session table below is a separate date-range view of sessions that actually exist.

- **Shift attendance sessions**: employee, shift, status, punch-in/out times, **Worked** duration, distances from geofence center, and policy version.
- **Offline punch decisions**: employee, in/out event, observed and received time, reported distance/accuracy, current review status, and any previous decision reason.

If the session list is empty, confirm site and date range. If the offline-decision list is empty, confirm site, date range and status filter (default **Pending review**). No record is not the same as an approved record. Client users do not decide punches. The **Worked** value is elapsed time between accepted punches; active sessions have no final duration, and breaks/payroll rules are not applied. The employee's **Attendance** tab totals completed hours for a selected month.

## Decide a provisional offline punch

Open a **Pending review** item and compare employee, shift, event kind, observed time, received time, distance, accuracy, and the applicable policy. Ask about unusual time gaps or device/network problems. This screen does not show a full map of each punch point; do not claim you verified a route from the displayed distance alone.

Choose **Approve** only if the evidence and explanation satisfy HHCIL's policy. The server revalidates the shift and sequence before applying a decision; an approval request can still fail. Choose **Reject** when it must not count. Both decisions require a **Review reason of at least 10 characters**. Write a factual reason another reviewer can understand:

- Appropriate approval example: `On-site duty confirmed by the shift supervisor; network outage recorded at 08:02.`
- Appropriate rejection example: `GPS evidence is outside the approved site boundary; employee asked to contact HR.`
- Inadequate example: `ok`.

After saving, check the new status and reviewer/time. An employee can refresh the **Punches** tab to see the outcome. Never approve to “clear the queue” without reviewing the evidence. If you lack an Approve button, you need the `attendance` approval permission **and** the correct site scope; ask Super Administrator rather than using another person's login.

## Exception punch-out

For an **active** session whose employee cannot make a normal on-site punch-out, select **Exception punch-out**. Enter the employee's verified **actual departure date and time** in the **site's timezone**, not the time at which you are filling out the form. If appropriate, **Use scheduled end (verify first)** can prefill the planned end; it is not evidence of the real departure. Enter a reason of at least 10 characters explaining how the departure was checked, for example `Phone lost power; site register and supervisor confirm departure at 20:05.`

The actual time must be after the accepted punch-in and no later than now. For example, if an employee punched in yesterday at 08:00 and really left at 20:05, enter **yesterday's 20:05**, not today's current time. After saving, check the resulting **Worked** hours in the sessions table. The session is marked **exception_completed**; there was no verified punch-out location. The action is audited and can activate a pending transfer after the old session closes. It does **not** certify a two-person handover.

## Record an attendance correction

Use this when **both punches were missed**, when an employee **punched in late but is still on duty**, when they **missed punch-out**, or when an already saved time is wrong. Choose the correct company and site, then choose the duty's **start date** in **Daily attendance**. Find the employee and tap **Record attendance correction**. Field Officers can use **Menu → Attendance corrections** in the Field Portal for sites they are granted. Employees and linked Field Officers cannot correct their own attendance; ask an HR or Super Administrator instead.

Enter the **actual** in and out dates/times in the **site's timezone**, plus a factual reason of at least 10 characters. For example: `Duty register and site supervisor confirm 08:05 arrival and 20:10 departure.` Tap **Review hours**, read the calculated duration, and check any warning about early start, late finish, or longer-than-planned work. Confirm the warning only after checking the facts, then tap **Confirm and save**. The change applies immediately; there is no second approval step.

If the employee is **still working** and only the punch-in time needs correction, leave **Correct punch-in only; keep this duty open** selected. Enter the actual start time and reason, review, and save. The duty stays in progress; do not invent a punch-out time. Worked hours appear only after the employee later punches out or an authorized reviewer records the actual departure.

The entered period must overlap the selected duty, finish in the past, run in order, and be no longer than **16 hours**. You may enter time outside the planned shift if it is justified and you confirm the deviation. For example, for an 08:00–20:00 duty, an actual 07:45–20:15 period is allowed with the reason and warning confirmation; an 18-hour period is not.

The saved session uses these **effective** times for worked-hour totals. A manually entered side is labelled **not GPS-verified**. The original phone punch, GPS evidence, and earlier correction versions are never changed. Tap **History** on a duty to see who changed it, why, and the before/after times. The employee can refresh **Punches** to see the corrected result; the Client Portal site total also includes it and identifies how many sessions include manual time. These are elapsed hours, not a payroll decision.

## Attendance-phone settings and recovery

Super Administrators can open **App Configuration** to select **Limited changes** or **Unlimited changes** for attendance phones. The initial Limited value is `3`: this means three changes *after* the first enrollment, not three logins. Enter `0` to require an HR/Super Admin reset before each phone change. Each such reset grants one change. Changes apply at the next switch and do not erase employees' used counts or phone history. HR Administrators can view this policy but cannot edit it.

On an employee's detail page, open **Devices** to see the current phone, earlier phones, used count, and remaining allowance. If a lost or replaced phone prevents the employee from switching, a Super/HR Administrator with `employee.UPDATE` and `attendance.APPROVE` may choose **Reset change count**. Enter a factual reason of at least 10 characters, for example `Employee reported lost phone; identity checked by HR at Ahmedabad office.` A reset sets the used count to zero; it does **not** select a new phone or restore punches that only existed on the lost phone. The employee must sign in and choose **Use this phone for attendance**. Check reported missing punches through the normal attendance review/exception process, never by inventing a confirmed punch.

## Escalate instead of guessing

If a worker reports “saved on phone,” ask them to reconnect and check the **Punches** result; do not mark it confirmed verbally. If the result is **Checking with server**, ask them not to submit a new punch until the original reference is checked. If several staff at one site suddenly fail GPS checks, verify the active geofence policy version and physical duty point with HR; do not widen the radius without approval and a real-phone site test. For an incorrect duty, ask HR to check the current assignment and common shift. If you suspect abuse, preserve the event details and follow HHCIL's investigation procedure; GPS uncertainty alone is not conclusive misconduct.

Current release limitations: no continuous employee location map, background-tracking status, automated exit/no-show alerts, or two-person handover decision on this screen.

# 3. Shift scheduling and roster publication

[← Handbook](README.md) · [Previous: setup](02-clients-sites-employees.md) · [Next: field attendance →](04-employee-field-portal.md)

Open **Shift scheduling**, find the site, and choose **Open roster**. The site page has two tabs: **Templates and recurring rules** and **Roster and coverage**. A shift shown in the roster is *planned duty*, not proof that anyone attended or handed over the post.

## Before entering rules

Confirm the correct site and **timezone**, active security post, active assigned employees, required headcount, and weekday pattern with the client. An employee must be eligible for that site/post, and published shifts cannot overlap for the same employee. Use local site dates. For an overnight shift starting at 20:00 on 12 October and ending at 08:00 on 13 October, the **work date is 12 October**.

## Step 1 — Add shift templates

In **Templates and recurring rules → Add template**, enter one template per distinct duty period. Start time is the site's local 24-hour time (`HH:mm`). Duration is in **minutes**, not hours. Arrival/departure grace and handover window are in minutes.

| Example for 12-hour coverage | Start | Duration | End on local clock |
| --- | --- | ---: | --- |
| `DAY12` — Day duty | `08:00` | `720` | `20:00` same day |
| `NIGHT12` — Night duty | `20:00` | `720` | `08:00` next day |

For three 8-hour shifts, use `06:00`, `14:00`, and `22:00`, each with **480** minutes. Template code uses 2–50 letters, digits, `.`, `_`, or `-`; name should be understandable to a planner (for example, `Main gate night duty`). A duration must be **60–1,440 minutes**. Arrival and departure grace allow **0–180 minutes**; handover window allows **0–240 minutes**. Example values: arrival grace `15`, departure grace `15`, handover window `30`. Do not claim these fields automatically generate late-arrival or handover alerts; those workflows are not live.

The current attendance punch-in window opens before shift start by the larger of arrival grace and handover window, capped at 120 minutes. For an 08:00 start with 15-minute arrival grace and 30-minute handover window, the phone can show **Punch in opens at 07:30**. This is eligibility to attempt a punch, not permission to leave early or proof of an actual handover. The field app obtains exact window hints from the server.

## Step 2 — State the coverage requirement

Choose **Add requirement** for each post/template combination that must be covered. Example: `Main gate guard` + `DAY12`, **Required headcount** `1`, weekdays `Mon–Sun`, **Effective from** `2026-10-12`, **Effective to** blank for ongoing. Use `2` only when **two people must work that same post and shift at once**; do not set `2` merely because day and night shifts each need one guard. Headcount must be 1–100. Select at least one weekday. End date, if entered, must be on or after start date.

For 24-hour coverage at one post, create a requirement for each template (day **and** night). A template by itself does not demand coverage. An uncovered required position appears as a **coverage gap** and blocks publication.

## Step 3 — Assign recurring employees

Choose **Add pattern**. Select the matching coverage requirement, an eligible **Employee assigned to this site**, a **Position number**, weekdays, and effective dates. Position numbers run from **1 through the requirement's headcount**. For headcount `1`, choose position `1`; for headcount `2`, use separate patterns for positions `1` and `2`. Pattern dates must fit inside the requirement's dates.

Example: employee `Asha Patel (HHC-01042)`, requirement `Main gate guard — DAY12 — 1 position`, position `1`, weekdays `Mon–Sat`, from `2026-10-12`. If Sunday also needs coverage, make sure an eligible Sunday pattern exists, possibly for another employee. Do not assign one employee to overlapping shifts, including across sites. An inactive/unassigned employee will be refused.

## Step 4 — Generate, inspect, publish

In **Roster and coverage**, select a **From work date** and **To work date**, then **Load schedule**. The screen shows up to 42 days at once. **Generate 6 weeks** creates concrete draft shifts from the selected start date; repeat generation is safe and does not duplicate existing shifts. Read the created/existing count.

Inspect the calendar or switch to **List** to see each employee, post, status, and history. Expand **Review uncovered post/shift dates** if a gap warning appears. Fill missing patterns or replace an employee where allowed, regenerate/reload, and check the gap disappears. **Publish drafts** is available only when the selected range has no coverage gap; review the confirmation before publishing. Only **published/scheduled** duties become employee punchable duties in the field portal. After publishing, ask the employee to use **Refresh** on the phone.

When a rule is changed or deactivated, **already-generated shifts remain** until revised or cancelled. Do not assume that editing a recurring pattern changes every published duty. Open the actual date range and check it.

## Changes after generation

In List view, use **Replace** to choose a different eligible employee, or **Extend** to enter a new end date/time and a reason of at least 3 characters. **Extend** uses your **browser's local timezone** in its date/time input; if you are planning for another city/timezone, double-check the displayed site-local result before saving. **Cancel** is shown for an eligible future shift and requires a reason. Use **History** to see the recorded revision. A stale or conflicting revision should be reloaded before retrying.

Example good reason: `Replacement requested by site supervisor; original employee on approved leave.` Poor reason: `change`. Avoid replacing a shift after it has begun without coordinating with the site and checking attendance.

## Important limits

The coverage warning checks the **published plan**, not who is physically present. This release does not automatically establish no-show, early departure, unattended-post, or completed-handover events. The supervisor must still use operational communication and **Attendance review** for actual punch evidence.

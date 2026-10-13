# 4. Employee field attendance — phone guide

[← Handbook](README.md) · [Previous: shift scheduling](03-shift-scheduling.md) · [Next: attendance review →](05-attendance-review.md)

This page is for employees and field officers marking **their own** attendance. Use the official field-portal link from HHCIL on a phone with location services enabled. The web app can show **English / हिंदी**; your selection is remembered on that device. A password and internet are needed to sign in. HHCIL must give you an account linked to your employee profile and a published shift; simply being on the site is not enough.

## The three bottom tabs

- **Home** shows the active duty first (including a night shift that started yesterday), otherwise a punchable duty or your next duty. It shows site, post, address, local time, status, and the main punch button above the map.
- **Shifts** lists upcoming duties in order and past duties separately. Past duties have no punch button. If you think a shift is missing, tap **Refresh**, then contact your supervisor.
- **Punches** shows server attendance sessions, server review decisions, and punches saved on this phone. Choose a month and tap **Show history** to retrieve older server records. A saved-only punch on a different phone cannot appear until that phone syncs it.

If Home says **Punch in opens at …**, wait until that time. If it says the shift can no longer be punched, contact the supervisor. Do not change your phone clock; the server checks the actual window. For a night shift, follow the date/time shown on the duty card, not just today's date.

## Before duty: check the correct site

Read the site name, post, address, and start time. Tap **Check my location** only when you want a fresh check. The phone asks for location permission. The screen then shows approximate GPS accuracy, straight-line distance to the site center, and whether the reading appears inside the configured boundary. The map can show directions after this check, but it does **not** draw the geofence circle. Showing directions sends the checked position to Google Maps. If the map is unavailable, the duty card and punch button can still work.

**A good location preview is not attendance.** When you tap **Punch in** or **Punch out**, the app requests a **new** GPS reading and waits for the server's decision. Do not walk away just because Check my location looked good.

## Punch in and punch out

1. At the assigned gate/post and within the allowed time, tap the large **Punch in** button. Allow location for the official site when the phone/browser asks. Keep the screen open while it says it is checking your position.
2. Wait for **Attendance is confirmed**. Check the **Punches** tab for a confirmed/on-shift record. If it is waiting, saved, unknown, or rejected, it is **not** confirmed; read the displayed guidance.
3. At the end of duty, while still at the site and within the allowed time, tap **Punch out**. Again wait for server confirmation. An ordinary punch-out does **not** certify a handover to the incoming guard; follow HHCIL's existing handover procedure.
4. If your punch-out window has closed, tell your supervisor. An authorized person can record an **exception punch-out** with a reason; it will be marked as an exception, not as a GPS-confirmed punch-out.

The phone's GPS uncertainty matters. Example: a site requires **50 m or better**, but the phone reports **138 m**. The app will tell you to move to an open area and retry. Even a 30 m reading can fail near the edge of the site because the server adds the reported uncertainty to the distance from the center. Do not use a different person's account or ask someone else to punch for you.

## Using another phone

Sign in normally. You can still see your published duties, confirmed attendance, and server review results. To punch from this phone, read the **Use this phone for attendance** card. It shows how many changes remain. The first phone enrollment is free; signing in again on the same phone does not use an allowance. HHCIL currently allows **three** changes unless a Super Administrator changes the App Configuration policy.

Before you tap **Use this phone for attendance**, sync any punches saved only on the old phone. They do not move to the new phone. Signing in on the old phone ends your login on this one, so return and sign in here afterward. If the old phone is lost or its saved punch cannot be recovered, tell your supervisor and provide the shift and approximate time; do not claim the missing punch was confirmed. If your change limit is reached, ask HR to review and reset your used count with a reason. A reset does not itself switch phones.

You may switch during an active duty. The server keeps the same attendance session, but you must still obtain a new GPS fix at the site for punch-out. The previous phone stops being eligible for further punches and cannot send its unsynced evidence after the switch. This web-browser phone identifier is an operational control, not proof of who physically held the phone.

## If internet is unavailable

The **No internet** banner means the server has **not confirmed** any new punch. In limited conditions, the phone may offer **Save punch in on phone** or **Save punch out for review**. This requires a fresh on-site GPS reading and a still-valid, previously downloaded shift/policy bundle. Keep the already signed-in page open; after closing/reloading it, you may need to reconnect and sign in before using attendance. Browser storage is not guaranteed to survive clearing data, device loss, or reinstalling the app.

When connectivity returns, open **Punches** and tap **Sync punches** if needed. Status meanings:

| What you see | What it means | What to do |
| --- | --- | --- |
| **Confirmed** | Server accepted the punch or approved review was applied. | Keep the record; proceed with normal duty. |
| **Waiting to sync** | Evidence is only on this phone. | Reconnect; keep the phone data; sync. |
| **Checking with server** | The previous network response was lost; result is uncertain. | **Do not punch again.** Reconnect and sync/check status. |
| **Waiting for approval** | Offline evidence reached the server but needs a supervisor decision. | Tell your supervisor if it remains pending. |
| **Not accepted** | Server/reviewer rejected the evidence. | Read the reason and contact your supervisor promptly. |
| **Already sent — check attendance** | The same saved event was detected again. | Check session/confirmed status rather than making a new punch. |

Do not tell your supervisor “I punched successfully” if the phone says saved, queued, waiting, unknown, or rejected. Give the shift/site, approximate time, and any **Details for supervisor** reference when reporting a problem. Never share your password.

## If the phone cannot obtain a usable location

- **Permission denied:** turn on device location, allow location for the official HRMS website in browser settings, then retry.
- **GPS accuracy too weak:** move to a safe, open area **within the site**, wait for a better fix, and tap **Check again** or retry the punch. Do not cross a restricted area to improve GPS.
- **Outside boundary:** verify the duty site and enter the approved reporting area; if the configured pin/radius is wrong, ask the supervisor to escalate to HR. Do not change coordinates yourself.
- **No fresh position / timeout:** check that location services are enabled and try again. HTTPS is required for location outside local development.
- **Different phone/browser:** sign in, check the allowance, and use **Use this phone for attendance** after syncing old-phone evidence if possible. If the allowance is exhausted or evidence is missing, ask HR or your supervisor; creating another user is not the solution.
- **No duty / wrong duty:** ask the planner to check profile link, assignment, policy, and **published** roster. A draft shift is not punchable.

## Privacy and current limit

The present field web portal asks for a **foreground** location when you choose **Check my location** or a punch. This release does **not** continuously track you in the background or raise automatic geofence-exit alerts. HHCIL must communicate any later tracking-policy change before it is introduced. The map/distance is guidance; only a server-confirmed decision counts as current attendance.

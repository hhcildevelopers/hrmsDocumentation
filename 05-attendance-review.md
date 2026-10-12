# 5. Attendance review and supervisor exceptions

[← Handbook](README.md) · [Previous: field portal](04-employee-field-portal.md)

This page is for central administrators and authorized, site-granted Field Officers. Review only records within your responsibility. A shift on the roster is **not** attendance, and a reported GPS point is supporting evidence rather than proof the employee stayed at the post.

## Find a site's attendance

Open **Attendance review**. Search for the site by name/client/city, select the correct site, set **From local work date** and **To local work date**, choose an **Offline status** filter, and tap **Load attendance**. The date fields filter **attendance sessions**; the offline-decision list is filtered by **site and status**, not by those dates. For an overnight shift's session, use the shift's *starting local work date*. The screen shows:

- **Shift attendance sessions**: employee, shift, status, punch-in/out times, distances from geofence center, and policy version.
- **Offline punch decisions**: employee, in/out event, observed and received time, reported distance/accuracy, current review status, and any previous decision reason.

If the session list is empty, confirm site and date range. If the offline-decision list is empty, confirm site and status filter (default **Pending review**). No record is not the same as an approved record. Client users do not decide punches.

## Decide a provisional offline punch

Open a **Pending review** item and compare employee, shift, event kind, observed time, received time, distance, accuracy, and the applicable policy. Ask about unusual time gaps or device/network problems. This screen does not show a full map of each punch point; do not claim you verified a route from the displayed distance alone.

Choose **Approve** only if the evidence and explanation satisfy HHCIL's policy. The server revalidates the shift and sequence before applying a decision; an approval request can still fail. Choose **Reject** when it must not count. Both decisions require a **Review reason of at least 10 characters**. Write a factual reason another reviewer can understand:

- Appropriate approval example: `On-site duty confirmed by the shift supervisor; network outage recorded at 08:02.`
- Appropriate rejection example: `GPS evidence is outside the approved site boundary; employee asked to contact HR.`
- Inadequate example: `ok`.

After saving, check the new status and reviewer/time. An employee can refresh the **Punches** tab to see the outcome. Never approve to “clear the queue” without reviewing the evidence. If you lack an Approve button, you need the `attendance` approval permission **and** the correct site scope; ask Super Administrator rather than using another person's login.

## Exception punch-out

For an **active** session whose employee cannot make a normal on-site punch-out, select **Exception punch-out**. This requires a reason of at least 10 characters, such as `Phone lost power after duty; supervisor confirmed departure at 20:05 by site register.` Confirm only after checking the facts. The session is marked **exception_completed**; it is not presented as a location-verified normal punch-out. Actor, time, and reason are recorded for audit. This action does **not** by itself complete an incoming/outgoing employee handover.

## Escalate instead of guessing

If a worker reports “saved on phone,” ask them to reconnect and check the **Punches** result; do not mark it confirmed verbally. If the result is **Checking with server**, ask them not to submit a new punch until the original reference is checked. If several staff at one site suddenly fail GPS checks, verify the active geofence policy version and physical duty point with HR; do not widen the radius without approval and a real-phone site test. For incorrect roster/assignment, ask the planner to revise it. If you suspect abuse, preserve the event details and follow HHCIL's investigation procedure; GPS uncertainty alone is not conclusive misconduct.

Current release limitations: no continuous employee location map, background-tracking status, automated exit/no-show alerts, or two-person handover decision on this screen.

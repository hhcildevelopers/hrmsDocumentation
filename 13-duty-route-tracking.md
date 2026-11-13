# 13. Duty-route tracking pilot

[← Handbook](README.md) · [Field Portal](04-employee-field-portal.md) · [Attendance review](05-attendance-review.md)

Duty-route tracking records **reported phone locations** during an open attendance duty. It is a development pilot intended to start with Field Officers. It is **off for every employee by default**. HR may enable it for another employee when that use has been approved. A route shows where the phone reported being, with its accuracy and any gaps; it does not prove the exact path travelled or continuous presence at work. Tracking points do not change punches, worked hours, leave or payroll.

## HR: turn tracking on or off

In the Admin Portal, select the correct company and open **Employees → employee details → Tracking**. Switch **Track this employee during active duty** on or off, then choose **Save tracking setting**. The change takes effect immediately. A staff member needs the Tracking permission to view routes and the separate update permission to change the switch. Only authorized HR Administrators and Super Administrators can use these actions; Field Officers and clients cannot review other employees' routes.

For a company-wide review, open **Duty tracking** in the Admin sidebar. Choose a duty month, optionally search by employee name or code, then choose **Routes** for an employee. Open **View** beside a duty to see its map and point list. The selected company controls which duties appear. A transfer does not move an old duty's route to the new company: review that duty under its original company. You can also review an employee's duties directly on their **Tracking** tab.

The point list shows when each position was observed, whether it arrived later, the phone's reported accuracy, and coordinates. The map joins successive reported points with straight lines and leaves long gaps visible. **No points** means there is no route to open for that duty. If more than 500 points exist, only the first 500 are shown; **Last displayed** is then the last point on screen, not necessarily the last point recorded. If the map does not load, use the point list. Do not infer a route from a punch-in and punch-out location alone.

## Employee: what happens on the phone

After the server accepts your **Punch in**, the Field Portal checks whether HR enabled tracking for you. If it is enabled and this is your enrolled attendance phone, the Home screen shows a duty-tracking indicator. Allow location access to supply route points. The page takes a reading when tracking starts or resumes, then uses the site's reporting interval, normally **5–20 minutes**. **Last point** shows the last accepted upload, not a promise that the phone is continuously reporting.

Keep the Field Portal page open and visible during the duty if you are taking part in this pilot. Tracking pauses when the tab is hidden or the phone locks. It resumes by checking your current duty and setting when the page becomes visible again. It stops after punch-out, an approved exception or correction that closes the session, HR switching tracking off, sign-out, or the existing deadline six hours after the scheduled shift end. Your own portal shows tracking status, but does not have a route-history screen in this pilot.

If GPS permission is denied, the reading is too inaccurate, or the phone cannot get a position, the route will have a gap. **This does not cancel an otherwise valid punch.** Punching still follows the selected site's normal attendance method and rules. Do not submit extra punches to fill a tracking gap; tell your supervisor if the gap matters for an operational review.

If the connection drops while the page stays open, the phone can hold a small, temporary queue of at most **50 points for up to 15 minutes** and retry when connected. A delayed point shows its observation and receipt times. Older or unverifiable points are discarded. Phone storage can be lost, so a missing point cannot be recreated later or treated as proof of attendance. This pilot does not run reliable tracking in the background or while the phone is locked.

## Retention and help

Raw route points are intended to be kept for **30 days**; the deployment administrator must run the scheduled purge for that limit to take effect. Older duties may remain visible without their location points. Only authorized HR/Super staff should open a route for an approved work purpose. Route access and switch changes are audited. Do not share route screenshots or coordinates through an unapproved channel.

If the indicator says tracking is paused or unavailable, first check that the duty is open, this is the enrolled phone, the page is visible, location permission is on, and the connection has returned. Ask HR to check the employee switch and site policy if the problem continues. For the exact messages and recovery steps, see [Common Errors & Solutions](08-common-errors-and-solutions.md).

Before using this with real employees, HHCIL must approve the employee notice, monitoring purpose, who may review routes, use of personal phones, and the retention procedure. A native Android background-tracking service and automatic geofence-exit alerts are outside this pilot.

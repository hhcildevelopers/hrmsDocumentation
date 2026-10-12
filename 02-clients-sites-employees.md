# 2. Clients, sites, geofences, employees, and access

[← Handbook](README.md) · [Next: shift scheduling →](03-shift-scheduling.md)

Only authorized central staff should change workforce records. A site is where duty happens; a security post is the specific covered position at that site. A client is the customer organization that owns the site.

## Create a client and contact

Go to **Clients → Create client**.

| Field | Training example | Meaning / common mistake |
| --- | --- | --- |
| Client code | `EX_RETAIL` | A unique, stable identifier (2–50 letters, digits, `.`, `_`, `-`). Do not reuse a deleted code. |
| Client name | `Example Retail Pvt Ltd` | Short name operators recognise, 2–150 characters. |
| Legal name | `Example Retail Private Limited` | Optional registered name; do not put the contact person's name here. |

Open the saved client and choose **Add contact**. Enter a person's name (`Neha Shah`), optional designation (`Regional Facilities Manager`), optional valid email (`neha@example.com`), optional mobile, and tick **Primary contact** only for the correct main contact. Contacts can be edited or removed from the client page. For a client portal account, create a **User** separately; a contact does not become a login automatically.

## Create a site and security post

Go to **Sites & posts → Create site**, select the client, and enter the actual postal location.

| Field | Training example | What to check |
| --- | --- | --- |
| Client | `Example Retail Pvt Ltd` | Correct customer; do not place a site under a similar-looking client. |
| Site code | `EX_AHD_01` | Unique stable code, 2–50 permitted code characters. |
| Site name | `Example Retail - Ahmedabad West` | Name staff will recognise on the roster and phone. |
| Address | `123 Sample Road, Main Gate` | Real duty/reporting address, at least 3 characters. Include entrance/gate guidance if useful. |
| Address line 2 | `Near Sample Junction` | Optional landmark/building detail. |
| City / State | `Ahmedabad` / `Gujarat` | Spell consistently for search and reporting. |
| Postal code | `380001` | Enter the site's correct code, 4–12 characters. |
| Timezone | `Asia/Kolkata` | A valid timezone name, not `IST` or `GMT+5:30`. It controls local shift dates and times. |

Open the site and choose **Add post**. Example: post code `MAIN_GATE`, name `Main gate guard`, optional description `Guard stationed at the main customer entrance`. Create a separate post for each independently staffed duty point. An active assignment or published future shifts may prevent deactivation/archiving until they are dealt with. Do not delete a site or post just to remove a coverage warning; correct the roster first.

## Configure the geofence/tracking policy

On the site page, choose **Set policy** or **Create new version**. This is the circular site boundary used by GPS attendance. A new version takes effect immediately; old versions remain in history.

1. Search for the site or a nearby landmark. A search result is an approximate starting point, **not** the confirmed gate or post.
2. Click the map, drag the **blue duty-point pin**, or choose **Use map center as duty point** to confirm the actual reporting point. Check the radius circle. Search and map selection do **not** overwrite the separately saved postal address.
3. If maps/search fail, manually enter confirmed **Latitude** and **Longitude**. Latitude is −90 to 90; longitude is −180 to 180. Do not swap them. Use a surveyed, field-verified point; the training values below are not a real HHCIL site.
4. Enter the remaining values, choose **Review and create version**, read the immediate-effect warning, and confirm. Open **View geofence map** and **Policy version history** to verify the saved record. Test with a real phone at the duty point before enforcing punches.

| Policy field | Training value | Meaning / allowed input |
| --- | ---: | --- |
| Latitude / Longitude | `23.0225` / `72.5714` | Fictional example center only; obtain real coordinates for your site. |
| Radius (m) | `150` | Circle around center; 50–5,000 m. A tiny radius may reject genuine employees because GPS is uncertain. |
| Required accuracy (m) | `50` | Maximum uncertainty accepted for a punch; 5–500 m. Smaller means stricter, not better phone GPS. |
| Location max age (seconds) | `120` | Maximum age of an observed position; 15–900 seconds. |
| Reporting interval (minutes) | `5` | Choose only 5, 10, 15, or 20. This setting is for later tracking workflows; it does **not** enable live tracking today. |
| Stale after (minutes) | `10` | 10–120; must be at least **twice** the reporting interval. Example: interval 20 needs stale-after at least 40. Later tracking use; not a current alert. |
| Outside dwell (seconds) | `120` | 30–900; planned tracking threshold. It does **not** make the current portal alert on site exits. |

For a punch to pass the location test, the server checks that **distance from center + reported GPS accuracy ≤ radius**, as well as the maximum-accuracy and age rules. Example: with a 150 m radius, a phone 90 m from center with 40 m uncertainty can pass the distance check (`90 + 40 = 130`). At 120 m with 40 m uncertainty, it cannot (`160 > 150`), even if the map appears to show the employee inside. Time, assignment, account, shift, and device checks also apply.

## Create and link an employee

Go to **Employees → Create employee**. This creates an HR profile, **not** a login. Use a real employee identifier and official joining details.

| Field | Training example | Rule |
| --- | --- | --- |
| Employee code | `HHC-01042` | Unique, up to 40 permitted code characters; avoid spaces. |
| First / last name | `Asha` / `Patel` | Both required. Middle name optional. |
| Category | `Security guard` | Choose from Security guard, Security supervisor, Field officer, Facility staff, Other. |
| Designation | `Security Guard` | Job title, 2–100 characters; distinct from category. |
| Mobile | `9876543210` | Optional; use an HHCIL-approved contact number. Do not add spaces or a dummy number just to fill the field. |
| Email | `asha.patel@example.com` | Optional; must be a valid email if supplied. |
| Joining date | `2026-10-01` | Actual calendar date in the date picker (YYYY-MM-DD). |
| Portal account | `Asha Patel (guard_1042)` | Optional existing active Employee/Field Officer account. Link the correct person; this does not change their role. |

If the employee needs the field portal, first create the **User** under Users, then link it here or on the employee detail page. Do not create a second account/profile because the first is hard to find. A user-kind value of `employee` alone does not create or link a profile. An inactive or terminated employee must not be scheduled as an active guard.

## Assign the employee to a site/post

On the employee page, choose **Assign site**. Example: Site `Example Retail - Ahmedabad West`; Security post `Main gate guard`; Assignment start date `2026-10-01`. The post is optional for a site-wide assignment, but a scheduled security-post duty must have a suitable active assignment. An employee can have **only one active primary assignment**. To transfer the employee, choose **End assignment**, enter the effective end date and a meaningful reason (`Transferred to north site after client approval`), confirm, then create the new assignment. Revise or cancel any published future shifts that conflict with the change first. End dates and joining dates are calendar dates, not shift timestamps.

Changing employment status to inactive/terminated, ending an assignment, and archiving site records can be blocked if future published shifts still depend on them. Fix those shifts rather than forcing a change.

## Site access for field officers and client users

On the site page, **Site access → User to add → Add user → Save site access**. A Field Officer account receives **Field operations** scope; a Client User receives **Client read-only** scope. The account must already exist with the matching kind and role. Saving replaces the site's entire active grant list: check every listed user before saving, or you may remove someone else's access.

A grant controls *which site* can be read. Feature permission controls *which action* is allowed there. Client users should not receive exact tracking-policy coordinates or employee private contact data through client-scoped views. Field officers need the attendance **Approve** permission as well as a site grant before they can decide an offline punch. Ask Super Administrator to adjust a role/override if needed; do not grant broader sites as a substitute.

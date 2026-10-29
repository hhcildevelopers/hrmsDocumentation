# 2. Clients, sites, geofences and employees

[← Handbook](README.md) · [Next: common shifts and assignments →](03-shift-scheduling.md)

First choose the **correct company** in the Admin Portal. A client belongs to that company; its sites and employees' current assignments are checked against it. A site is where duty happens, and a post is the particular gate or position. You cannot make another company's record appear here by changing a filter.

## Company and client business profiles

A Super Administrator opens **Companies** and selects a company. Its **Company details** tab holds the legal name, address, contact and letter signatory details. **Allowance details** names the company's earning, deduction and reimbursement heads; **Other details** lists owners and managers. The **Document Bucket** holds private, versioned records such as the logo, authorized signature, registrations and licences. Check the chosen company before editing: a client, employee or letter must use its own company's identity.

Open a client under **Clients** to see its **Business profile**, **Document Bucket**, contacts, sites and portal account. The profile shows its fixed parent company. A blank client statutory setting inherits the corresponding parent-company value; a client value overrides it. The screen shows the source of each setting. **Client identity and bank details do not inherit** from the company, so enter them separately when needed. PF, ESI, PT, bonus and overtime settings are saved for future use; entering them does not run payroll or calculate deductions.

Business profiles are effective-dated. Use **View as of** and **Load date** to inspect an earlier version. To make a correction, load the latest version, set **Effective from**, and choose **Save new version**. The earlier version stays in history. Upload a new Document Bucket version when a logo, signature or registration changes; do not put private documents in a public link. Company identity, especially the signatory and current image files, is needed for [Formalities letter previews](12-formalities-letter-previews.md).

## Create a client and contact

Go to **Clients → Create client**.

| Field | Training example | Meaning / common mistake |
| --- | --- | --- |
| Client code | `EX_RETAIL` | A unique, stable identifier (2–50 letters, digits, `.`, `_`, `-`). Do not reuse a deleted code. |
| Client name | `Example Retail Pvt Ltd` | Short name operators recognise, 2–150 characters. |
| Legal name | `Example Retail Private Limited` | Optional registered name; do not put the contact person's name here. |

Creating a client opens its detail page. If the client needs portal access, choose **Create Client login**. HR or Super Administrator with client-update permission can create and link the fixed Client User account in one step. Share the displayed **Client Code** and one-time temporary password privately with the authorized client contact; the client must change the password at first sign-in. The password cannot be viewed again. If the response is lost, refresh before retrying; ask Super Administrator to reset a lost password. A Super Administrator can search and link an eligible existing Client User instead of creating a duplicate. Replacing an account ends the previous account's sessions.

The linked account automatically sees **all non-deleted sites** belonging to this client, including sites added later. Confirm that this is acceptable before creating or linking the account. The contact record is separate: choose **Add contact** and enter a person's name (`Neha Shah`), optional designation (`Regional Facilities Manager`), optional valid email (`neha@example.com`), optional mobile, and tick **Primary contact** only for the correct main contact. A contact does not become a login automatically.

## Create a site and security post

Go to **Sites & posts → Create site**, select the client, and enter the actual postal location.

| Field | Training example | What to check |
| --- | --- | --- |
| Client | `Example Retail Pvt Ltd` | Correct customer; do not place a site under a similar-looking client. |
| Site code | `EX_AHD_01` | Unique stable code, 2–50 permitted code characters. |
| Site name | `Example Retail - Ahmedabad West` | Name staff will recognise on the assignment and phone. |
| Address | `123 Sample Road, Main Gate` | Real duty/reporting address, at least 3 characters. Include entrance/gate guidance if useful. |
| Address line 2 | `Near Sample Junction` | Optional landmark/building detail. |
| City / State | `Ahmedabad` / `Gujarat` | Spell consistently for search and reporting. |
| Postal code | `380001` | Enter the site's correct code, 4–12 characters. |
| Timezone | `Asia/Kolkata` | A valid timezone name, not `IST` or `GMT+5:30`. It controls local shift dates and times. |

Open the site and choose **Add post**. Example: post code `MAIN_GATE`, name `Main gate guard`, optional description `Guard stationed at the main customer entrance`. Create a separate post for each independently staffed duty point. An active employee assignment or future duty can prevent deactivation/archiving. Review assignments before changing the site or post; do not delete one just to hide a scheduling problem.

## Configure the geofence/tracking policy

On the site page, choose **Set policy** or **Create new version**. This is the circular site boundary used by GPS attendance. A new version takes effect immediately; old versions remain in history.

1. Search for the site or a nearby landmark. A search result is an approximate starting point, **not** the confirmed gate or post. If you are standing at the real duty point, **Use my location** can fill the point from your device; grant location permission and check its accuracy. A desktop location may be wrong.
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

For a punch to pass the location test, the server checks that **distance from center + reported GPS accuracy ≤ radius**, as well as the maximum-accuracy and age rules. Example: with a 150 m radius, a phone 90 m from center with 40 m uncertainty can pass the distance check (`90 + 40 = 130`). At 120 m with 40 m uncertainty, it cannot (`160 > 150`), even if the map appears to show the employee inside. Time, current assignment, account, duty, and phone checks also apply. **Use my location** needs HTTPS or localhost and gives a suggestion, not proof that the pin is correct.

## Create an employee and first duty

Go to **Employees → Create employee** in Admin, or **Menu → Register employee** in the Field Portal. Choose the correct company first. A Field Officer can register only at a site currently granted to them in that company. Registration creates the employee, their first site/shift assignment, and an Employee-only Field Portal login together. It does not require Aadhaar or PAN verification.

Choose **Code type: Auto** for the normal case. The server assigns the next group-unique code on save, such as `HHCIL-000001` for the selected company's prefix. Do not type an estimated next number. Choose **Manual** only when an existing approved staff code must be retained; enter 2–40 letters, digits, dots, underscores or hyphens. The code must be unique across all group companies and cannot resemble an automatic code. It is the employee's Field Portal login identifier and does not change on transfer. Do not derive it from Aadhaar, a phone number, or another personal identifier.

Enter the employee's first and last name, optional middle name/contact details, and actual joining date. Select an active **Department**, then a **Designation** belonging to that department, and an active **Employment type**. Next choose the correct client/site, optional post, Common shift, and working weekdays. The company and client are taken from the site; do not assume a similarly named site belongs to the right client. **Client employee code** is optional: it is the customer's local reference for this assignment, not the employee's login code. It remains on a same-client move and is cleared on a move to another client unless a new value is entered.

After saving, the employee is active and the system creates dated duties automatically. Copy the displayed temporary password securely **once** and give it, with the Employee Code, to the employee privately. They must change the password at first sign-in. Do not put the password in a screenshot, ticket, spreadsheet, or chat group. If the page closes before you copy it, check whether the employee was created before trying again; ask Super Administrator to reset the password if needed.

Super Administrator manages the group-wide **Common → Departments, Designations, Employment Types, Nationalities, Worker Types, Relationships, and Payment modes** lists. HR Administrator can edit these only when explicitly granted Common-master edit permission. Field Officers can use active onboarding options but cannot edit them. Inactive options stay on older records; they cannot be chosen for a new entry.

For an employee that existed before this workflow, the profile page still supports linking an eligible existing account or creating a login from a saved, unlinked employee. Do not create a duplicate employee just to get a login. If an existing unlinked account is missing, ask Super Administrator to check its onboarding company or the Field Officer's company grant.

Open the saved employee's tabs for private profile, documents, attendance, devices, and assignment history according to your permissions. The sensitive details and files are explained in [Employee records and documents](07-employee-records-and-documents.md). A transfer uses **Assignments → Transfer / change shift** and needs a reason. If attendance is open, the new duty waits until punch-out at the old site; historical attendance stays there.

## Assign the employee to a site, shift and weekdays

The new registration form already creates the first duty. For an older employee who has no assignment, open the saved employee's **Assignments** tab and choose **Assign duty**. Select the client/site, optional post, **Common shift**, and working days. Example: `Example Retail - Ahmedabad West`, `Main gate guard`, `08:00–20:00`, Monday–Saturday. Only one primary assignment is active at a time. The system creates dated duties automatically; you do not create or publish a routine roster.

For a change of shift, site, client or company, use **Transfer / change shift** and enter a reason. Do not end the old assignment and manually create a new one for an ordinary transfer. If attendance is open, the transfer waits until punch-out at the old site. Old attendance and assignment history stay with the old site/company. Read the step-by-step [Common shifts and assignments guide](03-shift-scheduling.md) before moving someone during a shift. Changes to employment status or site/post availability can be blocked while active duties depend on them; resolve those duties first.

## Site access for field officers

On the site page, **Site access → User to add → Add user → Save site access**. A Field Officer account receives **Field operations** scope. The account must already exist with the matching kind and role. Saving replaces the site's active Field Officer grant list: check every listed user before saving, or you may remove someone else's access. Client users are not added here; their access comes from the account linked on the client page.

A Field Officer grant controls *which site* can be read or operated on. A staff company grant controls *which company* is available, and feature permission controls *which action* is allowed there. A cross-company employee transfer requires the officer to have both company grants and both relevant site grants. A Client User sees all non-deleted sites of its mapped client, but not exact tracking-policy coordinates or employee private contact data through client-scoped views. Field officers need the attendance **Approve** permission as well as a site grant before they can decide an offline punch. Ask Super Administrator to adjust a role/override if needed; do not grant broader sites as a substitute.

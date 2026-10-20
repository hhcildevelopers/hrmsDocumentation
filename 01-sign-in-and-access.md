# 1. Sign-in, companies and access

[← Handbook](README.md) · [Next: clients and employees →](02-clients-sites-employees.md)

## Use the correct portal

| Portal | Who uses it | Sign-in identifier |
| --- | --- | --- |
| **Admin Portal** | Super/HR Administrators and other authorized staff | **Username** and password |
| **Field Portal** | Employees and Field Officers | **Employee Code or username** and password. An unlinked Field Officer uses username. |
| **Client Portal** | The account linked to a client | **Client Code or username** and password |

These are separate entry points. A valid Employee Code does not let someone sign in to Admin, and a Client Code does not let someone sign in to Field. Every portal requires a password. Codes are unique across the group, so an employee or client does not choose a company before entering credentials. **For Admin, use your username even if the current sign-in field mentions an employee ID**; Employee Code login belongs to the Field Portal.

If you receive a temporary password, sign in and complete **Create a secure password** first. Use at least 12 characters with uppercase and lowercase letters, a number, and a symbol. Do not include your username or reuse the temporary password. Never share either password or send it in a chat group. An account has one active login session: signing in on another browser or phone can end the earlier session. After repeated failed attempts, stop guessing and contact an administrator.

## Choose a company and switch safely

After password change, Admin staff and Field Officers who have company access choose a company on **Select a company**. The Admin Portal's company switcher is near the top-right avatar; a multi-company Field Officer can switch in **Menu**. Switch before creating or reviewing records. For example, a client created while **Hitech Human Capital Pvt Ltd** is selected belongs to that company, not Hitech Human Capital (India) Ltd.

If you see **No company is assigned to you**, ask a Super Administrator for a company grant. Do not create another account. Super Administrators can use every active company. Other staff see only their granted active companies, and their feature permissions and Field Officer site grants restrict what they may do inside each one. Switching companies clears the previous company's working view; it does not copy or move records.

An employee's self-service company comes from their linked employee profile. A Client Portal account's company comes from its linked client. They do not choose a different company's data. A company transfer must use the employee's **Assignments** workflow, not the company switcher.

## Super Administrator: create and maintain access

Use **Companies** to review the group company list. New companies start inactive; review setup and grants before activation. A company with current clients, sites or employees may be blocked from deactivation. Use **Users → Create user** for general account creation; this remains Super-Administrator-only.

| Field | Training example | What it means |
| --- | --- | --- |
| Username | `guard_1042` | Unique internal sign-in name, 3–80 allowed characters. It is not automatically the Employee Code. |
| Display name | `Asha Patel` | Person's recognizable name. |
| Email | `asha.patel@example.com` | Optional; leave blank if unknown rather than typing `N/A`. |
| User kind | `employee` | `staff` for central staff/operations officers, `employee` for a field worker account, `client` for a client contact. A user is not an employee or client record until linked. |
| Role | `Employee` | Select the appropriate active role; use minimum necessary access. |
| Employee account company | `Hitech Human Capital Pvt Ltd` | Required when creating an unlinked Employee-kind account. It says where that account can be offered for linking; it is **not** a staff company grant. |
| Company access | `Hitech Human Capital Pvt Ltd` | For non-Super **staff**. Grant one or more companies where they work. Permissions and site grants still apply. |

Prefer the shorter onboarding flows: HR with the right permission can create an **Employee login** from a saved employee's **Profile → Portal account**, or a **Client login** from a saved client's **Client Portal account**. These fixed-role workflows create and link in one action. HR cannot thereby administer general users. A Client User does not receive staff company grants; linking it to a client determines its one company and gives read access to that client's non-deleted sites.

The temporary password appears **once** after creation. Share it privately. If it is lost, a Super Administrator must reset it; the old password cannot be retrieved. An existing unlinked Employee account may need its **Employee account company** set by a Super Administrator before HR can find it in the employee picker. Already-linked accounts are not candidates for another employee.

For a staff-kind Field Officer who also works their own duty, link the account to an employee profile and separately grant the needed companies, sites and permissions. A site grant alone does not add an action permission. An unlinked Field Officer can use username login for authorized operations but has no personal employee duty to punch.

## Roles, permissions and site access

In **Users → Manage**, Super Administrators can manage company access, roles, status and individual permission overrides. A role supplies default feature permissions; a specific allow or deny can change one user's rights, and a deny wins. A role or permission does not bypass company and site boundaries. For example, an officer with access to Company A and Site A cannot use those rights to open Site B in Company B.

In **Roles & permissions**, Super Administrators can create a named role and choose its feature actions. Use a clear code such as `regional_viewer` and give only the actions needed. A role change affects current holders on later requests. Do not assign Super Administrator just to make a missing menu appear. Common Shift editing is **group-wide**; HR needs explicit Common Shift create/update permission, while Field Officers only need the read access required for transfers.

**Reset password** creates a one-time password and ends sessions. **Revoke sessions**, disabling/locking, and deleting an account also affect sign-in and require confirmation. Deleting a user is a soft delete that keeps audit history. The system protects the final active Super Administrator. Use **Audit log** to see who made an administrative change, when, and to which record; do not put full ID numbers or passwords in notes or support messages.

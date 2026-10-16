# 1. Sign-in, passwords, users, and roles

[← Handbook](README.md)

## Sign in safely

Use the official portal link supplied by HHCIL. An administrator signs in on the **Admin Portal** with their username. Employees can sign in on the **Field Portal** with their Employee Code or username and password. A linked Client Portal account can use its Client Code or username and password. An unlinked Field Officer uses their username. Codes do not replace passwords.

If an administrator gives you a temporary password, sign in and complete **Create a secure password** before any other task. Enter the temporary password in **Current/Temporary password**, then a new password twice. The new password must have at least **12 characters**, uppercase and lowercase letters, a number, and a symbol. It must not contain your username or be the same as the current password. Example of the *format only*: `River!Cloud42S`; **do not use this published example as your password**. Never share your password or send it in a chat group.

One account has one active session. Logging in elsewhere can end an earlier session. After repeated wrong passwords, an account can be temporarily locked; stop guessing and contact an administrator. Use **Sign out** on a shared phone or computer.

## Super Administrator: create a portal user

Open **Users → Create user**. This operation requires Super Administrator access.

HR can instead create a fixed Employee login from a saved employee's **Profile → Portal account → Create Employee login**. This does not grant HR access to general user administration, role changes or password resets.

| Field | Good training example | How to fill it |
| --- | --- | --- |
| Username | `guard_1042` | Unique sign-in name, 3–80 characters: letters, numbers, dot, underscore, or hyphen. Avoid spaces. This is not automatically the employee code. |
| Display name | `Asha Patel` | Person's recognisable name, 2–150 characters. |
| Email (optional) | `asha.patel@example.com` | A real, working address if HHCIL uses it; otherwise leave blank. Do not type `N/A` into an email field. |
| User kind | `employee` | Choose `staff` for central staff, `employee` for a worker/field-officer field account, or `client` for a client contact. This choice does **not** create an employee profile. |
| Roles | `Employee` | Select at least one appropriate active role. Prefer the minimum access needed. |
| Employee account company | `Hitech Human Capital Pvt Ltd` | Required for Employee-kind accounts. Choose the company where HR will link this user to an employee. The user cannot sign in until linked. |

Existing unlinked Employee accounts may have no company assigned. Open **Users → Manage → Employee account company**, choose an active company, and save. Linked accounts change company through employee transfer. Non-Super staff instead require **Company access** grants; this is a separate setting.

For a field officer who must both punch for their own duty **and** review granted sites in the admin portal, use a **staff-kind** account with the **Field Officer** role, link that account to an active employee profile, grant the relevant sites, and give only the needed feature permissions. The field portal accepts Field Officer-role accounts; site-level attendance review specifically requires a staff-kind Field Officer with the appropriate grant and approval permission. A field officer who only uses their own field duties can have an employee-kind account, but that kind does not grant supervisor review access. Confirm HHCIL's intended responsibilities before choosing the kind. For a client user, choose **client-kind** and the **Client User** role; grant access to specific sites separately. Do not give everyone the Super Administrator role to fix a missing menu.

After **Create**, the screen shows a generated **Temporary password once**. Hand it to that individual through HHCIL's approved private channel, then close the dialog. The user changes it at first sign-in. If it was lost, open the account and use **Reset password**; you cannot reveal the old password again.

## Manage an account

In **Users → Manage**, an authorized Super Administrator can edit display name, email, user kind, status, roles, and per-feature permission overrides. Roles provide defaults; an explicit user **allow** or **deny** changes an individual action, and **deny takes precedence**. Overrides require a reason. Changes to a role's permissions affect its active holders on later requests; they are not copied into every user record.

The role/permission matrix includes actions such as **List** (open a list), **View** (open details), **Create**, **Update**, **Delete**, **Approve**, **Export**, and **Financial** where the feature supports them. A checked permission cannot bypass a client's or field officer's site scope. A user may have **View** permission and still be unable to open a site they were not granted.

Examples of access decisions:

- An HR Administrator can maintain workforce data only if the required feature permissions are present.
- A Field Officer granted Site A cannot use that grant to view Site B. To review Site A offline punches, the officer additionally needs the attendance **Approve** action.
- A Client User's site grant is read-only and does not expose policy coordinates or employee contact details in client-scoped responses.

**Reset password** generates another one-time temporary password and revokes sessions. **Revoke sessions** signs the user out. **Disabled/locked** stops use of the account; **Delete** soft-deletes it, revokes roles/sessions, and retains audit history. These actions ask for confirmation. If you act on your own account, expect to be signed out (for a self-reset, save the displayed temporary password before acknowledging it). The last active Super Administrator is protected from removal or demotion; do not work around this safeguard.

## Create or adjust a role

Open **Roles & permissions → Create role** (Super Administrator only). Example: name `Regional Viewer`, code `regional_viewer`, description `Read assigned site data`. Role codes use **lowercase letters, numbers, and underscores**, start with a letter, and are 2–50 characters. Enter a clear business purpose before assigning people. Open the role, tick only needed actions per feature, and select **Save permissions**. A role assignment does not automatically grant site access. Deactivating a role removes its permissions from active users on their next API request; confirm it only after checking affected users. A custom-role **Delete** deactivates it; system roles cannot be deleted.

## Audit log

The **Audit log** records actor, action, target, time, and outcome for administrative changes. Use it to investigate a changed account, permission, site policy, or roster. It is not a replacement for checking the current record. Audit access is permission-controlled.

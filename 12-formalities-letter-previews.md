# 12. Formalities letter previews

[← Handbook](README.md) · [Common Errors & Solutions](08-common-errors-and-solutions.md)

The **Formalities letters** page currently lets authorized HR and Super Administrators prepare and review a **Parking Assistant appointment letter preview**. Every page of the PDF says **PREVIEW - NOT ISSUED**. **View** beside **Generate preview** opens an unsaved PDF. A saved history row has its own **View** and **Download** actions. None of these actions issues a letter to the employee. Employees and Client Portal users cannot see these previews. Offer letters, other appointment styles, formal issuance and payslips are planned for later.

## Before you generate a preview

1. Select the **correct company** in Admin. Check the employee's name and Employee Code. The employee must be active, have an active assignment at an active client/site in that company, and have the **Parking Assistant** designation.
2. Confirm that the employee has an effective **monthly** salary in **Employees → Bank & Salary Pay → Salary**, or an applicable rate under **Common → Designation Rates**. Check the amounts against the approved salary record; the letter does not calculate payroll.
3. Ask a Super Administrator to complete the Company's **Legal / registered name**, address, **Letter signatory**, and **Signatory title** in its Company profile. The Company **Document Bucket** must have a current **Logo** and **Authorized signature** image. These images must be JPG or PNG.
4. Confirm the contract start and end dates, duration and notice period from the approved employment terms. The form does not derive these terms from attendance or the shift assignment.

If **Formalities letters** is missing from the Admin menu, ask a Super Administrator to check your Formalities permission and company access. Do not use another person's account.

## Generate and review

1. Open **Formalities letters**. Search for the employee by name or code, then select the employee and the available **Parking Assistant appointment** style/version. Version 1 is the current development style; when later versions are approved, choose the one required for this preview.
2. Choose the printed **Letter date**. Enter **Contract start**, **Duration (years)**, **Contract end**, and **Notice (days)**. If the end date differs from the date suggested by the duration, read the warning and verify the intended dates.
3. Choose **View** beside **Generate preview** to inspect both pages before saving. Check the employee and Company names, client/site, dates, contract wording, letterhead, signatory and salary annexure. Closing this view discards its temporary browser copy; no history entry is made.
4. Tick **I checked the contract dates, duration and notice period**, then choose **Generate preview**. The system checks the current employee, assignment, Company identity, images and monthly salary again. A successful preview appears in **Generated preview history**. Source details changed after View may appear differently in this saved preview.
5. Use **View** on a history row to inspect its saved version, or **Download** only when an authorized HR review needs a copy. Keep the **PREVIEW - NOT ISSUED** label visible; do not send the draft as an issued appointment letter.

The printed Letter date does not look up old employee or salary data. **View** and a new **Generate preview** each read current records. An older history row opens with the values and template version saved for that preview, even if the employee, salary or Company details have changed since then. Generate a new preview after a correction; the earlier entry remains in history.

## Check the salary annexure

The current preview always shows **Basic, DA, HRA, Special Allowance and Leave Wage**, including zero amounts. It also shows each other nonzero monthly earning included in **Gross Salary**, such as **Interim Bonus**, under its displayed name. Zero-valued extra heads are omitted. **Adjustment Arrear** is a one-time item and is excluded from this monthly Gross Salary annexure. The displayed rows must add up exactly to Gross Salary.

If the salary check fails, review the employee's **Salary** entry or inherited **Designation Rate**. Correct missing or inconsistent source amounts there before creating another preview. A per-day rate cannot use this monthly appointment style. Do not change a valid salary merely to make a letter pass.

## When to contact HR/Admin

| Problem | What to do |
| --- | --- |
| Employee or style is unavailable | Check the selected company, employee status, active assignment and Parking Assistant designation. Ask HR/Super Admin to review the record or access grant. |
| Company details or images are missing | Ask a Super Administrator to complete the Company profile and upload the current Logo and Authorized signature in its Document Bucket. |
| Salary amount is missing, invalid or does not match Gross Salary | Ask the salary owner to check the effective monthly Salary entry or Designation Rate. Review the annexure again after the source is corrected. |
| Preview cannot open or render | Refresh the history once. If the same preview still fails, give Admin/IT the selected company, employee code and preview history ID; do not share full salary or identity numbers in a support message. |
| Contract dates look wrong | Stop and confirm the written terms with HR. Generate a new preview with corrected inputs; the existing history row is retained. |

HHCIL still needs to approve the wording, expanded annexure, appearance and signing authority before formal issuance is added. An appointment preview is not proof that a letter was delivered or accepted.

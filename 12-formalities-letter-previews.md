# 12. Formalities letters

[← Handbook](README.md) · [Common Errors & Solutions](08-common-errors-and-solutions.md)

The **Formalities letters** page lets authorized HR and Super Administrators prepare letters, edit reusable wording, and review a PDF before issuing it. **View** opens an unsaved PDF. **Generate preview** saves a marked **PREVIEW - NOT ISSUED** copy in HR history; the employee cannot see it. Only the separate **Issue letter** action creates a letter visible in **My letters**.

The eight supplied default styles are **Parking Assistant appointment**, **Appointment Letter**, **Facility Supervisor appointment**, **Facility Staff appointment**, **First absconding show-cause notice**, **Second absconding show-cause notice**, **Contract extension**, and **Termination for absconding**. HR can also publish a reusable edited version or create a named **Custom** letter. Choose the style that matches the employee and the intended purpose. A source PDF is a formatting reference, not approval to issue its wording. Offer letters, payslips, Word export, and bulk issue are not part of this workflow.

## Before you generate a preview

1. Select the **correct company** in Admin. Check the employee's name and Employee Code. The employee needs an assignment in that company; appointment and extension letters require an active employee and assignment. Parking Assistant, Facility Supervisor, and Facility Staff styles require the matching designation.
2. For an appointment or extension style with a salary annexure, confirm an effective **monthly** salary on the employee's **Salary** tab, or an applicable rate under **Common → Designation Rates**. The generic **Appointment Letter** needs a positive monthly gross amount. Check all amounts against the approved salary record; the letter does not calculate payroll.
3. Ask a Super Administrator to complete the Company's **Legal / registered name**, address, **Letter signatory**, and **Signatory title** in its Company profile. The Company **Document Bucket** must have a current **Logo** and **Authorized signature** image. These images must be JPG or PNG.
4. For appointment and extension letters, confirm the contract start and end dates, duration and notice period from the approved terms. For absence or termination letters, confirm the recipient address and reported facts and dates. The second notice also needs the first-notice date. The form does not infer an allegation or disciplinary decision from attendance.

If **Formalities letters** is missing from the Admin menu, ask a Super Administrator to check your Formalities permission and company access. Do not use another person's account.

The **Issue letter** action requires the Formalities **Approve** permission. Super Administrators receive this protected permission automatically. A Super Administrator must enable **Formalities letters → Approve** on the HR Administrator role before HR users can issue, replace, or void letters.

## Generate and review

1. Open **Formalities letters**. Search for the employee by name or code, then choose the matching style and version. Company-specific published wording can take precedence over the group default. Confirm which version appears in the picker.
2. Set the printed **Letter date**. Complete the fields shown for that style: contract dates and notice for an appointment/extension, or reported facts, address and dates for an absence/termination letter. Check any duration warning. Do not enter a guessed fact to make the form pass.
3. Choose **View** to inspect the unsaved PDF. Check every page: employee, company, client/site, dates, wording, letterhead, signatory and any salary information. Closing this view discards its temporary browser copy; no history entry is made.
4. Tick the confirmation for the displayed fields, then choose **Generate preview**. The system checks current records again. A successful preview appears in **Generated preview history**. Details changed after View may appear differently in the saved preview, so open the saved copy too.
5. Use **View** on a history row to inspect its saved version, or **Download** only when an authorized HR review needs a copy. Keep the **PREVIEW - NOT ISSUED** label visible; do not send the draft as an issued letter.

The printed Letter date does not look up old employee or salary data. **View** and a new **Generate preview** each read current records. An older history row opens with its saved values and template version, even if those records later change. Generate a new preview after a correction; the earlier entry remains in history. Use the page controls below **Generated preview history** or **Issued letter history** to find older rows; the histories show 20 rows per page by default. Selecting an employee limits both histories to that employee.

## Edit reusable wording or create a Custom letter

1. Choose a style and **Edit reusable style**. It resumes the latest unfinished draft for that style and scope, or creates one if none exists. To reopen an older draft, choose it under **Reusable letter drafts**. To start a new letter type, enter a **Custom letter name** and choose **Create custom letter**. The selected company is the usual scope; only Super Admin can choose a group-wide scope.
2. In the editor, change wording and permitted tables. Blue **HRMS fields** show current employee values for review but stay as protected fields in the reusable template. Do not type an employee's name, ID, or salary as ordinary reusable text. Company letterhead and signature come from controlled Company records.
3. Choose **Save draft**, then **Preview draft PDF**. Complete the employee and style-specific fields in the main form first. Saving a draft does not publish it. An authorized Formalities approver checks the complete PDF, confirms that no employee-specific text was typed into reusable wording, and chooses **Publish version**. A published version is frozen; later changes need another draft and version.
4. Select the published version, **Generate preview** for the employee, review that saved PDF, then use **Issue letter** if the content and signing authority have been approved. Issuing a Custom letter also requires a separate confirmation of its wording and recipient.

**Clear company drafts** removes every unpublished draft for the selected company, including other HR users' drafts. It needs Formalities Approve permission and the typed confirmation `DELETE DRAFTS`. Published versions, saved previews, and issued letters remain. Ask the other editors before using it.

## Check the salary annexure

The **Parking Assistant** annexure shows **Basic, DA, HRA, Special Allowance and Leave Wage**, including zero amounts. It also shows each other nonzero monthly earning included in **Gross Salary**, such as **Interim Bonus**, under its displayed name. Zero-valued extra heads are omitted. **Adjustment Arrear** is a one-time item and is excluded from this monthly Gross Salary annexure. The displayed rows must add up exactly to Gross Salary. Other appointment and extension styles can require different annexure heads; review the generated PDF itself.

The generic **Appointment Letter** shows monthly gross salary and mentions a salary enclosure, but the supplied reference contains **no enclosure**. Do not issue it for real use until HHCIL supplies or explicitly resolves that enclosure and approves the wording. The Facility Staff and Contract Extension references also need HHCIL to confirm their incomplete or inconsistent contract terms. A local Issue button does not replace that business review.

If a salary check fails, review the employee's **Salary** entry or inherited **Designation Rate**. Correct missing or inconsistent source amounts there before creating another preview. A per-day rate cannot use a style requiring monthly pay. Do not change a valid salary merely to make a letter pass.

## When to contact HR/Admin

| Problem | What to do |
| --- | --- |
| Employee or style is unavailable | Check the selected company, employee status, assignment and any designation required by the chosen style. Ask HR/Super Admin to review the record or access grant. |
| Company details or images are missing | Ask a Super Administrator to complete the Company profile and upload the current Logo and Authorized signature in its Document Bucket. |
| Salary amount is missing, invalid or does not match Gross Salary | Ask the salary owner to check the effective monthly Salary entry or Designation Rate. Review the annexure again after the source is corrected. |
| Preview cannot open or render | Refresh the history once. If the same preview still fails, give Admin/IT the selected company, employee code and preview history ID; do not share full salary or identity numbers in a support message. |
| Contract dates look wrong | Stop and confirm the written terms with HR. Generate a new preview with corrected inputs; the existing history row is retained. |

HHCIL still needs to approve each style's wording, appearance, signing authority and retention before real-data issuance. A preview is not proof that a letter was delivered or accepted.

## Issue, replace or void a letter

This workflow is available for **synthetic local development testing**. Production issuance remains unavailable until HHCIL approves the applicable style and secure private storage. The local Issue action may be available for a style whose source wording still needs business review; do not use that action for real documents until the review is complete.

1. Open a saved preview in **Generated preview history** and check every page. Choose **Issue letter** on that row. Confirm the printed **Letter date** and actual issue time in the dialog. The system checks current employee, assignment, Company identity, applicable salary and images against the saved preview. If anything changed, create and review a new preview.
2. After issue, use **Issued letter history** to view or download the original final PDF. It no longer shows the preview mark. The linked employee sees the current letter under **Field Portal → Menu → My letters**. Appointment and contract-extension letters first offer a marked review View and **Accept**; the employee's Download becomes available after acceptance. HR can then open **Signed copy** from issued history. Absconding and termination letters keep their normal View and Download actions.
3. To correct a letter, generate a new preview, choose **Replace**, enter a clear reason and confirm. The old PDF stays in HR history but disappears from the employee's current letters.
4. To cancel a current letter issued in error, choose **Void** and enter a reason. The employee loses portal access to it; HR retains the PDF and decision history. A copy already downloaded by someone cannot be recalled.

The printed Letter date differs from the recorded issue timestamp. Issuing a letter does not prove that the employee received or accepted it. The embedded company signature image is not an electronic signature. Clients cannot see these letters.

## Accept an appointment or contract-extension letter

1. In **My letters**, choose **View** and read the marked review copy. Then choose **Accept**.
2. The dialog shows the current signature image from your Profile. If it is missing, use **Upload signature** to open the Profile document section and upload a JPG or PNG signature. A PDF signature document can be viewed but cannot be placed on the letter. Return to My letters and open Accept again.
3. Read and tick the declaration, then choose **Accept**. The system records the acceptance and creates a separate signed PDF. **View** and **Download** then show that signed copy. An appointment or extension cannot be downloaded from the portal before acceptance, although a browser may still save or capture the marked review view.

If the dialog says the letter needs an updated signature layout, contact HR to create a new preview and replace the earlier local letter. A replacement letter needs its own acceptance. If HR voids a letter, it disappears from My letters. This in-app acceptance uses an uploaded signature image; it is not a cryptographic digital signature.

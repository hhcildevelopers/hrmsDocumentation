# 9. Leave policies, requests and balances

[← Handbook](README.md) · [Attendance reports →](10-attendance-reports.md)

The Leave module is available in the development build. HHCIL HR/legal must approve each company's rules before staff apply a policy or use balances for real employees. A policy's annual CL/SL/PL amounts are **not** automatically added to an employee's balance. HR opens each leave year with a separate balance entry.

## Set up a company for leave (HR/Super Administrator)

1. Open **Common → Leave policies**. Review the HHCIL office example as a **draft**, including its leave year, leave amounts, notice rules and late-arrival rules. An undecided rule needs HR/legal confirmation; a blank field is not automatically zero. Save changes as a new version, obtain the required sign-off, then **Apply** the approved version to one or more companies with an effective date. A saved draft alone does not activate leave.
2. In the selected company, open **Common → Holidays**. Add company-wide or site-specific holidays. Weekly offs come from each employee's assigned working weekdays and are not entered as holidays.
3. On **Employees → employee details → Personal → Leave & field classification**, select **Internal employee** for eligible office staff; this also enables **Leave applicable**. For another eligible worker, such as a Field Officer, select **Leave applicable** without marking them internal when that is the correct policy. Leave both off for a worker who is not eligible. Enter the change reason and save. The **Field Officer** checkbox controls remote-location attendance; it does not create a login role or site grant.
4. Check the employee's current company, site, Common Shift and working weekdays. Use the real office shift; do not infer it from gender. A cross-company transfer needs the destination HR team to review eligibility and the destination policy.
5. Open **Employees → employee details → Leave**. Enter an **Opening balance** for each applicable CL, SL and PL type for the active leave year, including a zero balance where appropriate. Give every entry a factual reason. Later changes use **Adjustment (+/− days)**, not another opening entry. The history is retained, and a balance cannot become negative.

Policy editing and sign-off need their specific Common Leave Policy permissions. Balance changes and leave decisions need the applicable Leave permissions. If an action is missing, ask a Super Administrator to review your role and selected company.

## Request leave (employee or eligible Field Officer)

If **Leave applicable** is enabled, open **Field Portal → Menu → Leave** while online. Choose **CL**, **SL** or **PL**, enter the first and last dates and a reason of at least 10 characters, then choose **Send request**. A request may cover at most 31 calendar days. If it crosses a leave-year boundary or a policy-version change, submit separate requests for each period. You need a valid assignment for the requested dates.

The request first appears as **Pending**. It does not reserve or deduct days by itself. **My requests** shows its status, charged working days and decision history; refresh it after HR responds. Holidays and weekly offs within the range are not charged. An internal employee can see current-year balances; the Field Portal does not show balance numbers to eligible Field Officers. A displayed policy entitlement is not your actual remaining balance. If a balance has not been opened, HR must open it before approving your request.

The form does not require or upload a medical certificate. Do not put unnecessary medical or identity details in the reason. Leave requests need an internet connection; they are not saved to the phone as offline punches are.

If the **Leave** menu is missing, ask HR to check your eligibility, account link and company. If the page says there is no active policy, HR must finish the company setup. Do not use someone else's account to submit leave.

## Review requests (HR/Super Administrator)

In the selected company, open **Leave requests**. The initial filter shows items **Awaiting HR**; change the status filter to see approved, rejected, revoked or transferred requests. Choose **Review** to read the dates, reason, charged days, current balance and decision history. Enter a separate reason of at least 10 characters before **Approve** or **Reject**. Staff cannot decide their own request or change their own balance.

Approval rechecks the active policy, employee assignment, working days, holidays, overlapping leave, attendance evidence, any existing day classification and the opened balance. Only scheduled working days are deducted. If any check fails, resolve the source issue and reload the request; do not change attendance or create a second account to force approval. A request may need to be resubmitted if its policy, assignment or holiday snapshot changed.

For an approval made in error, choose **Revoke** and enter the reason. Revocation refunds the charged days and removes the approved-leave day code; check any attendance report already saved for those dates and reopen/regenerate it if needed. The original request and decision history remain visible.

After a cross-company transfer, earlier approved days remain with the old company. Future requests need the destination HR team to review the new company's policy, calendar and balance. A future approval is not carried forward as an automatic approval. Check the transferred request in **Awaiting HR / Transfer review** before deciding it.

## Late arrival is a separate HR decision

An approved company policy can also set the late grace period, maximum late arrivals per calendar month, maximum late duration and whether arrivals within the allowance need HR approval. An internal employee who arrives after grace must give a reason before the punch-in is accepted. An over-limit punch is still recorded; after punch-out the day is provisionally **HD** until HR approves it. Review these items in **Attendance review → Late arrivals**. Approval restores the normal day code; rejection leaves HD. This does not change the actual GPS time or calculate wages. See [Attendance review](05-attendance-review.md) for the review steps.

Leave requests, balances, and late decisions are in development review. Obtain HHCIL acceptance before treating their day codes as final payroll instructions.

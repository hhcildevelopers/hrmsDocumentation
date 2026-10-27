# 7. Employee personal details, bank details and documents

[← Handbook](README.md) · [Previous: troubleshooting](06-troubleshooting-and-terms.md)

These records are more private than the ordinary employee list. Work in the **correct company**, open **Employees → View**, and check the employee's name and code before entering anything. Only authorized HR/Super staff can edit personal and bank details. Field Officers may collect documents only for employees at granted sites when they have the required document permission. A client cannot open an employee's private HR record.

## Personal, address and statutory details

Open **Personal**. This tab contains the basic employee profile and portal account, guardian relationship/name, addresses, background, contacts, Aadhaar and PAN. Select a relationship from Common; if an old value is marked legacy, ask HR to review it. Select the domicile from the India state/union-territory list, and choose one or more known languages (use Other for a custom language). Enter the real date of birth if known; do not invent an estimated date. Present and permanent addresses may match, but confirm that with the employee. Unknown optional fields may be left blank and completed later.

Personal contains Aadhaar and PAN. The **Bank & salary pay** tab contains UAN, PF and ESIC details. These ID fields have format checks:

| Field | What to enter | Avoid |
| --- | --- | --- |
| UAN | Exactly 12 digits, if issued | Spaces, a phone number, or a made-up UAN |
| ESIC | 10–17 digits, if issued | Guessing a number from another document |
| PAN | Five letters, four digits, one letter | Spaces or another person's PAN |
| Aadhaar | Exactly 12 digits, only under HHCIL's approved collection procedure | Using a screenshot or unapproved copy as proof of verification |

Example PAN **format**: `ABCDE1234F` (a fictional pattern; do not save this as an employee's ID). The form can hide or show entered numbers while editing. Collect only details HHCIL has approved and verified through its own procedure. Entering a number here does **not** verify it with UIDAI, Surepass or another KYC provider. During development, use synthetic data only; live full identity-data collection needs HHCIL's consent, retention and security policy first.

Employees open **Field Portal → Menu → My profile** to see their own read-only details, including their full ID and current bank account numbers. These values are private: do not share screenshots or leave the portal open on a shared phone. Other employees, Field Officers viewing someone else's record, and clients cannot open this private record. If anything is wrong, use **Request profile changes** on that page; HR reviews the request before the record changes. See [Employee self-service](11-employee-self-service.md).

## Bank account: make a new version

In **Bank & salary pay → Bank accounts**, enter the official **Account holder name**, **Bank name**, **IFSC**, and **Full account number** twice. Choose Savings, Current or Salary only if known. IFSC has four letters, `0`, then six letters/numbers; for example, `ABCD0XXXXXX` is a **format illustration**, not a real branch. An account number must have 6–35 digits. Copy it from an approved bank proof and compare both entries before saving.

Choose **Add bank account**. The added account becomes current and all earlier versions stay in the table. To use an older account again, choose **Make current** on its row and confirm; the system copies it into a new current version. There is no delete or in-place account-number edit. Authorized Super/HR staff see full history; the linked employee sees the full current account in My profile. Do not put account numbers in notes, filenames, screenshots or support messages.

## Family, nominees and pay terms

Open **Family & nominees**. Authorized Super/HR staff see full details for the selected company; Field Officers and clients do not. Add family members separately from nominees. Choose each relationship from Common. The compact tables show existing rows with Edit and Delete actions; deletion is audited. You may record a family member's date of birth, mobile, address, occupation, education and whether they live with the employee. Ask only for information needed for the HR record.

Add nominees with their percentage shares. Optional Aadhaar and blood group may be recorded only when needed; entering Aadhaar requires confirmation that its holder consented. A stored number is **not** UIDAI/Surepass verification. Use synthetic numbers during development until HHCIL approves collection, retention and protection. You can save a draft below 100%. Choose **Mark nomination complete** only when shares total exactly 100%; reopen a completed nomination before editing. Check names and shares with the employee.

In **Bank & salary pay → Pay terms**, choose an effective date and an active Common payment mode. Monthly pay needs a **Pay scale on** choice: calendar days, scheduled working days, or fixed days such as 26. Per-day pay has no pay-scale basis. Older pay versions may say **Not specified**. Enter a positive gross rate for **As per employee**; leave it empty for **As per unit rate** until HHCIL approves those rules. Set applicable policy flags. **Save new version** retains earlier terms and must have a later effective date. These entries do not calculate payroll or issue a payslip. If HR cannot save, a Super Administrator should review `payroll.UPDATE`.

The employee sees their own currently effective family, nomination and pay terms in **Field Portal → My profile**. Future-dated pay changes are not shown there before they take effect. The employee cannot edit these records. Family, nominee and pay changes are outside the current profile-request form; ask HR to correct an error.

## Upload a document

Open **Documents** on the employee's Admin detail page. Choose the right type: **Aadhaar front**, **Aadhaar back**, **PAN**, **Voter ID**, **Bank proof**, **Signature**, or **Passport-size photo**. Other types are not accepted by this flow.

1. Choose the type **before** selecting the file. Use a PDF, JPG or PNG no larger than **5 MB**. A passport-size photo must be **JPG or PNG**, not PDF. Do not put an Aadhaar/PAN/account number in the filename.
2. Inspect the **Before upload** preview. Confirm it is the correct employee, correct side of the document, readable and upright. If it is wrong, choose **Choose another file**. A preview is for checking the file, not identity verification.
3. Choose **Upload version** and wait for success. The new file becomes the current version of that type; earlier versions remain in history unless separately removed.
4. Use **View** to inspect a saved file, or **Download** if your authorized task requires a copy. Downloads require a signed-in, permitted user; do not forward private files casually.

An employee can also open **Menu → My profile → My documents** in the Field Portal to upload permitted documents and view/download their own records. An authorized Field Officer uses **Menu → Collect documents**, searches for an employee at a granted site, selects the person, checks their identity, and uploads. Uploading requires a connection; it is not an offline punch queue.

The status **Received** means a file was uploaded. **Staff-reviewed** means a permitted staff member inspected it using **Mark reviewed**. Neither status means the number or identity was verified by a government or KYC service. Do not tell an employee or client that a file is KYC-verified on the strength of these labels.

## Correct or remove a wrong file

For a clearer or updated document, upload a new version of the same type. For a wrong employee's file or a file that should not be retained, an Admin user with **Document → Delete** permission can choose **Delete**, select a reason and confirm. This blocks access to that version and removes its private stored file; an audit record remains. An older version does **not** automatically become current. If the button is disabled, ask a Super Administrator to review permissions—do not use someone else's account. Employees and Field Officers should report a wrong file to authorized staff; they cannot delete it themselves.

Always confirm the employee and company before handling a sensitive record. Share documents only through HHCIL-approved channels, and do not use live personal documents in a local development database.

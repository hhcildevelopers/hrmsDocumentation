# 7. Employee personal details, bank details and documents

[← Handbook](README.md) · [Previous: troubleshooting](06-troubleshooting-and-terms.md)

These records are more private than the ordinary employee list. Work in the **correct company**, open **Employees → View**, and check the employee's name and code before entering anything. Only authorized HR/Super staff can edit personal and bank details. Field Officers may collect documents only for employees at granted sites when they have the required document permission. A client cannot open an employee's private HR record.

## Personal, address and statutory details

Open **Personal & bank**. In the personal section, enter the employee's father's name, date of birth and gender if known. The date picker uses a real past date; do not enter an estimated date just to complete the form. In the address section, put the current residence in **Present address** and the long-term residence in **Permanent address**. They may be the same, but confirm this with the employee. You may leave unknown optional fields blank and save an incomplete profile for later correction.

The statutory-ID fields have format checks:

| Field | What to enter | Avoid |
| --- | --- | --- |
| UAN | Exactly 12 digits, if issued | Spaces, a phone number, or a made-up UAN |
| ESIC | 10–17 digits, if issued | Guessing a number from another document |
| PAN | Five letters, four digits, one letter | Spaces or another person's PAN |
| Aadhaar | Exactly 12 digits, only under HHCIL's approved collection procedure | Using a screenshot or unapproved copy as proof of verification |

Example PAN **format**: `ABCDE1234F` (a fictional pattern; do not save this as an employee's ID). The form can hide or show entered numbers while editing. Collect only details HHCIL has approved and verified through its own procedure. Entering a number here does **not** verify it with UIDAI, Surepass or another KYC provider. During development, use synthetic data only; live full identity-data collection needs HHCIL's consent, retention and security policy first.

Employees open **Field Portal → Menu → My profile** to see their own read-only details. ID and bank account numbers are masked there. If anything is wrong, they should contact HR; editing the phone screen is not supported.

## Bank account: make a new version

In **Personal & bank → Bank account**, enter the official **Account holder name**, **Bank name**, **IFSC**, and **Full account number** twice. Choose Savings, Current or Salary only if known. IFSC has four letters, `0`, then six letters/numbers; for example, `ABCD0XXXXXX` is a **format illustration**, not a real branch. An account number must have 6–35 digits. Copy it from an approved bank proof and compare both entries before saving—do not guess from a masked value.

Choose **Save new bank version**. A correction creates another version; it does not erase earlier HR history. The screen displays only masked account numbers afterward, even to HR. The employee's My profile shows the current bank account masked. Do not put full account numbers in notes, filenames, screenshots or support messages.

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

# 10. Attendance reports

[← Handbook](README.md) · [Leave guide](09-leave-setup.md) · [Next: employee self-service →](11-employee-self-service.md)

The **Reports → Attendance** page lets an HR Administrator or Super Administrator view a company's attendance muster and save a report version. Select the correct company at the top of the Admin Portal first.

1. Choose a site or **All sites in selected company**.
2. Choose a period: calendar month, **21 to 20**, **26 to 25**, or **Custom dates**. Custom dates may cover 1 to 31 consecutive days. For a 21-to-20 report ending in October, choose October as the ending month; the report covers 21 September through 20 October.
3. Add a Payment Date only if needed for the report heading. This does not mean anyone was paid.
4. Click **Preview**. Scroll the table sideways to see all dates and totals. An all-sites preview has a separate section for each site in the selected company. A `?` marks a day that needs review, and the reason appears below that site's table. Correct the source record in **Attendance review** or **Leave requests**, then preview again. A missing punch is unresolved; it is not automatically an absence.
5. Once the period has ended and no days are unresolved, click **Finalize**. Confirm the selected company, site, dates and day codes. Use the saved version's **PDF** or **Excel** buttons to download the same saved data in either format. Preview by itself does not create a downloadable version.
6. If source attendance changes later, open the saved report under **Saved report versions** and **Reopen** it with a reason of at least 10 characters. Preview again and finalize a new numbered version. The older version remains available for audit, including its original downloads.

Common codes: `P` attended, `PW` worked an approved weekly off, `HD` half-day due to pending or rejected late approval, `WO` weekly off, `H` approved holiday without attendance or leave, `AB` absence explicitly marked by HR, `CO` compensatory off, and `CL`/`SL`/`PL` approved leave. A worked holiday or conflicting evidence currently appears as `?` until HR resolves the coding rule; do not force a different code to finish the report. Hours use the effective times after any authorized correction; a manual correction is **not GPS verified**. These codes and hours do not calculate wages.

If **Finalize** is unavailable, check for `?` days, a period that has not ended, or missing report permission. Ask HR to resolve the source records; changing the browser date will not help. If a PDF or Excel download fails, open the saved version again and try once more, then give IT the report version and error message. Do not send the downloaded employee report to another client or company.

This report is in development review. HR must approve the generated PDF layout and reconciliation rules before it is used for payroll or shared with clients. Word export, salary-derived data and Client Portal downloads are not available in this checkpoint. A saved report remains unchanged if source attendance or leave changes later; HR must review and create a new version where needed.

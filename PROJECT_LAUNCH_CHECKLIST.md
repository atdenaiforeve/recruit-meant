# Beyond the Horizon — pre-launch checklist

This checklist is for the project owner and the parent/guardian helping supervise recruitment. The recruitment system is **not open** until every required item below is completed.

## Current technical setup

- [x] Public GitHub repository exists.
- [x] Seven departments and 28 role listings are present.
- [x] Role numbers match the supplied list: 1, 2, then 4–29.
- [x] Every role-selection link carries the selected role forward.
- [x] Application preview contains the agreed contact choices: Email, Discord, Other.
- [x] The preview warns applicants not to provide phone numbers, home addresses, passwords or other sensitive information.
- [x] Production Cloudflare D1 database and application/status tables exist.
- [x] Production Cloudflare Worker is connected to the production D1 database.
- [x] Production application intake is disabled.
- [x] Production admin access is not configured.
- [x] Production database currently contains zero applications and zero status events.
- [x] Worker invocation logs and persisted logs are disabled.
- [x] GitHub Pages live site and latest page updates confirmed by the project owner.
- [x] Responsive phone and tablet styling added to the application page and shared stylesheet.
- [ ] Manual phone/tablet/desktop preview test completed using FIRST_TEST_GUIDE.md.
- [x] Separate fictional-only test database and test Worker created; production intake remains disabled.
- [x] Test form and test admin dashboard use a temporary shared PIN; the test Worker checks it server-side.
- [x] Test message field accepts any non-empty fictional text up to 120 characters without a special prefix; the isolated Worker stores it as the test message.
- [x] Test dashboard displays the submitted test message and experience field.
- [x] Isolated test submission and admin routes no longer require an ADMIN_TOKEN.
- [ ] Run the fictional-only submission test in a browser and verify the record in the isolated test database. Backend source is deployed and configured; browser runtime submission is not yet verified.
- [ ] Run the separate test dashboard check: review → status update → deletion.
- [ ] Worker health endpoint has been tested from a browser; the web check could not access the endpoint.

## Required before accepting real applications

1. A parent/guardian reviews the complete recruitment flow and agrees to supervise it.
2. Complete the privacy notice with:
   - the responsible adult/project contact method;
   - the exact reason each field is needed;
   - who can access application records;
   - how long each type of application is retained;
   - how applicants or guardians can request access, correction or deletion;
   - how deletion requests will be carried out.
3. Decide which contact methods are appropriate for applicants under 18. Do not require an applicant to provide a personal phone number, home address, school, password or exact birth date.
4. Before real recruitment, replace temporary test access with properly managed production access. Keep production administrator credentials out of GitHub, website files, screenshots and chat. A parent/guardian should supervise account security setup.
5. Keep test and production environments separate. Do not submit dummy records to the production database. Retain a safe way to delete test records and their status history.
6. Test the complete flow with dummy information only:
   - submit a test application after the guardian has approved testing;
   - confirm it appears in the private dashboard;
   - change its status and confirm the change is recorded;
   - delete the test record and its status history.
7. Verify the public site, API health check, form behaviour and admin access from a browser.
8. Only after all checks pass, have the responsible adult/project owner deliberately enable intake in Cloudflare and remove the preview-only launch lock in the website code.
9. Check the dashboard manually as planned. No automated email or notification system is configured.

## Security reminders

- Keep the admin page unlinked from public navigation.
- The temporary shared PIN is only for fictional test data. It is hardcoded in the isolated test Worker source and can be seen by anyone with access to that Worker in Cloudflare. It is not suitable for real applicant records.
- Replace the temporary test PIN before real recruitment. Do not reuse it as a personal account password.
- Never share production administrator credentials or give applicants access to the dashboard.
- Do not add applicants to the official game, project accounts or shared workspaces until permissions and supervision are agreed.
- Do not collect more personal information than is genuinely needed.
- If the privacy arrangements cannot be completed, keep intake disabled.

## Current launch decision

**NOT READY TO OPEN.** The live site has been confirmed by the project owner and mobile-responsive styling has been added. The manual device test, privacy review, guardian approval and isolated end-to-end test remain outstanding. Production intake remains disabled.

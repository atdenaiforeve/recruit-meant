# Beyond the Horizon — pre-launch checklist

This checklist is for the project owner and the parent/guardian helping supervise recruitment. The recruitment system is **not open** until every required item below is completed.

## Current technical setup

- [x] Public GitHub repository exists.
- [x] Seven departments and 28 role listings are present.
- [x] Role numbers match the supplied list: 1, 2, then 4–29.
- [x] Every role-selection link carries the selected role forward.
- [x] Application preview contains the agreed contact choices: Email, Discord, Other.
- [x] The preview warns applicants not to provide phone numbers, home addresses, passwords or other sensitive information.
- [x] Cloudflare D1 database and application/status tables exist.
- [x] Cloudflare Worker is connected to the D1 database.
- [x] Application intake is disabled in the Worker.
- [x] No admin token is configured yet.
- [x] The database currently contains zero applications and zero status events.
- [x] Worker invocation logs and persisted logs are disabled.
- [ ] GitHub Pages publishing and the live site have been independently verified.
- [ ] Worker health endpoint has been tested from a browser.

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
4. Configure the admin token as a Cloudflare Worker secret using the Cloudflare dashboard. Do not put it in GitHub, the website, screenshots, source code or chat. A parent/guardian should supervise this.
5. Test the complete flow with dummy information only:
   - submit a test application after the guardian has approved testing;
   - confirm it appears in the private dashboard;
   - change its status and confirm the change is recorded;
   - delete the test record and its status history.
6. Verify the public site, API health check, form behaviour and admin access from a browser.
7. Only after all checks pass, have the responsible adult/project owner deliberately enable intake in Cloudflare and remove the preview-only launch lock in the website code.
8. Check the dashboard manually as planned. No automated email or notification system is configured.

## Security reminders

- Keep the admin page unlinked from public navigation; the API token is the actual access control.
- Never share the admin token or give applicants access to the dashboard.
- Do not add applicants to the official game, project accounts or shared workspaces until permissions and supervision are agreed.
- Do not collect more personal information than is genuinely needed.
- If the privacy arrangements cannot be completed, keep intake disabled.

## Current launch decision

**NOT READY TO OPEN.** The technical foundation is partly in place, but the privacy review, guardian approval, admin access, live-site verification and end-to-end test remain outstanding.

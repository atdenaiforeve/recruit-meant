# Beyond the Horizon — first website test

**Test type:** Preview / device and navigation test  
**Status:** Ready for manual testing and no-token fictional submission check  
**Important:** This guide includes a fictional-only submission test against the isolated test Worker/database. It does not open recruitment or use the admin dashboard.

## Safety rules

- Use only the public preview website.
- Do not enter real names, ages, email addresses, Discord details, phone numbers, school details, passwords or other personal information.
- Do not ask friends or applicants to submit applications during this test.
- The Submit button is intentionally disabled. Do not try to bypass it.
- Do not share screenshots that show personal browser information, account names or private messages.

## Test devices

Test whichever devices are available:

- [ ] Android phone — portrait
- [ ] Android phone — landscape
- [ ] iPhone — portrait / landscape, if available
- [ ] iPad or other tablet — portrait
- [ ] iPad or other tablet — landscape
- [ ] Laptop or desktop

A device not available for testing should remain marked as **not tested**, not passed.

## Test links

- [Project overview](https://atdenaiforeve.github.io/recruit-meant/)
- [Requirements](https://atdenaiforeve.github.io/recruit-meant/requirements.html)
- [Roles](https://atdenaiforeve.github.io/recruit-meant/roles.html)
- [Application preview](https://atdenaiforeve.github.io/recruit-meant/application.html)
- [Isolated test submission form](https://atdenaiforeve.github.io/recruit-meant/test-application.html)
- [Isolated test admin dashboard](https://atdenaiforeve.github.io/recruit-meant/test-admin.html)
- [Privacy draft](https://atdenaiforeve.github.io/recruit-meant/privacy.html)

## Test 1 — page layout

On each available device:

- [ ] The page loads without an error.
- [ ] The site title and navigation are readable.
- [ ] No text or controls are cut off.
- [ ] There is no sideways scrolling at normal zoom.
- [ ] Buttons and links are easy to tap.
- [ ] Text fields fit the screen.
- [ ] The page works in portrait and landscape where supported.

## Test 2 — recruitment journey

1. Open the project overview.
2. Follow **Continue to requirements**.
3. Open the roles page.
4. Expand a role description.
5. Choose a role.
6. Confirm that the chosen role appears on the confirmation page.
7. Tick the confirmation checkbox and continue.
8. Confirm that the application preview displays the same selected role.

Checks:

- [ ] Navigation works between all public pages.
- [ ] Role descriptions expand and collapse.
- [ ] The selected role carries through to confirmation.
- [ ] The selected role carries through to the application preview.
- [ ] The privacy draft link opens.

## Test 3 — isolated submission test (no admin token)

1. From the roles page, choose a role.
2. On the confirmation page, use **Run isolated test submission**.
3. Confirm the role is carried into the test form.
4. Use only the fixed fictional test identity and contact details already filled in.
5. Tick the test-data acknowledgement and submit once.
6. Record the returned test ID. The record is stored only in `BTH_FIRST_TEST_DB`.
7. Verify the record exists in the test database using the Cloudflare D1 console/API. Do not use the production database.

**No ADMIN_TOKEN is needed for this submission test.** The test Worker accepts only the fixed fictional name, email, motivation, allowed role and test age range. The admin dashboard remains separate and locked for now.

## Test 4 — admin dashboard (later, separate test)

When the project owner is ready to test admin review, configure a fresh `ADMIN_TOKEN` secret on `bth-first-test` in Cloudflare. Then connect the dashboard using that secret, load the test record, update its status, and delete the fictional record and status history. Never put the token in GitHub, a chat message, or a source file. Parent/guardian supervision is recommended for this later setup.

## Test 5 — application preview controls

Use fictional placeholder text only, such as `TEST ONLY`. Do not enter real contact details.

- [ ] Name field is easy to select and type into.
- [ ] Age-range selector opens and options are readable.
- [ ] Text areas are usable on the device keyboard.
- [ ] Tool checkboxes are large enough to tap.
- [ ] Choosing **Other** for contact reveals the extra method field.
- [ ] Choosing Email or Discord hides the extra method field.
- [ ] Privacy acknowledgement checkbox is easy to tap.
- [ ] The Submit button remains disabled and says applications are not open.
- [ ] The page clearly explains that this is a preview and does not accept applications.

**Do not attempt to submit.** The disabled state is expected and is a pass for this preview test.

## Test 6 — report issues

For each issue, record:

- Device type and approximate screen size
- Browser name
- Page URL
- What you expected
- What happened instead
- Screenshot with personal information excluded

Do not send passwords, access tokens or private contact information in a bug report.

## What this first test does not prove

This test checks the public website's appearance, navigation and preview controls. It does not prove that application records can be safely submitted, stored, reviewed or deleted.

The production Worker is still configured with intake disabled. Its admin token is not configured. The production database must not be used for test submissions.

Before a separate end-to-end test, a parent/guardian should review the plan and the project needs an isolated test database and test Worker, a supervised admin access setup, and a way to remove test records. Keep real recruitment closed until that separate test is complete and the privacy arrangements are approved.

# Beyond the Horizon — first website test

**Test type:** Preview / device and navigation test  
**Status:** Ready for manual testing  
**Important:** This is not an application-submission test. Recruitment remains closed.

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

## Test 3 — application preview controls

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

## Test 4 — report issues

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

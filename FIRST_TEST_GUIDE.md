# Beyond the Horizon — first website test

**Test type:** Preview / device, navigation and isolated fictional submission test  
**Status:** Normal-style test application form published without an applicant PIN; end-to-end browser verification still required  
**Important:** The test application form is open for fictional test submissions only. The separate test admin dashboard remains passcode-protected. Production recruitment remains closed.

## Safety rules
- Use only the public preview website and isolated test pages.
- Do not enter real names, ages, email addresses, Discord details, phone numbers, school details, passwords or other personal information.
- Do not ask friends or applicants to submit applications during this test.
- The fixed fictional identity is `TEST APPLICANT` and the fixed fictional Roblox username is `FAKE_TEST_USER`. Fill the form with made-up test values only. The message field accepts fictional text up to 120 characters; never enter real personal or contact details.
- Do not share screenshots that show personal browser information, account names or private messages.

## Test devices
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

## Test 3 — open isolated test submission
1. From the roles page, choose a role.
2. On the confirmation page, use **Run isolated test submission**.
3. The test application form opens directly; there is no applicant PIN screen.
4. Confirm that the selected role is carried into the test form.
5. Fill the form with fictional values only. The display name is fixed as `TEST APPLICANT`.
6. Tick the test-data acknowledgement and submit once.
7. Record the returned test ID.
8. Verify the record exists in BTH_FIRST_TEST_DB, not the production database.

The test submission endpoint accepts the normal-style form without an applicant PIN. It is restricted to the isolated test Worker and test database, uses a fixed fictional display name, validates role and age-range values, and caps the test database at 100 records. This is not a real recruitment endpoint. Never enter real personal or contact information.

## Test 4 — test dashboard
1. Open the isolated test admin dashboard.
2. Enter the same temporary test passcode.
3. Load the fictional test submission.
4. Change its status if needed.
5. Delete the fictional test record and its status history when finished.

The same passcode protects the isolated test dashboard's read, status-update and delete routes. There is no separate admin token in this test setup. This is a temporary shared-PIN arrangement, not production-grade account security.

## Test 5 — normal-style test form controls
Use fictional placeholder text only. Do not enter real contact details.
- [ ] The fixed fictional test identity and Roblox username are displayed.
- [ ] Age-range selector opens and options are readable.\n- [ ] The Roblox username field is included in the normal application and a fake fixed value is used in the test form.
- [ ] The combined role-interest, skills and experience question accepts fictional test text.
- [ ] Tool checkboxes are large enough to tap.
- [ ] The Other tools field appears only when Other tools is selected and accepts fictional test text.
- [ ] The Other contact method field appears only when Other is selected.
- [ ] Contact method and test message fields work.
- [ ] Privacy/test acknowledgement checkbox is easy to tap.
- [ ] Submit button sends to the isolated test database and returns a test ID.

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
This test checks page layout, navigation, and the isolated fictional submission workflow. The admin dashboard remains passcode-protected. It does not prove that real applicant records can be safely submitted, stored, reviewed or deleted.

The production Worker remains intake-disabled and the production database must not be used for test submissions. Keep real recruitment closed until a parent/guardian has reviewed the privacy arrangements and the temporary test PIN has been replaced with a properly managed secret.

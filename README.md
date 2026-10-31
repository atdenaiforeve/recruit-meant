# Beyond the Horizon — developer recruitment

This repository contains the developer recruitment website for the Roblox project **Beyond the Horizon**.

## Website pages

- [Project overview](index.html)
- [General requirements](requirements.html)
- [Available roles](roles.html)
- [Role confirmation](confirm.html)
- [Application preview](application.html)
- [Privacy and applicant safety draft](privacy.html)

## Recruitment status

**Applications are not open.** The website is still in preview while the privacy arrangements, guardian review, admin access and live deployment checks are completed. Do not enter or submit real personal information.

All listed positions are voluntary and unpaid. The available roles are numbered 1, 2, and 4–29, matching the project's supplied role list.

## Technical overview

- Static website hosted from this repository if GitHub Pages is enabled.
- Cloudflare Worker provides the application API.
- Cloudflare D1 stores application records and status history.
- The application form includes a launch lock. The Worker also independently keeps intake disabled.
- The private admin dashboard requires a Cloudflare Worker secret; no admin token is stored in this repository.
- Automated email or notification messages are not configured.

## Before opening recruitment

Read [PROJECT_LAUNCH_CHECKLIST.md](PROJECT_LAUNCH_CHECKLIST.md). A parent/guardian must review and approve the privacy and applicant-safety arrangements before any real applications are accepted.

# Hub Assistant Privacy Website — GitHub Pages

Static privacy/support website for **Hub Assistant**, published by **A.I MY**.

Contact: `thiaimynguyen734@gmail.com`

## Current policy reference

- Reference package: **Hub Assistant 1.9.24 — 22 October 2026 final handoff**
- Source snapshot: **2f0713a7fa926c42bafb9c64cffbb1b180d7bd27**
- Manifest version: **1.9.24**
- Manifest version name (unchanged): **1.9.24 Halloween TEST_ONLY 20261020**
- Package date / website policy review / policy effective date: **22 October 2026**
- Reference extension ZIP: **HubAssistant-final-extension.zip**
- Reference ZIP SHA-256: **5df7f181ecd1614fce7e1cd984586c3407b2456fcc9d7d3b8536a10bdcd446cd**
- Verification status: **offline verified; owner native account/workflow acceptance pending**

This policy reference replaces the earlier September package reference. It does not assert a new live pass, store upload, store approval, or deployment. The website update does not change the extension package, manifest, permissions, runtime API, or data-handling implementation. The referenced ZIP is not hosted in this public policy repository.

Current data-handling points reflected by the website:

- PowerHub guidance runs on `https://vas.educator.powerschool.com/*`.
- PowerSchool SIS / PowerTeacher guidance runs on `https://vas.powerschool.com/*`.
- After a teacher explicitly opts in to Vietnamese natural-name display, the extension may request the current section roster from PowerSchool's same-origin `/ws/xte/student` endpoint.
- Student names, PowerSchool IDs, Student Code, roster payloads, and name maps used by the SIS name-display feature remain RAM-only; only its boolean opt-in `sisVietnameseNameDisplayEnabledV1` is persisted.
- No roster or student data is sent to an A.I MY backend or analytics service.
- Teacher-role preferences, walkthrough/resume progress, and certificate offer/issuance records remain in the browser profile. These records are not verified per-school-account records and do not contain the certificate name, quiz answers, or score.
- Quiz details remain in activity-page memory and are cleared before certificate-name entry. The name is used locally to render a PNG; downloaded PNGs retain the name and must be deleted separately.
- Active walkthroughs can use extension session storage. Grade Entry language changes also use per-tab PowerSchool `sessionStorage` for temporary navigation/guide/display state, including URL context and class/term labels. Handoff validation accepts an age of at most two minutes; this is not a timer that guarantees physical deletion at that age.

This website package contains no JavaScript, analytics, advertising, tracking pixels, web forms, or external font/CDN dependency.

## Recommended repository name

Create a public GitHub repository named:

`hub-assistant-privacy`

With GitHub Free, GitHub Pages is available for public repositories. This package is intentionally static so it can be published directly from a branch without a build tool.

## Files to upload

Upload the contents of this folder to the repository root:

- `index.html`
- `privacy.html`
- `safeguarding.html`
- `support.html`
- `styles.css`
- `.nojekyll`
- `README.md`

Do not upload real student/staff data, extension logs containing personal data, credentials, or private deployment files to this public repository.

## Publish with GitHub Pages

1. Sign in to GitHub and create a **public** repository named `hub-assistant-privacy`.
2. Upload all files in this folder to the repository root and commit them to the default branch, normally `main`.
3. Open the repository **Settings**.
4. In the left sidebar, open **Pages**.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
6. Choose the `main` branch and `/(root)` folder, then save.
7. Wait for the GitHub Pages deployment to finish.
8. Open the Pages URL shown by GitHub and verify all four pages.

Expected project-site URL pattern:

`https://artporttrairt-stack.github.io/hub-assistant-privacy/`

Then use:

- Privacy policy: `https://artporttrairt-stack.github.io/hub-assistant-privacy/privacy.html`
- Support: `https://artporttrairt-stack.github.io/hub-assistant-privacy/support.html`
- Safeguarding: `https://artporttrairt-stack.github.io/hub-assistant-privacy/safeguarding.html`
- Homepage: `https://artporttrairt-stack.github.io/hub-assistant-privacy/`

## Store fields

Recommended current values:

- Product: `Hub Assistant`
- Publisher: `A.I MY`
- Support email: `thiaimynguyen734@gmail.com`
- Privacy email: `thiaimynguyen734@gmail.com`
- Chrome initial visibility: `Unlisted`
- Edge initial visibility: `Hidden`
- Remote code: `No`
- A.I MY analytics/telemetry: `No`

After GitHub Pages is live, copy the real URLs from above into the Chrome Web Store and Microsoft Edge Add-ons metadata. Do not submit placeholder URLs.

## Important hosting note

This site itself contains no A.I MY tracking or analytics code. GitHub Pages is the hosting provider. GitHub documents that visitor IP addresses are logged and stored for security purposes when GitHub Pages sites are visited. The privacy page includes this hosting note so the website disclosure is not confused with the extension's own data-handling behavior.

## Official GitHub documentation

- Creating a GitHub Pages site: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- Configuring a publishing source: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Before using the URLs in a store submission

Verify:

- the Pages site opens without signing in;
- `privacy.html` opens directly from a new/private browser window;
- `support.html` shows the correct email;
- no real student/staff data appears anywhere in the public repository;
- the publisher name is `A.I MY`;
- the privacy policy still matches the exact extension build being submitted.

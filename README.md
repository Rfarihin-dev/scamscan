# ScamScan

An offline message checker for customers of trading and financial platforms. Paste a message to review possible scam indicators and steps for verifying the request safely.

## Run

Open `index.html` in a modern browser. The entire app is contained in this file: inline CSS and vanilla JavaScript, without frameworks, packages, API keys or a build step.

## Features

- English and Bahasa Malaysia interfaces, sample messages and advice.
- Weighted rules for pressure, credential requests, remote access, payments, suspicious domains, unrealistic offers, impersonation and private-channel requests.
- A 0–100 risk score, exact text highlights and explanations.
- Verification guidance, emergency actions and a copyable report.
- Responsive layout, keyboard navigation, result announcements and reduced-motion support.
- No message uploads, analytics or persistent storage.

## Scoring and limits

Each detected rule category contributes once. The total is capped at 100: 0–24 is Likely Safe, 25–59 is Suspicious, and 60–100 is High Risk. The score reflects rule matches, not a measured probability of fraud.

Rules are stored in the `RULES` array. UI text, samples and guidance are stored in `I18N`. The app checks text locally; it does not authenticate senders, visit links or query live threat databases. A low score does not establish that a message is legitimate.

## Deploy to GitHub Pages

The repository includes `.nojekyll` so GitHub Pages can serve the single-file app directly.

In **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/ (root)**, then save. GitHub will show the published URL after deployment completes.

The expected site address is https://rfarihin-dev.github.io/scamscan/ . This address is available only after Pages has been enabled and its deployment has succeeded.

## Deploy to Vercel

Import this repository in Vercel. Select the **Other** framework preset, use the repository root, leave the build command empty and serve the root directory. No environment variables are required.

## Open in Antigravity

Clone this repository into a new local folder and open the folder in Antigravity. All application code is in `index.html`; there are no dependencies to install.

## Design reference

Hierarchy and information grouping were informed by a publicly shared Wise screen credited to Mobbin: https://fivetaco.com/products/mobbin. The app does not include third-party screenshots or remotely loaded assets.

ScamScan is an independent tool and is not affiliated with Deriv.

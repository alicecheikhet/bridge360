# BRIDGE360 — The Encore Effect

**A GitHub-ready, interactive audience-loyalty prototype for Musical Bridges Around the World (MBAW), developed as an independent DECA Business Operations Research strategic-plan concept.**

> Not an official MBAW app. The dashboard contains illustrative scenario data, not verified MBAW research or outcomes. Event dates, venues, artist participation and concept programs must be verified before public use.

## What makes it different

The underlying problem is not a lack of concerts or an absence of an app: it is the **potential gap between a successful first concert and a measurable second visit**. BRIDGE360 turns that gap into a connected cultural journey.

| Component | What it does | Retention problem addressed |
| --- | --- | --- |
| **BRIDGE ID** | Voluntary profile, interests, accessibility choices, local activity | Disconnected audience touchpoints |
| **BRIDGE MATCH** | Live, explainable interest-based concert matching | Uncertainty about relevance of future shows |
| **ENCORE EXCHANGE** | Signature concert-A-to-concert-B artistic handoff | No clear next step after the final applause |
| **72-HOUR ENCORE** | Preview of a personalized post-event invitation | Lost momentum after a positive experience |
| **BRIDGE QUEST** | Cultural passport, meaningful missions and digital recognition | Lack of ongoing engagement between shows |
| **CULTURAL MICRO-STORIES** | Interactive short learning experiences | Limited connection between performances |
| **PASS IT FORWARD** | Shareable friend invitation and ambassador mission | Weak referral pathway |
| **DEMO CHECK-IN** | Try an attendance event and watch passport update | No obvious measurement of repeat attendance |
| **BRIDGE PULSE** | Scenario switcher, retention charts, journey funnel, budget | Reach measured instead of repeat attendance |
| **EVENTS** | Search, filters, demo itinerary | Difficulty discovering next relevant event |

## Run locally

Requires Node.js 20+.

```bash
npm install
npm run dev
```

Open the local URL printed by Vite (usually http://localhost:5173).

## Publish on GitHub Pages (free)

1. Create a **new GitHub repository** named `bridge360`.
2. Upload **all files and folders from this project**, including `src`, `index.html`, `package.json`, and `.github/workflows/deploy.yml`.
3. Open the repository's **Settings → Pages** and choose **Source: GitHub Actions**.
4. Push a commit to the `main` branch. The included workflow builds and deploys the site.
5. Open the deployment URL shown under **Actions** or **Settings → Pages**.

The Vite configuration uses `base: './'`, allowing the same static build to work on GitHub Pages project paths.

## File structure

```text
bridge360-github/
├── .github/workflows/deploy.yml  # Automatic GitHub Pages deployment
├── .gitignore
├── index.html                    # HTML shell
├── package.json                  # Dependencies and commands
├── vite.config.js                # Vite build settings
├── README.md                     # Instructions and strategic framing
└── src/
    ├── main.jsx                 # React entry point
    ├── App.jsx                  # Complete interactive app
    ├── data.js                  # Events, cultural stories, quests, demo analytics
    └── styles.css               # Responsive visual design
```

## How to demo for DECA judges (90 seconds)

1. **Discover**: explain the real research question: *Why do first-time attendees fail to turn into repeat participants?*
2. **Bridge Match**: click musical interests and show recommendations change instantly.
3. **Encore Exchange**: demonstrate the Armenian-to-vocal handoff; click **Accept the handoff**.
4. **Cultural Passport**: show the Encore Effect mission unlock, then complete a micro-story.
5. **Impact Lab**: switch **Baseline → Target pilot** and explain the proposed 90-day return rate and cost-per-incremental-return metrics. **Say these are scenarios, not achieved results.**

## Research and implementation guardrails

- This is a **front-end proof of concept**, not a production ticketing or CRM system.
- `localStorage` stores data only on the current browser/device. No server or database is used.
- The **Save my seat** action is a *demo itinerary save*, not a real ticket reservation.
- The **72-hour encore** is a preview only; no email is sent.
- Sharing copies invitation text when clipboard access is allowed.
- Dashboard values and budgets are **illustrative assumptions**. The $800 allocation is a proposed pilot budget; it is not a quote or expense report.
- The demo does not authenticate users, validate attendance, protect real personal data, or send analytics to MBAW.
- The recommendation algorithm is transparent tag matching, not an AI model or a promise of statistical accuracy.
- Dates and sample programs in `src/data.js` include prototype concepts and unverified venue/time details. Update from the official MBAW calendar before presenting as confirmed.

## Proposed real-world pilot architecture

For an approved deployment, integrate a consent-based attendee identifier with existing MBAW ticketing/check-in tools; record first-time attendance and 90-day returns; send opt-in event-specific follow-ups; and compare a pilot cohort with a comparable group receiving standard communication. Target **≤3 recurring staff hours per concert**, **≤$800 pilot expenses**, and **≤$25 cost per incremental returning attendee**. Those are design constraints and targets, not guaranteed outcomes.

### Primary metric

`90-day repeat-attendance rate = first-time attendees who check in to another eligible event within 90 days / eligible first-time attendee cohort`

### Secondary metrics

- Concert A → Concert B check-in conversion
- Recommendation engagement and subsequent attendance
- Cross-program participation
- Incremental returning attendees vs. comparison group
- Pilot cost / incremental returning attendees

## Customize

- **Events, musical traditions, quests, and sample charts:** `src/data.js`
- **App pages, interactions, and scenario logic:** `src/App.jsx`
- **Colors, typography, layouts, and responsive styling:** `src/styles.css`
- **Brand and page metadata:** `index.html`

## License and brand note

Created for an independent educational competition concept. MBAW's name is used to describe the proposed client organization; no official affiliation or endorsement is implied. Do not upload private customer data or copyrighted artist media without permission.

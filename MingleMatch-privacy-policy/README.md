# MingleMatch Content Manager — Privacy Policy

Public privacy policy for the private MingleMatch Content Manager Pinterest API application.

## Public website

**URL:** https://gandzekas.github.io/minglematch-privacy-policy/

Hosted on GitHub Pages (free, HTTPS enforced). Source lives in this repository.

## GitHub repository

**Source:** https://github.com/gandzekas/minglematch-privacy-policy

## Purpose

This policy describes how the MingleMatch Content Manager application processes personal data. The application is a private, owner-operated tool that manages the MingleMatch Pinterest Business account via the Pinterest API (Pin creation, scheduling, analytics). It is not a public SaaS and does not serve external users.

## Deployment

GitHub Pages is enabled on the `main` branch, root path (`/`). Pushing changes to `main` automatically rebuilds and redeploys the site.

To update the policy:

1. Edit `index.html`.
2. Commit and push to `main`:
   ```bash
   git add index.html
   git commit -m "Update privacy policy"
   git push origin main
   ```
3. GitHub Pages redeploys automatically (typically within 1–2 minutes).
4. Verify at https://gandzekas.github.io/minglematch-privacy-policy/

## Data-handling assumptions (verified during research)

- **Operator:** Individual operating under the MingleMatch brand, based in Lithuania (EU). GDPR applies.
- **Application scope:** Private, single-owner application managing only the Operator's own Pinterest Business account. No external users, no public SaaS.
- **Contact email:** `couplecorner.etsy@gmail.com` — address already used in project documents; mailbox ownership not independently verified.
- **Pinterest OAuth:** Application receives OAuth access/refresh tokens and the permissions approved on the Pinterest consent screen. Requested scopes: `boards:read`, `boards:write`, `pins:read`, `pins:write`. Analytics scopes only after verifying endpoint requirements.
- **Token storage:** OAuth tokens stored locally on the Operator's Windows computer using Windows Data Protection API (DPAPI). Design claim, not an independently audited security certification.
- **Local records:** Publication-queue state, Pin IDs/URLs, error/retry records, analytics observations stored in a local SQLite queue. Retained until the Operator requests deletion.
- **Data sharing:** Data is disclosed to Pinterest when using authorized API functions, and to Cloudflare/GitHub Pages only to the extent necessary to host the public policy page. No personal data is sold or used for advertising through this application.
- **AI-assisted processing:** No external AI providers process Pinterest account data, tokens, or analytics through this application. (Any AI image generation for Pins is a separate workflow outside this policy's scope.)
- **International transfers:** Pinterest is a US-based service; data processed via the Pinterest API may be transferred outside the EEA under Pinterest's own terms.
- **Cookies/tracking:** The policy page is a static HTML file with no cookies, analytics, or advertising trackers. GitHub Pages may process ordinary web-request information (IP address) under its own terms.
- **Children's privacy:** The application is not intended for children.

## Unresolved privacy / compliance questions

1. **Contact email verification:** `couplecorner.etsy@gmail.com` is used throughout project docs but mailbox ownership has not been independently confirmed. Confirm before publishing if this is the intended public contact address.
2. **DPAPI claim:** Local token encryption via Windows DPAPI reflects the application's design but is not an independently audited security control.
3. **Pinterest form validation:** Pinterest's Connect App form requires the privacy-policy URL to include the company name. `https://gandzekas.github.io/minglematch-privacy-policy/` contains "minglematch" in the path and is intended to satisfy this, but has not been submitted through the live Pinterest form as part of this task.
4. **Pinterest developer application:** Not created or submitted. The privacy-policy URL is ready to paste into the Connect App form when the application is created.

## Pinterest readiness

The public URL is ready to paste into Pinterest's Connect App "Link to Privacy policy" field:
- Public and accessible without authentication
- Served over HTTPS
- Contains the company name ("minglematch") in the URL path
- Not presented as Pinterest-endorsed

Do not submit the Pinterest developer application as part of this task.

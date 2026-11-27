# 合拍 Vowstyle — Wedding matching demo

A mobile-friendly, Traditional Chinese concept demo for Hong Kong couples to discover bridal makeup artists and wedding-day photographers by style, service budget and location.

**This is an interactive pretotype, not a production marketplace. All eight vendors, packages and prices are fictional.**

## Try the demo

**[Open the GitHub Pages demo](https://willychow2001.github.io/vowstyle-wedding-demo/)** · **[Open the MVP and trial handbook](https://willychow2001.github.io/vowstyle-wedding-demo/launch-kit.html)**

The public demo is hosted on GitHub Pages. Static website files are at the repository root, matching the repository's Pages configuration: `main` branch, `/ (root)`.

1. Choose bridal makeup or wedding-day photography.
2. Select one or two preferred styles.
3. Enter a budget, optional wedding date and location.
4. Explore the recommended sample packages.
5. Save up to three vendors for comparison, or copy an editable inquiry message.

The [MVP and pretotype handbook](launch-kit.html) is part of the site. A [downloadable development specification](MVP-and-pretotype.md) covers the two-week manual experiment, merchant pricing test, proposed data model, matching interfaces and acceptance checks.

## Desktop and mobile views

[View the screenshot gallery](screenshots/README.md) · [Download all screenshots](screenshots/vowstyle-desktop-mobile.zip)

Full pages, matching steps, package/inquiry dialogs, vendor comparison and empty results are included. Mobile captures use a 500 CSS px responsive browser viewport.

## Run locally

Requires Python 3 for the local server. Node.js 20 or later is required only for the checks. There are no npm dependencies and no build step.

```sh
npm start
```

Open `http://localhost:3000`. Alternatively:

```sh
python3 -m http.server 3000
```

## Check the matching rules

```sh
npm test
```

The eight checks exercise service separation, budget boundaries, location eligibility, style overlap, ranking and empty results. They are logic checks; they do not substitute for browser, accessibility or mobile layout testing.

## Repository layout

```text
index.html                 Main page and matching journey
launch-kit.html            Founder-facing MVP and trial handbook
MVP-and-pretotype.md        Downloadable detailed specification
app.js                     Sample data and interactions
styles.css                 Responsive styles
assets/                    Three wedding mood images
.nojekyll                  Serve static files without Jekyll
tests/matching.cjs         Matching rule checks
screenshots/               Desktop and mobile screenshot gallery
package.json               Local run and check commands
ASSETS.md                  Image sources and demo limitations
```

## Implemented

- Two service categories and four sample style directions.
- Budget and location filtering, followed by style ranking.
- Up to three recommendations with plain-language reasons.
- Sample package details, inclusions and additional charges.
- Three-vendor comparison, removal and an empty state.
- Editable inquiry message and clipboard copy with a manual-copy fallback.
- Responsive layouts, keyboard focus styles and native modal dialogs.
- No-match handling without silently relaxing the user's conditions.

## Prototype boundaries

- No database, accounts, live availability, real merchant contacts, payments or analytics reporting.
- Favorites last only until the page is refreshed.
- Clicking or copying does not send a message or make a booking.
- Images are wedding mood references, not vendor portfolios; makeup style validation requires authorized close-up makeup images.
- The current sample ranking is intentionally simple. The handbook describes a fuller production matching policy, which is not implemented here.
- External Google Fonts may load; system fonts are used if unavailable. The demo has no application tracking integration.
- Do not treat sample interactions as evidence of real demand or merchant willingness to pay.

## Hosting on GitHub Pages

In Settings → Pages, use **Deploy from a branch**, select **main**, and choose **/ (root)**. Changes to the website files are published through GitHub's Pages deployment service. No credentials belong in this repository.

## Next validation step

Recruit authorized real vendors, replace sample portfolios, and run the manual pretotype before implementing the proposed Next.js/Supabase MVP. See the handbook for consent, interview, pricing and launch checks.

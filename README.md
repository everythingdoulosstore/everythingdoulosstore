# Everything Doulos Store

Static single-page site. No build step, no dependencies.

## Files
- index.html: the whole site (HTML, CSS, JS)
- assets/favicon.svg
- vercel.json: clean URLs, security and cache headers
- package.json: only provides `npm run dev`
- robots.txt, .gitignore

## Run locally
`npm run dev`, or open index.html in a browser.

## Deploy to Vercel
Push to GitHub, import the repo in Vercel, set Framework Preset to "Other", leave Build Command and Output Directory empty, then Deploy.

## Editing links and dates
All links and the launch date live in the `CONFIG` object near the bottom of index.html (WHATSAPP_NUMBER, SELAR_URL, CARDS_NG_URL, CARDS_INTL_URL, JOURNAL_URL, YOUTUBE_URL, INSTAGRAM_URL, TIKTOK_URL, EMAIL_URL, LAUNCH_DATE). FACEBOOK_URL is still empty.

## Still open
- Notify Me form only shows a confirmation. Connect it to Mailchimp, Brevo, ConvertKit or Formspree to store emails.
- Replace the placeholder logo and card mockups with real brand assets.
- Add Privacy Policy and Terms pages (footer links are placeholders).

# Everything Doulos Store

Static, single-page launch site. No build step, no dependencies.

## Structure
```
everything-doulos-store/
├── index.html        # the whole site (HTML + CSS + JS)
├── assets/
│   └── favicon.svg
├── vercel.json       # clean URLs, security + cache headers
├── package.json      # only provides `npm run dev`
├── robots.txt
├── .gitignore
└── README.md
```

## Run locally
```
npm run dev
```
(or just open `index.html` in a browser)

## Deploy to Vercel
**Dashboard:** push to GitHub → vercel.com → Add New Project → import repo → Framework Preset "Other" → Deploy.
**CLI:** `npm i -g vercel` then `vercel` (preview) / `vercel --prod`.

## Still to fill in
All links are set in one place: the `CONFIG` object at the top of the `<script>` in `index.html` (WhatsApp number, Selar, YouTube, Instagram, Facebook, TikTok, and `LAUNCH_DATE`). Until a value is filled, its links are inert instead of broken.

Other open items:
- Real logo (replace inline SVG in nav + `assets/favicon.svg`)
- Product photography (replace illustrated card mockups)
- OG share image + `og:image` / `og:url` meta tags
- Privacy Policy and Terms & Conditions pages (footer links are `#`)

## Needs wiring
- **Notify Me form** only shows the confirmation message; it does not store emails. Connect to Mailchimp / Brevo / ConvertKit / Formspree, or a Vercel serverless function.

## Built-in behaviour
- Countdown targets `CONFIG.LAUNCH_DATE` (browser local time). After that date the site switches to its live state: "We're Live!", every "Launching 1 November 2026" label becomes "Available now", and all Selar buttons read "Buy Now on Selar". If the launch moves, change `LAUNCH_DATE`.
- Brand colours live in the `:root` CSS variables at the top of `index.html`.
- Fonts: Fraunces + Inter via Google Fonts.

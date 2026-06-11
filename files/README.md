# Deploying the Switzerland trip site

One static file, no build step.

## Fastest way (60 seconds)
1. Go to https://vercel.com/new
2. Drag this folder (or just `index.html`) into the upload area — Vercel treats `index.html` as the homepage automatically.
3. Hit Deploy, copy the URL, send it on WhatsApp.

## Via CLI
```bash
npm i -g vercel
cd <this folder>
vercel --prod
```

## Customising
- **Images**: all photo URLs live in one `IMG = {...}` object near the top of the `<script>`. Swap any value for your own image URL; anything missing or broken automatically falls back to the flat alpine illustration.
- **Prices**: the `ACTS`, `FLIGHTS`, `HOTELS`, `PASSES`, `FOOD` arrays hold every number. CHF prices are per person; `flat` prices are INR for two. Exchange rate is the `R` constant (₹105/CHF).
- **Budget**: change the `BUDGET` constant (currently 600000).

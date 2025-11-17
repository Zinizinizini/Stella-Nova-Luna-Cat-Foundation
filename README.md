StellaNovaLuna Foundation — README.md

StellaNovaLuna Foundation — a nonprofit supporting homeless cats. Donations and creator fees from the Solana token $Fuzzball help pay for food, vet bills, rehabilitation and long-term care. Started from the TikTok channel @StellaNovaLuna_catSister
.

Table of contents

Project overview

Live demo / Deploy

Donation & token info

Features

Pages & React components

Media & assets used

Embeds (Dexscreener / YouTube / TikTok)

How to run locally

Accessibility & privacy notes

Contributing

License & credits

Contact / Socials

Project overview

This repo contains a small nonprofit website for the StellaNovaLuna Cat Foundation, showcasing the mission, donation flow, gallery of rescued cats (Luna, Stella, Nova, Garfield), impact stories, partners/community, and a video showcase. The site accepts donations to a Solana wallet and highlights the $Fuzzball token and supporting partners.

Primary goals:

Provide a clear donation path (Solana wallet + $Fuzzball links).

Tell rescue & impact stories.

Show gallery and video highlights.

List partners and community links.

Be deployable on GitHub Pages or any static host.

Live demo / Deploy

You can deploy via GitHub Pages:

Push repo to GitHub.

Settings → Pages → Source: main branch /root.

Visit https://<your-username>.github.io/<your-repo>/

(You can also host on Netlify, Vercel, or any static host.)

Donation & token info

Primary donation Solana wallet (on-chain):
5rrJJykVDgeMYWiXRvMoMjGZiYyDj6791kiymaETXM4K — display prominently with one-click copy and QR code.

Token: $Fuzzball (Solana)
Live on Pump.fun:
https://pump.fun/coin/FhBE94EG8E2LyckpzWNLo6DmQvDr3zHsLU6BDRVZpump

Partners / supporting services

Fastex exchange — www.fastex.space

Shmoogle AI — https://shmooglestore.company.site/ and Telegram bot https://t.me/shmooglememe_bot

YouTube playlist & channel support (see Partners section below)

Security / UX suggestions: show wallet as text and QR, let users copy the address, and add a short warning to always verify addresses before sending funds.

Features

Hero section with CTA (Donate / Learn more).

Mission & Stats block (food / vets / animals helped).

Donation panel (copy wallet, QR, links to trade $Fuzzball).

Gallery (Luna, Stella, Nova, Garfield, plus uploaded images).

Impact Stories — timelines and follow-ups for helped animals.

Partners & Community block (YouTube, Pump.fun, Fastex, Shmoogle).

VideoShowcase with embedded YouTube video and TikTok thumbnail linking to TikTok.

Responsive layout, accessible markup, and light/dark theme switch (optional).

Pages & React components

The UI is split into small components (suggested filenames). Each file should live in src/components/ (or similar).

About.tsx
Brief foundation history, mission statement, how funds are used.

Donate.tsx

Display Solana address (copy button)

QR code generator (SVG/canvas)

Links: Pump.fun token page, Fastex exchange link, optional instructions for metamask/phantom.

Footer.tsx
Contact links, socials, small legal text, donate quick link.

Gallery.tsx
Grid / masonry layout of images with modal lightbox for each. Each card: image, name, short blurb, status (adopted/in-care).

Hero.tsx
Full-bleed hero with CTA buttons and prominent images.

ImpactStories.tsx
Timeline or card list with "before" and "after" and follow-up updates.

NavLink.tsx
Reusable navigation link (supports smooth scrolling/active state).

Partners.tsx
Logos and links for: Pump.fun, Fastex, Shmoogle AI, YouTube channels, Telegram bot, X account.

Token.tsx
Token info panel: token address, pump.fun link, small live price embed from Dexscreener (iframe).

VideoShowcase.tsx
Embedded YouTube player and a TikTok thumbnail linking to the TikTok page.

Notes on structure & props: keep components presentational and pass data as props. Example: Gallery accepts items: Array<{id,name,image,desc,status}>. Donate accepts walletAddress prop.

Media & assets used

You provided images; they were downloaded and are available under public/ (or /static depending on framework):

public/cat-1.png — uploaded Screenshot-2025-11-17-133747.png

public/cat-2.png — Screenshot-2025-11-17-133752.png

public/cat-3.png — Screenshot-2025-11-17-133828.png

public/luna.png — Screenshot-2025-11-17-133849.png (LUNA)

public/stella.png — Screenshot-2025-11-17-133856.png (STELLA)

public/cat-6.png — Screenshot-2025-11-17-133912.png

public/nova.png — Screenshot-2025-11-17-134013.png (NOVA; requested whiskers changed to Garfield — see edit notes)

public/garfield.png — Screenshot-2025-11-17-134408.png (GARFIELD; rescued)

public/tiktok-link.png — Screenshot-2025-11-17-134552.png (used as clickable TikTok thumbnail)

Image usage rule: keep originals in public/ and also create optimized/resized variants (e.g., 400/800/1200 px) for responsive loading. Add alt text for accessibility (e.g., "Luna resting on a blanket").

Requested graphic edit: “change whiskers to Garfield” — this implies image editing (replace whiskers/overlay Garfield). If you want automated edits, provide final art or let me produce an SVG overlay; otherwise perform the edit in an image editor and place the result in public/.

Embeds (Dexscreener / YouTube / TikTok)

Dexscreener iframe (works in Google Sites and GitHub Pages):

<iframe
  src="https://dexscreener.com/solana/FhBE94EG8E2LyckpzWNLo6DmQvDr3zHsLU6BDRVZpump?embed=1&theme=dark"
  style="width:100%; height:520px; border:0;"
  allowfullscreen
></iframe>


YouTube embed (Video in Partners / VideoShowcase):

Primary video (play on page):
https://www.youtube.com/watch?v=jQE0ihaluL8&list=PLl1AgsdrU6Ee11l3ZHKve3K_ViPgpw6zl&index=5

<iframe
  width="100%" height="480"
  src="https://www.youtube.com/embed/jQE0ihaluL8?rel=0"
  frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen>
</iframe>


TikTok thumbnail link (click opens TikTok channel):

<a href="https://www.tiktok.com/@StellaNovaLuna_catSister" target="_blank" rel="noopener">
  <img src="/tiktok-link.png" alt="StellaNovaLuna on TikTok" style="max-width:100%;cursor:pointer;">
</a>


Pulling multiple videos: list video IDs and embed them in a carousel or grid (use lazy loading).

Partners & community (to list in Partners.tsx)

Fuzzball Token — Pump.fun page: https://pump.fun/coin/FhBE94EG8E2LyckpzWNLo6DmQvDr3zHsLU6BDRVZpump

YouTube support playlist & channels:

Playlist item (amxCWr8wX3Q list referenced in your note)

Channel: https://www.youtube.com/@FuzzBall-Solana

Fastex exchange: https://www.fastex.space

Shmoogle AI: https://shmooglestore.company.site/ & Telegram Bot: https://t.me/shmooglememe_bot

Creator X account: https://x.com/ShMoogle_AI

Display clickable logos/icons, small descriptions, and external link icons. Consider rel="noopener noreferrer" and target="_blank" for external links.

How to run locally

Example (React / Vite):

Clone repo

Install dependencies:

npm install
# or
yarn


Start dev server:

npm run dev
# or
yarn dev


Build for production:

npm run build


If you prefer plain static HTML, the index.html version (with <iframe> to Dexscreener) can be deployed without a Node toolchain.

Accessibility & privacy notes

Add alt attributes for all images.

Make interactive elements keyboard accessible (focus states).

Show clear donation cautions and identity verification tips.

Do not log or store on-site donation private info. Only show public wallet address and links to official services.

Contributing

Open an issue to request features or report bugs.

Use branch feature/<name> and create pull requests to main.

Please include image sources and confirm copyrights for externally owned media.

License & credits

License: MIT (default) — change if needed.

Credits / Sources: content & media supplied by StellaNovaLuna team and associated creators (TikTok: @StellaNovaLuna_catSister, X: @ShMoogle_AI, Pump.fun, Dexscreener, Fastex, Shmoogle).

Contact / Socials

TikTok: https://www.tiktok.com/@StellaNovaLuna_catSister

X: https://x.com/ShMoogle_AI

YouTube playlist & support channel links (provided above)

Exchange: https://www.fastex.space

Shmoogle store: https://shmooglestore.company.site/

Telegram bot: https://t.me/shmooglememe_bot

Quick snippets (copy/paste)

Copy wallet button (JS):

<button id="copyBtn">Copy Wallet</button>
<script>
document.getElementById('copyBtn').addEventListener('click', async () => {
  try {
    await navigator.clipboard.writeText('5rrJJykVDgeMYWiXRvMoMjGZiYyDj6791kiymaETXM4K');
    alert('Wallet copied to clipboard');
  } catch (err) {
    alert('Copy failed — please copy manually: 5rrJJykVDgeMYWiXRvMoMjGZiYyDj6791kiymaETXM4K');
  }
});
</script>


QR using Google Chart API (simple):

<img src="https://chart.googleapis.com/chart?chs=300x300&cht=qr&chl=5rrJJykVDgeMYWiXRvMoMjGZiYyDj6791kiymaETXM4K" alt="Donate QR">

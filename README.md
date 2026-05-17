# Click 8 — June 2025 Content Calendars

A single production-ready dashboard containing content calendars for **two clients**:

- **Click 8** — Instagram + LinkedIn · 28 posts · 4 narrative arcs
- **Café La Mirajh** — Instagram + Google Ads · 30 posts · 4 campaign arcs

## Switching clients

Use the **client switcher bar** at the top of the page to toggle between Click 8 and Café La Mirajh. The entire sidebar, platform toggles, arc filters, and post grid all update instantly.

## What's inside each client

### Click 8
- 28 posts across June 2025
- Instagram + LinkedIn
- 4 arcs: Identity Crisis · Proof Machine · Enemy · Cultural Takeover
- Full post briefs: hook, caption, hashtags, KPI, CTA
- Copy to clipboard + export as .txt

### Café La Mirajh (Chennai)
- 30 posts across June 2025
- Instagram + Google Ads
- 4 arcs: The Reveal · Behind the Cup · Community Love · Signature Series
- Full post briefs: content direction, caption, hashtags, KPI, CTA
- Google Ads cards include: campaign type, budget, geo, audience, bid strategy, schedule

## Deploy to Vercel

### Option 1 — Vercel Dashboard (no code needed)
1. Go to [vercel.com](https://vercel.com) → sign in → **Add New → Project**
2. Click **Import** → **Upload** → drag and drop this folder
3. Click **Deploy** — live in under 60 seconds

### Option 2 — Vercel CLI
```bash
npm install -g vercel
cd combined
vercel
```

### Option 3 — GitHub + Vercel (for ongoing updates)
```bash
git init && git add . && git commit -m "Click 8 dual-client calendar"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```
Then connect the repo in Vercel → every push auto-redeploys.

## Customising

All content lives in two arrays inside `index.html`:
- `C8_POSTS` — Click 8 posts
- `CAFE_POSTS` — Café La Mirajh posts

Each post object:
```js
{
  arc: 1,               // Arc number (1–4)
  day: 2,               // Day of June
  dayName: "Mon",
  plat: "Instagram",    // "Instagram" | "LinkedIn" | "Google Ads"
  fmt: "Reel · 60 sec",
  time: "9:00 AM",
  title: "Post title",
  hook: "Hook/creative direction",
  hook2: "Caption/setup notes",
  tags: "#Tag1 #Tag2",
  goal: "Primary goal",
  kpi: "KPI target",
  cta: "Call to action",
  gaspec: null          // Google Ads only — "Campaign type: ... · Budget: ..."
}
```

## Tech stack
- Pure HTML + CSS + JavaScript — zero dependencies, zero build step
- Google Fonts: Syne + DM Sans
- Deploys as a static site — fast, free, maintainable

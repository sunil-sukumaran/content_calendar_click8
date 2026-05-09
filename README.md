# Click 8 — June 2025 Content Calendar

A production-ready interactive content calendar dashboard for Click 8, built for Instagram + LinkedIn.

## What's inside

- 28 posts across June 2025
- 4 campaign narrative arcs
- Instagram + LinkedIn only
- Interactive filtering by arc and platform
- Click-through post briefs with hooks, captions, hashtags, KPIs, and CTAs
- Copy to clipboard + export as .txt for each post

## Deploy to Vercel

### Option 1 — Vercel CLI (fastest)

```bash
# Install Vercel CLI if you haven't
npm install -g vercel

# From inside this folder
cd click8-calendar
vercel

# Follow the prompts — select your team/account, confirm project name
# Your dashboard will be live in ~30 seconds
```

### Option 2 — Vercel Dashboard (no CLI needed)

1. Go to [vercel.com](https://vercel.com) and sign in
2. Click **Add New → Project**
3. Click **Import** and choose **Upload** (drag and drop this folder)
4. Click **Deploy**
5. Done — your dashboard is live at a `.vercel.app` URL instantly

### Option 3 — GitHub + Vercel (recommended for ongoing updates)

1. Create a new GitHub repo
2. Push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "Click 8 June content calendar"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```
3. Go to [vercel.com](https://vercel.com) → **Add New → Project** → Import from GitHub
4. Select your repo → **Deploy**
5. Every future `git push` will auto-redeploy

## Customising

All content lives in the `POSTS` array inside `index.html`. Each post object has:

```js
{
  arc: 1,              // 1=Identity Crisis, 2=Proof Machine, 3=Enemy, 4=Cultural Takeover
  day: 2,              // Day of June
  dayName: "Mon",
  month: "June",
  plat: "Instagram",   // or "LinkedIn"
  fmt: "Carousel · 8 slides",
  time: "9:00 AM",
  title: "Your post title",
  hook: "The opening hook text...",
  hook2: "The caption text...",
  tags: "#Hashtag1 #Hashtag2",
  goal: "Primary goal description",
  kpi: "Target KPI",
  cta: "Call to action text"
}
```

## Tech stack

- Pure HTML + CSS + JavaScript — zero dependencies, zero build step
- Google Fonts: Syne + DM Sans
- Deploys as a static site — fast, free, and maintainable

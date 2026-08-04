AI Nails Lab — Static Site Deployment Package
==============================================

WHAT'S IN THIS ZIP
-------------------
- index.html    → the entire website (HTML + CSS + JS + all photos/videos, all embedded — nothing else to link up)
- og-image.jpg  → the social-share preview image referenced by the meta tags
- robots.txt    → tells search engines they're allowed to crawl the whole site, points to the sitemap
- sitemap.xml   → one-page sitemap (this is a single-page site, so it lists just the homepage)

This is a plain static site (no framework, no build step, no npm install needed).

HOW TO DEPLOY ON VERCEL
-------------------------
Option A — Drag & drop (easiest):
1. Go to vercel.com → your project (or "Add New... > Project").
2. Choose "Deploy" and drag this unzipped folder (or use the Vercel dashboard's
   file upload) so that index.html and og-image.jpg sit at the PROJECT ROOT
   (not inside a subfolder).
3. Vercel will detect it as a static site automatically — no framework preset,
   no build command needed. Deploy.

Option B — Vercel CLI:
1. Unzip this file into its own folder.
2. In that folder, run:
     npx vercel --prod
3. Follow the prompts (link to your existing ainailslab.com project when asked).

Option C — GitHub:
1. Push index.html and og-image.jpg to a new GitHub repo (root level).
2. In Vercel, "Add New... > Project" → Import that repo.
3. Framework preset: "Other" / static — no build command, no output directory override needed.

AFTER DEPLOYING
-----------------
- Confirm https://www.ainailslab.com/og-image.jpg loads directly in a browser.
- Confirm https://www.ainailslab.com/robots.txt and https://www.ainailslab.com/sitemap.xml
  both load directly (they must sit at the root, same level as index.html).
- Once robots.txt/sitemap.xml are live, submit the sitemap in Google Search Console
  (Search Console → Sitemaps → enter "sitemap.xml") so Google indexes the site faster.
- Test the link preview on iMessage/WhatsApp/Facebook using
  https://www.opengraph.xyz or Facebook's Sharing Debugger — paste your domain in.
- Everything else (fonts, images, videos, booking links) is already self-contained
  in index.html, so there's nothing else to configure.

DOMAIN
------
ainailslab.com is already referenced throughout the code (canonical URL, Open
Graph tags, structured data). Since you purchased it directly through Vercel,
it should already be attached to whichever Vercel project you deploy this to —
double check under Project Settings → Domains.

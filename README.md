# Voltage Drop Calculator — Deployment Guide

This folder is a complete, ready-to-upload static website. No build step, no server, no database — just these files.

## What's in here
- `index.html` — the whole site (tool + content), one file
- `favicon.svg` — the tab icon
- `robots.txt` — tells search engines they can crawl the site
- `sitemap.xml` — tells Google what page(s) exist

## 1. Before you upload — replace the placeholder domain

Open `index.html`, `robots.txt`, and `sitemap.xml` and replace every instance of
`https://yourdomain.com/` with your real domain once you've bought one (see step 2).

## 2. Get a domain + hosting on Hostinger

1. Go to hostinger.com and buy a hosting plan (any basic "Web Hosting" plan works — this site is lightweight).
2. During signup, either register a new domain or connect one you already own.
3. Once your Hostinger account is active, open **hPanel** (Hostinger's dashboard).

## 3. Upload the site

**Option A — File Manager (easiest, no extra tools):**
1. In hPanel, go to **Files → File Manager**.
2. Open the `public_html` folder — this is your site's root.
3. Delete the default placeholder files Hostinger puts there.
4. Upload all 4 files from this folder (`index.html`, `favicon.svg`, `robots.txt`, `sitemap.xml`) directly into `public_html`.

**Option B — FTP:**
1. In hPanel, go to **Files → FTP Accounts** and note the host, username, and password.
2. Connect with an FTP client (e.g. FileZilla).
3. Upload all 4 files into `public_html`.

Your site is now live at your domain — usually within a few minutes, sometimes up to 24 hours if DNS is still propagating on a brand-new domain.

## 4. Get it into Google

Buying hosting does not automatically put you in Google search results — you need to ask Google to index it:

1. Go to **Google Search Console** (search.google.com/search-console) and sign in with a Google account.
2. Add your domain as a property (Search Console will give you a TXT record or HTML file to verify ownership — Hostinger's hPanel has a DNS section where you can add the TXT record).
3. Once verified, go to **Sitemaps** in the left menu and submit `https://yourdomain.com/sitemap.xml`.
4. Use **URL Inspection** on your homepage URL and click **Request Indexing**.

Indexing typically takes anywhere from a few days to a couple of weeks. Ranking for your target search term ("voltage drop calculator") takes longer and improves with:
- Real people linking to it (post it once, genuinely, where electricians already hang out — a subreddit like r/electricians, a trade forum, a Facebook group)
- The page staying fast and mobile-friendly (it already is)
- Nobody else's tool being obviously better — check that periodically

## 5. Optional next steps
- Add a real custom favicon (`.ico`) if you want it to show in every browser tab style — SVG favicons aren't supported in a few older browsers.
- Add Google Analytics or Plausible if you want to see traffic.
- If this tool gets traction, the same page shell can be duplicated for other trade-specific calculators (see the tool itself for the formula it's built on).

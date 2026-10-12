# PressedLab Lens Pipeline (prd-pressedlab)

Automated content pipeline for **ASMR Hydraulic Press & Fruit Juice Extraction** videos dedicated exclusively to **PressedLab Lens** (Facebook Page ID: `1339129032621410`).

## What it does

1. **Fetches** satisfying fruit-crushing videos from Google Drive (`1NbBvT_JHzlPaG83U6f5aSNFdyNqbNgjn`).
2. **Processes** them using FFmpeg (vertical 1080x1920 9:16 aspect ratio, watermark removal, unsharp sharpening, and loudness normalization for ultra-crisp ASMR crunch and juice extraction sounds).
3. **Generates SEO Captions** using Pollinations AI (detects fruit/item from filename and crafts viral, high-retention titles, descriptions, and hashtags).
4. **Publishes Exclusively to PressedLab Lens**:
   - Publishes **Facebook Reels** (with auto video transfer & container finalization).
   - Posts a **Pinned Comment** containing high-engagement follow CTA.
   - Publishes **Facebook Stories** (24h story format).

---

## Automation Schedule

The pipeline runs automatically **3 times daily** via GitHub Actions with staggered timings to maintain organic distribution:
- `40 3 * * *` UTC
- `45 11 * * *` UTC
- `10 19 * * *` UTC
*(03:40 UTC, 11:45 UTC, 19:10 UTC (approx. 09:10, 17:15, 00:40 IST))*

It can also be manually triggered anytime via GitHub Actions **Run workflow** button (`workflow_dispatch`).

---

## GitHub Secrets Required

| Secret | Description |
|---|---|
| `FB_PAGE_ID` | Facebook Page ID (`1339129032621410`) |
| `FB_PAGE_ACCESS_TOKEN` | Direct Page Access Token |
| `GOOGLE_SERVICE_ACCOUNT_KEY` | Google Service Account JSON credentials |
| `GOOGLE_DRIVE_FOLDER_ID` | Drive folder ID (`1NbBvT_JHzlPaG83U6f5aSNFdyNqbNgjn`) |
| `POLLINATIONS_API_KEY` | Optional Pollinations AI key for SEO captions |

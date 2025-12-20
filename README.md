# Southern OC Weekly Event Picks → GitHub Pages

This repo runs the notebook on a weekly schedule and publishes a static report to GitHub Pages.

## Setup

1) **Add API keys (recommended)**
- Repo → **Settings → Secrets and variables → Actions → Secrets**
  - `TICKETMASTER_API_KEY` (Ticketmaster “Consumer Key” / Discovery API key)
  - `GOOGLE_PLACES_API_KEY` (optional)

2) **Enable GitHub Pages**
- Repo → **Settings → Pages**
- **Build and deployment → Source: GitHub Actions**

3) **Run it**
- Go to **Actions → “Publish weekly event report” → Run workflow** (manual)
- Or wait for the Tuesday schedule.

## Output

The action generates `site/index.html` and deploys it to GitHub Pages.


## Major venue focus (LA / OC / San Diego)

The notebook has a `MAJOR_CONCERT_VENUES` list and an `INCLUDE_MAJOR_VENUE_CONCERTS` toggle. This adds a second Ticketmaster pass that targets major venues directly (e.g., Hollywood Bowl, Kia Forum, Observatory North Park) so big shows don’t get missed just because they’re outside your radius.

You can disable it via Actions env var:

- `INCLUDE_MAJOR_VENUE_CONCERTS=false`

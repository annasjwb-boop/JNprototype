# AidFinder Gap Simulator — demo deploy (for Anna)

Single-file HTML prototype + assets. No build step, no framework, no server code.

## Deploy (2 minutes)
1. Go to vercel.com/new → drag this whole folder in (or `vercel deploy` from inside it).
2. All 6 files must sit at the project ROOT — index.html references /fema-fill.mp4, /fema-poster.jpg, and the icons by absolute path.
3. Optional: point demo.aidfinder.com at the deployment (Vercel → Settings → Domains).

## Files
- index.html         — the entire app (762 KB, self-contained except the two video assets)
- fema-fill.mp4      — FEMA form-fill demo clip (h264; external because iOS Safari can't play data-URI video)
- fema-poster.jpg    — poster frame for the video player
- apple-touch-icon.png — home-screen icon (navy / white AidFinder symbol)
- icon-512.png, icon-1024.png — favicon / larger icon

## iPhone demo setup (Jonathon's flow)
1. Open the deployed URL in Safari once on WiFi (caches everything).
2. Share → Add to Home Screen → launches chromeless, full-screen, native-feeling.
3. After ANY redeploy: delete the home-screen icon and re-add it (iOS caches aggressively), then force-quit and relaunch.

## Testing notes
- State is in-memory only; reload = clean slate (intentional for demos).
- Three properties: Palisades (fire), Reno (wind/flood), Scottsdale (heat). Recovery mode: tap the fire banner on Palisades → "Enter recovery".
- Score demo beat: Readiness tab → Add a policy → "Earthquake coverage · CEA" → activate → score 30→38. Flood beat belongs on Reno (41→46), not Palisades (by design — risk-weighted).
- Known placeholders flagged for later: area-average benchmarks (52/47/44) are illustrative; FEMA $43.6k cap hardcoded (verify annually).

Built/tested against iPhone 17 Pro Safari + Chrome. Last regression: all interactive flows pass, zero console errors.

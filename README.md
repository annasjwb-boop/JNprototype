# AidFinder — Gap Simulator Prototype

A single-file, self-contained HTML prototype of the AidFinder experience: coverage
gap simulation, policy connection, readiness scoring, damage documentation, and
FEMA/SBA application flows.

## Running it

No build step, no dependencies, no server required. Open `index.html` in a browser.

If you'd rather serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## What's inside

Everything lives in `index.html` — markup, styles, script, and all imagery as
embedded base64. The only external request is to Google Fonts (DM Sans, Fraunces).
That means the file can be emailed, dropped on a static host, or opened straight
from disk and it will still work.

Flows covered in the prototype include:

- Coverage gap breakdown — how insurance, FEMA, SBA, and out-of-pocket stack
  against a rebuild estimate
- Policy connection (carrier link, add-a-policy, flood/NFIP quote confirmation)
- Readiness score and the actions that raise it
- Damage walkthrough and claim filing status
- FEMA and SBA application tracking
- Guide library, community Q&A, and messages
- Account settings, properties, and language

## Publishing

To put this on a URL, enable GitHub Pages in **Settings → Pages**, source
**Deploy from a branch**, branch `main`, folder `/ (root)`. The prototype will be
served at `https://annasjwb-boop.github.io/JNprototype/`.

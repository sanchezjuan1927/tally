# Tally

A shared-expense settle-up calculator. Everyone enters what they paid; Tally
works out each person's balance and the fewest payments needed to even up.

## Run locally

It is a single static file — no build step, no dependencies to install.

```bash
# from this folder
python3 -m http.server 4173
# then open http://localhost:4173
```

Or just open `index.html` directly in a browser (`file://` works too).

## Does it need internet?

**No — not for anything that matters.** All the logic, the settle-up math and
the saved state (`localStorage`) run entirely in your browser tab.

The only network request is to Google Fonts (Fraunces + IBM Plex). Offline, the
page silently falls back to system fonts — every number and button still works.
Backlog item #2 is to self-host the fonts and drop that last request.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The whole app — markup, styles and script in one file. |

# Benefits Desk demo

A working sample of a benefits practice where the repetitive work is handled for the team: census cleanup,
fully insured quote comparison, self-funded bids, savings models (first-dollar care and ICHRA), proposals,
service email, billing checks, compliance, and a guided tour. All companies, people and figures are fictional.

## Run locally

```
python3 server.py
```

Open http://127.0.0.1:8400/benefits/

## Layout

- `benefits/` the app (`app.js`, `ops.js`, `data.js`, `parsers.js`) and the sample documents it reads
- `shared/` design system (`app.css`), UI helpers (`core.js`) and the guided tour engine (`guide.js`)
- `server.py` static files plus a small per-visitor progress API, standard library only

## Deploy

Railway runs `python3 server.py` (see `railway.json`); the server binds to `$PORT`. Saved progress lives in
`.data/`, keyed by a session cookie, so each visitor has their own demo. It resets on redeploy.

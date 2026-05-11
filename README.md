# petey-site

Informational landing site for [Petey](https://petey.cc). Static HTML, no build step.

The functional web app lives in `petey-web` (deployed at petey.cc). This site is purely marketing — it links out to the app, the GitHub repo, and the desktop downloads.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Structure

- `index.html` — single-page site (nav, hero, demo, how-it-works, modes, pricing, security, about, footer)
- `static/` — logo, favicon, OG image, demo screenshots

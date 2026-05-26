# petey-site

Informational landing site for [Petey](https://petey.cc). Static HTML, no build step.

The desktop app is the canonical product the site sells. The hosted petey-web is a try-it-now demo, not a parallel product — secondary CTA only. The Python package is a credibility surface for engineers.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Structure

- `index.html` — single-page homepage. Sections: nav, hero, feature strip, demo (3-blueprint toggle), how it works, modes (desktop + Python), deploy (local / container / VPC), developers (code snippet + plugins/CLI/MCP), privacy (3-tier claim block + audit bullets), footer.
- `download/index.html` — standalone download landing. Mac + Windows buttons (link to GitHub releases), what's in the app, system requirements, alternatives (browser demo, Python package, self-host).
- `static/` — logo, favicon, OG image, demo screenshots.

Blueprint library (`/library` + `/library/{format}`) is planned but not built yet; the site can launch without it.

## Notes

- Download buttons in `/download/` point at `https://github.com/afriedman412/petey-web/releases/latest`. Verify this matches the desktop release URL once the next release lands.
- The hero CTA on the homepage and the nav CTA both point at `/download`.
- The hosted petey-web is linked as "Try in browser" — secondary CTA — and is expected to live at `app.petey.cc` once migrated off the apex.

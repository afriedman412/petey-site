# petey-site

Landing site for [Petey](https://petey.cc). Static HTML, no build step.

As of 2026-10-09 the site is a single "coming soon" page for the forms product: drop in a filled PDF form, Petey
recognizes it against its library of mapped forms and returns every field as structured data. It no longer links
to the earlier product (desktop app, app.petey.cc, the PyPI package, Docker image or GitHub repo); `/download/`
redirects to the homepage so old links land somewhere.

Lives at `~/Documents/code/petey-site` (moved out of petey-master 2026-10-09; the copy there is stale). Kept
separate from petey-2.

## Deploy

petey.cc is served by Netlify, which builds from this repo's `main` branch and publishes `site/` (`netlify.toml`).
Work lands on `dev`; a PR into `main` puts it live. A manual deploy from a linked checkout also works:

```sh
npx netlify-cli deploy --prod --dir site
```

## Local preview

```sh
python3 -m http.server 8000 -d site
# open http://localhost:8000
```

## Structure

- `site/index.html`: the homepage. Nav, hero (coming soon), three steps, how it works (no LLM calls, forms
  mapped ahead of time, no third parties, same answer every time), footer (the earlier
  site's bottom row; its link columns pointed at the old product). No contact address: petey.cc has no MX records
  (checked 2026-10-09), so info@petey.cc does not receive mail.
- `site/download/index.html`: redirect to `/`.
- `site/static/`: logo, favicon, OG image.

## Copy rules

Say only what the product does today. No form counts, no launch dates, no privacy or hosting promises until
those are decided. Inputs are clean digital PDFs (fillable forms and their flattened copies), not scans.

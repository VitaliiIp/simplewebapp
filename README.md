# simplewebapp

A simple static website for **Lingvex**, a professional translation services company. Built with plain HTML and CSS — no build step, no dependencies.

## Pages

- `index.html` — Home (services overview, testimonials, CTAs)
- `pricing.html` — Three-tier pricing (Economy / Professional / Premium)
- `about-us.html` — Company info, partnership opportunities, FAQ
- `contact.html` — Contact form and company details

## Run locally

Open `index.html` directly in your browser, or serve the folder with any static server:

```sh
# Python
python -m http.server 8080

# Node (npx)
npx serve .
```

Then visit http://localhost:8080.

## Structure

```
simplewebapp/
├── index.html
├── pricing.html
├── about-us.html
├── contact.html
├── css/
│   └── styles.css
└── .github/
    └── workflows/
        └── ci.yml      # HTML validation + link check on every PR
```

## CI

Every pull request runs:
- **HTML validation** via `html-validate`
- **Link check** via `lychee` to catch broken internal links

See `.github/workflows/ci.yml` for details.

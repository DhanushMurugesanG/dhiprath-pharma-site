# Dhiprath Pharma — company website

Marketing website for **Dhiprath Pharma Private Limited**, Bengaluru — a pharmaceutical
company and authorised distributor supplying critical care, oncology, dialysis,
diagnostics and surgical products to hospitals across Karnataka.

Built from the company profile document.

## Structure

A single self-contained page: `index.html`. No build step, no dependencies, no bundler.
Everything is inline except the Google Fonts stylesheet — CSS, JavaScript, the logo
(inline SVG) and the favicon (SVG data URI) all ship inside the file.

- Responsive, light and dark themes with a header toggle (persisted to `localStorage`)
- Searchable / filterable product catalogue — 40 products across 8 principals, all
  rendered server-side so it works with JavaScript disabled
- Print stylesheet: the page doubles as a printable company profile on A4
- `schema.org` Organization structured data, Open Graph and Twitter card tags

## Local preview

Open `index.html` in a browser, or:

    python3 -m http.server 8000

## Deployment

Served by GitHub Pages from the `main` branch, repository root.

To point a custom domain at it later, add a `CNAME` file containing the bare hostname
and update the three URL references in `index.html`: the `<link rel="canonical">` tag,
the `og:url` meta tag, and `url` in the JSON-LD block.

# Category Checks — What to Parse

For each target URL, extract every item below from the fetched HTML. Record pass/fail per item and feed the result into the priority rules.

---

## Core SEO

| Item | Check | Ideal |
|------|-------|-------|
| `<title>` | Present, non-empty | 50-60 chars |
| `<meta name="description">` | Present, non-empty | 150-160 chars |
| `<h1>` | Exactly one, matches page intent | 1 per page |
| Heading hierarchy | No skipped levels (no H3 before H2) | H1 → H2 → H3 |
| `<link rel="canonical">` | Present, points to itself (or master version) | Self-referencing on primary page |
| `<meta name="robots">` | No `noindex` or `nofollow` on pages meant to rank | `index, follow` or absent |

---

## Social Meta

### Open Graph
- `og:title` — present
- `og:description` — present
- `og:image` — present, absolute URL, 1200x630 recommended
- `og:url` — present, canonical URL
- `og:type` — present (`website`, `article`, `product`, etc.)

### Twitter
- `twitter:card` — present (`summary_large_image` usually best)
- `twitter:title` — present
- `twitter:description` — present
- `twitter:image` — present

The social image is the single biggest CTR lever on shared links. Flag hard if missing.

---

## Schema Markup (JSON-LD)

1. Find all `<script type="application/ld+json">` blocks.
2. Parse each as JSON. Flag any that fail to parse.
3. Check `@type` is present.
4. Confirm `@type` matches the page:
   - Blog post → `Article` or `BlogPosting`
   - Product page → `Product`
   - Local business → `LocalBusiness`
   - FAQ content → `FAQPage`
   - How-to content → `HowTo`
   - Site-wide → `Organization` or `WebSite` (usually in footer/header)
5. Check required properties per type (e.g., `Product` needs `name`, `image`, `offers`).

---

## Images

- Count all `<img>` tags.
- Count images with missing `alt` attribute.
- Count images with empty `alt=""`.
- Distinguish:
  - **Decorative images** → `alt=""` is correct
  - **Content images** → must have descriptive alt text
  - **Logo** → alt should be the brand name
  - **Icons** → `alt=""` if paired with visible text; otherwise descriptive

Flag any content image with missing or empty alt.

---

## Links

- Count internal links (same domain or same root domain).
- Count external links.
- Scan anchor text for generic phrases: `click here`, `read more`, `learn more`, `here`, bare URLs like `https://example.com/page`.
- Flag if internal links < 3 on a standalone page (orphan risk).
- Flag if external links all go to one domain (looks spammy).

---

## Mobile + i18n

- `<meta name="viewport" content="width=device-width, initial-scale=1">` — present and correct.
- `<html lang="...">` — present with a valid language code.
- `hreflang` alternates — required if site serves multiple regions/languages. Each alternate must be reciprocal.

---

## Content

- Strip HTML tags and count visible words.
- Flag < 300 words on content-type pages (blog, article, guide).
- Homepage and product pages: word count less critical, but flag < 100.
- Flag keyword stuffing: any single word/phrase appearing more than 5% of total word count.

---

## robots.txt

Fetch `https://{domain}/robots.txt`.

- `Disallow: /` with no `Allow:` = entire site blocked. Critical issue.
- Missing `Sitemap:` line = missed opportunity. Flag as P2.
- Syntax errors = flag as P1.
- Blocks on `/assets/`, `/images/`, or `/css/` that Google needs to render the page = flag as P1.

---

## sitemap.xml

Fetch the URL from the `Sitemap:` directive in robots.txt, or try `https://{domain}/sitemap.xml` directly.

- 404 on sitemap file = P0.
- Malformed XML = P1.
- The audited URL is not listed in the sitemap = P2.
- Sitemap references URLs that 404 = P1 (spot check a few).

---

## How to record findings

Keep a simple running tally per URL:

```
URL: https://example.com/page
- Title: PASS (54 chars)
- Meta description: FAIL (missing)
- H1: PASS (1 present, matches intent)
- Canonical: PASS (self-referencing)
- Robots meta: PASS
- og:image: FAIL (missing)
- Twitter card: PASS
- Schema: FAIL (invalid JSON in Product schema)
- Images: 12 total, 3 missing alt
- Links: 18 internal, 5 external, 2 generic anchors
- Viewport: PASS
- Lang: PASS (en)
- Hreflang: N/A
- Word count: 847
- robots.txt: PASS, sitemap referenced
- sitemap.xml: URL present
```

Feed this into the priority rules to generate the report.

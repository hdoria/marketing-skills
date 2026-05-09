---
name: auditoria-seo
description: Run an on-page SEO audit on any public webpage using only native Claude Code tools — no CLI, no npm install, no browser automation. Use when the user asks to audit a page, check their SEO, review meta tags, check schema, diagnose why a page isn't ranking, or run a pre-launch SEO check. Triggers on "SEO audit", "site audit", "check my SEO", "audit this page", "is my page SEO-friendly", "review meta tags", "check schema", "check title tags", "audit my landing page", "why isn't this ranking". Outputs a graded report (A-F) with prioritized P0-P3 fixes and exact copy-paste code where relevant.
---

# SEO Audit

Most SEO tools promise 148 rules and deliver a PDF nobody reads. For a non-technical marketer, the ranking wins live in about 20 of those rules: title, meta, H1, canonical, social cards, schema, alt text, internal links. This skill checks exactly those, on any URL, with nothing to install.

---

## the core job

Pull a public webpage's HTML, parse the on-page SEO signals, grade the result A-F, and hand back a priority-ordered fix list with exact code snippets. Every audit ends with a clear "what I did NOT check" disclosure so the user knows where the audit's edges are.

**Output format:** A single markdown report per URL (or one summary + per-URL reports for multi-page runs). Graded, prioritized P0-P3, with copy-paste fixes.

---

## before starting: gather context

**STOP. Do not start fetching or parsing until every field below is confirmed with the user. Ask for any missing field first. Do not guess the URL, do not assume single vs multi-page.**

1. **Target URL(s)** — Which URL? Up to 10 for a batch. (Required — without this there's nothing to audit.)
2. **Specific concern** — Anything they're worried about? Like "we dropped in Google rankings last week" or "I just redesigned this page." (Optional, but changes which findings get lead-billing in the report.)
3. **Target keyword** — Is there a specific keyword they're trying to rank for on this page? (Optional, but unlocks title/H1/meta keyword checks.)

Once confirmed, before running WebFetch, state the audit's scope caveat in one line so they don't walk away with wrong expectations:

> "This covers on-page SEO only — no Core Web Vitals, page speed, or security headers. If you need those, run Google PageSpeed Insights on the same URL."

---

## fetch: pull the page and its robots/sitemap

For each URL:

1. `WebFetch` the page itself.
2. `WebFetch` `https://{domain}/robots.txt`
3. `WebFetch` `https://{domain}/sitemap.xml` (or whatever the robots.txt `Sitemap:` directive points to)

**Sanity check before parsing:** Confirm the HTML contains real content. If the `<body>` is empty or contains only `<script>` tags (common on React/Vue SPAs without SSR), stop and tell the user:

> "This page looks JavaScript-rendered — the raw HTML I can fetch doesn't contain the visible content. A proper audit needs a real browser. Try using Screaming Frog or ask your dev to add server-side rendering."

Anti-pattern: don't silently continue on a JS shell. The audit will be wrong and you'll have no idea.

---

## parse: run every category check

For each URL, extract the items listed in [references/category-checks.md](references/category-checks.md).

Keep a running tally per URL:

```
URL: [the URL]
- Title: [PASS/FAIL + details]
- Meta description: [PASS/FAIL + details]
- H1: [...]
- [etc. through every category]
```

Anti-pattern: don't skip the tally and go straight to the report. Without the raw findings written out, grading and prioritization become guesses.

---

## prioritize: map findings to P0-P3

Use this matrix:

| Priority | Triggers |
|----------|----------|
| **P0 — Fix now** | Blocks indexing: `noindex` on a page meant to rank, `Disallow: /` in robots.txt, canonical pointing to a different URL, sitemap.xml returns 404. Missing `<title>`. Missing `<h1>`. |
| **P1 — Fix this week** | Missing meta description. Missing `og:image`. No schema on a page that needs it (product, article, FAQ). Duplicate or off-topic H1. Broken canonical. Title missing the target keyword when one was given. |
| **P2 — Easy wins** | Title too short (<30) or too long (>65). Meta description > 170. Multiple H1s. Missing alt text on content images. Missing hreflang on multi-region site. `twitter:card` set to `summary` instead of `summary_large_image`. |
| **P3 — Nice to have** | Generic anchor text. Minor heading hierarchy polish. Open Graph description tweaks. Thin word count on a non-content page. |

Anti-pattern: don't invent new priority levels or reorder items inside a level without reason. The matrix above is the source of truth.

---

## grade: A through F

Rough scoring (gut-feel weight, not a formula):

| Grade | Score | Meaning |
|-------|-------|---------|
| A | 90-100 | Ship it |
| B | 80-89 | A handful of fixes |
| C | 70-79 | Meaningful gaps |
| D | 60-69 | Serious problems |
| F | <60 | The on-page needs a rebuild |

P0 issues drag hard (each one -15 to -25). P1 each -5 to -10. P2 each -1 to -3. P3 barely moves the number.

---

## output format

Deliver in this exact shape. Do not reorder sections.

```markdown
# SEO Audit — [URL]

**Grade: [A-F] ([score]/100)**
**One-line summary: [the single biggest issue in plain English]**

## P0 — Fix now
- **[Issue name]**
  - Why it matters: [plain English — avoid jargon]
  - Exact fix: [copy-paste code or specific instruction]

## P1 — Fix this week
[same format, one entry per issue]

## P2 — Easy wins
[same format]

## P3 — Nice to have
[same format]

## What this audit did NOT check
- Core Web Vitals / page speed — run Google PageSpeed Insights at pagespeed.web.dev
- HTTP security headers (CSP, HSTS, X-Frame-Options) — ask your dev
- [Add JS-render warning if applicable]
- [Add anything else flagged as out-of-scope]

## Next steps
1. [Specific first action]
2. Re-run this audit after changes to confirm the grade moved.
```

For multi-page runs, add a **"Shared issues across pages"** section at the top listing problems appearing on more than one URL. Those are template-level fixes — one change solves many pages.

---

## worked example

See [references/worked-example.md](references/worked-example.md) for a complete run — context gathering, fetching, category tallies, and the final graded report on a realistic SaaS pricing page.

---

## how this connects to other skills

**Feeds into this skill:**
- **vibe2-keyword-research** or **pesquisa-keywords** — if the user already has target keywords, bring them in as input.
- **vibe2-seo-content** — after publishing content from that skill, audit it here before going live.

**This skill feeds into:**
- **escrever-copy** or **vibe2-direct-response-copy** — once the audit finds weak titles/meta, those skills rewrite them.
- **landing-page** — if the audit grades a landing page D or F, rebuild using that skill.

---

## the test

A good audit:

1. **Leads with the user's actual concern** — If they said "not ranking for X," the first P0 or P1 issue must address that keyword.
2. **Includes copy-paste code for every technical fix** — Not "add schema" but the actual JSON-LD block with their data.
3. **Scopes honestly** — The "What this audit did NOT check" section appears in every report, always.
4. **Catches the real blockers first** — A `noindex` tag on a page meant to rank must never end up below any P2 cosmetic issue.
5. **Skips JS-rendered sites properly** — If the HTML is a shell, the skill stops and says so instead of reporting "no content found" as findings.
6. **Gives a verdict** — The grade is a single letter + score, and the one-line summary names the single biggest issue.

If the report reads like a generic checklist that could apply to any website — it failed. If the user could act on it without any further questions — it passed.

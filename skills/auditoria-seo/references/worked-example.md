# Worked Example — Auditing a SaaS Pricing Page

Real run of the skill on a made-up but realistic URL: `https://acme-crm.com/pricing`.

---

## Step 1 — Gather context

```
User: audit acme-crm.com/pricing

Claude: Before I start, I need to confirm:

1. Target URL: https://acme-crm.com/pricing — correct?
2. Single page or batch? (if batch, paste up to 10 URLs)
3. Anything specific you're worried about? (optional — e.g. "I just redesigned the page" or "we dropped in Google rankings last week")

Also a heads-up: this audit covers on-page SEO only. It does NOT check Core Web Vitals, page speed, or security headers. If you need those, run Google PageSpeed Insights on the same URL.
```

User confirms single page, concern is: "we're not ranking for 'CRM software pricing' even though we built the page for that keyword."

---

## Step 2 — Fetch

Claude runs three WebFetch calls:

1. `https://acme-crm.com/pricing` → returns HTML
2. `https://acme-crm.com/robots.txt` → returns text
3. `https://acme-crm.com/sitemap.xml` → returns XML

HTML has real content (not a JS shell) — good, continuing.

---

## Step 3 — Parse (findings recorded)

```
URL: https://acme-crm.com/pricing
- Title: "Pricing" (7 chars) — TOO SHORT, missing keyword
- Meta description: missing — FAIL
- H1: "Pricing plans" — present but weak for target keyword
- Canonical: self-referencing — PASS
- Robots meta: index, follow — PASS
- og:title: "Pricing - Acme CRM" — present
- og:description: missing — FAIL
- og:image: missing — FAIL (CRITICAL for social CTR)
- Twitter card: summary (not summary_large_image) — weak
- Schema: none present — FAIL (Product schema expected on pricing page)
- Images: 8 total, 2 missing alt (plan comparison icons)
- Links: 23 internal, 1 external, 3 generic "learn more" anchors
- Viewport: PASS
- Lang: en — PASS
- Hreflang: N/A (single locale)
- Word count: 412
- robots.txt: PASS, sitemap referenced correctly
- sitemap.xml: /pricing URL present — PASS
```

---

## Step 4 — Grade

Calculation:
- 0 P0 issues, 4 P1 issues, 3 P2 issues, 2 P3 issues
- Weighted: 4×8 + 3×3 + 2×1 = 43 points off
- **Grade: D (57/100)**

The title and missing schema are the big drags. The missing OG image also hurts because the user shares this page in sales conversations.

---

## Step 5 — Report

```markdown
# SEO Audit — https://acme-crm.com/pricing

**Grade: D (57/100)**
**One-line summary: Your title tag says "Pricing" — that's why you're not ranking for "CRM software pricing".**

## P0 — Fix now
_(none — good news)_

## P1 — Fix this week

- **Title tag is 7 characters and missing the target keyword**
  - Why it matters: Google uses the title as the strongest signal for what a page is about. "Pricing" alone is generic. It competes with every pricing page on the internet.
  - Exact fix: Change to something like "CRM Software Pricing — Plans from $29/month | Acme CRM" (55 chars).

- **Meta description is missing**
  - Why it matters: Google often generates its own snippet when this is missing, and it's usually worse than what you'd write. You lose control of the click decision.
  - Exact fix: Write a 150-160 character description that includes the target keyword and one compelling reason to click. Example: "Acme CRM pricing starts at $29/user/month. Compare our Starter, Growth, and Scale plans. 14-day free trial, no credit card needed."

- **Missing og:image — social shares look broken**
  - Why it matters: When someone shares this URL in Slack, LinkedIn, or a sales email, it shows up as a text-only link. That drops click-through dramatically.
  - Exact fix: Create a 1200x630 image with "Acme CRM Pricing" and the headline price, upload it, and add `<meta property="og:image" content="https://acme-crm.com/og/pricing.png">`. Also add og:description.

- **No Product schema on a pricing page**
  - Why it matters: Google rewards pricing pages that use Product schema with rich results (price, review stars). Without it, you're invisible in the rich result competition.
  - Exact fix: Add JSON-LD Product schema with Offer nodes for each plan. Template:
    ```
    <script type="application/ld+json">
    { "@context": "https://schema.org", "@type": "Product",
      "name": "Acme CRM", "offers": [
        { "@type": "Offer", "name": "Starter", "price": "29", "priceCurrency": "USD" },
        { "@type": "Offer", "name": "Growth", "price": "79", "priceCurrency": "USD" }
      ]
    }
    </script>
    ```

## P2 — Easy wins

- **H1 says "Pricing plans" — doesn't include target keyword**
  - Why it matters: H1 is the second-strongest on-page ranking signal after title. Generic wording leaves rankings on the table.
  - Exact fix: Change H1 to "Acme CRM Pricing Plans" or "CRM Software Pricing".

- **Twitter card is `summary` not `summary_large_image`**
  - Why it matters: Large image cards get 2-3x more engagement on Twitter/X and LinkedIn.
  - Exact fix: Change `<meta name="twitter:card" content="summary_large_image">`.

- **2 images missing alt text**
  - Why it matters: Accessibility + a small ranking signal. If the icons are decorative, set `alt=""` explicitly.
  - Exact fix: Add descriptive alt text to the plan comparison icons, or set `alt=""` if they're purely decorative.

## P3 — Nice to have

- **3 generic anchor texts ("learn more")**
  - Fix: Rewrite to something descriptive — "see Growth plan features" instead of "learn more".

- **Word count is 412 — a bit thin for a commercial page**
  - Fix: Add a short FAQ section (3-5 questions) at the bottom. Gets you more words AND more schema opportunities (FAQPage).

---

## What this audit did NOT check

- Core Web Vitals and page speed — run Google PageSpeed Insights (pagespeed.web.dev) on this URL
- Security headers (CSP, HSTS, etc.) — ask your dev
- JavaScript-rendered content — the HTML looked complete, but if you use client-side routing, double-check

## Next steps

1. Fix the 4 P1 items this week. Title + meta description alone will likely move you up the rankings for "CRM software pricing".
2. Re-run this audit after launch to confirm the grade moved to B or A.
```

---

## Notes for Claude running this skill

- Don't hedge. If the title is too short, say it's too short. The user came for a verdict.
- Lead with the finding the user actually asked about. They said "not ranking for X" — the title tag is the first thing they need to see.
- Give exact copy-paste fixes when possible. Non-technical marketers can't translate "improve your schema" into working code.
- Always end with the "what this did NOT check" disclosure. Don't let them walk away thinking this was a full SEO audit.

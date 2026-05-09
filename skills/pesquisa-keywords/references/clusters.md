# Clustering Deep Dive: Foundation Filter & Anchor Sorting

Detailed reference for the CLUSTER step of the keyword research process. SKILL.md gives the summary — this file holds the full gate-by-gate logic, scoring template, and edge cases.

---

## the foundation filter — full detail

Every anchor needs to clear four gates before you commit resources to it. Skipping this step is the fastest way to write content nobody finds.

### Gate 1: Search demand

Does this anchor attract more than 1,000 combined monthly searches across its cluster?
- **Pass** → Valid anchor
- **Fail** → Downgrade to a single article, or cut it

**The trap:** Naming an anchor after your signature method. Nobody searches your method name. They search the problem it fixes.

Example of the trap:
- Wrong anchor: "The Smith Method for AI Marketing"
- Right anchor: "AI Marketing Workflows for Solopreneurs"

### Gate 2: Audience language

Are you using the words THEY type, or the words YOU use internally?

- Wrong: "My signature culinary system"
- Right: "Learn to cook at home"
- Wrong: "[Your brand] recipes"
- Right: "Easy recipes for beginners"
- Wrong: "Holistic content amplification framework"
- Right: "How to repurpose blog posts"

Search engines reward content that matches how real people phrase things. Run every anchor name past the question: "Would a stranger type this exact phrase into Google?"

### Gate 3: Competitive reality

Pull up the top three results for your anchor keyword:
- All major authority sites (Food Network, Bon Appetit, NYT Cooking, Forbes, HubSpot)? Find a tighter angle or niche down.
- Mix of big and small publishers? Winnable with superior content.
- Weak content from unknown sites? Open territory — move fast.

**Tighter angle techniques when blocked by giants:**
- Add an audience qualifier ("for solopreneurs", "for non-developers")
- Add a constraint ("under $50", "in 30 minutes")
- Add a year ("in 2026")
- Add a contrarian framing ("without coding", "without ads")

### Gate 4: Unfair advantage

What do you bring that nobody else can?
- Your own data, results, or case studies → High priority
- A unique teaching method you built and named → High priority
- Hands-on practitioner experience (you do this daily, not just write about it) → Priority
- The same recycled tips everyone publishes → Deprioritize

If you have no unfair advantage on a topic, you can still write it — but it goes to the back of the queue behind topics where you have one.

---

## scoring each anchor

Use this exact template for every candidate anchor:

```
Anchor: [Name]
Search demand: PASS/FAIL — [evidence]
Audience language: PASS/FAIL — [evidence]
Competitive reality: PASS/FAIL — [evidence]
Unfair advantage: YES/NO — [what is it]
VERDICT: VALID ANCHOR / DEMOTE TO ARTICLE / CUT
```

**Verdict logic:**
- 4 passes (or 3 passes + YES on advantage) → VALID ANCHOR
- 2 failures → DEMOTE TO ARTICLE (fold into another anchor)
- 3+ failures → CUT
- Search demand FAIL alone → automatic DEMOTE regardless of other gates (no demand = no traffic)

---

## how to sort keywords into clusters

1. **Meaning** — Keywords describing the same core concept go together
2. **Intent** — Keywords where the searcher wants the same type of answer get grouped (informational stays separate from commercial even if topic overlaps)
3. **Pick the anchor keyword** — Broadest term in the group becomes the label
4. **Tag the supporters** — More specific variations sit underneath

**Example sort:**

Raw keywords:
- 30-minute dinner recipes for families
- meal prep vs cooking fresh every night
- easy dinners with 5 ingredients or less
- weeknight dinner mistakes everyone makes
- best one-pot meals for beginners
- best instant pot for families
- instant pot recipes for beginners

After sort:
- **Anchor: Quick Weeknight Dinners** (informational, recipe-focused)
  - 30-minute dinner recipes for families (how-to)
  - Meal prep vs cooking fresh every night (comparison)
  - Easy dinners with 5 ingredients or less (practical guide)
  - Weeknight dinner mistakes everyone makes (problem-solution)
  - Best one-pot meals for beginners (listicle)
- **Anchor: Instant Pot Cooking** (separate — different equipment focus, partly commercial)
  - Best instant pot for families (commercial)
  - Instant pot recipes for beginners (informational)

The two could feel related, but their intent and tooling differ enough that a single anchor would dilute both.

---

## edge cases

**One keyword sits between two anchors.** Put it under the anchor where it ranks more naturally as a supporting article. If you're truly torn, write the article once and link it from both anchor hubs.

**An anchor only has 2 supporting clusters.** It's not an anchor — it's a thick article with two sub-sections. Demote and merge.

**An anchor has 15+ supporting clusters.** Split it into two anchors. Look for a natural fault line (audience type, intent type, time-bound vs evergreen).

**Keywords don't match any anchor.** Either you missed an anchor (review the Prism scan output for clusters of 4+ orphans) or those keywords are noise from the expansion step. Drop them.

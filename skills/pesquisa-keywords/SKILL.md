---
name: pesquisa-keywords
description: "Find what your audience searches for and build a content plan around it. No paid tools required. Use when someone needs topic ideas, a content strategy, SEO direction, or asks what should I write about. Runs a Prism Scan to expand seed keywords, organizes them into topic anchors, and delivers a scored content calendar. Triggers on: keyword research for X, content strategy for X, what topics should I cover, SEO strategy, content calendar, topic clusters. Outputs scored keyword clusters with content recommendations."
---

# Keyword Research

Most keyword research dies in a spreadsheet because it starts with the tool, not the buyer. This skill flips that: pull the language from the business and the audience first, then expand outward through six angles, then score every cluster against opportunity AND revenue before a single article gets written. The output is a ranked content plan with a clear first move — not a 500-row CSV nobody opens twice.

## the core job

**What this produces:** A scored content plan containing keyword clusters sorted into topic anchors, ranked on real opportunity, matched to specific content formats, and topped with one explicit first-move recommendation.

**Output format:** Markdown deliverable with four sections — (1) summary of biggest opportunities + first move, (2) anchor detail tables with intent and format per cluster, (3) 90-day publishing calendar, (4) optional appendix of full keyword universe organized by anchor. See [output format](#output-format) section below for the exact template.

---

## before starting: gather context

**STOP. Do not produce keyword research until context is in hand. Cap questions at 2 max.**

### Step A: Gather context (fast)

Keyword research needs two dimensions from context: **ICP** (their language IS the keyword list) and **business** (what maps to offers). Voice is not needed here.

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for audience pain, exact phrases they use, products, services, content pillars.
2. **If missing, check the project folder** for `Context/icp.md` and `Context/business.md`. Read whichever exist.
3. **If audience is still unclear after both:** ask inline, don't guess. The ICP's language IS the research output.

### Step B: Confirm the brief (≤2 questions, combined)

Skip anything CLAUDE.md or `Context/` files cover. Prioritize and combine into at most 2 questions:

1. **Offer + audience + website** — "What's being sold, to whom, and what's the current URL?" (combine into one question)
2. **Goal + competitors + timeline** — "Goal (traffic, leads, sales, authority), two or three competitors if you have them, and quick wins vs. long-term?" (combine)

---

## the process

Five named stages, run in order. Do not skip ahead — clustering before mining produces shallow groups, scoring before clustering produces meaningless rankings.

```
MINE → EXPAND → CLUSTER → SCORE → MAP
 |        |         |         |       |
seeds   universe  anchors  priorities calendar
```

1. **MINE** — Extract 20-30 starter keywords from what the business actually does
2. **EXPAND** — Run the Prism Scan (6 angles) to grow a 100-200 keyword universe
3. **CLUSTER** — Sort the universe into 5-10 topic anchors, run the Foundation Filter
4. **SCORE** — Rate each anchor on business value, opportunity, time to rank
5. **MAP** — Pair top anchors with content formats and a 90-day publishing schedule

---

## mine: surface starter terms

**Instruction:** Pull 20-30 starter keywords from the business context, spread evenly across four buckets. Don't over-index on one bucket — a list with 25 offer terms and 0 frustration terms misses how buyers actually search.

**Framework — the 4-Bucket Starter Matrix:**

| Bucket | What goes here | Example (online cooking school) |
|--------|---------------|--------------------------------|
| Offer terms | Your actual products and services | "online cooking classes", "meal prep course", "home chef program" |
| Pain terms | Frustrations that drive them to search | "can't cook healthy meals", "wasting money on takeout", "boring weeknight dinners" |
| Result terms | Outcomes they dream about | "cook restaurant-quality food at home", "impress dinner guests", "healthy family meals" |
| Industry terms | The broader category you belong to | "online culinary school", "cooking courses", "learn to cook" |

**Short example:** A workshop selling Claude Code training would mine: offer = "claude code workshop", pain = "claude code overwhelming", result = "automate marketing tasks", industry = "AI for marketers".

**Anti-pattern:** Listing only your product names ("Acme Cooking Pro Plus", "Acme Knife Mastery"). Buyers don't search brand names they've never heard of. Search the problem, not the SKU.

---

## expand: the prism scan

**Instruction:** Feed each starter keyword through 6 different angles to surface terms you'd otherwise miss. This is the 6-angle Prism — each angle refracts the seed into a different keyword set.

**Framework — the 6 Angles:**

| Angle | Focus | Example keywords |
|-------|-------|-----------------|
| **Your offer** | Products, programs, packages you sell directly | "8-week cooking bootcamp", "virtual chef lessons", "knife skills course" |
| **Their frustration** | Problems they're googling late at night | "everything I cook tastes bland", "scared of the kitchen", "keep burning food" |
| **Their desired result** | The transformation, not the process | "cook like a pro at home", "healthy dinners in 20 minutes", "host a dinner party confidently" |
| **Your edge** | Why you instead of thousands of alternatives | "cooking for absolute beginners", "30-minute meals only", "chef who couldn't boil water at 25" |
| **Adjacent interests** | Related topics your audience also explores | "kitchen organization", "grocery budgeting", "food photography", "wine pairing basics" |
| **Names and brands** | People, tools, and methods you want associated with you | "Blue Apron alternative", "Gordon Ramsay techniques", "MasterClass cooking", "cast iron cooking" |

After running all six angles, multiply each keyword using the patterns in [references/topic-mining.md](references/topic-mining.md) (modifiers, question stems, comparison patterns, time/place qualifiers).

**Goal:** Grow from 20-30 starters to 100-200 expanded keywords.

**Short example:** Seed "claude code workshop" through Angle 2 (frustration) yields "claude code too technical", "stuck setting up claude code", "claude code tutorial overwhelming". Through Angle 6 (names/brands) yields "cursor vs claude code", "claude code for marketers reddit".

**Anti-pattern:** Running only Angle 1 (your offer). You end up with 50 variants of your product name and zero terms representing how the audience actually phrases their pain. The Prism only works if you actually rotate through all 6.

---

## cluster: form topic anchors

**Instruction:** Take the expanded keyword list and organize it into topic anchors. Each anchor is a broad subject that can support a flagship guide PLUS supporting articles, with room to keep adding content for years. Aim for 5-10 anchors total. Then run every anchor through the Foundation Filter — anchors that fail two or more gates get demoted or cut.

**Framework — the Anchor Test (4 questions):**

Each anchor must support:
- One comprehensive flagship guide (3,000-8,000 words)
- Three to seven supporting articles underneath it
- Room to keep adding content over time
- A sustainable answer to "everything someone needs to know about X"

### how to sort keywords into clusters

1. **Meaning** — Keywords describing the same core concept go together
2. **Intent** — Keywords where the searcher wants the same type of answer get grouped
3. **Pick the anchor keyword** — Broadest term in the group becomes the label
4. **Tag the supporters** — More specific variations sit underneath

### sample anchor

**Anchor:** Quick Weeknight Dinners

**Supporting clusters:**
- 30-minute dinner recipes for families (how-to)
- Meal prep vs cooking fresh every night (comparison)
- Easy dinners with 5 ingredients or less (practical guide)
- Weeknight dinner mistakes everyone makes (problem-solution)
- Best one-pot meals for beginners (listicle)

### the foundation filter

Every anchor needs to clear four gates before you commit resources to it. Skipping this step is the fastest way to write content nobody finds.

- **Gate 1: Search demand** — anchor attracts >1,000 combined monthly searches across its cluster (the trap: naming it after your signature method nobody searches)
- **Gate 2: Audience language** — uses the words THEY type, not what YOU say internally
- **Gate 3: Competitive reality** — top 3 results aren't all major authority sites (or you've found a tighter angle)
- **Gate 4: Unfair advantage** — you bring data, method, or hands-on experience competitors don't have

**Scoring template:**

```
Anchor: [Name]
Search demand: PASS/FAIL — [evidence]
Audience language: PASS/FAIL — [evidence]
Competitive reality: PASS/FAIL — [evidence]
Unfair advantage: YES/NO — [what is it]
VERDICT: VALID ANCHOR / DEMOTE TO ARTICLE / CUT
```

Two or more failures means it doesn't qualify as an anchor. Fold it into a single article elsewhere, or drop it.

**Full gate-by-gate examples, edge cases (one keyword between two anchors, anchors that should split, keywords that don't fit anywhere), and the verdict logic table:** [references/clusters.md](references/clusters.md).

**Anti-pattern:** Calling every keyword cluster an "anchor" because it sounds important. If a topic only supports one article, it's an article — not an anchor. Inflating anchor count produces a thin content map that collapses under the first attempt to publish.

---

## score: the action ladder

**Instruction:** Not every cluster deserves attention right now. Rate each one across three dimensions, then combine the scores into a priority tier. The scoring step is what separates a content plan from a keyword dump.

**Framework — the 3-Dimension Score:**

### business value

- **High** — Directly tied to revenue. Commercial intent keywords. Close to a purchase decision. Core offer.
- **Medium** — Indirect path. Builds credibility. Captures email signups. Educational content.
- **Low** — Awareness only. Loosely related to the business. Nice to have, not essential.

### opportunity level

Signals pointing to high opportunity:
- No quality content exists yet (you'd own the space)
- Existing content is stale (two-plus years old)
- Top results are shallow and generic
- You have a unique angle competitors miss
- Interest is trending upward (check Google Trends)

Signals pointing to low opportunity:
- Dominated by massive authority sites
- Already packed with excellent content
- Extremely competitive commercial terms
- Declining search interest

### time to rank

- **Fast (3 months)** — Low competition, genuine expertise or unique data, obvious content gap
- **Medium (6 months)** — Moderate competition, needs thorough content, clear path to stand out
- **Long (9-12 months)** — High competition, requires building domain authority, may need backlink work

### combining the scores

- High value + High opportunity + Fast → **First priority**
- High value + High opportunity + Medium → **Second priority**
- High value + Medium opportunity + Fast → **Third priority**
- Medium value + High opportunity + Fast → **Quick win**
- High value + Low opportunity + Any speed → **Long play**
- Low value + Any combination → **Backlog**

**Short example:** "Best AI tools for marketers 2026" — High business value (commercial intent), Medium opportunity (competitive but beatable with real testing data), Medium time → Second priority.

**Anti-pattern:** Putting every cluster on "First priority" because they all feel important. The action ladder only works if it actually filters. If everything is priority one, nothing is.

---

## map: assign content pieces

**Instruction:** For each high-priority cluster, decide exactly what to build — format, intent match, CTA, and publish week. The map turns scored clusters into a real calendar with dates next to titles.

**Framework — the Format-Intent-CTA grid:**

### matching format to purpose

- **Flagship Guide** (5,000-8,000 words) — When you want to completely own a topic
- **Step-by-Step Tutorial** (2,000-3,000 words) — Teaching a process from start to finish
- **Comparison Piece** (2,500-4,000 words) — X vs Y articles, "best of" roundups
- **Listicle** (2,000-3,000 words) — Collections of tools, examples, or tips
- **Use Case Article** (1,500-2,500 words) — Targeting a narrow niche or specific scenario
- **Explainer** (1,500-2,500 words) — Answering "what is [term]" questions

### reading search intent

| Intent signal | Keyword clues | Content approach | Best CTA |
|--------------|---------------|-----------------|----------|
| Informational / Learning | what, how, why, guide | Teach thoroughly | Newsletter signup, free resource |
| Commercial / Evaluating | best, vs, review, compare | Help them decide | Free trial, demo |
| Transactional / Buying | buy, pricing, get, hire | Remove friction | Purchase, book a call |
| Navigational | brand or product name | Confirm + redirect | Direct to product page |

### publishing cadence

- **Tier 1 (Weeks 1-4):** Highest priority flagship content
- **Tier 2 (Weeks 5-8):** High priority supporting pieces
- **Tier 3 (Weeks 9-12):** Medium priority depth builders
- **Tier 4 (Backlog):** Lower priority items for later

**Short example:** Cluster "claude code for non-technical marketers" → Informational intent → Flagship Guide format (5,000 words) → CTA = workshop waitlist signup → Publish Week 1-2.

**Anti-pattern:** Picking format by what you feel like writing. Format is determined by intent. A "buying" intent keyword does not get a 5,000-word flagship — it gets a tight comparison page with a clear CTA above the fold.

---

## anti-slop on prose sections

Keyword lists and topic clusters don't need anti-slop — they're research data. But any PROSE output (article briefs, positioning statements, content angle descriptions, "First Move" recommendations) should be passed through the `anti-slop` skill before delivery. Scan for robot phrases (leverage, unlock, delve, supercharge) and generic claims with no specifics.

---

## output format

### summary

```
# Keyword Research: [Business Name]

## Biggest Opportunities
1. [Keyword/cluster] — [Why this matters]
2. [Keyword/cluster] — [Why this matters]
3. [Keyword/cluster] — [Why this matters]

## Fast Wins (rankable in 3 months)
- [Keyword] — [Why it's quick]
- [Keyword] — [Why it's quick]

## Long Game (6-12 months)
- [Keyword] — [Strategy needed]

## First Move
[The exact first piece to create and the reasoning behind it]
```

### anchor detail

```
## Anchor: [Topic Name]
**Priority:** [Critical / High / Medium / Low]
**Content pieces:** [Number]

| Cluster | Priority | Intent | Format | Target Date |
|---------|----------|--------|--------|-------------|
| [name]  | [H/M/L]  | [type] | [format] | [date]    |
```

### article brief

```
## Article Brief: [Working Title]
**Target keyword/cluster:** [primary + 3-5 supporting]
**Intent:** [informational / commercial / transactional / navigational]
**Format:** [flagship / tutorial / comparison / listicle / use case / explainer]
**Target word count:** [range]
**Angle:** [what makes this piece different from top 3 results]
**CTA:** [what readers do at the end]
**Publish week:** [Wk N]
```

### 90-day content calendar

```
## Month 1
- Week 1-2: [Flagship piece] — [Target cluster]
- Week 3: [Supporting piece] — [Target cluster]
- Week 4: [Supporting piece] — [Target cluster]

## Month 2
- Week 5-6: [Second anchor piece] — [Target cluster]
...
```

---

## example: claude code workshop for non-technical marketers

### context gathered
- **Business:** Live workshop teaching non-technical marketers to set up and use Claude Code
- **Audience:** Marketers, creators, solopreneurs who saw the hype, tried Claude Code, got stuck — feel left behind
- **Goal:** Workshop signups + cohort upsell
- **Timeline:** Quick wins to fill next workshop, plus long-term authority

### starter keywords mined (4-bucket matrix)
- **Offer:** claude code workshop, claude code course, claude code training, claude code for marketers
- **Pain:** claude code too technical, claude code stuck setup, claude code overwhelming, claude code not working
- **Result:** automate marketing with ai, write content with claude code, stop paying for ai tools, marketing automation no code
- **Industry:** ai for marketers, ai content creation, ai marketing tools, claude vs chatgpt

### expanded via prism scan (sample of 100+ keywords)

**Angle 1 (Offer):** claude code workshop, claude code bootcamp, claude code tutorial for beginners, claude code skill files
**Angle 2 (Frustration):** claude code installation problems, why is claude code so hard, claude code commands not working, gave up on claude code
**Angle 3 (Result):** ship a newsletter with ai, ai content workflow that works, automate weekly content, marketing on autopilot
**Angle 4 (Edge):** claude code without coding, claude code for non-developers, marketer's guide to claude code, claude code for content creators
**Angle 5 (Adjacent):** n8n automations for marketers, ai newsletter tools, ai for solopreneurs, prompt engineering for marketing
**Angle 6 (Names/brands):** cursor vs claude code, anthropic claude code review, claude code reddit, simon willison claude code

### organized into 5 topic pillars (anchors)

**Pillar 1: Claude Code for Non-Technical Users** (Priority: Critical)
- claude code without coding
- claude code for marketers
- claude code beginner guide
- claude code setup walkthrough

**Pillar 2: Common Claude Code Problems & Fixes** (Priority: High)
- claude code installation issues
- claude code commands not working
- claude code skill files explained
- claude code overwhelming where to start

**Pillar 3: Claude Code for Marketing Workflows** (Priority: Critical)
- ai content workflow with claude code
- automate newsletter writing
- claude code for social media
- claude code n8n integration

**Pillar 4: Claude Code vs Other AI Tools** (Priority: High — commercial intent)
- claude code vs cursor
- claude code vs chatgpt
- claude code vs perplexity for research
- best ai tool for marketers 2026

**Pillar 5: Claude Code Skills & Prompts Library** (Priority: Medium)
- best claude code skills for marketers
- claude code prompt library
- claude code skill files download
- how to write a claude code skill

### 12 keyword clusters with intent classification

| Cluster | Intent | Pillar | Priority |
|---------|--------|--------|----------|
| claude code for marketers | Commercial | 1 | Critical |
| claude code without coding | Informational | 1 | Critical |
| claude code setup walkthrough | Informational | 1 | High |
| claude code installation issues | Informational | 2 | High |
| claude code commands not working | Informational | 2 | Medium |
| automate newsletter writing | Informational | 3 | Critical |
| claude code n8n integration | Informational | 3 | High |
| claude code vs cursor | Commercial | 4 | High |
| claude code vs chatgpt for marketing | Commercial | 4 | High |
| best ai tool for marketers 2026 | Commercial | 4 | Medium |
| claude code workshop | Transactional | 1 | Critical |
| best claude code skills | Commercial | 5 | Medium |

### 3 article briefs

**Brief 1: First Priority — Flagship**
- **Working title:** Claude Code for Marketers: The Complete Setup Guide (No Coding Required)
- **Target keyword/cluster:** claude code for marketers (primary) + claude code without coding, claude code beginner guide, claude code setup walkthrough
- **Intent:** Informational with commercial undertone
- **Format:** Flagship guide
- **Target word count:** 6,000 words
- **Angle:** Written by a non-technical marketer who set it up the easy way — every screenshot, every error, every fix. Top results are written by devs and skip the parts marketers actually get stuck on.
- **CTA:** Workshop waitlist signup (lead magnet: skill files pack)
- **Publish week:** Week 1-2

**Brief 2: Second Priority — Comparison**
- **Working title:** Claude Code vs Cursor vs ChatGPT: Which One Should a Marketer Actually Use in 2026?
- **Target keyword/cluster:** claude code vs cursor (primary) + claude code vs chatgpt, best ai tool for marketers 2026
- **Intent:** Commercial
- **Format:** Comparison piece
- **Target word count:** 3,500 words
- **Angle:** Real marketing tasks tested side-by-side (newsletter draft, social repurpose, landing page). Most comparisons are written for developers — this one scores them on marketing workflows.
- **CTA:** Workshop signup with "see Claude Code in action live" framing
- **Publish week:** Week 3-4

**Brief 3: Quick Win — Tutorial**
- **Working title:** Why Your Claude Code Won't Run (And the 5-Minute Fix)
- **Target keyword/cluster:** claude code installation issues + claude code commands not working
- **Intent:** Informational, support-flavored
- **Format:** Step-by-step tutorial
- **Target word count:** 1,800 words
- **Angle:** Documents the exact errors marketers hit on a fresh Mac, in order of frequency. Every other tutorial assumes you already have Node, brew, git — this one starts before that.
- **CTA:** "If setup still won't work, the workshop walks you through it live" → waitlist
- **Publish week:** Week 5

### top 3 recommendations summary

**1. "Claude Code for Marketers: The Complete Setup Guide" (First Priority)** — Owns the core commercial keyword. Top results today are dev-focused or shallow. Practitioner credibility from real workshop completions.

**2. "Claude Code vs Cursor vs ChatGPT for Marketers" (Second Priority)** — Captures buyers in active evaluation. Commercial intent, weak existing comparison content for the marketer angle.

**3. "Why Your Claude Code Won't Run" (Quick Win)** — Solves a panic-state problem with high search volume. Builds trust and funnels into the workshop as the "do this with me live" upsell.

---

## alternate worked example

For a second full walkthrough of the same Mine → Expand → Cluster → Score → Map process applied to a different vertical (online cooking school), see [references/example-cooking-school.md](references/example-cooking-school.md).

---

## boundaries

This produces **strategic direction**, not:
- Real-time search volume data (use free tools to verify if needed)
- Automated search results analysis (check manually)
- Finished written content (pass to the escrever-copy skill)
- Technical SEO audits (separate discipline entirely)

The output is a scored plan. Writing comes next.

---

## free validation tools

When you want to sanity-check the research with real numbers:

- **Google Trends** (trends.google.com) — Spot whether interest is climbing or fading
- **Google Search** — Autocomplete suggestions and "People Also Ask" boxes are free gold
- **AnswerThePublic** (free tier) — Pulls question-based keyword ideas
- **AlsoAsked** (free tier) — Shows how questions connect to each other
- **Reddit/Quora search** — Reveals the actual words people use when discussing your topic

---

## how this connects to other skills

**pesquisa-keywords** determines WHAT topics to pursue. It produces the foundational strategy that other skills execute on.

Hand off to:
- **positioning-angles** — discovers the strongest angle for each piece in the plan
- **brand-voice** — maintains consistent voice across all the content this plan calls for
- **escrever-copy** — writes sales pages and conversion copy for commercial-intent clusters
- **vibe2-seo-content** — turns informational clusters into ranked long-form articles
- **escrever-newsletter** — repurposes anchor content into newsletter editions
- **sequencia-email** — builds nurture sequences for the lead magnets the plan recommends
- **lead-magnet** — creates the freebies that capture email at the top of each pillar
- **reaproveitar-conteudo** — atomizes flagship pieces into platform-native posts

This skill builds the strategy. Other skills handle execution.

---

## the test

Strong keyword research output meets these standards. Run every check before delivering:

1. **Context was gathered** — ICP + business info from CLAUDE.md or `Context/icp.md` / `Context/business.md` was referenced (or absence flagged) before any keyword work begins
2. **All 6 Prism angles ran** — keyword universe shows expansion across offer, frustration, result, edge, adjacent, and names/brands (not just one or two)
3. **Has a clear first move** — exactly ONE specific "start here" article recommendation with reasoning, not a tied-for-first list
4. **Ranked by real opportunity** — every cluster has an explicit priority tier with the score logic visible (value × opportunity × time)
5. **Honest about competition** — at least one cluster is explicitly flagged "long play" or "demote / cut" — if everything is winnable, the Foundation Filter wasn't run
6. **Tied to business goals** — each top recommendation traces back to a revenue path (workshop signup, lead magnet, cohort upsell), not just traffic
7. **Includes format + intent + CTA per priority piece** — at least the top 3 clusters have an article brief with format, intent classification, and CTA assigned

**Failure condition:** If the deliverable is a flat list of keywords with no priority scoring, no first move, and no format guidance — it failed. Reads "here are 500 keywords, figure it out" → reject and rerun the SCORE and MAP steps.

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` next to this SKILL.md.

### At the start of every session
1. Read `feedback.log` in this skill's folder. Apply every rule.
2. If it doesn't exist, create it with header: `# Keyword Research Workshop — Learned Rules`

### Triggers that require a log write

When the user says any of the following, immediately append a rule:
- "Don't include X in keyword research anymore" / "Stop suggesting X"
- "Always prioritize Y" / "From now on, group by Y"
- "I hate when you..." / "I don't like..."
- "That's perfect, keep doing that"
- Silent deletes where the user removes a keyword type — infer the rule

### Format for each rule
```
## YYYY-MM-DD — [short title]
**Rule:** [imperative sentence]
**Why:** [reason]
**How to apply:** [when this kicks in]
```

### What to log vs skip
**Log:** keyword filter rules, topic-clustering preferences, source preferences (never suggest X platform), output format rules.
**Skip:** one-off "remove this specific keyword" — that's task-specific, not a rule.

### Cleanup every ~10 entries. Consolidate, delete reversed rules, keep under 100 lines.

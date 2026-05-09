---
name: escrever-copy
description: "Write copy that converts — landing pages, sales pages, emails, CTAs, ads, social posts, hero sections. Use when the user says: write copy for X, help me sell X, make this convert, punch this up, write a landing page, write sales copy, write a hero section, write a CTA. Reads the user's business, ICP, and voice from CLAUDE.md or the project's `Context/` folder before writing. Runs every draft through the anti-slop skill before shipping. Outputs copy that reads like a smart friend talking, not a marketing team."
---

# Copywriting Workshop

Most copy sounds like a marketing team wrote it. Hedged, generic, trying to please everyone. The stuff that converts sounds like one person talking to one person — opinionated, specific, proof-backed.

This skill writes that. It pulls the user's actual business context, ICP language, and voice from CLAUDE.md (or `Context/` files at the project root), then runs classic direct-response principles (Schwartz, Ogilvy, Sugarman) through a modern internet-native filter. Every draft gets passed through `anti-slop` before delivery.

---

## the core job

Turn a copy request into a converting draft that sounds like the user, speaks to their ICP, and uses proven persuasion structures under the hood.

**Output:** Copy in the requested format (headline, hero, full landing page, email, CTA, ad, etc.), grounded in the user's business + ICP + voice context, with an anti-slop pass applied.

---

## before starting: gather context

**STOP. Do not produce any copy until the context below is in hand. Ask at most 2 quick questions before writing — no more.**

### Step A: Gather context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md` into this conversation. Scan what's already loaded for:
   - **Business** — what the user sells, pricing, tools. Grounds offers and claims.
   - **ICP** — who the customer is, their pain, the exact phrases they use. The copy must sound like it was written for THIS person.
   - **Voice** — do/don't rules, tone, sample sentences. The copy must read like the user wrote it.
2. **If any of those is missing, check the project folder.** Look for `Context/business.md`, `Context/icp.md`, `Context/voice.md` at the project root. Read whichever exist.
3. **Still missing something critical? Ask ≤2 questions, then write.** Never more — keep the workshop flow fast.

### Step B: Confirm the brief (merge into the ≤2-question cap)

When you need inputs, prioritize in this order and stop at 2:

1. **Format + offer** — "Quick — what format (landing page, email, hero, CTA, ad?) and what are we selling?" Combine into one question.
2. **Awareness level OR the one thing** — pick whichever is less obvious from context. (See [references/classic-frameworks.md](references/classic-frameworks.md) for Schwartz's 5 stages.)

**Skip anything CLAUDE.md or the `Context/` files already answer.** If the ICP is clear in context and the user just said "write my landing page hero," confirm the offer + awareness level in one message, then go.

---

## the process

```
GROUND → STRUCTURE → DRAFT → ANTI-SLOP → SHIP
```

Five steps. Don't skip any.

---

## Step 1 — Ground: pull the raw material

Before writing a word, extract from your gathered context (CLAUDE.md + any `Context/` files):

- **Transformation** — the before/after for this ICP (pains → outcomes)
- **Proof** — numbers, testimonials, case studies, personal results (business side)
- **Voice markers** — 3-5 sample sentences to match rhythm
- **Customer language** — phrases the ICP uses verbatim, not the user's paraphrases of them.
- **Objections** — what's stopping them

Write these as a short brief (~100 words) before drafting. This is the raw material everything else pulls from.

**Anti-pattern:** Don't invent numbers, testimonials, or proof. If the context doesn't have it, ask the user. Fake specifics destroy trust faster than vague claims.

---

## Step 2 — Structure: pick the skeleton

Pick the structure based on the format and awareness level.

### Hero section / landing page top
Outcome headline → quantified pain → transformation promise → CTA

### Full landing page / sales page
1. Hook (outcome headline with specific number or timeframe)
2. Problem (quantify the pain — hours wasted, money lost)
3. Agitate (scenario that makes the problem vivid)
4. Credibility (founder story or proof numbers)
5. Solution (framed as transformation, not features)
6. Proof (specific-outcome testimonials)
7. Objections (FAQ or fit/not-fit section)
8. Offer (pricing with value justification)
9. CTA (benefit-oriented, friction reducers below)

Not every page needs all nine. Higher awareness = fewer sections. Lower awareness = longer copy.

### Email
Subject line (open loop) → short first line → one story or one idea → single CTA

### CTA / button
Benefit-oriented verb + friction reducer below (price + social proof + speed)

### Tweet / social post
See `post-longo-x` or `kieran-writing`. This skill covers everything else.

**Framework depth:** For headline formulas, see [references/headlines.md](references/headlines.md). For opening lines, see [references/openings.md](references/openings.md). For transitions and flow, see [references/flow.md](references/flow.md). For Schwartz awareness stages, see [references/classic-frameworks.md](references/classic-frameworks.md).

---

## Step 3 — Draft: write it

Write the copy section by section. Apply these principles throughout:

### Specificity beats vagueness
- "Save $327 on your taxes" beats "Save money on your taxes"
- "2,894 makers shipped with us" beats "thousands of happy customers"
- "$47,329 in one day" beats "significant revenue"
- Numbers create belief. Details create mental images. Use the exact numbers from `business.md`.

### The So What? Chain
For every feature, ask "so what?" until you hit something emotional or financial.

> Feature: Fast database
> So what? → Queries load in milliseconds
> So what? → Users don't bounce, revenue doesn't leak
> So what? → You stop waking up stressed about churn

Write from the bottom of the chain. Not "saves 4 hours" but "close your laptop at 5pm instead of 9pm."

### Quantify the pain
Don't describe the pain. Do the math.

> "4 hrs for emails + 6 hrs for landing pages + 4 hrs for Stripe + 2 hrs for SEO + ∞ hrs overthinking
> = 22+ hours of headaches.
> There's an easier way."

When readers see "22+ hours," they calculate whether it's worth paying to skip.

### Rhythm: alternate short and long
All-short reads choppy. All-long reads exhausting.

Short punch. Then a longer sentence that breathes, adds context, feels like actual conversation. Then punch again.

Pattern: hook (short) → expand (longer) → land it (kicker).

### Open loops, then close them
End paragraphs with hooks: "But there's more." "Here's where it gets interesting." "But the second one is where it gets weird." Use 2-4 per piece. Always close what you open.

### Proof beats claims
Every claim needs a number, a name, a date, or a testimonial behind it. If you can't back it up, cut it or soften it.

### Testimonial structure
[Before state] + [Action] + [Specific outcome] + [Timeframe] + [Emotion]

> "I shipped in 6 days as a noob coder. Would have taken months. I wanna cry 🥲"

### Disqualification
Tell some people they're NOT a fit. Flips "please buy" to "prove you're worthy."

### CTA formula
Benefit verb + friction reducer: **[Action]** → "$199 once. 2,600+ marketers. 2 minutes to install."

### Use the ICP's actual phrases
Pull quotes from `icp.md` → "How they talk about their problem." Drop them into the copy where relevant. This is the single biggest credibility signal in the whole piece.

---

## Step 4 — Anti-slop: mandatory pass

Before showing ANY draft to the user, run it through the `anti-slop` skill.

**How:** Invoke the `anti-slop` skill with the draft as input. It will catch AI patterns (binary opposites, em-dash overuse, robot phrases like "game-changer" / "unlock" / "leverage", throat-clearing hedges, rhetorical questions, forced threes) and return a cleaned version.

**If `anti-slop` is not available**, run the checks manually. Scan for:
- Rhetorical questions meant to build fake tension ("The best part?", "Want to know...", "Sound familiar?")
- Binary opposites ("It's not X, it's Y")
- Robot phrases (game-changer, supercharge, leverage, unlock, delve, dive in, robust, cutting-edge, seamless, unleash)
- Throat-clearing ("It's worth noting that...", "In today's fast-paced world...", "Let's dive in")
- Em dashes used as a crutch (1-2 max per piece)
- Same-length paragraphs throughout
- Every bullet starting with the same structure
- Zero contractions

Rewrite anything flagged.

**Non-negotiable:** No draft ships without this pass.

---

## Step 5 — Ship: deliver

Present the final copy. Keep the preamble short:

> Here's the [format] for [offer]. Based on [ICP phrase pulled from your context]. Ran through anti-slop.
>
> [Copy]

If there's anything the user needs to fill in (a specific number, a testimonial name, a price not in the context), mark it with `[PLACEHOLDER]` so they can see exactly what's missing.

---

## output format

The output is the copy itself, in whatever format was requested. No preambles about what copywriting is. No "here are 3 options" unless the user asked for options.

For longer pieces (landing page, sales page), structure with clear section headers so the user can scan:

```markdown
## Hero
[Headline]
[Subhead]
[Primary CTA]

## Problem
[Copy]

## Solution
[Copy]

## Proof
[Testimonials]

## Offer
[Pricing + guarantee]

## Final CTA
[Button text]
[Friction reducer line]
```

For short pieces (tweet, email, single CTA), just output the copy clean.

---

## example: landing page hero for a $99 Claude Code workshop

### Context pull (Step 1)
- Business: $99 live workshop teaching Claude Code to non-technical marketers. First run did ~$30k revenue. 350+ waitlist.
- ICP: "I've seen Claude Code everywhere, I know I should learn it, I tried it, I got stuck, I feel left behind."
- Voice: Direct. No thesaurus syndrome. Casual profanity OK. Parentheticals. No em dashes.
- Proof: 350 waitlist, ~$30k revenue from first workshop, attendees ship in the session.
- Objection: "I'm not technical enough."

### Awareness level
Solution-aware. They know AI tools exist. They've tried Claude Code. They need to see THIS approach is different.

### Draft

```markdown
## Hero

You've opened Claude Code 4 times this month.
Each time you closed it within 15 minutes.

This workshop fixes that in one afternoon.

**Get Claude Code actually set up →**
$99 · 350+ marketers on the waitlist · you ship something live in the session

## Problem

Here's what "learning Claude Code" usually looks like:
- Watch a 2-hour YouTube video
- Try to follow along
- Get stuck on setup
- Close the laptop
- Feel slightly worse about yourself
- Repeat next month

6+ hours gone. Nothing shipped. The people who "get it" pull further ahead.

## Solution

I'm not a dev. I hate touching code. I figured out the easiest route and built this workshop around it.

Three hours, live, hands-on. By the end:
- Claude Code fully configured on your machine
- My personal skill files loaded (the ones I use to run marketing)
- Something you actually produced (newsletter, landing page, ad — your pick)

No watching. No nodding along. You follow, I check your screen, you leave with output.

## Proof

First workshop: ~$30k revenue, 350+ on the waitlist, attendees shipped newsletters and landing pages during the live session.

## Offer

- Workshop only: **$99**
- Workshop + 2x 1hr 1:1: **$297**

Bonuses: my n8n automation library ($99 value).

## Final CTA

**Get set up in one afternoon →**
$99 · 3 hours live · you walk away with Claude Code running and something shipped
```

### Anti-slop pass notes
- Removed "game-changer" from the solution section
- Rewrote "it's not a course, it's a workshop" (binary opposite) → "No watching. No nodding along."
- Cut 2 em dashes, replaced with periods
- Added one parenthetical to match voice ("(newsletter, landing page, ad — your pick)")
- Swapped "utilize" → "use"

---

## how this connects to other skills

**Runs before this skill:**
- `entrevista-negocio` — builds business + ICP + voice context (writes to CLAUDE.md or `Context/business.md`) via guided questions.
- `vibe-keyword-research` — feeds search demand data into angles.

**Runs after this skill:**
- `anti-slop` — mandatory pass, called in Step 4.
- `polir-texto` — optional second polish pass for longer pieces.
- `landing-page` — for full page builds with design specs.
- `sequencia-email` — when the CTA leads into a sequence.

**Adjacent:**
- `post-longo-x` — for social-native long-form posts.
- `kieran-newsletter-writing` — for newsletter-specific voice.
- `interesting-idea` — for sharpening the angle before drafting.

---

## the test

Good copy from this skill:

1. **Sounds like the user** — pull the `voice.md` sample sentences next to the draft. Rhythm and word choice should match.
2. **Uses the ICP's exact language** — at least 2 phrases pulled from `icp.md` customer quotes appear verbatim.
3. **Proof-backed** — every claim has a number, name, date, or testimonial. No floating adjectives.
4. **Specific, not generic** — "$47,329" not "significant revenue." "2,894 makers" not "thousands of users."
5. **One thing** — a reader could tell you the main point in one sentence.
6. **Passed anti-slop** — run through the skill, no flagged patterns remaining.
7. **Benefit-oriented CTA** — the button verb describes what the user gets, not what they do.

If a competitor could run the same copy word-for-word with their name swapped in — it failed. Grounded copy is specific to this business, this ICP, this voice. Not "this category."

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` sitting next to this SKILL.md.

### At the start of every session using this skill
1. **Read `feedback.log`** in this skill's folder before writing anything. Apply every rule in it to this session's output.
2. If `feedback.log` doesn't exist yet, create it with a header: `# Copywriting Workshop — Learned Rules`

### During every session — triggers that require a log write

When the user says any of the following, **immediately append a rule to `feedback.log` before continuing**:

- "Don't do X anymore" / "Stop doing X" / "Never do X"
- "Always do Y" / "From now on, do Y" / "Whenever you write X, do Y"
- "I hate when you..." / "I don't like..."
- "That's perfect, keep doing that" (log positive patterns too — so you don't drift away from what works)
- "Remember that..." / "Keep in mind..."
- Direct rewrites where the user silently fixes your draft — infer the rule from the diff

### Format for each logged rule

```
## YYYY-MM-DD — [short title]

**Rule:** [the rule in one sentence, imperative voice]
**Why:** [the reason the user gave, or what they were reacting to]
**How to apply:** [when this kicks in — which step, which format, which trigger]
```

### What to log vs skip

**Log:**
- Voice rules ("never use the word 'leverage'")
- Format preferences ("always put the CTA in a code block")
- Structural choices ("skip the FAQ section unless I ask for it")
- Tone calibrations ("my ICP hates emoji — drop them from CTAs")

**Skip:**
- One-off task corrections ("change $99 to $149 on this page") — that's task-specific, not a general rule
- Preferences already covered in CLAUDE.md or `Context/voice.md` — those belong in the context source, not here

### Cleanup

Every ~10 entries, consolidate: merge duplicates, delete rules that were later reversed, keep the log under 100 lines. Stale rules that contradict current ones = drift.

**This is how the skill gets better.** Every rejection is a rule. Every "yes that's right" is a pattern to keep. Read the log. Apply the rules. Append new ones. Forever.

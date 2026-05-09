---
name: landing-page
description: "Write high-converting sales pages using a proven 5-part framework. Use when creating sales pages, landing pages, long-form sales copy, or product launch pages. Triggers on: write a sales page, create a landing page, help me sell this, write copy for my offer, landing page for X. Reads the user's business, ICP, and voice from CLAUDE.md or the project's `Context/` folder before writing. Writes in strategic order (story first, headline last) and runs every draft through the anti-slop skill before shipping. Outputs complete sales page copy ready to publish."
---

# Sales Page Builder

Most sales pages fail because people write them top to bottom. They start with the headline, get stuck, and quit. Or they copy a template and end up with generic copy that sounds like everyone else.

The trick is writing in the wrong order. You write the story first (it finds the voice), then the offer, then the close, then the lead, and the headline dead last — because by then you actually know what you're selling and why it matters.

This skill builds a complete sales page using that backwards process.

---

## the core job

Produce a **complete sales page** with all 5 sections:

1. Headline (prehead + main headline + deck copy)
2. Lead (150–200 word teaser)
3. Story (credibility through narrative)
4. Offer (what they get, broken into components)
5. Close (price justification + guarantee + CTA + FAQ)

**Output:** Full sales page copy, assembled in reading order, ready to paste into a page builder.

---

## before starting: gather context

**STOP. Do not write any copy until context is in hand. Cap questions at 2 max.**

### Step A: Gather context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md` into this conversation. Scan for:
   - **Business** — what the user sells, pricing tiers, delivery model, current proof. Grounds the offer and price sections in reality.
   - **ICP** — who the customer is, their pain, objections, the exact phrases they use. The headline, lead, and story must speak to THIS person.
   - **Voice** — do/don't rules, tone, sample sentences. Every section must read like the user wrote it.
2. **If missing, check the project folder** for `Context/business.md`, `Context/icp.md`, `Context/voice.md` at the project root. Read whichever exist.
3. **If voice is still missing:** note it and proceed — the draft will be generic-tone. The user can pass the output through `/anti-slop` or paste voice samples inline.

### Step B: Confirm the brief (≤2 questions, combined)

Skip anything CLAUDE.md or `Context/` files already cover. Combine related inputs into at most 2 questions:

1. **Offer + price + outcome** — "What's the product (name + format), the price (exact number, plus tiers or payment plans), and the single biggest outcome the customer gets?"
2. **Proof + what's included** — "What proof can you cite (testimonials, results, numbers, credentials), and what's literally inside the offer (modules, bonuses, calls, deliverables)?"

Never ask more than 2 questions. If the user's initial prompt already answers one, ask only what's missing.

---

## the process

```
RESEARCH → STORY → OFFER → CLOSE → LEAD → HEADLINE → ASSEMBLE → CHECK
```

Write in this order. The page reads in a different order. This is intentional — each step informs the next.

| You write... | It appears as... |
|--------------|------------------|
| 1. Research  | (doesn't appear — it informs everything) |
| 2. Story     | Section 3 on the page |
| 3. Offer     | Section 4 on the page |
| 4. Close     | Section 5 on the page |
| 5. Lead      | Section 2 on the page |
| 6. Headline  | Section 1 on the page |

---

## the core truth

Every sales page comes down to two things:

1. **Promise** — what outcome are you offering?
2. **Proof** — why should they believe you can deliver it?

If you're stuck on any section, ask: "Am I making a promise here? Am I providing proof? Am I doing both?"

---

## step 1: research the audience

Before writing a word, map these four things:

| Element | Question to answer |
|---------|--------------------|
| **Pain** | What specific problem keeps them up at night? |
| **Failed solutions** | What have they already tried that didn't work? |
| **Desire** | What does their ideal outcome look like? |
| **Objection** | What's the #1 reason they'd say no? |

Pull as much as possible from the ICP context. Only ask the user what's genuinely missing. Present the four answers back in 2-3 lines before proceeding — gives them a chance to correct.

---

## step 2: write the STORY

Start here. It's the easiest section and it sets the voice for everything else.

**Three parts — in order:**

1. **Introduce yourself** — name, relevant credentials, why they should listen. Just enough to make the next part credible.
2. **The problem (tried and failed)** — paint the pain vividly, then walk through 3 things they tried that didn't work, then the trigger-point insight.
3. **Finding the solution** — started experimenting → discovered the method → tested it → others asked for it → packaged it as the product.

**The "tried and failed" section is load-bearing.** It proves the user lived the problem. Skipping it makes the story sound like a guru pitch.

**Rules:**
- Use specifics. "200 cold emails" beats "a lot of emails." "$800" beats "almost nothing."
- Keep it 300-500 words.
- End with a line that transitions into the offer: "And that's what became [Product Name]."

For full story templates and worked examples across industries (copywriting, freelancing, coaching, SaaS), see [references/stories.md](references/stories.md).

---

## step 3: build the OFFER

Introduce what you're selling. Big picture first, then specifics.

**Four parts:**

1. **Introduce it** — name + one-sentence description + optional mockup image.
2. **The big promise** — main outcome, what makes it different, timeframe, objections handled, why it's easy, proof.
3. **The specifics** — break the offer into named components (modules, parts, bonuses). Each gets one sentence of purpose + 3–9 specific benefit bullets.
4. **Testimonials** — 3 to 5 only. Full name, location/title, pull the best phrase as a headline above each.

**Testimonial rules:**
- Specific results ("4.7% conversion", "booked in 3 weeks") beat vague praise ("really helped me").
- Variety matters — different people, different starting points, different outcomes.
- Never fabricate. If the business context doesn't have testimonials, mark `[TESTIMONIAL PLACEHOLDER]` and flag it in the output.

For component templates, bonus patterns, and 20+ varied testimonial examples, see [references/offers.md](references/offers.md).

---

## step 4: write the CLOSE

The close converts the fence-sitters. Most readers have already decided "yes" or "no" — this section moves the "maybes."

**Four parts:**

1. **Price justification** — anchor (what this normally costs) → state the price → explain why this price → trivialize it (compare to something they already spend on without thinking).
2. **Guarantee** — name it, make it longer than expected (60 days beats 30), resell the benefits inside it, make refunds easy, no fine print.
3. **CTA** — recap what they're getting → if/then structure → button text that's a benefit, not "Buy Now."
4. **FAQ** — 5–7 questions that handle remaining objections. First question restates the offer; last question restates the guarantee. Answers stay 2–4 sentences.

**Button text that works:** "Yes, I Want [Benefit]" / "Get Instant Access" / "Save My Spot" / "Enroll Now — $[price]"
**Button text that fails:** "Buy Now" / "Submit" / "Purchase"

For price justification patterns, 4 guarantee styles with examples, CTA formulas, and standard FAQ templates, see [references/close.md](references/close.md).

---

## step 5: write the LEAD

The lead is the 150–200 words right after the headline. It's a teaser trailer for the sales page. Its job is to earn the next scroll — not to explain everything.

**The 8-step lead formula:**

1. **Call them out** — identify exactly who this is for. Make them feel seen.
2. **Make them a promise** — the big outcome. Bold but believable.
3. **Within a timeframe** — specific, not "soon."
4. **Brief mechanism** — hint at the unique method. Don't explain it yet.
5. **Handle objections** — address the biggest doubt before they think it.
6. **Easy and/or quick** — remove friction. Make it feel achievable.
7. **Proof** — numbers, results, social proof.
8. **Transition out** — bridge into the story ("But first, let me tell you how I figured this out...").

**Rules:**
- Tease, don't tell. Details go in the offer section.
- 150–200 words. Longer = doing too much.
- Match the energy of the headline.

For the full formula with 4 worked-example leads across industries, see [references/leads.md](references/leads.md).

---

## step 6: write the HEADLINE

Write this LAST. It's the most important part of the page. Spend the most time here. Its only job is to earn the next line.

**Three components:**

1. **Prehead** — sits above the main headline. Calls out the audience, the problem, a credibility marker, urgency, or sets up the main headline ("Finally...").
2. **Main headline** — the big promise.
3. **Deck copy** — sits below the headline. Explains the mechanism and provides proof.

**The main headline formula:**

```
How to go from [where they are now] to [where they want to be] in [timeframe] — without [objection] / even if [limiting belief]
```

**Four pieces:**

- Where they are now (paint the painful current state — specific, in their words)
- Where they want to be (desired outcome — concrete)
- How fast (timeframe — specific and believable)
- Handle the objection — `without [external obstacle]` or `even if [internal limiting belief]`

**Deck copy formula:**

```
Using [mechanism/method name] that [proof of results]
```

**Alternative main headline formulas** (use when the "How to go from X to Y" shape fights the offer): Promise headline, Problem headline, Story headline, Intrigue headline. See [references/headlines.md](references/headlines.md) for all four alternatives plus 20+ prehead options and full assembled headline+deck examples across industries.

---

## step 7: assemble the page

Put it all in reading order:

```
1. HEADLINE (prehead → main headline → deck copy)
2. LEAD (150–200 word teaser)
3. STORY (introduce → problem → solution)
4. OFFER (introduce → big promise → specifics → testimonials)
5. CLOSE (price → guarantee → CTA → FAQ → final CTA)
```

Add CTA buttons throughout — not just at the end. Minimum: one after the offer section, one after the FAQ.

For a fully assembled worked example, see [references/full-page-example.md](references/full-page-example.md).

---

## step 8: anti-slop pass (mandatory)

Before showing the page to the user, run the draft through the `anti-slop` skill (or `humanizar-texto`).

**Catches:** rhetorical questions ("The best part?"), binary opposites ("It's not X, it's Y"), robot phrases (game-changer, unlock, leverage, delve, robust, seamless), em-dash overuse, throat-clearing hedges, same-structure paragraphs, zero contractions.

**Rewrite every hit.** A sales page that feels AI-written loses trust before the offer lands.

---

## step 9: pre-flight checklist

Before delivering, verify every box:

- [ ] Headline makes a clear promise
- [ ] Deck copy includes proof
- [ ] Lead is 150–200 words (not longer)
- [ ] Story includes "tried and failed" section
- [ ] Story ends with transition to offer
- [ ] Offer is broken into components with bullets
- [ ] Each component has 3–9 specific benefits
- [ ] 3–5 testimonials (not a wall of 20)
- [ ] Price is anchored against higher value
- [ ] Guarantee has a name
- [ ] Guarantee restates benefits
- [ ] CTA button is a benefit, not "Buy Now"
- [ ] FAQ first question sums up the offer
- [ ] FAQ last question restates the guarantee
- [ ] Multiple CTA buttons throughout (not just at the end)
- [ ] Anti-slop pass ran, zero hits

If 2+ fail: return to the failing step before delivering.

---

## output format

```
## Sales Page: [Product Name]

### HEADLINE
[Prehead]
[Main Headline]
[Deck Copy]

### LEAD
[150–200 word teaser]

### STORY
[Introduction → Problem → Solution]

### OFFER
[Introduction → Big Promise → Components → Testimonials]

### CLOSE
[Price Justification → Guarantee → CTA → FAQ → Final CTA]

**Pre-flight check:** ✓ All items pass (or: list items flagged for user input)
```

If the business context is missing numbers, testimonials, or specifics, mark them `[PLACEHOLDER — needs real number]` so the user can see exactly what to fill in. Never fabricate specifics.

---

## cheat sheet formulas

**Main headline:**
```
How to go from [where they are] to [where they want to be] in [timeframe] — without [objection] / even if [limiting belief]
```

**Deck copy:**
```
Using [mechanism] that [proof]
```

**Lead (8 steps):**
Call out → Promise → Timeframe → Mechanism → Handle objection → Easy/quick → Proof → Transition

**Story (3 parts):**
Introduce yourself → Problem (tried and failed) → Found the solution → Others wanted it → Became the product

**Offer (4 parts):**
Introduce it → Big promise → Specifics with bullets → Testimonials

**Close (4 parts):**
Price (anchor → state → explain → trivialize) → Guarantee → CTA → FAQ

---

## gotchas

The failure modes that show up again and again:

1. **Writing top to bottom.** The process is backwards for a reason. Writing the headline first produces a 2-hour staring contest with a blank page. Writing the story first finds the voice, then every other section borrows it.

2. **Vague "tried and failed" sections.** "I tried lots of things but nothing worked" is not a story. Three specific things, each with a specific reason it failed, or cut the section.

3. **Fabricated testimonials or numbers.** If the business context doesn't supply them, use `[PLACEHOLDER]` markers. AI-invented "4.7% conversion" testimonials get caught and destroy the page's trust.

4. **Copy that sounds like the template.** The 5-part framework is scaffolding. If the finished page reads like a template with blanks filled in, the voice is missing — go back to Step 2 and pull voice samples from context more aggressively.

5. **Lead that explains everything.** The lead is a teaser. If it's over 200 words, it's trying to be the offer section. Cut it back.

6. **"Buy Now" buttons.** Generic CTAs leak conversion. The button text is a benefit statement.

7. **One CTA at the bottom.** Readers don't scroll. Minimum: one CTA after the offer, one after the FAQ, usually one in the close as well.

8. **Skipping the anti-slop pass.** Everything else can be perfect and the page still fails if it reads AI-written. The pass is non-negotiable.

9. **Asking more than 2 context questions upfront.** If the user has to answer 5 questions before seeing a draft, they bail. Combine. Use what's in CLAUDE.md and `Context/`. Get to draft fast, then iterate.

10. **Writing for "everyone."** A page that targets "entrepreneurs" converts worse than one that targets "SaaS founders doing $10k-$50k MRR who haven't raised a round." Specificity wins.

---

## the test

A good sales page from this skill:

1. **Opens with a throat-grab** — the headline earns the next line. If the reader doesn't feel "this is about me" in 3 seconds, it failed.
2. **Teases before it tells** — the lead creates desire without explaining everything. Over 200 words = doing too much.
3. **Builds credibility through story** — "tried and failed" proves lived experience. No failures = guru pitch.
4. **Breaks the offer into pieces** — named components with specific benefits. One big paragraph = nobody reads it.
5. **Closes with confidence** — price justified, guarantee named, CTA a benefit.
6. **Sounds like a conversation** — read it out loud. Brochure = rewrite.
7. **Has multiple CTAs** — at least 3 buttons throughout. Not just the bottom.
8. **Passed anti-slop** — zero flagged patterns.

If a competitor could swap their name in and the page would still make sense — it failed. Grounded copy is specific to this business, this ICP, this voice.

---

## how this connects to other skills

**Runs before this skill:**
- `entrevista-negocio` — generates business / ICP / voice context (into CLAUDE.md or `Context/*.md`) that Step A pulls from.
- `pesquisa-keywords` — feeds search demand and audience-language data.
- `arquitetar-oferta` — produces the Offer Map that Step 3 turns into copy.

**Runs after this skill:**
- `humanizar-texto` — mandatory pass, Step 8.
- `polir-texto` — optional second polish on long pages.
- `sequencia-email` — builds the email sequence that drives traffic to this page.

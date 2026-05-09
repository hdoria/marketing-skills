---
name: sequencia-email
description: "Build email sequences that convert subscribers into customers. Use when you have a lead magnet and need a welcome sequence, nurture sequence, sales sequence, launch campaign, win-back series, or buyer onboarding. Triggers on: write welcome emails, email sequence for, nurture sequence, convert my list, onboarding emails, launch sequence, drip campaign, email funnel. Reads the user's business, ICP, and voice from CLAUDE.md or the project's `Context/` folder before writing. Runs every email through the anti-slop skill before shipping. Outputs complete sequences with subject lines, preview text, timing, and full copy."
---

# Email Sequence Builder

Subscribers are cheap. Customers are expensive. The gap between "signed up" and "paid" is a graveyard of abandoned inboxes and ignored autoresponders. Most people either blast sales emails too early or send so much free content they never ask for the sale. This skill builds the path from opt-in to purchase — step by step, email by email — and refuses to ship a draft that hasn't been grounded in the reader's actual voice and pain.

---

## the core job

Produce a **complete, ready-to-load email sequence** that moves someone from new subscriber to paying customer without torching the relationship along the way.

Every sequence ships with subject lines, preview text, full written copy, send timing, and one CTA per email.

**Output:** A single markdown deliverable in the format defined under `## output format`, ready to paste into the user's email tool (ConvertKit, Beehiiv, Kit, ActiveCampaign, etc.).

---

## before starting: gather context

**STOP. Do not write a single email until context is in hand. Cap your brief-confirmation at 2 questions max.**

### Step A: Gather context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for:
   - **Business** — what the user sells, pricing. Grounds the paid offer and bridge.
   - **ICP** — who the subscriber is, their pain, exact phrases. Subject lines must sound written for THIS person.
   - **Voice** — tone, do/don't rules, sample sentences. Emails must read like the user wrote them.
2. **If missing, check the project folder** for `Context/business.md`, `Context/icp.md`, `Context/voice.md`. Read whichever exist.

### Step B: Confirm the brief (≤2 questions)

Skip everything CLAUDE.md and `Context/` files already cover. Then ask AT MOST 2 questions from this priority list:

| Priority | Input | Question | Why it matters |
|----------|-------|----------|----------------|
| 1 | **Freebie + bridge** | "What did they sign up for, and how does it connect to what you're selling?" (combine into one question) | Shapes email 1 and makes the pitch feel natural |
| 2 | **Paid offer + price** | "What are you selling them and at what price?" (combine) — skip if business context covers it | Determines pitch intensity and trust-building length |
| 3 | **Blockers** | "Top 1-2 reasons they might NOT buy?" — skip if ICP context covers it | Shapes objection-handling emails |

Combine related fields into one question so you never cross 2 total. Pull from context before you ask.

---

## the process

Five steps. Each one gates the next. Don't skip ahead.

```
GROUND → PICK → DRAFT → CHECK → SHIP
   │        │       │       │       │
context  choose   write   anti-   deliver
 + ICP   sequence  every  slop +  in output
loaded    type     email   quality format
                            gate
```

| Step | What happens | Output of this step |
|------|--------------|---------------------|
| 1. Ground | Scan CLAUDE.md + `Context/` files + confirm brief | Brief locked, voice/ICP loaded |
| 2. Pick | Choose the right sequence type | One playbook selected |
| 3. Draft | Write subject + preview + body for each email | Full sequence draft |
| 4. Check | Anti-slop pass + quality gate | Cleaned sequence |
| 5. Ship | Format output, hand to user | Ready-to-load deliverable |

---

## ground: pull context

Already covered in `## before starting: gather context` above. Don't move to **Pick** until both Step A (context) and Step B (brief, ≤2 questions) are complete.

**Framework:** context first, brief second, never reverse. CLAUDE.md + `Context/` files constrain what you need to ask. Without them, Step B becomes a 30-question interrogation.

**Anti-pattern:** Asking the user for their voice/ICP when it's already in CLAUDE.md or `Context/voice.md` / `Context/icp.md`. They wrote it once so they wouldn't have to write it again.

---

## pick: select sequence type

Match the user's situation to one of six playbooks. If they ask for something that fits two, ask which job is most urgent right now.

**Decision matrix:**

| User says... | Sequence type |
|--------------|---------------|
| "I have a lead magnet, need a welcome sequence" | **Welcome Path** |
| "My list is warm, I want to sell my course/offer" | **Sales Run** |
| "I'm launching a cohort/product on [date]" | **Campaign Blitz** |
| "Half my list stopped opening" | **Win-Back Series** |
| "Welcome path didn't convert, want to nurture before pitching again" | **Trust Builder** |
| "Someone just bought, what do I send?" | **Buyer Onboarding** |

**Sequence catalog (one-line each):**

- **Welcome Path** (5-7 emails) — Delivers the freebie, builds rapport, plants offer seeds
- **Trust Builder** (4-6 emails) — Pure value emails that deepen the relationship
- **Sales Run** (4-7 emails) — Pitches the paid product directly
- **Campaign Blitz** (6-10 emails) — Time-boxed promotion with a hard deadline
- **Win-Back Series** (3-4 emails) — Wakes up subscribers who've gone cold
- **Buyer Onboarding** (4-6 emails) — Reduces refunds and sets up upsells

For the full progression, framework table, anti-pattern, and timing of each playbook, see [references/sequence-playbooks.md](references/sequence-playbooks.md).

For the welcome path specifically — email-by-email structures, subject formulas, and section-by-section breakdowns — see [references/welcome-path.md](references/welcome-path.md).

**Anti-pattern:** Picking "all of them" because the user wants a complete funnel. Build one sequence at a time, ship it, then layer the next. Trying to draft welcome + nurture + sales + win-back in one pass produces 30 mediocre emails instead of 7 great ones.

---

## draft: write every email

For each email in the chosen sequence, write in this order:

1. **Subject line** — pick a subject formula (curiosity / benefit / story / question / urgency / pattern interrupt) — see [references/email-craft.md](references/email-craft.md)
2. **Preview text** — 40-90 chars that extend the subject hook, never "view in browser"
3. **Body** — short paragraphs (1-3 sentences), one CTA, real specifics not vague claims
4. **P.S. line** — only if it adds value (deadline, second hook, personal note, CTA repeat)

### Writing rules for every email

**P.S. lines are high-value territory.** Nearly half of readers scan the P.S. before the body. Put your CTA, a second hook, a personal note, or a deadline reminder there.

**One action per email.** Multiple CTAs cancel each other out. Pick the one thing you want them to do.

**Short paragraphs only.** 1-3 sentences. People scan email. They don't read it top to bottom.

**Preview text is your second headline.** First 40-90 characters show in the inbox. Don't waste them on "View in browser."

**Curiosity loops keep them coming back.** Drop a teaser for tomorrow's email: "I'll show you what happened next" or "Tomorrow: the part nobody talks about."

**Specifics beat generalities every time.** Not "made money" but "$47,329 in one launch." Not "recently" but "last Thursday." Numbers and dates make claims believable.

For subject line formulas, open-rate tactics, P.S. strategies, and detailed copy principles, see [references/email-craft.md](references/email-craft.md).

### Sequence wiring patterns

Pick one based on the user's tooling:

- **Linear** — Email 1 → 2 → 3 → 4 → Pitch. Straightforward. No branches. Works for simple sequences.
- **Behavioral split** — Email 1 → 2 → Did they click? Yes → pitch track. No → more value track. Smarter but needs automation tools.
- **Full lifecycle** — Welcome path (5 emails) → 7-day pause → Sales run (5 emails) → No purchase → Trust builder (ongoing). The complete subscriber journey.

### Timing guidelines

**How often to email by sequence type:**

| Sequence | Frequency | Why |
|----------|-----------|-----|
| Welcome path | Days 0, 2, 4, 6, 8, 10, 12 | Value-heavy upfront while attention is high |
| Trust builder | 1-2x per week | Steady rhythm without fatigue |
| Sales run | Every 2 days | Enough contact without being annoying |
| Campaign blitz | Daily or every other day | Deadline justifies the intensity |
| Win-back | Days 0, 3, 7, 10 | Space to respond between each |

**When to send:**
- **B2B:** Tuesday through Thursday, 9-11am in recipient's timezone
- **B2C:** Tuesday through Thursday, 7-9am or 7-9pm
- **Skip:** Monday morning (inbox chaos), Friday afternoon (mentally gone)

**How much trust before you sell:**

| Price range | Value emails first |
|-------------|-------------------|
| Under $100 | 3-5 |
| $100-500 | 5-7 |
| Over $500 | 7-10 (or a sales call) |

Trust required goes up with price. Don't rush the pitch.

**Anti-pattern:** Drafting all subject lines first, then all bodies, then all P.S. lines. Each email is a unit. Write it whole, in order, so the bridge to the next email lives in the same head as the body. Batching by section produces sequences that feel like 7 disconnected emails.

---

## check: anti-slop + quality gate

This is the gate before Ship. Two passes, in this order.

### anti-slop: mandatory pass

Before showing ANY email to the user, run it through the `anti-slop` skill.

**How:** Invoke `anti-slop` with the full draft (all emails in the sequence) as input. It catches AI patterns — binary opposites, em-dash overuse, robot phrases like "game-changer" / "unlock" / "leverage", throat-clearing hedges, rhetorical questions, forced threes — and returns a cleaned version.

**If `anti-slop` is not available**, run the checks manually. Scan every email for:
- Rhetorical questions ("The best part?", "Sound familiar?", "Want to know...")
- Binary opposites ("It's not X, it's Y")
- Robot phrases (game-changer, supercharge, leverage, unlock, delve, robust, cutting-edge, seamless)
- Throat-clearing ("It's worth noting...", "In today's fast-paced world...", "Let's dive in")
- Em dashes as a crutch (1-2 max per email)
- Same-structure subject lines across the sequence
- Zero contractions

Rewrite anything flagged. Subject lines especially — slop there kills the open rate before the body even matters.

**Non-negotiable:** No sequence ships without this pass.

### quality gate

Run the 7-point test in `## the test` below. If any check fails, return to **Draft** and fix that email before proceeding to Ship.

---

## output format

```
# [Sequence Name] — [Product/Offer]

## Goal
[One sentence: what this sequence accomplishes]

## Schedule
[Send timing overview]

## Emails

### Email 1: [Label]
**Send:** [Timing]
**Subject:** [Subject line]
**Preview:** [First 60 characters of preview text]
**Goal:** [What this specific email does]

[FULL EMAIL COPY]

**P.S.** [If applicable]

---

### Email 2: [Label]
**Send:** [Timing]
**Subject:** [Subject line]
**Preview:** [Preview text]
**Goal:** [Purpose]

[FULL EMAIL COPY]

---

[Continue for all emails in sequence]
```

---

## example: welcome path for a $197 content course

A short inline example so you can see the shape. For the complete 7-email worked example with every email written out in full, see [references/welcome-example.md](references/welcome-example.md).

**Setup:**
- Freebie: Free content-planning template
- Paid offer: Full content system course ($197)
- Bridge: Template is step 1. Course covers the other 6 steps.
- Audience: Small business owners making content but not seeing results
- Blockers: "I don't have time for a course," "I can figure it out myself," "Is this just theory?"

**Sequence shape:** Welcome Path, 7 emails, days 0–12.

### Email 1: Hand Off
**Send:** Immediately
**Subject:** Your content template is here
**Preview:** Start with step 3 — that's where most people get stuck
**Goal:** Deliver the freebie, give one quick action, ask for a reply

> Hey,
>
> Your content planning template is attached. [LINK]
>
> Here's how to use it right now:
>
> 1. Open the template
> 2. Skip to step 3 (content pillars) — that's where most people get unstuck
> 3. Fill in your top 3 topics. Takes 5 minutes.
>
> Over the next couple weeks I'll send you a few emails on how to get the most out of this template — and what the rest of the system looks like.
>
> One question: what type of content are you making right now? Hit reply and tell me. I read every response.
>
> — Ole

### Email 2: Bond
**Send:** Day 2
**Subject:** How I wasted 6 months posting content
**Preview:** 47 posts. Zero leads. Here's what I missed.
**Goal:** Build rapport with a specific origin story

> Last year I posted content every single day for almost two months straight.
>
> 47 posts. Not a single lead. Not one DM. Nothing.
>
> [continues — see references/welcome-example.md for full body]

### Emails 3-7

Teach (Day 4) → Teach Again (Day 6) → Gap (Day 8) → Gentle Ask (Day 10) → Direct Ask (Day 12).

Full text of every email lives in [references/welcome-example.md](references/welcome-example.md), including the $197 pitch in email 6 with a module-by-module table and the disqualification list ("Skip this if you already have a working content system / want someone to do content for you / aren't making content yet").

---

## how this connects to other skills

**Feeds into this skill:**
- **Brand Voice** — Keeps email tone consistent with your brand
- **Positioning Angles** — The winning angle shapes the pitch emails
- **Lead Magnet** — The freebie determines email 1 and the bridge
- **Direct Response Copy / Copywriting Workshop** — Copy principles apply to every individual email

**This skill feeds into:**
- **Content Atomizer / Repurpose Workshop** — Best-performing emails become social content
- **Newsletter Workshop** — Sequence insights inform newsletter strategy and cadence

**The typical flow:**
1. Lead Magnet skill creates the opt-in offer
2. This skill builds the welcome → sales path
3. Direct Response Copy principles sharpen each email
4. Best-performing emails get repurposed via Content Atomizer
5. Subscriber becomes customer

---

## the test

Run all 7 checks before delivering. If any one fails, the sequence isn't ready.

1. **Earns before it asks** — Are there at least 3-5 value emails before any pitch? (Sales Run is the exception; it's a sales sequence by definition.)
2. **Every email has a single job** — Can you describe each email's purpose in one sentence? If not, that email is doing two things and needs to be split or cut.
3. **One CTA per email** — Count the links and asks in each email. More than one = rewrite. (Email 1 of Welcome Path can have download + reply. That's the only exception.)
4. **Reads like a human wrote it** — Did anti-slop pass without flagging anything? Read each email aloud. If a sentence sounds like writing instead of talking, rewrite it.
5. **Specific, not generic** — Every claim has a number, date, name, or concrete detail. No "made money," no "recently," no "many customers."
6. **Subject lines vary** — No two subject lines in the sequence use the same structure. Mix curiosity, benefit, story, question, pattern interrupt.
7. **Pull toward the next email** — Emails 1 through (n-1) end with a curiosity hook or forward tease that makes them want to open the next one.

**Failure condition:** If the sequence reads like "free stuff, free stuff, free stuff, BUY NOW BUY NOW" — it failed. Return to Draft. The pitch should feel like the natural next step, not a bait-and-switch. Likewise, if anti-slop flagged anything and it wasn't rewritten, do not ship.

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` sitting next to this SKILL.md.

### At the start of every session using this skill
1. **Read `feedback.log`** in this skill's folder before writing anything. Apply every rule in it to this session's output.
2. If `feedback.log` doesn't exist yet, create it with a header: `# Email Sequence Workshop — Learned Rules`

### During every session — triggers that require a log write

When the user says any of the following, **immediately append a rule to `feedback.log` before continuing**:

- "Don't do X anymore" / "Stop doing X" / "Never do X"
- "Always do Y" / "From now on, do Y" / "Whenever you write a subject line, do Y"
- "I hate when you..." / "I don't like..."
- "That's perfect, keep doing that" (log positive patterns — don't drift away from what works)
- "Remember that..." / "Keep in mind..."
- Silent rewrites where the user fixes your draft — infer the rule from the diff

### Format for each logged rule

```
## YYYY-MM-DD — [short title]

**Rule:** [one-sentence, imperative voice]
**Why:** [reason the user gave, or what they were reacting to]
**How to apply:** [when this kicks in — which sequence type, which email slot, which trigger]
```

### What to log vs skip

**Log:**
- Subject line rules ("never use emojis in subject lines")
- Structural rules ("always skip Trust Builder for under-$100 offers")
- Voice calibrations ("my audience hates the word 'friend' — cut it")
- Timing preferences ("space welcome path over 14 days not 12")

**Skip:**
- Task-specific fixes ("change the price to $149 in email 3") — not a rule
- Preferences already in CLAUDE.md or `Context/voice.md` — those belong in the context source, not here

### Cleanup

Every ~10 entries, consolidate: merge duplicates, delete reversed rules, keep log under 100 lines. Stale contradictory rules cause drift.

**This is how the skill gets better.** Every rejection is a rule. Every "yes that's right" is a pattern to keep. Read the log. Apply the rules. Append new ones. Forever.

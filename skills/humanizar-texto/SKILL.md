---
name: humanizar-texto
description: "Strip AI writing patterns from any content so it reads like a human wrote it. Use when editing AI-generated drafts, cleaning up copy that sounds robotic, or checking content before publishing. Triggers on: clean this up, de-slop this, make this sound human, remove AI patterns, does this sound like AI, edit for slop, humanize this, check this for AI patterns. Runs 5 editing passes (structure, phrases, verbs, formatting, content) and outputs cleaned version with a changelog of what was fixed."
---

# Anti-Slop

People can spot AI writing in about two seconds. Not because they're experts — because the patterns are that predictable. Same sentence structures, same filler phrases, same fake enthusiasm. Every AI tool produces the same voice.

This skill runs content through 5 editing passes that catch every common AI pattern and replace them with something a human would actually write. Not just "don't do X" — specific fixes for each problem.

---

## the core job

Take any AI-generated or AI-assisted content and **strip the patterns that make it sound robotic.**

**Output:** Cleaned version of the content + a changelog of what was fixed, grouped by pass.

---

## before starting: gather context

**STOP. Do not edit until you have the content and know the context. Ask for any missing field before proceeding.**

1. **The content** — What are you cleaning? (paste it or point to a file)
2. **The tone** — What voice are you going for? (casual, professional, technical, conversational)
3. **The format** — What type of content is this? (email, social post, landing page, article, newsletter)

Tone matters because some fixes depend on context. An em dash in a casual LinkedIn post is different from one in a technical doc. A rhetorical question in a sales page may stay. In a technical explainer it goes.

---

## the process

Run content through these 5 passes in order. Each pass catches a different category of AI pattern.

```
STRUCTURE → PHRASES → VERBS → FORMATTING → CONTENT
```

Don't try to fix everything at once. One pass at a time.

**Full detail for every pass — scan patterns, before/after examples, and specific fixes — lives in [references/passes.md](references/passes.md). Read it before editing.**

### Pass 1: Structure
Catches repeated sentence structures: binary opposites ("it's not X, it's Y"), forced threes, infomercial questions ("Want to know the secret?"), "No X. No Y. Just Z." openers.

### Pass 2: Phrases
Catches filler phrases: robot buzzwords (game-changer, supercharge, leverage), throat-clearing hedges, thesaurus syndrome (utilize → use), melodramatic realizations, "Enter: [Thing]," "If you're serious about," "To your success," "Not because of X. But because of Y."

### Pass 3: Verbs
Catches verb problems: -ing overuse, passive voice, corporate zombie verbs (facilitate, empower, enable, drive engagement).

### Pass 4: Formatting
Catches formatting tells: arrow spam, emoji confetti, em dash addiction, over-bolding.

### Pass 5: Content
Catches content-level AI patterns: generic claims with no specifics, fake case studies (Sarah Chen, Marcus Johnson), symbolism overdose ("this represents..."), authenticity theater (using "real" 5 times), universal transformation claims ("this changed everything").

---

## output format

Deliver two things:

### 1. The cleaned content
The full rewritten version, ready to use.

### 2. The changelog

```
## Changes Made

**Structure (X fixes)**
- [What was changed and why]

**Phrases (X fixes)**
- [What was changed and why]

**Verbs (X fixes)**
- [What was changed and why]

**Formatting (X fixes)**
- [What was changed and why]

**Content (X fixes)**
- [What was changed and why]

**Total: X changes across 5 passes**
```

---

## example: cleaning a sloppy AI LinkedIn post

### Original (AI-generated)

> **Want to know the secret to 10x-ing your productivity? 🚀**
>
> In today's fast-paced world, it's not about working harder — it's about working smarter. I recently discovered a game-changing framework that completely revolutionized how I approach my day.
>
> Here's the kicker: it only takes 15 minutes.
>
> The framework focuses on three key principles:
> → Prioritizing high-impact tasks
> → Eliminating unnecessary meetings
> → Leveraging AI tools for automation
>
> Implementing this system has been a total game-changer. It's worth noting that the results speak for themselves — my team's productivity increased significantly, and we've been able to facilitate better collaboration across departments.
>
> If you're serious about leveling up your productivity, this is the deep dive you need.
>
> Ready to supercharge your workflow? Drop a 🔥 in the comments!

### After 5 passes

> **15 minutes changed how my team works**
>
> Last month I tracked where my time went for a full week. 11 hours in meetings. 6 hours on email. About 3 hours on work that actually moved projects forward.
>
> So I tried something: I blocked the first 90 minutes of every day for focused work. No Slack, no meetings, no email. Just the one task that matters most.
>
> After 4 weeks:
> - Meeting time dropped from 11 hours to 6 (I declined anything without an agenda)
> - The team started doing the same thing without me asking
> - We shipped two features that had been stuck for months
>
> I also started using AI to draft routine communications. Status updates, meeting summaries, first-pass project plans. Saves me about 45 minutes a day.
>
> The setup takes 15 minutes: block your calendar, pick your one priority, turn off notifications. That's it.

### Changelog

**Structure (2 fixes)**
- Removed binary opposite ("not about working harder, it's about working smarter")
- Removed forced three-point list, replaced with specific results

**Phrases (6 fixes)**
- Removed "Want to know the secret" (infomercial question)
- Removed "game-changing" and "game-changer" (2x)
- Removed "revolutionized", "it's worth noting", "here's the kicker"
- Removed "deep dive", "supercharge", "leveling up"

**Verbs (2 fixes)**
- "Implementing this system has been" → specific past tense actions
- "facilitate better collaboration" → "team started doing the same thing"

**Formatting (3 fixes)**
- Removed emoji from headline and CTA
- Replaced arrow bullets with standard dashes
- Removed over-bolding

**Content (2 fixes)**
- "Productivity increased significantly" → specific numbers (11hrs to 6hrs, 2 features shipped)
- Generic framework → specific actions with timeline

**Total: 15 changes across 5 passes**

---

## the banned list

Quick reference — if any of these appear in the cleaned content, a pass failed.

Game-changer, revolutionize, supercharge, level up, unlock your potential, the secret is, here's the thing, the catch?, want to know?, it's worth noting, at the end of the day, in today's fast-paced world, to your success, if you're serious about, no fluff/no X/just Y, enter: [thing], this changed everything, [thing] on steroids, actionable insights, deep dive, unpack, circle back, move the needle, low-hanging fruit, synergy, leverage (as verb), comprehensive solution, facilitate, empower, enable, drive engagement.

---

## how this connects to other skills

**Anti-slop is the final pass for any writing skill.** Run it after:
- `polir-texto` — invoked as the final pass (Pass 10) of the 9-pass editing workflow
- `post-longo-x` — tight formats show slop faster
- `afiar-ideia` — clean the sharpened angle before turning it into a draft
- Any first-draft writing skill — humanizar-texto is the universal final filter

**The workflow:**
1. Write content with any skill
2. Run humanizar-texto as a final editing pass
3. Review the changelog to learn which patterns repeat in your output

---

## the test

Clean content passes all 6 checks:

1. **The read-aloud test** — Read every sentence out loud. If it sounds like "writing" instead of talking, rewrite it.
2. **The anyone test** — Could this sentence appear in anyone's content? If yes, it's generic. Make it specific.
3. **The -ing count** — More than 2 -ing forms per paragraph is a red flag. Fix them.
4. **The banned phrase test** — Zero phrases from the banned list. No exceptions.
5. **The specificity test** — Every claim has a number, name, date, or real example behind it.
6. **The rhythm test** — Sentence lengths vary. Not every sentence is the same beat. Short ones. Then a longer one that takes its time. Then short again.

If someone reads the content and thinks "AI wrote this" — it failed.

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` sitting next to this SKILL.md.

### At the start of every session using this skill
1. **Read `feedback.log`** in this skill's folder before editing anything. Apply every rule in it to this session's output.
2. If `feedback.log` doesn't exist yet, create it with a header: `# Anti-Slop Workshop — Learned Rules`

### During every session — triggers that require a log write

When the user says any of the following, **immediately append a rule to `feedback.log` before continuing**:

- "Don't flag X anymore" / "Stop removing X" / "X is fine, leave it"
- "Always remove X" / "From now on, catch X" / "Add X to the banned list"
- "You missed X" / "Also catch X"
- "That's perfect, keep doing that" (log positive patterns — don't drift)
- Silent rewrites where the user restores something you removed — infer the rule: "leave [pattern] alone"

### Format for each logged rule

```
## YYYY-MM-DD — [short title]

**Rule:** [imperative sentence — "always remove X" or "never flag Y"]
**Why:** [reason the user gave, or the context]
**How to apply:** [which pass this belongs to — Structure, Phrases, Verbs, Formatting, Content — and when it kicks in]
```

### What to log vs skip

**Log:**
- New banned phrases the user wants caught ("always flag 'mission-critical'")
- Exceptions to existing rules ("em dashes are fine in my LinkedIn posts")
- Voice calibrations ("my audience uses 'leverage' unironically — stop flagging it for them")
- Format-specific rules ("in newsletters, keep the P.S. casual hedge")

**Skip:**
- One-off edits to a single piece ("change this word here") — not a rule
- Things already covered in `references/passes.md` — those aren't learning, just reminders

### Cleanup

Every ~10 entries, consolidate: merge duplicates, delete reversed rules, keep log under 100 lines. Stale rules that contradict the latest ones cause drift.

**This is how the skill gets better.** Every rejection is a rule. Every "yes that's right" is a pattern to keep. Read the log. Apply the rules. Append new ones. Forever.

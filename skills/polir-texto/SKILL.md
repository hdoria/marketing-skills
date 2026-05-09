---
name: polir-texto
description: "Polish any draft using 9 structured passes that cut fluff, sharpen details, and make content sound human. Works on newsletters, tweets, LinkedIn posts, emails, landing pages, or any written content. Triggers on: edit this, tighten this up, make this better, review my draft, polish this, clean up my writing, run editing passes. Processes content through 9 sequential filters that eliminate weak language, add punch, and ensure a conversational tone — then runs a final anti-slop sweep before delivery."
---

# Editing Workshop

Most editing advice is vibes. This isn't. Nine passes, in this order, every time. Skip a pass and the draft keeps the flaw that pass was built to catch.

The job is to take a rough draft — yours, an AI's, a guest writer's — and turn it into something the user would actually publish under their name.

**IMPORTANT: After the 9 passes, run the anti-slop final gate (Pass 10) before showing anything to the user. Editing handles voice, hedging, and fingerprint. Anti-slop catches the AI patterns the 9 passes don't target. Both are mandatory.**

---

## the core job

Take a draft and run it through 9 sequential passes (plus a final anti-slop gate) to produce a publish-ready version that:
- Reads like the user wrote it
- Earns every sentence
- Carries one clear mission
- Sounds like talking, not "writing"

**Output:** Polished draft + pass-by-pass change notes + biggest win + remaining gap.

---

## before starting: gather context

**STOP. Do not start editing until voice is in hand AND the draft is in front of you. Cap inputs at 2 questions max.**

### Step A: Gather voice context (fast)

Editing only needs one thing from context: **voice**. (ICP is nice-to-have for Pass 7. Business/strategy are out of scope.)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for the user's do/don't rules, tone, sample sentences, banned phrases. That's usually enough.
2. **If missing, check the project folder** for `Context/voice.md` (and optionally `Context/icp.md` for Pass 7). Read whichever exists.
3. **If voice is still missing:** tell the user "I don't have your voice yet. Paste 3-5 sentences in your voice inline — or add them to your CLAUDE.md — otherwise I'll edit for clarity and structure only, not voice match."

### Step B: Confirm the inputs (≤2 questions, combined)

When you need inputs, merge them into at most 2 questions. Priorities, in order:

1. **The draft** — paste it. Full text, not a summary. (Non-negotiable.)
2. **One combined question:** format (newsletter, tweet, LinkedIn post, email, landing page, blog post, ad copy) + aggressiveness (light polish / standard / heavy). Ask both in one message.

Only ask the "protect any specific line?" question if the user hints at it; don't volunteer a third question.

Don't proceed until the draft is in front of you and aggressiveness is set.

---

## the process

```
ZOOM IN → HEADLINE SCAN → 3-IDEA CAP → CONFIDENCE → BAR TEST →
MISSION → AUDIENCE → FINGERPRINT → FINAL CUT → ANTI-SLOP GATE
```

Run the passes in order. Each one targets a specific failure mode. Don't skip ahead — Pass 9 (cut a third) only works after Passes 1-8 have done their work, because cutting before sharpening removes the wrong words.

---

## pass 1: zoom in

Generic writing is invisible. Concrete detail is magnetic.

For every story, anecdote, or example in the draft, check three things:

| Question | Weak Version | Strong Version |
|----------|-------------|----------------|
| Is there an exact moment? | "A while back" | "Last Thursday at 7am, standing in line at the post office" |
| Is there a physical sensation? | "I felt nervous" | "My stomach dropped" |
| Are there real names? | "A popular tool" | "Notion, specifically the database view" |

**The test:** Could someone picture this as a scene in a movie? If it reads like a summary instead of a moment, rewrite it.

**Anti-pattern:** Don't invent details. If the draft is too vague to zoom in on, ask the user for the specifics — don't fabricate a Thursday at 7am that didn't happen.

---

## pass 2: headline scan

Cover up everything except your headlines, subheads, and opening sentences of each section.

Does the piece still make sense? Could a skimmer get 80% of the value from just those lines?

If the answer is no, the headlines aren't pulling their weight. Rewrite them until they carry the story on their own.

**Anti-pattern:** Headlines that are clever but empty ("The Truth About Email") fail this test. Headlines that state the actual point ("Your welcome email is asking for the sale too early") pass it.

---

## pass 3: the three-idea cap

Name the three most important ideas in this piece.

| Count | Verdict |
|-------|---------|
| Exactly 3 | You're good |
| More than 3 | You have zero. Trim until you're back to 3. |
| Fewer than 3 | The piece might be too thin. Add depth or combine with another idea. |

Everything in the draft either supports one of those three ideas or it's dead weight. Cut the dead weight.

**Anti-pattern:** Don't keep a paragraph "because it's interesting." If it doesn't support one of the three, it weakens the piece by competing for attention.

---

## pass 4: confidence sweep

Hunt down and remove every hedge:

| Kill These | Replace With |
|-----------|-------------|
| "I think..." | State it directly |
| "Maybe..." | Commit or cut |
| "Kind of..." | Drop the qualifier |
| "Sort of..." | Drop the qualifier |
| "It seems like..." | Say what it IS |
| "In my opinion..." | Just say it — your name's on it |
| "I believe..." | State the belief as fact |
| "Probably..." | Commit to yes or no |

You either mean it or you don't. Hedging tells the reader you're not sure, so why should they be?

**Anti-pattern:** Don't strip hedges that are doing real work (e.g., "I think Claude 4.7 is faster than 4.6, but I haven't benchmarked it" — the hedge is honesty, not weakness). Use judgment.

---

## pass 5: the bar test

Read the whole thing out loud. All of it.

Would you actually say this to a friend over drinks? If any sentence makes you cringe or stumble, it needs to go.

Three warning signs to watch for:
1. Words you would never use in conversation
2. Sentences so long you run out of breath reading them
3. Anything that sounds like corporate content from five years ago

If it sounds like "writing," it's wrong. Good writing sounds like talking.

**Anti-pattern:** Don't replace formal words with thesaurus alternatives. "Utilize" → "use," not "leverage." The fix is plainer, not fancier.

---

## pass 6: one-sentence mission

Answer this in a single sentence: what is this piece trying to do?

If you can't answer clearly, the piece doesn't know what it's about. Rewrite until you can say it in one line.

Now go paragraph by paragraph. Does each one serve that mission? Any paragraph that doesn't is a candidate for deletion.

**Anti-pattern:** Missions that are too broad ("teach people about marketing") fail this. Specific missions ("convince the reader that their welcome email needs a story before the offer") pass.

---

## pass 7: audience of one

Check who you're talking to. Are you addressing one person or a crowd?

| Crowd Language (kill it) | One-Person Language (use this) |
|-------------------------|-------------------------------|
| "Some of you" | "You" |
| "Many people" | "You" |
| "Entrepreneurs" | "You" |
| "Readers" | "You" |
| "For those who" | "If you" |

The reader should feel like you're in their inbox, not on a stage giving a keynote. Write to one human being.

**Anti-pattern:** Don't make it weirdly personal in formats where it doesn't fit (e.g., a landing page H1 that says "you, specifically, with your exact problem"). One-person tone, not surveillance creep.

---

## pass 8: the fingerprint test

Ask yourself: could anyone have written this, or could only I have written this?

If someone could swap in their name and it would still make sense, the piece is missing your fingerprint. Find the insight that comes from your specific experience, your specific screw-up, your specific weird angle on the topic.

If that fingerprint isn't in the draft, add it. If you can't find one, the piece might not be worth publishing.

**Anti-pattern:** Don't fabricate a fingerprint. If the draft is generic and the user has no specific story to add, flag it back to them — "this needs a moment from you, I can't invent one."

---

## pass 9: the final cut

After all eight passes above are done:
1. Check the word count
2. Cut one-third of the remaining words
3. Read it out loud one final time

If it's tighter and still lands, you're done with editing.

**Anti-pattern:** Don't cut a third just to hit the math. Cut the third that's least load-bearing. If the draft is already tight, cut 10-15% and flag it.

---

## anti-slop: mandatory pass (pass 10)

The 9 passes don't catch every AI tic. Anti-slop is a separate skill with its own banned-phrase list, sentence-shape checks, and AI-tell detection. Run it as the final gate.

**How to run:**
1. Take the output of Pass 9.
2. Invoke the `humanizar-texto` skill (or apply the rules from `~/.claude/anti-slop-writing.md` if running standalone).
3. Scan for: banned phrases ("game-changer," "here's the kicker," "it's not X, it's Y"), em dashes, fake-profundity patterns, throat-clearing, robot rhythm, fragment-only sentences with no subject.
4. Fix every hit. Do not negotiate.

**Why it's separate:** The 9 passes target voice, structure, and confidence. Anti-slop targets the residue of AI generation that can sneak through even after good editing. Both are needed. Skip this and the draft will read "edited but still AI."

**Pass criteria:** Zero hits on the anti-slop checklist. If 3+ hits remain after one cleanup pass, restart from Pass 5 (bar test) — the draft is more AI-shaped than you thought.

---

## output format

After running content through all 10 passes, deliver this:

```
## Polished Draft

[The fully edited content. Ready to publish.]

---

## Pass Notes

**Pass 1 (Zoom In):** [What you sharpened, or "no changes needed"]
**Pass 2 (Headline Scan):** [What you rewrote]
**Pass 3 (3-Idea Cap):** [What you cut, or which ideas survived]
**Pass 4 (Confidence):** [Hedges removed, count]
**Pass 5 (Bar Test):** [Sentences rewritten for spoken rhythm]
**Pass 6 (Mission):** [The one-sentence mission you locked]
**Pass 7 (Audience):** [Crowd → one-person swaps made]
**Pass 8 (Fingerprint):** [The specific moment/insight kept or added]
**Pass 9 (Final Cut):** [Word count before → after, % cut]
**Pass 10 (Anti-slop):** [Hits found and fixed, or "clean"]

---

## Biggest Win

[The single edit that improved the piece the most. One sentence.]

---

## Remaining Gap

[What still needs attention from the user — usually a missing fingerprint, a CTA decision, or a fact you couldn't verify. Or "none — ready to ship."]
```

---

## example: editing a mediocre AI newsletter intro

**Format:** newsletter intro paragraph
**Aggressiveness:** standard

### Before (the draft)

> In today's fast-paced world, many entrepreneurs are looking for ways to leverage AI to grow their business. I think it's important to note that AI tools can be a real game-changer if used correctly. Recently, I had an experience that really opened my eyes to the potential. It's not just about saving time — it's about unlocking new possibilities. If you've ever felt overwhelmed by all the AI options out there, you're not alone. Here's what I learned.

### After (10 passes done)

> Last Tuesday at 11pm, I asked Claude to rewrite a sales page I'd been stuck on for three weeks. It gave me a draft in 90 seconds that beat mine. Not by a little. By a lot. That's the moment I stopped treating AI like a faster typewriter and started treating it like a co-writer. The difference changed how I work. Here's exactly what I changed.

### Pass-by-pass changes

- **Pass 1 (Zoom In):** Replaced "recently I had an experience" with the actual moment — Tuesday, 11pm, three-week-old sales page.
- **Pass 2 (Headline Scan):** Not applicable to a single paragraph. Skipped.
- **Pass 3 (3-Idea Cap):** Original had 5 vague ideas. Kept 3: the moment, the mindset shift, the promise of specifics.
- **Pass 4 (Confidence):** Killed "I think it's important to note" and "you're not alone."
- **Pass 5 (Bar Test):** "Unlocking new possibilities" — nobody says that. Cut. "Real game-changer" — cut.
- **Pass 6 (Mission):** Locked mission: convince the reader the next paragraphs are worth reading because something specific happened.
- **Pass 7 (Audience):** "Many entrepreneurs" cut entirely. The whole para now talks to one person.
- **Pass 8 (Fingerprint):** Added the specific scene — only the user (with that exact stuck sales page) could have written this.
- **Pass 9 (Final Cut):** 95 words to 64 words. 33% cut.
- **Pass 10 (Anti-slop):** Removed "in today's fast-paced world" (slop), "leverage" (banned verb), "it's not X, it's Y" pattern, "game-changer" (banned phrase), em dash density reduced.

### Biggest win

Replacing the abstract "had an experience" with a specific Tuesday-at-11pm scene. Everything else flows from that single concretization.

### Remaining gap

The user needs to confirm the actual numbers (was it really 90 seconds? was it really three weeks?). If those are wrong, swap them — but keep the same level of specificity.

---

## how this connects to other skills

**Feeds in (this skill runs AFTER):**
- `post-longo-x` — tweet drafts go through editing before posting.
- `afiar-ideia` — sharpened ideas turn into drafts that get the 9 passes.
- Any first-draft writing skill — polir-texto is the universal polish layer.

**Feeds out (this skill runs BEFORE):**
- `humanizar-texto` — invoked as Pass 10. Final gate before delivery.
- Publication / send / post — nothing else after the anti-slop gate.

**Does NOT feed:**
- Idea generation (`afiar-ideia`) — different job, runs before writing.
- Strategy or offer skills — editing is prose-level, not concept-level.

If the user asks for an "edit" but the draft has structural problems (wrong angle, no offer, missing hook), flag it back: "this needs to go back to [writing skill] before editing — passes 1-10 won't fix a structural miss."

---

## the test

Before delivering, verify each one. If any fail, fix or flag.

1. **Voice match:** Does the polished version sound like the user (per `voice.md`), not like a generic editor? PASS / FAIL
2. **All 10 passes run:** Pass notes show real changes (or "no changes needed" with reason) for every pass — no skipped passes? PASS / FAIL
3. **Fingerprint present:** Could only the user have written this, or could anyone? PASS / FAIL
4. **Mission clear:** Can you state in one sentence what the piece does? PASS / FAIL
5. **Anti-slop clean:** Zero hits on the banned-phrase list, zero em dashes (unless voice.md allows), no AI-tells? PASS / FAIL
6. **Cut achieved:** Word count down 25-35% from the original (unless light-polish mode)? PASS / FAIL
7. **Bar test:** Read aloud — every sentence sounds like talking, not writing? PASS / FAIL

**Failure condition:** If 2+ tests fail, do NOT deliver. Restart from the failing pass. If voice match fails and no voice context was gathered, that's the root cause — go back to Step A.

---

## rapid-fire checklist

Use this as a final glance before output. (This is the original checklist — keep it; it's the fastest way to spot a missed pass.)

| Pass | Check | Done? |
|------|-------|-------|
| 1 | Specific moments, sensations, real names? | |
| 2 | Headlines tell the story on their own? | |
| 3 | Only 3 core ideas? | |
| 4 | Zero hedging language? | |
| 5 | Would say every sentence over drinks? | |
| 6 | Purpose fits in one sentence? | |
| 7 | Talking to one person, not a crowd? | |
| 8 | Only-I-could-write-this fingerprint present? | |
| 9 | Cut one-third of the words? | |
| 10 | Anti-slop sweep clean? | |

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` sitting next to this SKILL.md.

### At the start of every session using this skill
1. **Read `feedback.log`** in this skill's folder before editing anything. Apply every rule in it to this session's output.
2. If `feedback.log` doesn't exist yet, create it with a header: `# Editing Workshop — Learned Rules`

### During every session — triggers that require a log write

When the user says any of the following, **immediately append a rule to `feedback.log` before continuing**:

- "Don't do X anymore" / "Stop doing X" / "Stop cutting X"
- "Always do Y" / "From now on, do Y" / "Always preserve X"
- "I hate when you..." / "You always..." (correction signal)
- "That's perfect, keep doing that" (log positive patterns — don't drift)
- Silent rewrites where the user restores a line you cut, or recuts a line you kept — infer the rule and log it.

### Format for each logged rule

```
## YYYY-MM-DD — [short title]

**Rule:** [imperative sentence — "always preserve X" or "never cut Y"]
**Why:** [reason the user gave, or the context]
**How to apply:** [which pass this belongs to — 1 through 10 — and when it kicks in]
```

### What to log vs skip

**Log:**
- New protected patterns ("never cut my P.S. signoff")
- Voice calibrations ("my hedges in technical posts are intentional — leave 'I think' alone in those")
- Format-specific rules ("for tweets, skip Pass 2 — there's no headline")
- Pass-weight overrides ("for landing pages, double-weight Pass 7")

**Skip:**
- One-off edits ("change this word here") — not a rule
- Things already in CLAUDE.md or `Context/voice.md` — those are context, not learning

### Cleanup

Every ~10 entries, consolidate: merge duplicates, delete reversed rules, keep log under 100 lines. Stale rules that contradict the latest ones cause drift.

**This is how the skill gets better.** Every rejection is a rule. Every "yes that's right" is a pattern to keep. Read the log. Apply the rules. Append new ones. Forever.

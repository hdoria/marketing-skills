---
name: escrever-newsletter
description: "Write magnetic newsletters using a proven 8-step framework. Use when crafting emails, writing newsletters, or starting copywriting projects. Triggers on: write a newsletter, draft an email, write an edition, help me write, newsletter about [topic]. Multi-step process from raw input to polished output. Outputs publication-ready newsletter with subject lines."
---

# Newsletter Writer

Most newsletters read like blog posts with a subscribe button. Stiff, educational, forgettable. The ones people actually forward sound like a letter from a smart friend who happened to learn something worth sharing.

This skill turns raw ideas into newsletters that feel personal and hit hard — using proven frameworks for angles, structure, and momentum.

**IMPORTANT: All output from this skill must follow the anti-slop editing rules. Run the humanizar-texto skill as a final pass on every newsletter before presenting it. Zero tolerance for AI-sounding copy.**

---

## the core job

Produce a **complete newsletter edition** that:
- Follows the Rule of One (one problem, one story, one solution, one CTA)
- Opens with a hook that earns the next sentence
- Sounds like a person wrote it, not a content machine
- Ends with a line worth remembering

**Output:** Subject line + full newsletter + P.S. — ready to send.

---

## before starting: gather context

**STOP. Do not write a newsletter until context is in hand AND the core idea is clear. Cap questions at 2 max.**

### Step A: Gather context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for:
   - **Business** — what the user sells, current launches, proof. Grounds takes in reality.
   - **ICP** — who the reader is, their pain, exact phrases. The newsletter must sound written TO this person.
   - **Voice** — tone, do/don't, sample sentences. Must read like the user wrote it.
2. **If missing, check the project folder** for `Context/business.md`, `Context/icp.md`, `Context/voice.md`. Read whichever exist.

### Step B: Confirm the brief (≤2 questions, combined)

Skip anything context already covers. Combine into at most 2 questions:

1. **Raw material + core idea** — "What are we working with (voice memo, notes, starting fresh?), and what's the ONE point? Not three — one." (If unclear, help them find it.)
2. **CTA + opener style** — "What should the reader do (reply/click/buy/think differently?) and want a Snapshot opener (scene with time/sensory) or a Snipershot (direct hook)?"

The angle (Step 2 in the process) is picked from context, not asked up front.

---

## the process

```
EXTRACT → ANGLE → OUTLINE → OPEN → PROVE → CLOSE → EDIT → PRESENT
   |        |        |         |       |        |       |        |
  raw     pick     skeleton   hook   body+   CTA+    3-pass    subject +
  input   from 10   for      that   But &   PS that  + anti-   final
  to      angles   approval  earns  There-  ends     slop      output
  gold              by user   line  fore    hard     check
                              two
```

Work through these 8 steps in order. Each step produces a specific piece of the newsletter.

---

## extract: pull the gold from raw input

If the user provides a voice memo, transcript, or messy notes — extract the gold before anything else.

**What to pull out:**
- The core idea buried in the ramble (the ONE thing they're trying to say)
- Stories or anecdotes mentioned (with specific details)
- Opinions or hot takes (where they got fired up — that's the fuel)
- Numbers, names, quotes worth keeping
- Emotional beats (where energy spiked)

**Present back to user:**

```
## Extracted from your input

**Core idea I'm hearing**: [One sentence]
**Stories you mentioned**: [List any]
**Your take**: [The opinion/stance]
**Good details to keep**: [Specifics worth preserving]
**Best angle for this**: [Which of the 10]
**What I still need**: [Gaps — e.g., "How did this story end?"]

Does this capture it? Anything to add or correct before I outline?
```

Don't proceed until they confirm this captures it.

**Anti-pattern:** Don't invent details they didn't mention. If the transcript is thin, say so and ask for more.

---

## angle: pick one of the 10 lenses

Every newsletter needs a single angle. Not a theme — an angle. The angle determines what lens you tell the story through.

**The 10 Angles:**

| # | Angle | Best when... |
|---|-------|-------------|
| 1 | **Opinions** | You have a strong belief most people don't share |
| 2 | **Observations** | Something you see makes you sad, mad, or curious |
| 3 | **Predictions** | You see where your space is headed |
| 4 | **Obstacles** | You can name what's blocking your reader |
| 5 | **Personal Stories** | Mistakes, fears, doubts — how you got here |
| 6 | **Stories About Others** | Client wins/fails, historical figures, friends |
| 7 | **Surprising Facts** | Something you learned that surprised you |
| 8 | **Audience Questions** | Someone asked something worth answering publicly |
| 9 | **Authority by Association** | An insight from someone influential, filtered through your take |
| 10 | **Current Trends** | Something just happened in your space |

**How to pick:** Match the raw material to the angle that creates the most tension. Tension = interest. If the user's story is about their own failure, that's #5. If they're reacting to an industry move, that's #10. If they have a spicy opinion, that's #1.

**Anti-pattern:** Don't default to "Personal Stories" every time. Vary angles across editions.

---

## outline: build the skeleton before writing

Build the skeleton before writing a word. Present this to the user for approval.

**The outline framework:**

```
## Newsletter Outline

**Core Idea**: [One sentence — the Rule of One]
**Angle**: [Which of the 10]
**Reader Problem**: [Why they care]
**Opening**: [Snapshot or Snipershot] — [Hook idea]

### Sections:
1. **Open**: [What it establishes — the scene or hook]
2. **Build**: [First supporting point or story beat]
3. **Prove**: [Evidence, framework, or deeper insight]
4. **Turn**: [The pivot — where it connects to the reader]
5. **Close**: [CTA + strong final line idea]
6. **P.S.**: [Tease or secondary CTA]

**Closing line idea**: [The mic-drop ending]
```

**Rules:**
- Each section is 1-3 paragraphs. Not a textbook.
- Must pass the Rule of One: one problem, one story, one solution, one CTA
- If there are more than 3 core ideas, there are zero. Cut until you hit 3.

Don't write the newsletter until the user approves the outline.

**Anti-pattern:** Don't outline 8 sections. A newsletter isn't a whitepaper. 4-6 sections max.

---

## open: earn the second sentence

The first line earns the second. The second earns the third. If the opener fails, nothing else matters.

**Two opener types:**

**Snapshot** (scene-setting) — Drop the reader into a specific moment:
- Time + Location + Sensory detail
- "Last Tuesday, 6am, Berlin apartment. My phone buzzed with a number I couldn't believe."
- Works best for: personal stories, observations, client stories

**Snipershot** (direct hit) — Open with the hook, no scene:
- "Most creators are building their business backwards."
- "I almost sold everything last month."
- Works best for: opinions, predictions, surprising facts

**After the opener:**
- Create a slippery slide — short sentences that pull the reader down the page
- Make an early promise — what will they get by reading this?

> Example Snapshot: "6am Cologne airport. The guy next to me is scraping ice off the wing with what looks like a spatula. I'm drinking an iced flat white because I'm that guy. My girlfriend thinks I'm insane. Anyway."

> Example Snipershot: "I charged $50 for my first product. It took me three years to realize that was the single worst decision I made."

**Anti-pattern:** Never open with setup ("In today's fast-paced..." / "I've been thinking about..."). Start with the actual thought.

---

## prove: build momentum with But & Therefore

This is the body. Use the **But & Therefore** technique to create momentum — never "and then."

**The rule:** Connect ideas with "but" and "therefore" to create tension:
- Weak: "I started a newsletter and then I got subscribers and then I made money."
- Strong: "I started a newsletter. But nobody subscribed for three months. Therefore I had to rethink everything. But when I did..."

**Tools of Trust** (use at least 2 per newsletter):
1. **Results** — real numbers, real outcomes
2. **Metaphor** — make complex things simple through comparison
3. **Specificity** — "$47,293" not "a lot of money"
4. **Story** — show, don't tell through narrative
5. **Stats/Facts** — borrowed credibility from research
6. **Elegant articulation** — say it in a way the reader couldn't say themselves

**Keep the slide slipping** with micro-loops:
- "But here's where it gets interesting..."
- "That wasn't even the craziest part."
- "Which brings me to the real lesson..."

**Bounce between "me" and "you"** — alternate between your story and the reader's situation. Don't stay in your own head for more than 2 paragraphs before pulling the reader in.

**Anti-pattern:** Don't educate. Excite. Emails excite. Courses educate. If you're explaining a 7-step framework, you've left the newsletter and entered a blog post.

---

## close: pivot to the ask without breaking the spell

The close does three things: lands the point, pivots to the ask, ends strong.

**The pivot:** Continue the conversation naturally into the CTA. Don't drop the story to suddenly sell.

**CTA rules:**
- Never be needy
- Give a reason why
- Apply pressure only if real (urgency, scarcity)
- Finish as a friend (casual sign-off)

**P.S. rules:**
- Summarize to intrigue (not to repeat)
- Crank up curiosity — appeal to self-interest, tease more information
- Secondary CTA if needed

**The closing line** is the most important sentence after the opener. It should:
- Land with impact
- Feel like a mic drop, not a fizzle
- Never end on logistics or a weak CTA

> Example pivot: "Which is exactly why I'm running this workshop again next Thursday — same setup, smaller group, more 1:1 time. If you've been on the fence, this is the one. [Link.]"

> Example closing line: "The choice is yours. But the clock's ticking."

> Example P.S.: "P.S. Last time we ran this, three people set up Claude Code in the first 20 minutes and shipped a piece of content before lunch. I'm not saying that'll be you. But it might be."

**Anti-pattern:** Don't sign off with "Hope this helps!" or "Let me know your thoughts!" — those are throat-clearing. End on the line that lands.

---

## edit: three passes plus anti-slop

Three passes before presenting. No exceptions.

**Pass 1: The Scanner** (overall feel)
- Rule of One intact? One problem, one story, one solution, one CTA?
- Personal perspective included?
- Any points out of place?
- Happy with the hook?

**Pass 2: The Surgeon** (line-by-line)
- Is it clear? Can I be more specific? (replace generalities, paint pictures, use numbers)
- Is it brief? Can I say it in less? Can I cut, combine, or replace?
- Is it strong? Remove passive voice, adverbs, hedging language

**Pass 3: The Speaker** (read aloud)
- Friction? Smooth it.
- Fakeness? If you wouldn't say it, don't write it.
- Flow? Vary sentence length. Short. Then long. Then short again.

**The 1/3rd Rule:** Check word count. Cut 1/3rd. The first draft is always too long.

**Pass 4: Anti-slop check (MANDATORY)**
Run the **humanizar-texto** skill on the final draft. Every newsletter must pass through all 5 anti-slop filters (structure, phrases, verbs, formatting, content) before being presented. If any banned phrases or AI patterns survive, fix them before showing the output.

**Anti-pattern:** Don't polish into corporate smoothness. Some rough edges sound real.

---

## anti-slop: mandatory pass

Before showing any newsletter draft to the user, run it through the `anti-slop` skill.

**Why this skill especially:** Newsletters are prose-heavy and prone to the worst AI patterns — rhetorical questions as section breaks ("Want to know the secret?"), forced threes, melodramatic realizations, robot phrases (game-changer, unlock, supercharge, leverage).

**How:** Invoke `anti-slop` with the full draft (subject line, preview text, body, CTA, P.S.) as input.

**If `anti-slop` is not available,** scan manually for: rhetorical questions, binary opposites ("it's not X, it's Y"), robot phrases, throat-clearing ("It's worth noting..."), em dash overuse, zero contractions, same-length paragraphs throughout.

Pay special attention to the subject line and first sentence — slop there kills the open rate and the read rate before the body matters.

Rewrite anything flagged. Non-negotiable: no newsletter ships without this pass.

---

## present: write the subject line last and ship

Write the subject line LAST — after the newsletter is done, you know what it's actually about.

**Subject line rules:**
- 3-second rule: Does it earn the open?
- Don't be boring (surprise, shock, familiarity, sticky statements, questions)
- Lowercase preferred over title case (feels personal, not promotional)
- Under 50 characters when possible
- Write 3 options — main + 2 alternatives

**Preview text rules:**
- Continues the subject — don't repeat it
- 40-90 characters
- Adds curiosity or a second hook
- Treat it as the second subject line, not afterthought

> Example subject: "i almost canceled the workshop"
> Example preview: "then 47 emails arrived in 6 hours."

**Anti-pattern:** Don't write the subject first and force the body to match. The body knows what it's about — the subject just delivers it.

See the **output format** section below for the exact template to use.

---

## fundamentals & advanced techniques

Every newsletter must pass the **5 fundamentals** (Curious, Clear, Conversational, Concise, Credible) and should use at least one **advanced technique** (Polarization, HEAL microstories, Sticky Statements, Me/You bouncing, Slippery Slide).

For full breakdowns with examples and tactics, see [references/deep-techniques.md](references/deep-techniques.md).

For the 13 angle-specific newsletter templates (Opinions, Observations, Predictions, Obstacles, Personal Stories, Client Stories, Surprising Facts, Audience Questions, Authority, Current Trends, Listicle, Opening Offers, Closing Offers), see [references/templates.md](references/templates.md).

---

## output format

Every newsletter ships in this exact structure. No exceptions.

```
## Subject Line: [main option, lowercase, under 50 chars]
- Alt 1: [alternative subject]
- Alt 2: [alternative subject]

**Preview text:** [40-90 chars, continues the subject, doesn't repeat it]

---

[Opening hook — Snapshot or Snipershot. 1-3 short paragraphs that earn the next sentence.]

[Body — Build, Prove, Turn. Use But & Therefore. Bounce between "me" and "you". 4-6 sections total, each 1-3 paragraphs.]

[Closing line — the mic drop. One sentence worth quoting.]

[CTA — natural pivot from the close. Why now, why this, what to do.]

[Casual sign-off — first name only, or a one-line tag.]

P.S. [Tease, secondary CTA, or curiosity bomb. 1-2 sentences max.]

---

**Word count:** [X]
**Angle used:** [Which of the 10]
**Rule of One check:** ✓ One problem, one story, one solution, one CTA
**Anti-slop check:** ✓ Passed all 5 filters
```

---

## example: announcing the second workshop run

**Scenario:** Ole writes to his 350-person waitlist + recent attendees to announce the second workshop run. Audience is non-technical marketers who feel overwhelmed by Claude Code. Angle: #5 Personal Story (his own near-cancellation). CTA: book the workshop seat.

```
## Subject Line: i almost canceled the second workshop
- Alt 1: 47 emails in 6 hours
- Alt 2: this almost didn't happen

**Preview text:** then 47 emails arrived in 6 hours.

---

Tuesday morning, 6:42am, my kitchen in Berlin. I'm staring at the
draft email that says "hey, I'm pulling the second workshop, refunds
incoming." Coffee getting cold. Finger hovering over send.

I didn't send it.

Here's why.

The first workshop wrapped three weeks ago. ~$30k in revenue. 350
people on the waitlist. By every spreadsheet metric, I should've been
sprinting to run it again.

But I was fried. The week of the workshop I slept 4 hours a night.
My girlfriend threatened to hide my laptop. I opened the second-run
draft seven times and closed it seven times.

So Tuesday I decided to kill it. Drafted the email. Made coffee.
Re-read the email.

Then I checked the inbox.

47 messages from the waitlist had landed overnight. Not pitches.
Not "looks cool!" Real ones. "I tried Claude Code three times and
quit. When's the next workshop?" "I bought your skills. I can't get
them to load. Help." "Please tell me you're running this again. I
have a launch in May."

I read them all. Then I deleted the draft.

Therefore: the second run is happening. May 2nd. Same setup, same
hands-on format, same "everyone leaves with Claude Code working
and a piece of content shipped." Smaller group this time. More 1:1
time per person. I'm capping it at 40.

If you've tried Claude Code and bounced off, this is built for
you. I'm not a dev. I hate touching code. I figured out the easy
route and I'll walk you through it live.

The waitlist gets first pick. Spots open Friday 9am Berlin time.
Public link goes out Sunday.

If you want in, reply with "in" and I'll send you the link an hour
before it goes public.

The 47 emails almost made me run. Then they made me stay.

— Ole

P.S. Three people in the first run set up Claude Code in the first
20 minutes and shipped a piece of content before lunch. I'm not
saying that'll be you. But it might be.

---

**Word count:** 348
**Angle used:** #5 Personal Story
**Rule of One check:** ✓ One problem (overwhelm + waitlist), one story (the 47 emails), one solution (run it again), one CTA (reply "in")
**Anti-slop check:** ✓ No rhetorical questions, no robot phrases, no em dashes, no fake profundity, opening uses sensory detail, closing line callbacks the hook
```

**Why this works:**
- Snapshot opener (time + place + sensory: "6:42am, my kitchen in Berlin", "Coffee getting cold")
- But & Therefore drives momentum: "I should've been sprinting. But I was fried." → "Therefore: the second run is happening."
- Specific numbers (~$30k, 350 waitlist, 47 emails, 4 hours sleep, 40 seats, May 2nd) — not "a lot" or "soon"
- Bounces between "me" (Ole's burnout) and "you" (the reader who tried Claude Code and bounced off)
- Casual asides (the girlfriend threat, "Then I checked the inbox.")
- CTA pivots naturally — doesn't break the spell to suddenly sell
- P.S. teases a result without overpromising
- Closing line ("almost made me run. Then they made me stay.") callbacks the opener and lands

---

## how this connects to other skills

**Feeds INTO this skill:**
- **afiar-ideia** — Run before this when the core idea is bland. Returns a sharper angle/proposition this skill can build a newsletter around.
- **post-longo-x** — High-performing long-form tweets are pre-validated newsletter ideas. Pull the winning hook + structure as raw input for Step 1 (Extract).
- **entrevista-negocio** — Generates business / ICP / voice context (into CLAUDE.md or `Context/*.md` files) that Step A pulls from before writing.

**Feeds OUT of this skill:**
- **humanizar-texto** — MANDATORY pass on every newsletter before presenting. Zero AI-sounding copy gets through.
- **sequencia-email** — Newsletters become the spine of welcome sequences and launch sequences. A great newsletter = a great Email 3.
- **reaproveitar-conteudo** — One newsletter becomes 5-8 platform-native posts (LinkedIn, X, Threads, IG carousel).
- **landing-page** — Newsletter CTAs link to sales pages built with this skill. Use the same angle and core story on both.

**Social > Email Flywheel:**
- Turn high-performing social posts into newsletter editions (noise → signal)
- Turn newsletter editions into social content (screenshots, sticky statements, big ideas)

---

## the test

A good newsletter:

1. **Passes the Rule of One** — One problem, one story, one solution, one CTA. If you have three main points, you have zero.
2. **Opens with a throat-grab** — First sentence makes you need the second one. No setup, no throat-clearing.
3. **Sounds like a person** — Read it aloud. Every sentence you'd say to a friend over drinks. Zero sentences that smell like AI.
4. **Moves with But & Therefore** — Not "and then, and then, and then." Tension and resolution pulling the reader forward.
5. **Includes personal perspective** — Stories, opinions, what makes you weird. If anyone could've written it, no one will read it.
6. **Ends hard** — The closing line is worth quoting. Not logistics, not a weak CTA.
7. **Survived the 1/3rd cut** — If you didn't cut 1/3rd of the words, you didn't edit.
8. **Passes anti-slop** — Zero banned phrases, zero AI patterns, zero corporate smoothness. If it sounds like AI wrote it, it failed.

If the newsletter reads like a blog post emailed to a list — it failed. Newsletters are conversations, not content.

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` next to this SKILL.md.

### At the start of every session
1. Read `feedback.log` in this skill's folder. Apply every rule to this session's output.
2. If it doesn't exist, create it with header: `# Newsletter Workshop — Learned Rules`

### Triggers that require a log write

When the user says any of the following, immediately append a rule before continuing:
- "Don't do X anymore" / "Stop doing X" / "Never do X"
- "Always do Y" / "From now on, do Y"
- "I hate when you..." / "I don't like..."
- "That's perfect, keep doing that" (log positive patterns — don't drift)
- Silent rewrites where the user fixes your draft — infer the rule from the diff

### Format for each rule
```
## YYYY-MM-DD — [short title]
**Rule:** [imperative sentence]
**Why:** [reason]
**How to apply:** [when this kicks in — which section, which newsletter type]
```

### What to log vs skip
**Log:** subject line rules, structural preferences (CTA placement, P.S. style), voice calibrations, format-specific rules.
**Skip:** one-off edits to a specific newsletter, preferences already in Context/voice.md.

### Cleanup every ~10 entries. Consolidate, delete reversed rules, keep under 100 lines.

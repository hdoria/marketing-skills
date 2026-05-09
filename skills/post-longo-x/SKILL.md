---
name: post-longo-x
description: "Write high-engagement long-form Twitter/X posts (500-3000 chars) using proven structural patterns from creators who consistently hit 100k+ views. Use when asked to write tweets, X posts, long-form posts, or social content. Triggers on: write a tweet, draft a post, write for X/twitter, create a viral post, help me post about [topic]. Applies anti-AI-slop principles automatically. Outputs a ready-to-post tweet."
---

# Viral Long-Form Tweets

Most long-form tweets die because they read like LinkedIn posts pasted into Twitter. Stiff paragraphs, corporate rhythm, and that unmistakable AI smell where every section follows the same beat.

The posts that actually break through sound like someone thinking out loud. A genuine opinion, some mess around the edges, and a structure that pulls you down the page without you noticing.

This skill captures 9 structural patterns from creators who consistently crack 100k+ views on long-form posts — and delivers them in writing that sounds like a real person typed it.

---

## the core job

Produce a single **long-form tweet** (500-3000 characters) that:
- Follows a proven structural pattern from high-performing creators
- Sounds human — conversational, direct, no corporate rhythm
- Carries a genuine point of view (not a restatement of common wisdom)
- Applies anti-AI-slop rules automatically

**Output:** One ready-to-post tweet + pattern label + char count.

---

## before starting: gather context

**STOP. Do not write a tweet until context is in hand AND the brief is clear. Cap questions at 2 max.**

### Step A: Gather context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for:
   - **Business** — what the user sells, public proof/numbers. Grounds the tweet in real stakes.
   - **ICP** — who the reader is, their language. The tweet must land for THIS audience.
   - **Voice** — tone, do/don't, sample sentences. Voice shows up faster in tight formats.
2. **If missing, check the project folder** for `Context/business.md`, `Context/icp.md`, `Context/voice.md`. Read whichever exist.

### Step B: Confirm the brief (≤2 questions, combined)

Skip anything context already covers. Combine related fields into at most 2 questions:

1. **Topic + angle** — "What's the post about, and what's the actual take?" (The opinion IS the content — "AI is changing things" is not an angle, "AI agents will make 80% of SaaS tools obsolete within 3 years" is.)
2. **Style + goal** — "Which pattern family (strategic, cultural/philosophical, raw builder update) and what's the goal (engagement, drive to product, authority, just share)?"

Audience calibrates vocabulary — pull from context, don't ask a separate question.

---

## the structural patterns

There are 9 patterns total. The 5 most-used live inline below — they cover ~85% of long-form tweet shapes you'll need. Patterns 3, 5, 6, 9 (Bookend Reframe, Paradox Reveal, Extended Analogy, Personal Honesty Drop) live in [references/extended-pattern-catalog.md](references/extended-pattern-catalog.md) — use them when the topic shape calls for them.

### Strategic Patterns (action-oriented, opportunity-focused)

**Pattern 1: The Numbered Opportunity List**
Best for: opportunities, tools, trends, "here's what's possible" posts

```
[Bold thesis — 1-2 sentences, can be ALL CAPS]

[Personal credibility hook or setup — 2-3 sentences]

1. [specific insight or capability]
2. [specific insight or capability]
...
8-19. [keep going — volume IS the point]

[Short, warm close — 2 sentences max]
```

Rules:
- Lists go 8-19 items. Not the AI-default 3-5. Volume creates the impression.
- Each item is self-contained. Not sub-bullets under a category.
- Mix practical items with philosophical ones. Vary the energy.
- Close warm and short: "Enjoy it." or "Happy building." Not a paragraph.

**Pattern 2: The Step-by-Step Framework**
Best for: how-to content, playbooks, process breakdowns

```
[Thesis framed as opportunity — 1-2 sentences]

step 1
[Full paragraph explanation — conversational, not bullet-pointed]

step 2
[Full paragraph explanation]
...
step 8-10
[Full paragraph explanation]

[Closing reframe that zooms back out]
```

Rules:
- "step 1" as literal text headers (lowercase, no bold)
- Each step is a real paragraph, not a one-liner
- Drop specific tool names, platforms, real details
- Close by zooming out — what does this add up to?

**Pattern 3: The Bookend Reframe** — math/logic reveal that ends where it began. Full framework in [references/extended-pattern-catalog.md](references/extended-pattern-catalog.md).

### Commentary Patterns (philosophical, cultural analysis)

**Pattern 4: The Cultural Analysis**
Best for: company moves, platform dynamics, power shifts, industry takes

```
[Observation stated as fact — strong judgment, not hedged]

[The deeper mechanics — what's actually happening underneath]

[Implication chain — what this means going forward]

[Personal take or sharp closing line]
```

Rules:
- Open with a strong judgment. "Absolutely savage." Not "quite interesting."
- Each paragraph is 2-4 sentences max. Dense, not sprawling.
- Build from observation → mechanism → implication
- No numbered lists. Flowing prose.
- Close with a line that hits. Not a summary.

**Pattern 5: The Paradox Reveal** — quote the naive view, dismantle it. Full framework in [references/extended-pattern-catalog.md](references/extended-pattern-catalog.md).

**Pattern 6: The Extended Analogy** — single metaphor domain extended across 3-6 items. Full framework in [references/extended-pattern-catalog.md](references/extended-pattern-catalog.md).

### Builder Patterns (raw, honest, in-progress)

**Pattern 7: The Build-in-Public Update**
Best for: sharing what you built, automation updates, tool discoveries

```
[What I built or tested — stated flat]

[How it works — arrows or numbered steps]

[Honest assessment — what works, what doesn't]

[What actually matters despite the limitations]
```

Rules:
- Typos and imperfections are fine. Don't over-polish.
- "→" or "->" for process flows
- Include honest limitations. "Only works because..." or "Maybe 60-70% there."
- Close casual. "So much fun" not "this will revolutionize your workflow."

**Pattern 8: The Provocative One-Take**
Best for: hot takes, opinions, observations that need no explanation

```
[Strong opinion — flat, no buildup]

[Optional: one line of supporting context]

[No conclusion — let it breathe]
```

Rules:
- The whole tweet is 1-3 sentences. That's it.
- No setup paragraph. No "here's what I've been thinking about."
- If you need to explain it, the take isn't sharp enough.
- Ending without a period is fine.

**Pattern 9: The Personal Honesty Drop** — surprisingly honest moment, no moral attached. Full framework in [references/extended-pattern-catalog.md](references/extended-pattern-catalog.md).

For full real-tweet examples of every pattern (1-9) with annotations, see [references/extended-examples.md](references/extended-examples.md).

---

## the voice rules

Apply these to every tweet regardless of pattern. This is what separates human-sounding posts from AI output.

### Always
- **Conversational first.** Write like you'd explain it to a smart friend. Not like you're presenting to a board.
- **Short sentences. Fragment sentences.** One thought per line when you want emphasis.
- **Contractions.** don't, can't, it's, won't. Always.
- **Specific details.** Tool names, dollar amounts, timeframes, real examples. Specificity is credibility.
- **Genuine reactions.** If something is wild, say it's wild. Don't describe it as "quite remarkable."
- **Imperfect punctuation is fine.** Skip the period on the last line. Use "..." for trailing thoughts. One exclamation mark per post max.
- **Vary paragraph length.** One line. Then four lines. Then two. AI writes in balanced blocks. Humans don't.

### Never
- Em dashes (—) more than once per post
- Semicolons in tweets
- "However," "Moreover," "Furthermore," "Additionally"
- Rule of three ("fast, efficient, reliable") — use two, or four, or one
- Rhetorical transition questions ("But what does this mean?" "The catch?" "The kicker?")
- "It's not about X, it's about Y" (binary opposite framing)
- Hedge phrases: "It's worth considering," "You might want to think about"
- Corporate vocabulary: utilize, leverage, facilitate, optimize, implement, synergy, game-changer, revolutionary, supercharge, transform, unlock, actionable, unpack, deep dive
- Passive voice: "it was discovered that..."
- Generic motivational closes: "Stay hungry." "What do you think?" "The future is yours."
- "No X. No Y. Just Z." — instant AI tell
- "If you're serious about..." — every AI CTA uses this

For the full anti-slop detection checklist, see [references/anti-slop-checklist.md](references/anti-slop-checklist.md).

For 8 proven hook formulas with 40+ real examples and a stacking technique for combining them, see [references/hook-patterns.md](references/hook-patterns.md).

---

## the process

```
PICK pattern → DRAFT body → KILL warm-up → CHECK voice →
TIGHTEN close → STRESS-TEST specificity → MEASURE length →
SLOP-PASS (mandatory) → DELIVER
```

Each step has a single job. Don't skip ahead — order matters because slop sneaks in when you edit without a draft to react to.

### pick: the pattern

Match the topic to one of the 9 patterns above. Don't force it — if the topic is a hot take, don't stretch it into a 12-item list.

**Framework:** Topic shape → Pattern.
- Opportunity, tools, "what's possible" → Pattern 1 or 2
- Logic chain, math reveal → Pattern 3
- Industry move, cultural read → Pattern 4 or 5
- Comparison, dynamics → Pattern 6
- Just shipped something → Pattern 7
- One sharp opinion → Pattern 8
- Vulnerable observation → Pattern 9

**Anti-pattern:** Picking Pattern 1 (numbered list) for everything because it feels safe. Lists are fine, but a hot take crammed into 12 items dies.

### draft: the body fast

Write version one without editing. Get structure + point down. It will be messy. That's the job.

**Framework:** Open with the angle (not setup), follow the pattern's skeleton, close on the actual last point. No second-guessing on this pass.

**Anti-pattern:** Editing while drafting. You'll never finish, and the result reads like a committee wrote it.

### kill: the warm-up

Look at the first sentence. Is it setup? ("In today's fast-paced..." / "I've been thinking about...") Delete it. Start with the actual thought. If the opener feels weak, see [references/hook-patterns.md](references/hook-patterns.md) for 8 proven formulas.

**Framework:** Cover the first 1-2 sentences with your hand. Does the post still work? If yes, those sentences were warm-up. Delete.

**Anti-pattern:** Keeping a "context" sentence because it explains the setup. The reader doesn't need the setup. They need the punch.

### check: the voice

Read it out loud. Every sentence that sounds "written" instead of "said" — rewrite it. If you wouldn't say it to someone at a bar, it doesn't belong in a tweet.

**Framework:** The Speech Test. For each sentence ask: "Would I say this exact sentence to a friend over coffee?" If no, rewrite.

**Anti-pattern:** Sentences that work on paper but no human would say them out loud. ("In essence, the dynamic at play here is...")

### tighten: the close

If it ends with a motivational platitude or "what do you think?" — cut it. End on the actual last point. Or leave it hanging. Both work better than a tidy bow.

**Framework:** Three legal endings — (1) the actual last beat of the argument, (2) a sharp question that does work, (3) nothing (let it breathe).

**Anti-pattern:** "What do you think?" / "Stay hungry." / "The future is now." All three say "AI wrote this" louder than any other tell.

### stress-test: the specificity

Could you swap in any other topic and the post still makes sense? If yes, it's too generic. Add a specific number, tool name, personal detail, or concrete reference.

**Framework:** The Substitution Test. Replace your topic with a random other topic (e.g., "barbecue sauce" or "marathon training"). Does the post still kind of work? Then it's too generic. Inject specifics until substitution would make the post nonsense.

**Anti-pattern:** "AI is changing everything fast." Swap "AI" for "barbecue sauce." Still works as a generic statement. Useless.

### measure: the length

Match the pattern's natural range:
- Numbered lists: 1200-3000 chars
- Step frameworks: 1500-3000 chars
- Bookend reframe: 400-700 chars
- Cultural analysis: 500-800 chars
- Paradox reveal: 400-700 chars
- Extended analogy: 400-600 chars
- Build update: 500-1200 chars
- Hot takes: 100-400 chars
- Personal drops: 200-500 chars

**Framework:** If you're outside the range, the pattern is wrong OR you're padding. Both fixable. Don't ship a 1500-char hot take.

**Anti-pattern:** Hitting an arbitrary "long-form means 3000" target by adding filler. Length serves the pattern, not the other way around.

---

## anti-slop: mandatory pass

Before showing any tweet to the user, run it through the `anti-slop` skill.

**Why this skill especially:** Long-form tweets concentrate slop. Every robot phrase (game-changer, unlock, leverage), every "Here's the kicker", every binary opposite ("it's not X, it's Y") is more visible because there's no body text to hide behind. One slop line kills the whole post.

**How:** Invoke `anti-slop` with the full tweet draft as input.

**If `anti-slop` is not available,** scan manually for: rhetorical questions ("Here's the kicker?", "Sound familiar?"), binary opposites, robot phrases, forced threes (adjective triplets, three-bullet lists), emoji confetti, em dash overuse, zero contractions. Also scan for fake profundity — "Not because of X. But because of Y." is the #1 long-form tweet tell.

Rewrite anything flagged. Non-negotiable: no tweet ships without this pass.

---

## output format

Deliver in exactly this shape. No preamble, no "here's your tweet," no commentary above the post.

```
[HOOK LINE — 1-2 sentences. The opener that stops the scroll. Lowercase OK. ALL CAPS OK if the pattern calls for it.]

[BODY — pattern-specific structure. Numbered list, stepped framework, cultural commentary, etc. Paragraph lengths VARY. Specific details inline (numbers, tool names, real moments).]

[SIGNATURE / CLOSE LINE — the final beat. The actual last point, OR a sharp question, OR nothing tidy. Never "what do you think?" Never a motivational platitude.]
```

Followed by:
- **Pattern**: [1-9 + name, e.g. "Pattern 4 — Cultural Analysis"]
- **Chars**: [exact character count, e.g. "1647"]
- **Flags**: [anything the user must swap in — "[insert your real Q1 number]" — or "None"]
- **Dial check**: [hook score 1-10 + one-line rationale. If below 7, propose a sharper hook.]

---

## example: "lessons from running a $30k claude code workshop"

**Context:**
- Topic: What I actually learned running my first live Claude Code workshop for non-technical marketers
- Angle: The thing that made it work wasn't the curriculum — it was setting people up so they got a dopamine hit in the first 30 minutes
- Style: Step-by-Step Framework (Pattern 2), with builder-update voice
- Audience: Creators, course makers, people thinking about running live cohorts
- Goal: Authority, drive to waitlist for the next round

**Output:**

```
ran my first live claude code workshop a few weeks ago. 350+ people on the waitlist, ended up doing about $30k in revenue. here's what actually worked and what I'd do differently if I ran it tomorrow.

most people teaching "AI for non-technical folks" lose the room in the first 20 minutes. setup hell. terminal errors. someone's on windows and the install path is different. by minute 30 the chat is dead and half the room is checking email. I knew if I lost them in setup, I'd never get them back.

step 1
I cut the entire intro. no "what is claude code, why does it matter, here's the history of LLMs." nobody paid $99 to hear me explain things they already googled. I started with "open your terminal, paste this, press enter." within 4 minutes everyone had something installed. that one decision saved the workshop.

step 2
I built a personal skill file pack and gave it away in the first 10 minutes. write a tweet, draft a newsletter, repurpose a podcast. these are the exact things marketers actually do. people ran their first command and got a usable output before they understood what was happening. dopamine first, theory later.

step 3
I treated every error live. someone's claude wouldn't authenticate. instead of pretending it didn't happen, I screen-shared and walked through it. that one moment got more positive feedback than any of the polished content. people don't want a flawless presenter. they want proof that when it breaks, you can fix it.

step 4
I scoped the first "win" tiny. not "build an n8n automation that posts to all your platforms." just "use claude to rewrite this paragraph in your voice." everyone hit that win. then we layered. by the end of hour two people were chaining skills together without realizing it had gotten complex.

step 5
I sold the upsell from inside the workshop, not after. for people who wanted to go deeper there was a 4-week cohort. I mentioned it once at the 90-minute mark, while they were riding the high of having something work. didn't pitch hard. just said "if you want help applying this to your specific business, here's the next step." 18% took it.

what I'd change next time: add a 15-minute pre-workshop setup video so the install is done before we start. and cap it at 100 people so I can actually see what's going wrong in chat.

the workshop format works because it solves the one thing courses cant — the moment something breaks and you don't know what to do. opening the next one in a few weeks. waitlist link in bio
```

**Pattern**: 2 — Step-by-Step Framework
**Chars**: 2487
**Flags**: Replace "in bio" with actual link before posting. Confirm the 18% upsell number against actual numbers.
**Dial check**: 8/10 — "$30k in revenue" + "350+ waitlist" in line 1 does the work. Could push to 9 by leading with the most counterintuitive lesson ("I cut the entire intro") instead of the result, but the proof-first opener fits the workshop ICP better.

---

## example: "AI agents replacing SaaS"

**Context:**
- Topic: AI agents replacing traditional SaaS
- Angle: Most SaaS is just a database and some if/then logic — agents don't need that
- Style: Cultural analysis (Pattern 4)
- Audience: Builders and founders
- Goal: Authority, engagement

**Output:**

```
the entire saas industry is built on a lie nobody talks about

most saas products are a database, a form, and some if/then logic wrapped in a $49/mo subscription. the actual value is maybe 3% of the codebase. the rest is auth, billing, dashboards, settings pages, onboarding flows — infrastructure tax.

agents don't need any of that.

an agent doesn't need a pretty UI. doesn't need a settings page. doesn't need a pricing tier. it just needs context and a task.

we're about to watch thousands of saas tools get compressed into prompt + context + api call. the whole middle layer just evaporates.

the founders who see this are already building agents-as-a-service. the ones who don't are adding "AI features" to their existing product and calling it innovation.

one group eats the other. it won't take long.
```

**Pattern**: 4 — Cultural Analysis
**Chars**: 721
**Flags**: None
**Dial check**: 8/10 — "a lie nobody talks about" is strong. Could push to 9 by naming a specific SaaS tool as the example.

---

## example: "building content automations"

**Context:**
- Topic: Content repurposing automation
- Angle: Just built something, sharing honestly
- Style: Build-in-public (Pattern 7)
- Audience: Builders, content creators
- Goal: Share progress, drive to newsletter

**Output:**

```
been working on a content repurposing flow in n8n and its kinda wild how far you can push it

the flow:
-> takes my latest newsletter
-> breaks it into 5 tweet angles using claude
-> drafts each one with my past viral posts as style reference
-> drops them into a notion board for review

the drafts arent perfect. maybe 60-70% there. but thats the whole point — you still need taste to pick the right ones and edit them into something real

the actual unlock isnt "ai writes your tweets." its "ai gives you 5 starting points instead of staring at a blank screen for 20 minutes"

took about 3 hours to build. ill share the full breakdown in my newsletter this week
```

**Pattern**: 7 — Build-in-Public Update
**Chars**: 618
**Flags**: Newsletter link needed
**Dial check**: 7/10 — honest and relatable. Could push to 8 by including a specific result ("one of the drafts got 2x my normal engagement without editing").

---

## how this connects to other skills

**Feeds INTO this skill (use these first to find raw material):**
- **afiar-ideia**: Use the Murray Davis framework to sharpen the angle BEFORE writing the tweet. A boring angle can't be saved by structure.

**This skill feeds INTO:**
- **reaproveitar-conteudo**: Once a long-form tweet lands, repurpose it into LinkedIn, Instagram carousel, threads, etc. Don't write each one from scratch.
- **polir-texto**: Run the 9-filter editing pass on longer strategic posts before publishing.

**Mandatory partners:**
- **humanizar-texto**: Final filter on every tweet output. Non-negotiable.

---

## the test

Run every draft through these 7 pass/fail checks before delivering. One fail = rewrite.

1. **Passes the screenshot test** — Someone would screenshot this and send it to a friend. The insight is specific enough to be worth saving.
2. **Has a real opinion** — Not "AI is interesting" but a claim someone could argue against. If everyone agrees, it's not sharp enough.
3. **Sounds human on first read** — Zero sentences that make you pause and think "AI wrote this." No corporate rhythm, no rule-of-three, no em-dash chains, no hedge words.
4. **Follows one pattern** — Matches one of the 9 structures. Not a hybrid of three mashed together.
5. **Opens strong** — First line stops the scroll. No throat-clearing, no setup paragraph.
6. **Closes without flinching** — Ends on the point, a question, or nothing. Not "what do you think?" Not a motivational one-liner.
7. **Hits the right length** — Matches the pattern's natural range. A hot take at 1500 chars is bloated. An opportunity list at 300 chars is thin.

**Failure condition:** If the tweet reads like a LinkedIn post reformatted for Twitter — it failed. Do not ship. Do not deliver. Rewrite from the hook line down. The platform has its own energy. Respect it, or don't post.

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` next to this SKILL.md.

### At the start of every session
1. Read `feedback.log` in this skill's folder. Apply every rule to this session's output.
2. If it doesn't exist, create it with header: `# Longform Tweets Workshop — Learned Rules`

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
**How to apply:** [when this kicks in — which hook type, which format]
```

### What to log vs skip
**Log:** hook preferences, structural rules (line breaks, opener style), voice calibrations, emoji rules.
**Skip:** one-off tweaks to a specific tweet, preferences already in Context/voice.md.

### Cleanup every ~10 entries. Consolidate, delete reversed rules, keep under 100 lines.

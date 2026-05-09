---
name: lead-magnet
description: "Create lead magnet concepts that grow your list and convert to paid offers. Use when someone needs top-of-funnel ideas, wants to build their email list, or asks what freebie to create. Triggers on: lead magnet ideas for X, how do I build my list, what freebie should I create, top of funnel for X, opt-in ideas, grow my email list. Outputs 3-5 lead magnet concepts with angles, formats, and clear paths to the paid offer — and, when asked, the actual content inside the magnet."
---

# Lead Magnet Generator

Your prospect doesn't care about your freebie. They care about the problem eating at them right now. The best lead magnets solve that problem fast and leave them wanting the full solution you sell. Most lead magnets fail because they're built around what the seller wants to give away instead of step 1 of a journey toward what they actually sell.

This skill builds lead magnet concepts that pull their weight as the first chapter of the paid offer — and, when asked, drafts the actual content inside the magnet.

---

## the core job

Produce **3-5 distinct lead magnet concepts** the user can pick from, each with a clear angle, format choice, and connection to their paid product. When the user explicitly requests it, also produce the **full content** inside the chosen magnet (PDF body, quiz questions, challenge emails, checklist, etc.).

Every business has multiple valid approaches. The job is finding which one fits their audience, model, and offer best — then optionally executing on the chosen one.

**Output format — concept deliverable:**

| Element | What it covers |
|---------|---------------|
| Concept | What the lead magnet is, in one sentence |
| Format | Quiz, PDF, calculator, challenge, template, etc. |
| Angle | Why someone would hand over their email for this |
| Path to paid | How consuming this naturally leads to wanting the full offer |
| Build notes | Difficulty level and resources required |

**Output format — content deliverable (when requested):**

The actual lead magnet itself: title, intro/promise, full body content broken into named sections, and a soft CTA bridge to the paid offer.

---

## before starting: gather context

**STOP. Do not produce lead magnet concepts or content until context is in hand. Cap questions at 2 max.**

### Step A: Gather context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for:
   - **Business** — what the user sells, the paid offer the magnet bridges to.
   - **ICP** — audience pain, their phrases. The promise must solve a pain they have TODAY.
   - **Voice** — tone, do/don't. The magnet title and landing copy must sound like the user.
2. **If missing, check the project folder** for `Context/business.md`, `Context/icp.md`, `Context/voice.md`. Read whichever exist.
3. **If audience is still unclear after both:** ask inline — a lead magnet without an ICP is just a free PDF nobody wants.

### Step B: Confirm the brief (≤2 questions, combined)

Skip anything context already covers. Prioritize and combine into at most 2 questions:

1. **Paid offer + ICP's #1 pain** — "What's the paid offer this bridges to (product + price), and what's the #1 pain stopping the ICP today?" (combine)
2. **Business model + resources** — "Course/coaching, software, or service? And what can you actually build — quiz, video, PDF, calculator?" (combine)

**Identify the business model** — optimal formats shift by what they sell:

- **Courses, memberships, coaching:** quizzes, multi-day challenges, PDF frameworks, short video series, free chapters. See `references/course-creator-patterns.md`.
- **Software and tools:** free utilities, ROI calculators, templates that pair with the product, setup guides, free trials. See `references/software-patterns.md`.
- **Agencies, consultants, freelancers:** audits, diagnostic assessments, case studies, strategy calls, methodology templates. See `references/service-business-patterns.md`.

**Identify the transformation** — not the product. The change in the customer's life. What does their world look like AFTER? Which pain vanishes? What new ability appears? The lead magnet needs to deliver a BITE-SIZED version of that same shift.

**Identify the prospect:**
- Where are they right now?
- What have they already tried that didn't work?
- What do they currently believe about the problem?
- What would make them think "this is exactly what I was looking for"?

---

## the process

```
ground (context) → identify (gap) → bridge (paid path)
   ↓
form (format) → title (angle) → [draft (content)]?
   ↓
anti-slop pass → deliver
```

Steps in detail below. Steps 1-6 always run. Step 6 (draft) only runs when the user explicitly asks for the actual lead magnet content. Step 7 (anti-slop) is mandatory before any deliverable ships.

---

## ground: load context

Pull from CLAUDE.md and any `Context/` files listed above. If business + ICP context are missing from both, ask the user to paste them inline before continuing. Never invent an ICP — generic lead magnets convert at noise-floor rates.

**Anti-pattern:** Skipping this step "because the brief is obvious." It isn't. The brief tells you WHAT they sell. The context tells you HOW the user talks about it and WHO they're talking to.

---

## identify: spot the quick-win gap

Find the one problem the ICP has TODAY that a 30-minute freebie could plausibly solve. Not the deepest pain — the closest pain.

**Framework — the gap test:**
1. List 5 specific pains from `icp.md`
2. For each, ask: "Could a free piece of content fully resolve this in under 30 minutes of consumption?"
3. The "yes" answers are your quick-win candidates
4. Among those, pick the ones whose resolution naturally creates appetite for the deeper paid solution

**Example:** ICP is non-technical marketers stuck on Claude Code setup. Pains include: "don't know what to install," "afraid of the terminal," "no clue what to do once it's installed," "can't connect it to my marketing workflow." The first ("don't know what to install") is a perfect quick-win gap — solvable in a 10-step setup checklist, leaves them wanting workflow guidance (which the paid workshop teaches).

**Anti-pattern:** Picking the BIGGEST pain. The biggest pain is the paid offer's job. The lead magnet's job is the closest, smallest, most-solvable pain that proves you understand the bigger one.

---

## bridge: map freebie to paid offer

Before designing the magnet, map the path. The lead magnet is step 1 of N steps toward the paid thing. If you can't draw that line, the concept fails.

**The connection rule — the lead magnet must link logically to the paid offer.**

The strongest lead magnets function as "Step 1" of what you sell:
- Dog training program → Lead magnet: "The First 3 Commands" (the foundation taught in week one)
- Marketing agency → Lead magnet: Free mini-audit (preview of what the full audit uncovers)
- Productivity coach → Lead magnet: "The Morning Reset Worksheet" (taste of the coaching method)

The connection should be obvious: "If this free piece helped, the paid version goes deeper and further."

**Bridge formula:** [Lead magnet outcome] proves [skill/method] works → reader wants [next outcome] → paid offer delivers [next outcome] at [scope/depth].

**Anti-pattern:** A productivity coach giving away a recipe PDF. Audience interest mismatched to offer = wrong list.

---

## form: pick the format

Choose the format that fits the audience, the promise, and the user's build resources. Cite `references/format-guide.md` for full breakdowns including best-in-class examples per format.

**Quick reference — format strengths:**

| Format | Strongest for | Build effort |
|--------|---------------|--------------|
| Quiz / Assessment | Personalization, segmentation, transformation offers | Medium |
| PDF Guide / Framework | Authority, complex topics, depth | Low |
| Checklist / Template | Quick wins, immediate use, showing method | Low |
| Calculator / Tool | SaaS, financial services, ROI offers | Medium-High |
| Challenge (5-7 day) | Community, transformation, coaching | Medium |
| Video series / Mini-course | Teaching style demo, premium offers | Medium |
| Free Audit | Service businesses, agencies, consultants | Medium (per lead) |
| Swipe File / Resource Pack | Creative, marketing, education | Low |

**Format choice rules:**
- Match the format to the closest path to the paid offer (course → preview-style; SaaS → tool; agency → audit)
- Match the format to build capacity (no quiz tool → don't pitch a quiz)
- Match the format to the audience's preferred consumption mode

**Anti-pattern:** Defaulting to PDF for everything because it's easy. Easy to build is not the same as right for the audience.

---

## title: craft the promise

Every lead magnet needs an angle strong enough to earn an email address. Apply the **three rules** below, then run the title through one of the **angle formulas**. Cite `references/conversion-drivers.md` for the deeper psychology.

### the precision rule

**Narrow crushes broad. No exceptions.**

"The 3-Step System to Stop Your Dog from Pulling on Leash in One Weekend (Even If You've Tried Everything)" massively outperforms "Dog Training Tips."

Precision signals three things:
1. This was built for someone in my exact situation
2. The creator genuinely understands what I'm dealing with
3. This isn't recycled advice available on page one of Google

When building concepts, always sharpen:
- Specific outcome (not "train your dog" but "stop leash pulling in 48 hours")
- Specific timeframe (not "eventually" but "this weekend")
- Specific audience (not "pet owners" but "first-time puppy parents over 40")
- Specific method (not "training tips" but "The Calm Walk Protocol")

### the instant payoff rule

**Fix one specific problem completely.**

Prospects want value they can use RIGHT NOW. A lead magnet requiring weeks of study before anything happens feels like homework, not a gift.

Strong lead magnets produce immediate results:
- A checklist completable in 10 minutes that exposes gaps
- A template customizable in an hour for their situation
- An assessment delivering a score and action steps on the spot
- A calculator showing their personal numbers immediately

Instant results trigger reciprocity. When someone thinks "I couldn't have built this on my own," they're ready to value your paid offer.

### the worth formula

Rate every lead magnet concept on four dimensions:

**Worth = (Desired Result x Believability) / (Wait Time x Effort Required)**

Push up:
- **Desired Result** — What transformation does this promise?
- **Believability** — Why will THIS work when past attempts failed?

Push down:
- **Wait Time** — How soon do they see results? (Now beats next month)
- **Effort Required** — How easy to consume and act on? (5-minute checklist beats 50-page manual)

### angle formulas

| Angle type | Formula | Example |
|-----------|---------|---------|
| The Shortcut | "Get [outcome] without [usual pain/time]" | "Stop Barking in 3 Days Without Yelling or Shock Collars" |
| The Hidden Truth | "The [overlooked thing] that [impressive result]" | "The Socialization Mistake That Creates Aggressive Dogs" |
| The Named Method | "The [method name] for [specific outcome]" | "The Calm Walk Protocol: Loose Leash Walking in One Weekend" |
| The Number | "[X] [things] to [outcome]" | "7 Commands That Prevent 90% of Behavior Problems" |
| The Diagnostic | "Discover your [type/score/level]" | "What's Your Dog's Anxiety Score? Take the 2-Minute Assessment" |
| The Before/After | "How to go from [painful now] to [desired then]" | "From Reactive Mess to Calm Companion: The 30-Day Roadmap" |
| The Proof | "How [person/company] achieved [specific result]" | "How a 'Hopeless' Rescue Dog Passed CGC in 8 Weeks" |

**Anti-pattern:** Vague titles with "Ultimate Guide to X." Strip "Ultimate," "Complete," "Comprehensive," "Essential" — these signal generic. Replace with a specific outcome and timeframe.

---

## draft: write the actual content (when requested)

Run this step ONLY when the user explicitly asks for the lead magnet content itself (not just concepts). Otherwise stop after `deliver`.

**Drafting framework by format:**

- **PDF / framework:** intro (1 paragraph naming the problem and the promise) → 3-7 named sections, each with one specific tactic + one example + one micro-action → final page with bridge CTA to the paid offer
- **Checklist:** intro (problem + how to use the list) → grouped checkpoints with tight, scannable phrasing → "what to do next" CTA
- **Quiz:** 5-10 questions with 3-4 answers each → scoring logic mapped to outcome types → personalized result page that names the type, lists the 3 priorities for that type, and offers the paid next step
- **Challenge (5-7 day):** day 0 welcome (set expectation + first task) → daily emails (one task per day, ~300-500 words) → final day delivers visible result + CTA to paid offer
- **Calculator:** input prompts (5-10 fields max) → output number + interpretation → "if this number alarms you, here's the next step" CTA
- **Video / mini-course:** 3-5 short videos (under 8 min each), each teaching one concept fully → final video previews the paid offer

**Content rules (apply to all formats):**
1. Open with the pain in the ICP's words (lift from `icp.md`)
2. Deliver the promised outcome inside the magnet — no upsell-blocked content
3. Show the method, not just the result — proof of teaching style is what converts
4. Soft CTA at the end: "If [next outcome] is what you need, [paid offer] is the next step"
5. Voice = the user's voice from `voice.md`. Read it before drafting a single sentence.

**Anti-pattern:** Withholding the actual value to "make them buy the paid version." The lead magnet must deliver completely on its narrow promise. The paid offer earns the sale by being deeper, not by being the only place value lives.

---

## anti-slop: mandatory pass

Before showing any lead magnet title, landing copy, or lead magnet content to the user, run it through the `anti-slop` skill.

**Why this skill especially:** Lead magnet copy is prone to "ultimate guide" slop — generic titles, inflated value claims, authenticity theater.

**How:** Invoke `anti-slop` with the full draft as input — titles, subheads, landing page promise, and body content.

**If `anti-slop` is not available,** scan manually for: "ultimate" / "complete" / "comprehensive" / "essential" in titles, robot phrases (game-changer, unlock, leverage), generic claims with no specifics, forced threes in bullet lists, rhetorical questions ("Want to know the secret?"), AI transitions ("Here's the thing...").

Rewrite anything flagged. Non-negotiable: no lead magnet ships without this pass.

---

## deliver: present the output

Use the templates below. Always show all 3-5 concepts in the table format, then add a "recommended first move" with reasoning. If content was drafted, attach it after the concepts section under a clear `## Lead Magnet Content` header.

---

## output format

### Lead Magnet Concepts for [Product/Offer]

**Concept 1: [Name]**

| Element | Detail |
|---------|--------|
| Concept | [One sentence description] |
| Format | [Quiz/PDF/Calculator/Challenge/etc.] |
| Angle | "[The headline/promise]" |
| Path to paid | [How this leads to the paid offer] |
| Build notes | [Difficulty + what's needed] |

**Concept 2: [Name]**

| Element | Detail |
|---------|--------|
| Concept | [One sentence description] |
| Format | [Quiz/PDF/Calculator/Challenge/etc.] |
| Angle | "[The headline/promise]" |
| Path to paid | [How this leads to the paid offer] |
| Build notes | [Difficulty + what's needed] |

[Continue for 3-5 total concepts]

**Recommended first move:** [Which concept to test first and the reasoning behind it]

---

### Lead Magnet Content (only when requested)

**Title:** [Final title from the title step]

**Promise (one paragraph):** [What the reader gets and by when, in their language]

**Outline:**
1. [Section 1 name] — [one-line description]
2. [Section 2 name] — [one-line description]
3. [Section 3 name] — [one-line description]
4. [Section 4 name] — [one-line description]
5. [Section 5 name] — [one-line description]

**Body:** [Full drafted content per outline, formatted for the chosen format — PDF prose, quiz Qs+scoring, daily challenge emails, etc.]

**Bridge CTA:** [The exact closing copy that points to the paid offer]

---

## example: $297 Claude Code workshop for non-technical marketers

### context
- **Product:** $297 live Claude Code workshop (workshop-only $99, with 2x 1:1 calls $297)
- **Transformation:** Non-technical marketer goes from "tried Claude Code, got stuck, feels behind" to "Claude Code installed, configured for marketing, produced something real in 90 minutes"
- **Audience:** Non-technical marketers who saw the hype, attempted setup, hit a wall, now feel FOMO
- **Acute pain TODAY:** Don't know what to install or configure first; terrified of the terminal; assume everyone else "gets it"

### lead magnet concepts

**Concept 1: The Non-Coder's Claude Code Setup Checklist**

| Element | Detail |
|---------|--------|
| Concept | One-page printable checklist of the exact 10 steps to install and configure Claude Code if you've never touched a terminal |
| Format | PDF checklist |
| Angle | "Install Claude Code in 20 Minutes (Even If You've Never Opened a Terminal)" |
| Path to paid | Setup proves they can do the easy part. Workshop teaches them what to actually USE it for in marketing — the part the checklist deliberately doesn't touch. |
| Build notes | Low — write + Canva design |

**Concept 2: What's Your AI Marketing Block? (2-Minute Quiz)**

| Element | Detail |
|---------|--------|
| Concept | Quiz that diagnoses why the user is stuck with AI tools — wrong tool, wrong workflow, wrong skill, or wrong mindset — and recommends the next step |
| Format | Quiz with branched results |
| Angle | "Why You're Stuck With AI (And What to Do About It): The 2-Minute Diagnostic" |
| Path to paid | Most results funnel toward "you need a guided setup + workflow" — which is exactly the workshop |
| Build notes | Medium — Typeform or ScoreApp, branching logic, 4 result pages |

**Concept 3: 5 Claude Code Recipes for Marketers (Steal These)**

| Element | Detail |
|---------|--------|
| Concept | PDF with 5 ready-to-paste prompt+skill combos for common marketing tasks (newsletter draft, repurposing, ICP research, landing page, email sequence) |
| Format | Swipe file PDF |
| Angle | "5 Claude Code Recipes That Replace Your Most Painful Marketing Tasks (Copy-Paste Ready)" |
| Path to paid | Recipes prove the workflow works. Workshop installs Claude Code AND walks through customizing recipes live. |
| Build notes | Low-Medium — write 5 recipes + design |

**Concept 4: The 5-Day Claude Code for Marketers Challenge**

| Element | Detail |
|---------|--------|
| Concept | One email per day for 5 days; each delivers a tiny win (day 1 install, day 2 first prompt, day 3 first skill, day 4 first workflow, day 5 first published piece) |
| Format | Email challenge |
| Angle | "5 Days to Your First Claude Code Marketing Win (One Email a Day)" |
| Path to paid | Day 5 email demonstrates the gap between scrappy DIY and a configured system → workshop offer |
| Build notes | Medium — 5 emails + ESP automation + supporting screenshots |

**Concept 5: The "Am I Behind on AI?" Marketing Audit**

| Element | Detail |
|---------|--------|
| Concept | 15-question self-audit that scores the user's current AI maturity for marketing tasks and gives a personalized 30-day path |
| Format | Self-audit PDF + scoring sheet |
| Angle | "How Far Behind Are You on AI for Marketing? Score Yourself in 5 Minutes" |
| Path to paid | Most readers score lower than they expect. The 30-day path's first milestone is "set up Claude Code properly" — which is the workshop. |
| Build notes | Low — design a scoring grid + interpretation page |

**Recommended first move:** Concept 1 (Setup Checklist). It directly removes the #1 blocker the waitlist named (overwhelm at setup), is fastest to ship, and leaves a clean, obvious gap for the workshop to fill (what to USE Claude Code for once it's running).

### chosen concept fully built — Concept 1

**Title:** Install Claude Code in 20 Minutes (Even If You've Never Opened a Terminal)

**Promise:** A printable, no-jargon checklist that walks a non-technical marketer through installing and configuring Claude Code — every command spelled out, every "you'll see this screen" warning included, every common error pre-debugged. By the end, you'll have Claude Code running and a single test prompt working. You will not have to Google a single error.

**Outline:**
1. **Before you start (5 min)** — accounts you need, what to download, why this is easier than it looks
2. **The actual install (8 min)** — exact commands, copy-paste ready, with screenshots of what success looks like
3. **First-run configuration (4 min)** — minimum settings to make it usable for marketing work
4. **Your first test prompt (2 min)** — paste this exact prompt to confirm it works
5. **What to do next** — the 3 things that turn an install into a workflow

**Body:** Each section follows the pattern: "What you're doing" → "Exact steps" → "What you'll see" → "If it breaks, do this." Every command in monospaced blocks. Every screenshot annotated. No paragraph longer than 4 lines. Final page is the bridge.

**Bridge CTA:**
"You've installed Claude Code. Most people stop here. The hard part isn't the install — it's knowing what to actually USE it for in your marketing without it becoming another tool you abandon in two weeks. That's what the live workshop does. Same setup you just did, then 90 minutes of configuring it for newsletters, repurposing, and ICP research with skills I use daily. [Workshop link]."

---

## how this connects to other skills

- **Feeds from:** ICP research / business interview skills. The lead magnet only works if `icp.md` and `business.md` are populated.
- **Feeds into:** `landing-page` — the chosen concept becomes the offer on the opt-in page. `sequencia-email` — the chosen concept becomes the deliverable in the welcome email + the bridge to the nurture sequence.
- **Pairs with:** `vibe2-positioning-angles` if the angle isn't landing. `humanizar-texto` runs as the mandatory final pass before delivery.
- **Triggered by:** `landing-page` when it needs a lead magnet offer to reference. `sequencia-email` when it needs a lead magnet to deliver in the welcome path.

---

## the test

Before delivering, every concept must pass these checks:

1. **Precision** — Is the promise sharp and specific? Vague lead magnets ("Marketing Tips") fail.
2. **Complete quick win** — Does it solve one problem fully in under 30 minutes of consumption? Not a teaser — genuine value.
3. **Clear connection** — Can you trace a straight line from consuming this to wanting the paid offer? If not, the magnet attracts the wrong list.
4. **Real desire** — Would the target audience actually want this RIGHT NOW? Not "should want." WANT.
5. **Buildable** — Does the implementation difficulty match the user's available resources?
6. **Voice match** — Does the title sound like the user, per `voice.md`? No "ultimate guide" slop.
7. **Anti-slop pass complete** — Did the `anti-slop` skill run on the final draft?

**Failure condition:** If any concept fails two or more checks, rework it before including it. If the chosen-and-drafted concept fails the anti-slop pass, do not deliver — rewrite and re-test.

---

## references

Deeper frameworks organized by business type in the `references/` folder:
- [format-guide.md](references/format-guide.md) — Best-in-class examples sorted by format
- [course-creator-patterns.md](references/course-creator-patterns.md) — Strategies from Brunson, Porterfield, and top course creators
- [software-patterns.md](references/software-patterns.md) — HubSpot, Ahrefs, and SaaS-specific approaches
- [service-business-patterns.md](references/service-business-patterns.md) — Agency and consulting lead magnet playbooks
- [conversion-drivers.md](references/conversion-drivers.md) — The psychology behind why lead magnets convert

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` next to this SKILL.md.

### At the start of every session
1. Read `feedback.log` in this skill's folder. Apply every rule.
2. If it doesn't exist, create it with header: `# Lead Magnet Workshop — Learned Rules`

### Triggers that require a log write

When the user says any of the following, immediately append a rule:
- "Don't suggest X format anymore" / "Stop pitching PDF guides"
- "Always connect to Y offer" / "From now on, prioritize Y"
- "I hate when you..." / "Too generic"
- "That's perfect, keep doing that"
- Silent rewrites where the user tightens the promise — infer the rule

### Format for each rule
```
## YYYY-MM-DD — [short title]
**Rule:** [imperative sentence]
**Why:** [reason]
**How to apply:** [when this kicks in — which lead magnet type, which audience]
```

### What to log vs skip
**Log:** format preferences (video > PDF for this ICP), bridge rules, title calibration, promise specificity.
**Skip:** one-off edits to a specific piece — not a rule.

### Cleanup every ~10 entries.

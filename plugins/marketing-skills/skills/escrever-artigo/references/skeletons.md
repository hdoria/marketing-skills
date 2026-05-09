# Skeletons — Tutorial and Breakdown

Detailed structure for both article types. Load during Step 3 (filling the body).

---

## Skeleton A: The Tutorial

Use when the article is "here's how to set up / build / do this exact thing."

### Full structure

```
1. Hook (2-4 sentences)
2. Why it matters
3. What it does (overview of the system/workflow)
4. What the output looks like (show a real example)
5. How to use it (the workflow once it's set up)
6. How to set it up (exact numbered steps with copy-paste)
7. Closer (direct instruction)
```

### Section-by-section rules

#### 1. Hook (2-4 sentences)

Covered in SKILL.md Step 2. Most effective for tutorials: **personal result + timeframe**.

> "I set up [TOOL/METHOD] [TIMEFRAME] and [CONCRETE RESULT]."

Follow-up sentence shows what changed.

> "My [THING] went from [BEFORE] to [AFTER]. With [CONSTRAINT, e.g. 'zero manual work']."

#### 2. Why it matters

One paragraph. The problem this solves, made concrete.

**Pattern:**
- Name the pain in a specific, recognizable way
- Anchor it in a real scenario (not "many people struggle with X")
- Land on what changes if the reader fixes it

**Example shape:**
> Most of your [skills/prompts/workflows] work most of the time. But when they fail, they fail silently — you ship the output, your audience sees it, and you never know why it didn't land. This fixes that.

#### 3. What it does

2-4 sentences. The plain-English description of the thing.

**Pattern:**
- One sentence stating the mechanism
- One sentence stating what the user does vs what the system does
- One sentence naming the inputs and outputs

**Example shape:**
> [Method] runs [thing] over and over and keeps changes that improved it. You give it a starting point and a rubric. It handles the rest.

#### 4. What the output looks like

Show the actual end result. Readers don't trust descriptions of output — they trust seeing it.

Options:
- Paste a real before/after
- Screenshot a dashboard
- Quote a real piece of output with context

**Example shape:**
> Here's what mine produced on its 40th run:
> 
> ```
> [Real output, not a summary]
> ```
> 
> [One line framing what to notice about it.]

#### 5. How to use it

For tools/systems where setup is separate from use, describe daily use BEFORE setup. Readers want to know what life looks like after, not what the install commands are.

**Pattern:**
- 3-5 sentences
- Present tense ("I open X, paste Y, watch Z")
- End by teasing the setup: "Setup takes [TIME]. Here's exactly how."

#### 6. How to set it up (the meat)

Numbered steps. Imperative verbs. Copy-paste blocks.

**Step format:**

```
[N]. [Short action title]

[1-3 sentences: what to do and why]

[Code block with the exact command/prompt, if applicable]

[Optional: anticipate where people get stuck, fix inline]
```

**Rules:**
- Every step starts with an imperative verb (Open, Click, Copy, Paste, Type, Tell, Set, Run)
- Keep explanation to 1-3 sentences
- Put copy-paste content immediately after the explanation
- If a step involves UI, describe what the button or icon looks like ("click the gear icon in the top-right")
- If a step commonly breaks, add the fix inline: "If X happens, try Y"

**Step count:** 5-10 steps is the sweet spot. Under 5 feels thin. Over 10 feels overwhelming — consider whether some steps can combine.

#### 7. Closer

Covered in SKILL.md Step 5. For tutorials, the closer points at the tool they just learned:

> "Go set it up right now while it's fresh. [CONCRETE TIMEFRAME — e.g. '15 minutes and you're running'] and you'll wonder how you worked before."

---

## Skeleton B: The Breakdown

Use when the article is "here's what changed (news/update) and what to do about it."

### Full structure

```
1. Hook (2-4 sentences): News + gap
2. Problem 1 (what's new → how it works → what to do with results)
3. Problem 2 (same structure)
4. Problem 3 (same structure — optional, if the news has 3+ angles)
5. How to get started (quick setup steps)
6. Closer (direct instruction)
```

### Section-by-section rules

#### 1. Hook — News + gap

For breakdowns, the hook pattern is:

> "[PRODUCT/FEATURE] just dropped and most people missed [SPECIFIC THING]."

Follow-up line makes the gap concrete.

> "Here's what it actually does and the 3 workflows I'm running on it this week."

#### 2-4. Problem sections (the core)

Each problem is a self-contained unit with 4 parts:

```
## [Short title — sounds like something you'd say out loud]

[What's new — 2-3 sentences describing the specific capability]

[How it works — 3-5 numbered steps OR a paragraph if no steps needed]

[What to do with the results — 2-4 sentences connecting the capability to the reader's actual work]
```

**Rules:**
- Use 2-3 "problem sections" total, not 5+
- Each section should stand alone — a reader who only reads Section 2 should still get value
- "What to do with the results" is where the article earns its keep. Don't skip it to get to the next section faster.

#### 5. How to get started

Short. Usually 3-5 numbered steps that get the reader from zero to running the first of the capabilities described above.

Often simpler than the tutorial skeleton's setup section because each "problem section" already has its own how-it-works mini-steps.

#### 6. Closer

For breakdowns, the closer points at action, not at the tool:

> "Pick one of the three above and try it today. [ONE-SENTENCE PAYOFF]."

---

## Section headers (both skeletons)

Short. Conversational. Sound like something you'd say out loud to a friend.

**Good headers:**
- "What my task does"
- "How to set it up (exact steps)"
- "Where this comes from"
- "What happened to my landing page skill"
- "This works on way more than skills"
- "Go run it"

**Bad headers (don't use):**
- "Step-by-Step Implementation Guide"
- "Understanding the Output Format"
- "Introduction to the Methodology"
- "Conclusion"

Test: if the header could appear unchanged in a corporate whitepaper, rewrite it.

---

## Micro-examples — section shapes

### Example hook + "why it matters" pair (Tutorial)

> I set up a daily metrics dashboard 3 weeks ago and it replaced the 45 minutes I used to spend every Monday pulling numbers from 6 different tools.
> 
> Now I drink my coffee and read one page.
> 
> Here's exactly how I built it.
> 
> **Why it matters**
> 
> Most founders I know spend 2-4 hours a week reconciling numbers across tools. That time isn't replaced with strategic thinking — it's just lost. Building the dashboard pays itself back in the first week, and every week after is free.

### Example "what it does" + "what the output looks like" pair

> **What my dashboard does**
> 
> It pulls my 7 most-used metrics from Stripe, PostHog, Beehiiv, and Google Analytics every morning at 8am. Runs them through a small Python script. Drops a formatted summary into a Notion page I keep pinned.
> 
> I set the metrics once. The script handles everything after.
> 
> **What the output looks like**
> 
> Here's yesterday's:
> 
> ```
> MRR:             $14,230 (+$340 WoW, +2.4%)
> New trials:      47 (-8 WoW)
> Trial-to-paid:   6.2% (7-day rolling)
> Newsletter:      +218 subs this week
> Top post:        "Autoresearch for skills" — 14.2k views
> ```
> 
> That's the whole thing. 6 numbers I actually use, zero fluff.

### Example numbered step with copy-paste

> **3. Paste this into the script config**
> 
> This tells the script which metrics to pull from each tool. Swap the bracketed placeholders for your own IDs.
> 
> ```
> metrics = {
>   "stripe_mrr": "[YOUR_STRIPE_ACCOUNT_ID]",
>   "posthog_events": ["trial_started", "payment_completed"],
>   "beehiiv_list_id": "[YOUR_LIST_ID]",
>   "ga_property_id": "[YOUR_GA4_PROPERTY]"
> }
> ```
> 
> If you don't have the account IDs handy, each tool has them in Settings → API. Takes 30 seconds.

---

## Common failure shapes (specific to article structure)

These are structural problems (not voice problems — those live in voice-rules.md).

1. **Tutorial with no "what the output looks like" section.** Steps make no sense if the reader can't picture where they're going. Always include the example before the steps.

2. **Breakdown with 5 problem sections.** Readers lose the thread after 3. If the update has more than 3 angles, pick the 3 most useful and cut the rest. The article can be "part 1 of 2" if the content really justifies it.

3. **Step list with no copy-paste.** A "how to" section with prose-only steps and no code blocks reads like a summary, not a walkthrough. Find one thing to put in a code block even if it's just a template prompt.

4. **"Why it matters" that restates the hook.** The hook says what the thing is. "Why it matters" says why the reader should care specifically. If they overlap, the "Why it matters" is dead weight — cut it or rewrite.

5. **Closer that summarizes.** This is the most common failure in the entire skeleton. Summaries kill the momentum the steps built up. The closer is a push, not a recap.

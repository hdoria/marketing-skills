# Interview Question Bank

The full question library for the 8-step interview. Primary questions (ask these first), probe-deeper follow-ups (ask when the first answer is too shallow), and "what to listen for" notes.

Load this during the interview whenever you need a sharper question than the ones in SKILL.md.

---

## Table of contents

1. [Step 1: Scope](#step-1-scope)
2. [Step 2: Sequence](#step-2-sequence)
3. [Step 3: Decisions](#step-3-decisions)
4. [Step 4: Tools and artifacts](#step-4-tools-and-artifacts)
5. [Step 5: Quality checks](#step-5-quality-checks)
6. [Step 6: Failure modes](#step-6-failure-modes)
7. [Step 7: Template](#step-7-template)
8. [Step 8: Package](#step-8-package)

---

## Step 1: Scope

### Primary questions

- In one sentence, what does this workflow do?
- What makes you start this workflow? A request from someone, a recurring calendar item, a moment in your day?
- What does "done" look like? Describe the final artifact or action.
- Who will use the skill — just you, or teammates too?

### Probe deeper when

- **User gives a category, not a task.** If they say "it helps with marketing" or "it does research," ask: "What's the most common version of that you actually do week to week?"
- **Scope is too broad.** If the answer could fit three different workflows, pick one: "Which one should the skill do? We can build the other two later."
- **The trigger is vague.** "When I feel like it" isn't a trigger. Ask: "Last time you did this, what was happening right before you started?"
- **"Done" is hand-wavy.** Ask: "If someone else did this task for you, what would they hand back? A doc? A spreadsheet? A Slack message?"

### What to listen for

- The trigger phrase — this is what goes in the `description` field under "Triggers on."
- The deliverable format — this drives the output template in Step 7.
- Any mention of frequency ("every Monday," "after each launch") — that's a reliable trigger.

### Ask if still unclear after probes

- Walk me through the last 3 times you did this. Were they all the same kind of task, or different?
- Do you have a name for this workflow, even an internal nickname?

---

## Step 2: Sequence

### Primary questions

- Walk me through the last time you did this — step by step, start to finish.
- At any point do you go back and redo something?
- How long does each step take, roughly?

### Probe deeper when

- **User gives labels instead of actions.** "First I research the audience" is a label, not an action. Ask: "What exactly do you do when you research them? What do you open? What do you look at? What do you write down?"
- **Steps jump.** If the user goes from "I start" to "I have a draft," ask: "What happened between those two moments? Walk me through the middle."
- **Step boundaries are fuzzy.** Ask: "How do you know you're done with step 1 and ready for step 2?"

### What to listen for

- **Verbs.** "Open," "write," "compare," "paste," "check." These are the real steps. Nouns and adjectives are labels.
- **Loops.** If the user goes back to earlier steps, that's a loop — important for Step 3 (decisions) and the final process diagram.
- **Batch markers.** Does the user do step 2 for all items before moving to step 3, or step 2 → step 3 → step 2 → step 3? This changes how the skill executes.

### Probe patterns

| When user says... | Ask... |
|-------------------|--------|
| "I do some research" | "On what? For how long? Where do you save it?" |
| "I draft it" | "Do you start from a blank page or a template? What's the first sentence usually?" |
| "I review it" | "What do you actually look for when you review?" |
| "I polish it" | "What does polishing mean — typo fixes, restructuring, adding sections?" |

### Ask if still unclear

- If I were watching you do this over your shoulder, what would I see you clicking, typing, copying?
- What's the messiest part? Where do you get stuck most often?

---

## Step 3: Decisions

### Primary questions

- Where in the sequence do you have to make a judgment call?
- What are the criteria? What tells you "this is a yes" vs "this is a no"?
- What changes downstream based on that decision?

### Probe deeper when

- **User says "I just know."** Every time. Ask: "When you 'just know,' what are you reacting to? What in the input tells you?" Keep digging until you hit a concrete signal.
- **User describes one path, not a branch.** Ask: "Has it ever gone the other way? What was different that time?"
- **The decision is implicit in the workflow.** If they say "then I write the short version," ask: "When do you write the short version vs the long version?"

### What to listen for

- **If/then rules.** "If the audience is cold, I start with a story. If they've bought before, I skip to the offer." These go into decision tables.
- **Thresholds.** "If the conversion rate is under 2%, I rewrite from scratch." Capture the number.
- **Defaults.** "By default I do X, unless Y is true." Defaults are your friend — they let the skill act without a decision.

### Probe patterns

| User says... | Ask... |
|--------------|--------|
| "I decide if it's worth doing" | "What makes it worth doing? What are the signals?" |
| "It depends" | "On what? Give me 2-3 real examples and what you picked each time." |
| "I use my judgment" | "You used your judgment last Tuesday — what were you actually weighing?" |
| "It's obvious" | "It's obvious to you. Pretend I've never done this. What tells me?" |

### Ask if still unclear

- Can you think of a time when you changed your mind halfway through? What flipped it?
- If a new hire were doing this, where would they get stuck first?

---

## Step 4: Tools and artifacts

### Primary questions

- What tools do you open during this workflow? (files, apps, tabs, docs, sheets, URLs)
- Do you reuse any templates, checklists, or reference docs?
- Are there any scripts or automations you rely on — even small ones?

### Probe deeper when

- **User names a tool but not how they use it.** "I use Notion" → "What specifically do you open in Notion? A specific doc? A database view? A template?"
- **User doesn't mention templates but clearly uses them.** If their process looks repeatable but they claim to "just write it," ask: "Do you start from a blank page, or do you usually have a structure in mind? Where does that structure come from?"
- **User runs commands or scripts offhandedly.** "Oh I just run the ingest script" → "What's the command? What does it do? Where does it live?"

### What to listen for

- **Reusable reference docs** — these become `references/[name].md` files inside the skill folder.
- **Scripts/commands** — these become `scripts/[name].sh` or `.py` files.
- **Templates** — these go directly into the `output format` section of the skill, verbatim when rigid.
- **URLs the user keeps opening** — may be documentation worth linking to, or data sources worth fetching automatically.

### Probe patterns

| User says... | Ask... |
|--------------|--------|
| "I check the analytics" | "Which dashboard? What metrics do you look at in order?" |
| "I grab the template" | "Where does it live? Can you share it? I want to include it in the skill." |
| "I usually just copy from last time" | "Last time's output is your de facto template. Can I see it?" |

### Ask if still unclear

- If I wiped your laptop and gave you a blank one, what's the first file or tool you'd recreate to do this task?
- Is there a doc you keep open in a tab the whole time you're doing this?

---

## Step 5: Quality checks

### Primary questions

- Before you send/publish/commit the output, what do you check?
- What would make you throw out a draft and start over?
- Are there specific numbers or markers you look for?

### Probe deeper when

- **User says "it just has to be good."** Ask: "Last time you rejected a draft, what was wrong with it? Specifically."
- **Checks are all subjective.** If every check is a vibe ("it should feel right"), ask: "What's one thing you could point to on the page that proves it's good or bad?"
- **User under-reports checks.** People often do 5-10 quality checks without realizing it. Probe for: "Do you read it out loud? Do you check formatting? Do you verify numbers? Do you look at it on mobile?"

### What to listen for

- **Verifiable checks** — "word count is under 200," "headline includes a specific number," "first sentence doesn't start with 'In today's...'" — these go directly into the "the test" section.
- **Deal-breakers** — things that force a rewrite. These belong in the failure condition at the end of "the test."
- **Reference outputs** — if the user compares against a past "good version," that past version is the gold-standard example.

### Ask if still unclear

- Describe a recent output you were proud of. What made it good?
- Describe a recent output you were embarrassed by. What was wrong with it?

---

## Step 6: Failure modes

### Primary questions

- What are the 3-5 most common mistakes people make when doing this?
- Have you caught yourself making any of them recently? What was the tell?
- Anything Claude or an AI would probably get wrong by default?

### Probe deeper when

- **User struggles to name mistakes.** Ask about drafts that got rejected, clients who complained, or output they later regretted publishing.
- **Mistakes are too vague.** "Sometimes it sounds off" → "What specifically sounds off? Word choice? Structure? Tone?"
- **User blames themselves instead of the process.** "I was rushing" isn't a failure mode. "Skipping the quality check under deadline pressure" is.

### What to listen for

- **AI-specific failure modes.** "It always adds a conclusion paragraph I didn't ask for" — exactly the kind of thing to warn against in the gotchas.
- **Workflow drift.** Places where the user's own process breaks down — often the same places Claude will.
- **Fabrication risks.** Numbers, names, testimonials, dates — any content Claude might invent if it's missing from context.

### Ask if still unclear

- What's the thing that goes wrong when you rush?
- If you had to train a new hire on this, what would you warn them about first?

---

## Step 7: Template

### Primary questions

- What sections does the final output have, in order?
- Is there a fill-in-the-blank structure you reuse? (If yes, paste it.)
- How strict is the format — rigid template, or flexible guide?

### Probe deeper when

- **User says "it varies every time."** Ask: "Compare the last 3 outputs. Do they have any of the same sections? Headings? Opening lines?"
- **Template exists but isn't explicit.** If every output has the same shape, capture that shape even if the user doesn't call it a template.
- **Rigid format but user says flexible.** Look at sample outputs. If they all hit the same beats, the format is rigid — just not labeled.

### What to listen for

- **Placeholders** — the parts that change every time. These become `[PLACEHOLDER]` markers in the template.
- **Fixed sections** — headers, signoffs, boilerplate that appears every time.
- **Order** — Claude follows order literally. Capture the sequence exactly.

---

## Step 8: Package

Not many questions here — this step is mostly assembly. But do ask:

### Primary questions

- Where should I save the skill? (Default: `~/.claude/skills/[skill-name]/`)
- What should we call it? (Default: derive from the one-sentence job description)
- Do you want to test it on a real task right now? (Optional, but helps catch obvious gaps.)

### What to listen for

- **The user hesitating on the name.** A good skill name reads like a slash command — short, specific, unambiguous. If the user is torn between two names, offer both, let them pick.
- **A desire to test immediately.** If the user wants to run the skill on real input right now, do it. Feedback from one real use is worth three hypothetical reviews.

---

## General probing principles

Four patterns that work across every step of the interview:

1. **"Walk me through the last time you did X."** Concrete beats abstract. Recent beats hypothetical. The most recent real instance is usually the richest source of workflow detail.

2. **"What do you actually do when you do that?"** Whenever the user gives a label ("research," "draft," "review"), translate it into actions by asking this question. Repeat until you hit verbs.

3. **"What's the signal?"** Whenever the user says "I just know" or "I use my judgment," ask what they're reacting to. There's always a signal. Keep digging.

4. **"What would a new hire get wrong?"** Excellent way to surface both decisions (Step 3) and failure modes (Step 6). Users who can't see their own judgment can often see a hypothetical new hire stumbling over it.

---

## When to stop probing

Not every answer needs to be drilled into. Stop probing when:

- The answer is concrete enough that Claude could execute it. ("Open the sales dashboard, filter by last 7 days, copy the top 3 metrics into the template" = done.)
- Further detail would be overfit to this specific instance and wouldn't generalize.
- The user is getting fatigued — interview energy matters. Better to ship a good draft and iterate than to extract a "perfect" workflow they never want to revisit.

Budget roughly 30-45 minutes for a first-pass interview. Longer than that and the returns diminish fast.

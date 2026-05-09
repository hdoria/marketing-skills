# Reference Article — High-Performing Case Study

A real X/Twitter article that hit 1.2M views. Studied here as a **structural case study**, not a voice template.

**Important:** Pull structural patterns from this article (concept-first order, stacked analogies, origin story, results section). Do NOT copy phrasing, rhythm, or voice. Voice comes from the user's CLAUDE.md. Copying this article's voice produces output that sounds like the original creator, not the user.

---

## Patterns to replicate

Eight patterns that drove the performance. These generalize to any X article; the voice around them is specific to the original creator.

### 1. Concept-first structure

The actual tutorial steps don't appear until ~60% through the article. The first half teaches the concept so clearly (through analogies) that the steps feel obvious by the time the reader arrives at them.

**Why it works:** Readers who don't understand the concept skim the steps and bounce. Readers who understand the concept read every step. Teaching first grows the audience that sticks.

**When to use:** Any article explaining a non-obvious method. Skip this pattern for articles about well-known tools (e.g., "how to set up Gmail filters") — readers already have the concept.

### 2. Stacked analogies as teaching engine

Two extended analogies, each building on the last. Paragraph-length, not one-clause. The analogies carry the entire conceptual weight — readers understand the method through the analogies before any real-world details.

**Analogy 1 (the recipe):** "You have a recipe that turns out great 7 out of 10 times. Change one ingredient, cook it 10 times, keep or revert..."

**Analogy 2 (the teacher grading):** "A teacher grading papers with a checklist. Pass or fail per item. Consistent across 100 papers..."

**Why it works:** Different readers connect to different analogies. Stacking two catches more of the audience.

**When to use:** Any article explaining a method with more than 2 conceptual moving parts.

### 3. Origin story section

A "Where this comes from" section that credits the source, explains the original context, then bridges to the writer's adaptation: "I took his method and turned it into..."

**Why it works:** Establishes credibility without fabricating expertise. Positions the writer as a curator/adapter, not an inventor. Readers trust people who credit sources.

**When to use:** Any time the article's method is adapted from someone else's work. If the method is original, skip this section.

### 4. "What happened to my X" results section

Not just numbers. A breakdown of:
- The specific before/after metric (56% → 92%)
- How many rounds (4)
- What was tried (3 kept, 1 undone)
- The agent's actual changes, listed concretely

Real numbers + specifics of what was kept and what was reverted make the result believable. Round numbers without specifics read as fabricated; specific counts like "3 kept, 1 undone" read as real.

**Why it works:** Readers are used to marketing numbers being directional or inflated. The specificity of "1 undone" ("why would they mention this if it wasn't real?") earns trust.

**When to use:** Any tutorial where the writer has actually run the method on their own work. If you don't have real numbers, skip this section rather than inventing them.

### 5. "This works on way more than X" expansion

After the specific use case, broaden to 3-4 other applications. Each gets a concrete example (specific number, specific metric).

**Why it works:** Reader finishes the article thinking "I could use this for 5 things" instead of one. Expands the article's applicability without diluting the central teaching.

**When to use:** Any tutorial where the method generalizes beyond the specific case shown. If the method is narrow, skip this.

### 6. Early P.S. CTA placement

First CTA appears right after the hook — catches readers who are already sold and want more content. Second CTA at the very end — catches readers who went all the way through.

**Why it works:** Different segments of readers convert at different points. Two placements catches both.

**When to use:** Any article over 800 words. Shorter articles, one CTA at the end is enough.

### 7. Bullets with decision logic

> Did it get better? Keep the change.
> Did it get worse? Put the old ingredient back.

Bullets carry if/then decisions, not just feature lists. This makes abstract methods feel executable.

**Why it works:** Readers imagine running the method themselves when they can see the decision gates. Feature-list bullets ("fast, easy, accurate") don't do this.

**When to use:** Any section explaining a process with choice points. Not for sections listing static facts.

### 8. Specific contrast examples inline

When explaining a quality criterion, show the bad output it catches in parentheses:

> "Does the headline include a specific number or result?" (catches vague headlines like "Grow Your Business")

**Why it works:** Abstract criteria ("must be specific") are forgettable. Concrete before/after pairs are memorable. The parenthetical shows exactly what the criterion filters out.

**When to use:** Any checklist, rubric, or list of quality criteria.

---

## Full article text (for structural study only)

Read the article below with the patterns above in mind. Notice where each pattern appears and how it's executed. Do not copy the voice.

> **How to 10x your Claude Skills (using Karpathy's autoresearch method)**
> 
> Your Claude skills probably fail 30% of the time and you don't even notice.
> 
> I built a method that auto-improves any skill on autopilot, and in this article I'm going to show you exactly how to run it yourself.
> 
> You kick it off, and the agent tests and refines the skill over and over without you touching anything.
> 
> My landing page copy skill went from passing its quality checks 56% of the time to 92%. With zero manual work at all.
> 
> The agent just kept testing and tightening the prompt on its own.
> 
> Here's the method and the exact skill I built so you can run it on your own stuff:
> 
> **P.S.** If you want more AI workflows like this one delivered to your inbox every week, join [X] readers getting them free: `[NEWSLETTER URL]`
> 
> **Where this comes from**
> 
> [Source name] (co-founder of [org], former [role], who coined "[term]") released a method called autoresearch.
> 
> The idea is simple: instead of you manually improving something, you let an AI agent do it for you in a loop.
> 
> It tries a small change. Checks if the result got better. Keeps it if it did, throws it out if it didn't.
> 
> Then it does it again. And again.
> 
> He used it for machine learning code. But the method works on anything you can measure and improve.
> 
> Including the skills you've built in Claude.
> 
> I took his method and turned it into a skill that works in both Claude Code and Cowork. I just run it on any other skill in my setup.
> 
> I say "run autoresearch on my landing page skill" and it handles the whole thing.
> 
> **How one loop auto-improves your skills**
> 
> Think of it like this.
> 
> You have a recipe that turns out great 7 out of 10 times. The other 3 times, something's off. Maybe the sauce is bland, maybe the seasoning is wrong.
> 
> Instead of rewriting the whole recipe from scratch, you change one ingredient. You cook it 10 times with that change.
> 
> * Did it get better? Keep the change.
> * Did it get worse? Put the old ingredient back.
> 
> Then you change the next thing. Cook 10 more times. Better or worse? Keep or revert.
> 
> After 50 rounds of this, your recipe works 9.5 out of 10 times.
> 
> That's exactly what autoresearch does to your skills.
> 
> * The "recipe" is your skill prompt.
> * The "cooking" is running the skill.
> * The "tasting" is scoring the output.
> 
> The only thing you need to provide is the scoring criteria.
> 
> **The checklist that tells the agent exactly what 'good' means**
> 
> You give the agent a simple checklist of what "good" looks like. That's your only job in this whole process.
> 
> You do it with a simple checklist of yes/no questions.
> 
> Each question checks one specific thing about the output. Pass or fail. That's it.
> 
> The agent uses this checklist to score every output, and those scores tell it whether its changes are helping or hurting.
> 
> Think of it like a teacher grading a paper with a checklist.
> 
> But instead of "rate the writing quality 1-10" (which is vague and different every time), each item on the checklist is a clear yes or no:
> 
> * Did the student include a thesis statement? Yes or no.
> * Is every source cited? Yes or no.
> * Is it under 5 pages? Yes or no.
> 
> You can grade 100 papers with that checklist and get consistent results every time.
> 
> Same idea here. For a landing page copy skill, your checklist might look like:
> 
> * "Does the headline include a specific number or result?" (catches vague headlines like "Grow Your Business")
> * "Is the copy free of buzzwords like 'revolutionary,' 'synergy,' 'cutting-edge,' 'next-level'?"
> * "Does the CTA use a specific verb phrase?" (catches weak CTAs like "Learn More" or "Click Here")
> * "Does the first line call out a specific pain point?" (catches generic openers like "In today's fast-paced world...")
> * "Is the total copy under 150 words?" (catches bloated pages that lose the reader)
> 
> You don't need to figure these out on your own. When you start the autoresearch, the agent walks you through it.
> 
> It asks what good looks like, helps you turn your vibes into specific yes/no questions, and even offers to pull from existing style guides if you have them.
> 
> 3-6 questions is the sweet spot. More than that and the skill starts gaming the checklist (like a student who memorizes the answers without understanding the material).
> 
> **Here's how to run it**
> 
> Step 1: Download the skill. Grab it here. Drop it into your skills folder in Claude Code or Cowork.
> 
> Step 2: Pick a skill to improve. Say "run autoresearch on my [skill name] skill." Pick the one that annoys you most. The one where you get a great output half the time and garbage the other half.
> 
> Step 3: The agent asks you 3 things. Which skill to optimize. What test inputs to use (like "write landing page copy for an AI productivity tool"). And what your checklist questions are.
> 
> Step 4: It runs your skill and shows you your starting score. This is the baseline. My landing page skill started at 56%. Vague headlines, buzzword soup, weak CTAs. More than half the checks were failing.
> 
> Step 5: It opens a live dashboard in your browser. Score chart going up over time. Pass/fail breakdown for each checklist question. A log of every change it tried. Auto-refreshes every 10 seconds.
> 
> Step 6: Walk away. The agent enters the loop. Analyzes what's failing. Makes one small change to the skill prompt. Tests again. Keeps the change if the score goes up, undoes it if it goes down.
> 
> Then does it again. And again. It keeps going autonomously until you stop it or it hits 95%+ three times in a row.
> 
> You can watch the dashboard or walk away entirely. It runs without you. And it saves the improved version as a separate file, so your original skill stays untouched.
> 
> **What happened to my landing page skill**
> 
> I ran it on my landing page copy skill. Here's what came back:
> 
> 56% → 92%. 4 rounds of changes. 3 kept, 1 undone.
> 
> Here's what the agent actually changed in my skill prompt:
> 
> * Added a specific rule for the most common failure: "Your headline must include a specific number or result. Never use vague promises like 'Transform Your Business.'"
> * Added a banned buzzwords list: "NEVER use: revolutionary, cutting-edge, synergy, next-level, game-changing, leverage, unlock, transform."
> * Added a worked example of a strong landing page section with the pain point opener and CTA highlighted, so the skill could see what good looks like instead of guessing.
> * Tried a tighter word count, undid it because the copy got too thin and the CTA suffered. (The system catches changes that seem like improvements in isolation but hurt the overall output.)
> 
> When it was done, I got:
> 
> * The improved skill, saved separately (the original stays untouched in case you want to revert)
> * A results log showing every round's score
> * A changelog explaining every change that was tried, why the agent tried it, and whether it helped
> * A backup of my original skill in case I ever want to go back
> 
> That changelog is probably the most valuable piece. It's a complete record of what works and what doesn't for that specific skill.
> 
> When smarter models come out down the road, you hand them that changelog and they pick up right where the last agent left off.
> 
> **This works on way more than skills**
> 
> The method works on anything you can score.
> 
> * Website speed: One person ran this on page load time. Changed one thing, measured the speed, kept or reverted. Went from 1100ms to 67ms in 67 rounds.
> * Cold outreach: Define your checklist: "Does it mention the prospect's company? Is it under 75 words? Does it end with a specific question?" Let the agent run 50 variations.
> * Newsletter intros: "Does the opener include a personal detail?" and "Is it free of cliche phrases?" Let the agent tighten your writing on autopilot.
> * Any prompt you use repeatedly
> 
> If you can score it, you can autoresearch it.
> 
> **Go run it**
> 
> Pick your worst-performing skill. Start the autoresearch. Come back to something that actually works.
> 
> **P.S.** If you want more AI workflows that help you get more [specific outcome] without working more hours, I send them to [X] readers every week for free. Plus [free bonus]: `[NEWSLETTER URL]`

---

## How to use this reference when drafting

Work through it in this order:

1. **Pick the patterns that fit the article you're writing.** Not every article needs all 8. A news breakdown rarely needs the origin-story pattern. A quick tool tutorial doesn't need stacked analogies.

2. **Map the patterns to the user's skeleton (Tutorial or Breakdown).**
   - Hook → Opening sentences
   - Origin story (if used) → Inside "Why it matters" or right after
   - Analogies → Inside "What it does" or "How it works"
   - Results section → "What happened to my X" (Tutorial only)
   - Expansion section → "This works on more than X" (near end, before closer)

3. **Write using the user's voice, not the reference article's voice.** The reference taught you HOW to structure the article. The user's CLAUDE.md tells you WHAT IT SOUNDS LIKE.

4. **If the reference and the user's voice conflict, voice wins.** Always.

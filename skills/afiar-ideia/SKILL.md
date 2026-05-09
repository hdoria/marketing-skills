---
name: afiar-ideia
description: "Make any idea more interesting, surprising, or compelling. Use when someone has a bland take, wants a contrarian angle, needs a hook that stops the scroll, or asks how to make content stand out. Triggers on: make this more interesting, find a surprising angle, give me a hot take on X, this is boring how do I fix it, counterintuitive insight about X, challenge conventional wisdom on X. Outputs reworked ideas with both the intellectual angle AND the presentation technique to deliver it."
---

# Idea Sharpener

Most content fails because it tells people what they already believe. Nobody shares "yep, that's what I thought." They share "holy shit, I never thought of it that way." This skill exists to manufacture that second reaction on demand — by treating "interesting" as a craft, not a vibe.

The position this skill takes: interesting isn't a personality trait, it's a structural property. Murray Davis proved an idea is interesting when it denies one specific thing the audience assumes is true. Get the assumption right, deny it the right way, deliver it with the right technique — and "interesting" becomes reproducible.

---

## the core job

Take a bland or generic idea and produce 3-5 reworked versions, each pairing a Murray Davis proposition type (the angle) with a novelty technique (the delivery). Every version must deny one specific audience assumption and survive a stress-test for substance.

**Output format:** A markdown brief listing 3-5 angles. Each angle includes proposition type, the assumption it denies, the novelty technique used, the rewritten idea ready to use as a hook/post/headline, and a one-line "why it works." Ends with a "strongest option" recommendation.

---

## before starting: gather context

**STOP. Do not produce angles until voice is in hand AND the brief is confirmed. Cap questions at 2.**

### Step A: Gather voice context (fast)

This skill only needs one thing from context: **voice**. Audience and topic come from the brief.

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for do/don't rules, tone, sample sentences.
2. **If missing, check the project folder** for `Context/voice.md`. Read if present.
3. **If voice is still missing:** note it and proceed. Angles will be generic-tone; the user can pass the output through `/anti-slop` or paste voice rules inline.

### Step B: Confirm the brief (≤2 questions, combined)

Combine into at most 2 questions:

1. **Idea + audience** — "What's the idea/topic, and who needs to find it interesting?" (one question, two halves)
2. **Format** — tweet, newsletter, headline, talk, landing page — delivery changes length and rhythm.

Skip anything already clear from context or the user's initial prompt.

---

## the process

Six steps, in order. Don't skip — each one feeds the next.

```
  Ground          Classify         Invert            Sharpen          Stress-test       Anti-slop         Deliver
   |                |                |                 |                  |                  |                |
 voice        surface the     pick a Davis      apply 1 of the      surprise +        kill AI         3-5 angles
 + brief      assumption      proposition       14 novelty           share +          patterns         with strongest
              the audience    type to deny      techniques           "so what"                         flagged
              holds           it                                     tests
```

Each step below cites the reference file it pulls from. Don't reinvent the lists — use them.

---

## ground: load voice and brief

You already did this in "before starting." This is the explicit anchor for the rest of the process.

**Instruction:** Confirm you have (a) voice context loaded (from CLAUDE.md or `Context/voice.md`) or noted as missing, (b) the idea, (c) the audience, (d) the format. Without all four, stop and ask.

**Why:** Voice determines whether the angles sound like the user. Audience determines what counts as "surprising" — what's revelatory to a beginner is wallpaper to an expert. Format determines length and rhythm of the rewritten idea.

**Anti-pattern:** Producing angles before you know the audience. "Marketers are wasting time on AI" is bland to senior marketers and shocking to skeptical execs. Same sentence, opposite reaction.

---

## classify: surface the audience assumption

Before you can deny something, name what the audience already takes for granted.

**The core rule from Murray Davis:** An idea is interesting when it denies something the audience assumes to be true. Not everything they believe — just one specific thing.

| If the denial is... | The audience says... |
|---------------------|---------------------|
| Too weak (confirms what they think) | "That's obvious" |
| Just right (challenges one belief) | "That's interesting!" |
| Too strong (rejects their entire worldview) | "That's absurd" |
| Irrelevant (challenges something they don't care about) | "So what?" |

**How to surface the assumption:**
- What does "everyone knows" about this topic?
- What advice gets repeated so often it's become wallpaper?
- What do experts in this space agree on?
- What would feel risky or uncomfortable to challenge?

The assumption you're looking for is the one that feels so true nobody even questions it anymore.

**Short example:** Topic = "AI tools make marketers more productive." Audience assumption = "More AI tools = more output = more results." That's the belief to deny in the next step.

**Anti-pattern:** Naming the topic instead of the assumption. "AI productivity" isn't an assumption — it's a category. The assumption is the unspoken if/then the audience runs in their head.

---

## invert: pick a Davis proposition type

There are 12 ways to deny an assumption. Each one creates a different flavor of "interesting." Pick the one that best fits the assumption you surfaced.

For full details, examples, and both directions of each type, see [references/proposition-types.md](references/proposition-types.md).

| # | Angle Type | The Move | Quick Example |
|---|-----------|----------|---------------|
| 1 | Organization | Chaos is actually ordered (or order is actually chaos) | "Markets aren't random — they follow predictable emotional cycles" |
| 2 | Composition | Many things are actually one thing (or one thing is actually many) | "All productivity advice is actually about managing energy" |
| 3 | Abstraction | Personal problem is actually systemic (or systemic is actually personal) | "Your impostor syndrome isn't personal — it's structural" |
| 4 | Generalization | Universal rule is actually local (or local truth is actually universal) | "What works in Silicon Valley fails everywhere else" |
| 5 | Stabilization | Stable thing is actually changing (or changing thing is actually stable) | "The 'AI revolution' is following the same hype cycle as every tech before it" |
| 6 | Function | Broken thing actually works (or working thing is actually broken) | "Meetings work — you're just running them wrong" |
| 7 | Evaluation | Bad thing is actually good (or good thing is actually bad) | "Procrastination is a feature, not a bug" |
| 8 | Correlation | Unrelated things are connected (or related things aren't) | "Sleep quality predicts startup success better than funding" |
| 9 | Co-existence | Compatible things can't coexist (or incompatible things can) | "You can't have work-life balance AND exceptional success" |
| 10 | Co-variation | More X means less Y, not more (or vice versa) | "The more you optimize, the less you achieve" |
| 11 | Opposition | Similar things are actually opposite (or opposites are actually the same) | "Hustle culture and anti-hustle culture come from the same place" |
| 12 | Causation | The cause is actually the effect (or vice versa) | "You don't write because you have ideas — you have ideas because you write" |

**Combining types:** The strongest propositions often stack two types. "That 'bad' habit isn't hurting your productivity — your productivity obsession is creating the habit" combines Evaluation + Causation.

**Short example (continuing):** Assumption = "More AI tools = more output." Inverting with Causation gives: "Output isn't going up because of AI — AI is going up because output expectations are." Inverting with Co-variation gives: "The more AI tools a marketer adopts, the less original their work becomes." Two different angles, both deny the same assumption.

**Anti-pattern:** Picking the same type every time (usually Evaluation or Co-variation, because they feel "edgy"). Force yourself to consider 3-4 types per idea — the less obvious choice often produces the sharpest angle.

---

## sharpen: apply a novelty technique

The angle is WHAT you say. The delivery technique is HOW you say it. Both matter.

**The Content Hierarchy** — always aim for Level 3 or 4:

| Level | Formula | Result |
|-------|---------|--------|
| 1 (skip) | Obvious info + obvious delivery | Eye roll |
| 2 (decent) | Obvious info + surprising delivery | "New wrapper" |
| 3 (strong) | Surprising info + straightforward delivery | "Mind blown" |
| 4 (elite) | Surprising info + surprising delivery | "Life-changing" |

Pick a delivery technique from the 14 options. For full details and examples, see [references/novelty-techniques.md](references/novelty-techniques.md).

| # | Technique | When it works best |
|---|-----------|-------------------|
| 1 | Powerful Analogy | Connecting something familiar to something unexpected |
| 2 | "Most People Think X, But Actually Y" | Direct assumption-denial with evidence |
| 3 | Personification | Attaching insight to a memorable character or archetype |
| 4 | Story-First | Leading with a specific moment before revealing the lesson |
| 5 | Preframing | Borrowing credibility from a source before sharing the insight |
| 6 | Weird Specific Names | Creating curiosity through unusual naming |
| 7 | Strategic Ridicule | Using absurd numbers or titles for attention |
| 8 | Outcome over Mechanism | Leading with what they get, not how it works |
| 9 | Scientific Anchor | Opening with an unknown research finding |
| 10 | Ancient Wisdom | Connecting to historical stories or concepts |
| 11 | Strategic Tension | Building conflict between two positions, then resolving |
| 12 | Strategic Paradox | Highlighting genuine contradictions without easy answers |
| 13 | Illuminating Question | Letting the reader arrive at the conclusion themselves |
| 14 | "Screw the Obvious" | Listing and dismantling all the cliche advice first |

**Short example (continuing):** Take "Output isn't going up because of AI — AI is going up because output expectations are." Sharpening with Scientific Anchor (#9): "A McKinsey survey of 1,200 marketers found AI adoption tracked one variable, and it wasn't curiosity. It was workload. Marketers reach for AI when their output bar moves, not when they want better work." Sharpening with Strategic Paradox (#12): "The harder marketers work to use AI 'productively,' the less productive marketing becomes — because everyone is producing the same AI-shaped content."

**Anti-pattern:** Picking a delivery technique before the angle is sharp. A Powerful Analogy wrapping a soft assumption is just a pretty bow on a generic gift.

---

## stress-test: run the three checks

Before delivering, every angle must survive these three tests. If it fails any, send it back to the Invert or Sharpen step — don't ship a weak angle.

1. **The Surprise Test** — If you showed this to someone in the target audience, would they pause? Not agree or disagree — just pause. That's the signal.
2. **The Share Test** — Would someone send this to a friend or colleague? Interesting ideas create the urge to say "you need to see this."
3. **The "So What" Test** — Does this change what the reader thinks, feels, or does? If it's just clever without consequence, sharpen it.

**Both levels required** — an interesting idea must work on both:

| Level | What it means | If it's missing, add... |
|-------|--------------|------------------------|
| Intellectual | Challenges something they believe | "This works because of a counterintuitive truth..." |
| Practical | Changes something they should DO | "So what? Here's what to do differently..." |

Pure theory without practical implication = "Huh, cool" then forgotten. Pure practical tip without insight = useful but not shareable. Both together = "I need to send this to someone."

**Anti-pattern:** Confusing "shocking" with "interesting." Shocking gets attention once. Interesting gets shared because it changes something. If the only thing your angle has going for it is taboo, it fails the "So What" test.

---

## anti-slop: mandatory pass

Before showing any angle, hook, or proposition to the user, run it through the `anti-slop` skill.

**Why this skill especially:** Interesting-angle generators are prone to AI slop patterns — fake profundity ("it's not X, it's Y"), melodramatic realizations ("that's when everything changed"), and forced contrarianism without substance.

**How:** Invoke `anti-slop` with the full draft (all angles + supporting copy) as input.

**If `anti-slop` is not available,** scan manually for: binary opposites, rhetorical questions, "Not because of X, but because of Y," manufactured insights, shock-value contrarianism without real insight.

Rewrite anything flagged. Non-negotiable: no angles ship without this pass.

**Anti-pattern:** Treating anti-slop as optional polish. The whole point of an interesting angle is that it sounds like a real human had a real thought. Slop patterns kill that immediately.

---

## deliver: format and present

Hand the user 3-5 angles in the output format below. Lead with the strongest, but show variety in proposition type and technique so they can pick the one that fits their voice.

**Anti-pattern:** Delivering only one angle. Without options, the user can't see the trade-off between, say, a Causation flip and an Opposition reframe — both might work, but for different formats.

---

## output format

### Interesting Angles for [Topic/Idea]

**Audience assumption:** [What they currently take for granted]

---

**Version 1: [Name]**

| Element | Detail |
|---------|--------|
| Angle type | [Which of the 12 types] |
| The denial | [What assumption it breaks, in one sentence] |
| Delivery technique | [Which of the 14 techniques] |
| Content hierarchy level | [2, 3, or 4] |

**The reworked idea:**
> [The actual rewritten idea/hook/take, ready to use]

**Why it works:** [1-2 sentences on the psychology]

---

**Version 2: [Name]**
[Same structure]

---

[Continue for 3-5 versions]

**Strongest option:** [Which version to lead with and why]

---

## example: making "AI tools make marketers more productive" interesting

### Context
- **The idea:** "AI tools make marketers more productive"
- **The audience:** Mid-level marketers who've already adopted ChatGPT, Claude, and a few specialized AI tools
- **The format:** LinkedIn post / newsletter hook

**Audience assumption:** "More AI tools = more output = better results."

---

**Version 1: The Treadmill**

| Element | Detail |
|---------|--------|
| Angle type | Causation (reverse) |
| The denial | Output isn't going up because of AI — AI is going up because output expectations are |
| Delivery technique | Scientific Anchor (#9) |
| Content hierarchy level | 4 |

**The reworked idea:**
> Marketers think AI is making them more productive. The data says otherwise. A McKinsey survey of 1,200 marketers found AI adoption tracked one variable, and it wasn't curiosity. It was workload. The output bar moved up the same week the tools shipped. Marketers reach for AI when their boss expects 5x output by Friday — not when they want to do better work. AI didn't raise the ceiling. It raised the floor everyone now has to clear.

**Why it works:** Reverses the causal arrow. Audience believes AI → productivity. This says expectations → AI adoption. Reframes a "wins" story as a "treadmill" story. Stress-test: pauses (yes — uncomfortable truth), shareable (yes — every marketer feels this), so-what (yes — changes how you negotiate workload).

---

**Version 2: The Sameness Paradox**

| Element | Detail |
|---------|--------|
| Angle type | Co-variation (more X = less Y) |
| The denial | The harder marketers work to use AI "productively," the less productive marketing becomes |
| Delivery technique | Strategic Paradox (#12) |
| Content hierarchy level | 4 |

**The reworked idea:**
> The AI productivity paradox: the harder you work to use AI, the worse marketing gets. Not for you — for everyone. When 50,000 marketers all prompt the same five tools with the same five frameworks, the output converges. Same hooks. Same structures. Same "Most people think X, but actually Y." Productivity went up. Distinctiveness went to zero. The more "productive" the industry gets, the less anything cuts through.

**Why it works:** Names a tension marketers feel but haven't articulated. No clean answer — just a better framework. Paradoxes are inherently shareable. Stress-test: pauses (yes), shareable (yes), so-what (yes — pushes toward originality over speed).

---

**Version 3: The Wrong Bottleneck**

| Element | Detail |
|---------|--------|
| Angle type | Composition (many → one) |
| The denial | Productivity tools don't fix productivity — judgment is the bottleneck, not output |
| Delivery technique | "Screw the Obvious" (#14) |
| Content hierarchy level | 3 |

**The reworked idea:**
> Everyone's optimizing the wrong layer. New AI tool. New prompt library. New workflow automation. Meanwhile the actual bottleneck — deciding what's worth making in the first place — gets zero attention. You can crank out 100 AI-assisted posts this week. If they're aimed at the wrong audience with the wrong hook, you've just industrialized your mistakes. AI makes execution cheap. That makes judgment expensive. The marketers winning now aren't the ones with the best stack. They're the ones who think hardest before they prompt.

**Why it works:** Reframes the entire conversation from "which tools" to "what to build." Validates effort while redirecting it. Stress-test: pauses (yes — most marketers know this in their gut), shareable (yes — feels like advice worth passing on), so-what (yes — practical: spend less time on tool-stacking, more on strategy).

---

**Version 4: The Trojan Horse**

| Element | Detail |
|---------|--------|
| Angle type | Function (working → broken) |
| The denial | "Productivity gains" from AI are real for individuals, but they're a layoff signal for teams |
| Delivery technique | Personification (#3) |
| Content hierarchy level | 4 |

**The reworked idea:**
> Meet Sarah. She's a marketing manager who 3x'd her output with AI. Her boss noticed. Her boss promoted her. Her boss also fired two of her teammates. Same week. The "productivity revolution" looks different from the org chart than it does from your laptop. Every individual win compounds into a team-level reduction. The marketers celebrating their AI workflow are quietly making the case for their own coworkers' redundancy. Read the memo your CFO is writing while you're prompting.

**Why it works:** Personification makes an abstract org dynamic visceral. Calls out the gap between individual and collective outcomes. Stress-test: pauses (yes — uncomfortable), shareable (yes — but in private DMs more than feeds), so-what (yes — changes how you frame your AI use to leadership).

---

**Strongest option:** Version 1 (The Treadmill) for the LinkedIn post. The Scientific Anchor gives it shareable credibility, and the causation flip is the cleanest "I never thought of it that way" moment. Version 3 (The Wrong Bottleneck) is the runner-up if the audience is more senior and would respond to the "judgment is the bottleneck" reframe over the workload critique.

---

## how this connects to other skills

**Feeds into:**
- Newsletter skill (interesting angles become newsletter hooks)
- Social content skill (angles become posts)
- Landing page skill (interesting positioning for offers)
- Lead magnet skill (counterintuitive angles drive opt-ins)

**Receives from:**
- Keyword research skill (topics to make interesting)
- Positioning angles skill (angles to sharpen further)
- Brand voice skill (tone for delivery)

---

## the test

Before delivering, verify each version passes:

1. **Specific assumption denied** — Can you name the exact belief being challenged? If it's vague, it won't land.
2. **One denial, not many** — Challenging one belief is interesting. Challenging everything is absurd. Check you're not overreaching.
3. **Both levels present** — Does it have intellectual insight AND practical implication? Both required.
4. **Content hierarchy 3+** — Is either the info or the presentation (ideally both) non-obvious?
5. **Audience-calibrated** — Would THIS specific audience find it surprising? What's obvious to experts is revelatory to beginners, and vice versa.
6. **Not just contrarian** — Is there a real insight behind the denial? Disagreeing for shock value is empty.
7. **Passes the share test** — Would someone tag a friend or forward this?

**Failure condition:** If any version is just "clever" without substance, just "true" without surprise, or just "shocking" without changing what the reader thinks/feels/does — cut it and try another angle type. Don't ship to the user. A skill that delivers four sharp angles and one weak one teaches the user to distrust the whole batch.

---

## Feedback Log — progressive learning

This skill gets sharper over time. Every correction the user gives becomes a permanent rule in `feedback.log` next to this SKILL.md.

### At the start of every session
1. Read `feedback.log` in this skill's folder. Apply every rule.
2. If it doesn't exist, create it with header: `# Interesting Workshop — Learned Rules`

### Triggers that require a log write

When the user says any of the following, immediately append a rule:
- "Don't use X angle anymore" / "Stop doing contrarian for contrarian's sake"
- "Always lead with Y" / "From now on, check Y first"
- "I hate when you..." / "This angle is too generic"
- "That's perfect, keep doing that" (log positive — don't drift)
- Silent rewrites where the user sharpens an angle — infer the rule

### Format for each rule
```
## YYYY-MM-DD — [short title]
**Rule:** [imperative sentence]
**Why:** [reason]
**How to apply:** [when this kicks in — which proposition type, which audience]
```

### What to log vs skip
**Log:** angle-type rules, contrarian calibration, specificity requirements, domain-specific examples.
**Skip:** one-off tweaks to a specific angle — not a rule.

### Cleanup every ~10 entries.

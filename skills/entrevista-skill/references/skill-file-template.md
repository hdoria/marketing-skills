# Skill File Template (Anthropic Blueprint)

The annotated template for the final SKILL.md file produced by this interview. Follow the structure, fill in each section from the interview answers, and ship.

Use this when assembling in Step 8.

---

## Annotated template

```markdown
---
name: [skill-name-kebab-case]
description: "[1-sentence what it does]. Use when [specific situations]. Triggers on: [phrase 1], [phrase 2], [phrase 3]. Use this skill even when the user doesn't explicitly say [skill category] — if they describe [scenario], this is the right tool. Outputs [deliverable format]."
---

# [Skill Title — Noun or Noun Phrase]

[Opinionated intro — 2-3 sentences. Take a stance on why the typical approach fails. Claude triggers better on confident, specific skills than on vague ones.]

---

## the core job

[1-2 paragraphs: what the skill produces, how it differs from a generic Claude response.]

**Output:** [Format + where it lands.]

---

## before starting: gather context

**STOP. Do not [produce output / execute] until context is in hand. Cap questions at 2 max.**

### Step A: Gather context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for [business/ICP/voice/whatever this skill needs].
2. **If missing, check the project folder** for `Context/[relevant-file].md`. Read whichever exist.
3. **Still missing? Ask ≤2 questions, then go.**

### Step B: Confirm the brief (≤2 questions)

Combine related fields into at most 2 questions. Skip anything already covered by context.

---

## the process

```
STEP 1 → STEP 2 → STEP 3 → ... → OUTPUT
```

[One sentence explaining why the sequence is in this order.]

---

## Step 1: [Verb + object, e.g. "Extract the hook"]

[1-2 sentences: what this step does and why.]

### Framework

[The repeatable structure — a formula, matrix, checklist, or set of categories. THIS IS WHERE THE SKILL GETS ITS EDGE. A step without a framework tells Claude to improvise, which produces generic output every time.]

### Mini-example

> [One real use of this step with concrete content. Not a placeholder — real values.]

### Anti-pattern

[1-2 lines on the most common mistake at this step.]

---

## Step 2: [Verb + object]

[Same structure as Step 1.]

---

## [...continue for every step]

---

## output format

[Template with placeholders. Claude follows this literally — be precise.]

```
[Exact format of the final deliverable, with [PLACEHOLDER] markers for the parts that change per invocation.]
```

---

## gotchas

The failure modes to catch before delivering:

1. **[Specific failure].** [How to spot it or avoid it.]
2. **[Specific failure].** [How to spot it or avoid it.]
3. **[Specific failure].** [How to spot it or avoid it.]
4. **[Specific failure].** [How to spot it or avoid it.]
5. **[Specific failure].** [How to spot it or avoid it.]

[Minimum 5, ideally 8-10. This section is one of the highest-signal parts of any skill. Pull directly from Step 6 of the interview.]

---

## the test

Before delivering, verify:

1. **[Specific check].** [How to check it — must be verifiable, not subjective.]
2. **[Specific check].** [How to check it.]
3. **[Specific check].** [How to check it.]
4. **[Specific check].** [How to check it.]
5. **[Specific check].** [How to check it.]

**Failure condition:** If [specific bad thing that would make the output unusable] — it failed. [Action to take: return to which step.]

---

## worked example

[This section is the most important part of the whole skill. It's what Claude pattern-matches against. Never summarize — show the full output.]

### Scenario

[A realistic use case. Not trivial. Specific enough that the example has texture.]

### Step-by-step run

**Step 1 — [Name]:**
[Full output of this step, not a summary.]

**Step 2 — [Name]:**
[Full output of this step.]

[...continue through every step.]

### Final output

[The complete deliverable, fully assembled.]

[If the worked example is long (>150 lines), move it to references/worked-example.md and link from here.]

---

## how this connects to other skills

**Feeds into this skill:**
- [Skill anterior 1] — [what it produces that this skill consumes]
- [Skill anterior 2] — [what it produces that this skill consumes]

**This skill feeds into:**
- [Downstream skill 1] — [what they do with this skill's output]
- [Downstream skill 2] — [what they do with this skill's output]

**Adjacent:**
- [Related skill that does a nearby job]
```

---

## Section-by-section cheat sheet

### Frontmatter `description`

This is the single highest-leverage part of the whole skill file. Claude only scans this to decide whether to trigger. Rules:

- **Open with what it does, not what it IS.** "Write X" beats "A skill for writing X."
- **List 3-5 trigger phrases** the user would actually type. Real phrasing, not abstract categories.
- **Add a "pushy" line** encouraging Claude to trigger even when the user doesn't name the skill. Per Anthropic, skills under-trigger more often than they over-trigger.
- **Close with the deliverable.** "Outputs X" tells Claude what success looks like.

Example of the "pushy" line:

> "Use this skill even when the user doesn't explicitly say 'sales page' — if they mention writing copy for a product, a launch, or something they're selling, this is the right tool."

### Opinionated intro

2-3 sentences that take a stance. This is also a subtle triggering signal — vague intros make Claude hesitant to commit to using the skill. Strong openings:

- "Most [X] fail because [common mistake]. The ones that work [counter-intuitive truth]."
- "People think [common assumption]. In practice, [reality that forces a different approach]."
- "The usual way to do [X] is [method A]. This skill does [method B] because [reason]."

Avoid: "This skill helps with [X]."

### Core job

Two purposes:
1. Name the output format precisely.
2. Explain how this skill's output differs from what a baseline Claude response would produce.

If you can't tell a user "the skill produces X, in Y format, and it differs from a generic Claude answer because Z" — the skill is too vague.

### Process diagram

Use arrow-chain ASCII. Short and simple.

```
RESEARCH → DRAFT → EDIT → SHIP
```

Not a flowchart. Not a fancy diagram. Just the named sequence. Claude reads this first and uses it as the skeleton for everything below.

### Step sections

Each step needs four things:
- Instruction (what to do)
- Framework (how to do it repeatably)
- Mini-example (what good output looks like)
- Anti-pattern (what to avoid)

A step with only the instruction produces generic output. Every time. No exceptions.

### Output format

Be literal. Claude follows templates exactly. If the user wants:

```
**Subject:** [Subject line]
**Preview:** [Preview text]
**Body:** [Body copy]
```

...write exactly that, with those formatting marks. Don't describe it in prose.

### Gotchas

Minimum 5. Ideal 8-10. Pulled straight from Step 6 of the interview.

Good gotcha format:
> **Specific failure mode.** How to spot it or avoid it. [1-2 sentences.]

Bad gotcha format (too vague):
> **Be careful about quality.** Make sure the output is good.

### The test

5-7 verifiable checks + 1 failure condition.

A verifiable check:
> "The subject line is under 60 characters."

A non-verifiable check (avoid):
> "The subject line is compelling."

Verifiable = you could grade it with a script. Non-verifiable = requires human judgment. Aim for verifiable.

### Worked example

Non-negotiable. This is what Claude pattern-matches against. A skill without a worked example produces generic output forever, no matter how detailed the rest is.

Rules:
- Realistic scenario. Not "Write an email about X" — "Write a re-engagement email for an analytics SaaS whose trial users churned at day 7 because the activation metric was unclear."
- Full output, not summary. Every section of the deliverable, filled with real content.
- Placeholder-free. If the skill generates 5 items, show all 5. If it generates a 7-step sequence, show all 7 steps fully written out.

---

## When to split into references/

The SKILL.md should stay under ~500 lines. If the interview produced a workflow that requires:

- **Extensive domain knowledge.** → `references/domain.md`. Reference it from the relevant step.
- **A long worked example.** → `references/worked-example.md`. Link from the "worked example" section.
- **Variant-specific instructions** (different handling for different input types). → `references/variant-[name].md` for each. Main SKILL.md picks which to load based on input.
- **Scripts the workflow runs.** → `scripts/[name].sh` or `.py`. Reference by path from the step that runs them.
- **Templates (long or many).** → `references/templates.md` or `assets/[template].md`.

**Rule:** The SKILL.md must explicitly link to every reference file. Unlinked files don't exist as far as Claude is concerned — they won't get loaded.

---

## Final pre-ship checklist

Before handing the file to the user:

- [ ] Frontmatter `description` includes 3+ trigger phrases and a "pushy" line
- [ ] Opinionated intro takes a stance (no "this skill helps with...")
- [ ] Every step has instruction + framework + mini-example + anti-pattern
- [ ] Output format is literal, with placeholders, not described in prose
- [ ] Gotchas section has ≥5 specific failure modes
- [ ] "The test" has 5-7 verifiable checks + 1 failure condition
- [ ] Worked example shows the FULL output, not a summary
- [ ] SKILL.md under ~500 lines (or split into references/)
- [ ] All references/ files explicitly linked from SKILL.md
- [ ] File saved to the path the user chose, with directory created if needed

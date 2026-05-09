---
name: entrevista-skill
description: "Interview a user to extract a repeatable workflow from their head, then package it into a production-ready Claude skill file. Use this when someone wants to turn something they do manually every week into a reusable skill. Triggers on: interview me to build a skill, help me extract my workflow, turn my process into a skill, I want to automate what I do, walk me through building a skill from scratch, capture how I do [task]. Use this skill even when the user doesn't explicitly say 'interview' — if they describe a repeatable task they do and want Claude to do it for them, this is the right tool. Outputs a complete SKILL.md file (with references/ subfolder when needed) saved to the user's chosen skills directory."
---

# Workflow Extraction Interview

Most skill files read like Wikipedia entries. They explain what a thing IS instead of telling Claude how to DO it. The result: Claude uses them once, gets generic output, and the user stops using the skill.

A good skill captures a **workflow** — the actual sequence someone follows when they do the task, with the judgment calls, tool choices, and quality checks that make the output specialist-level. Those details never show up when you just describe the process at a high level. They show up when someone asks the right follow-up questions.

This skill runs that interview. It walks the user through 8 steps, asks targeted questions at each one, keeps probing until the workflow is concrete enough to execute, and packages the result into an Anthropic-blueprint skill file.

---

## the core job

Run a structured interview that extracts the user's workflow, then produce a complete skill file they can install and call.

**Output:** A `SKILL.md` (plus `references/` files if needed) saved to the directory the user picks — defaults to `~/.claude/skills/[skill-name]/` if they have no preference.

---

## before you start

Two quick checks before launching into the interview:

1. **Scan CLAUDE.md.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. If it already contains business context, voice rules, or ICP info, you can skip asking about those things later — just reference what's there.
2. **One opening question only.** Before Step 1, ask: "What's the one task you want to capture? In plain language, one sentence." This anchors the interview and prevents scope drift.

Everything else comes out of the 8-step interview below. Don't batch questions. Ask one step's worth at a time, wait for the answer, then move on.

---

## the process

```
SCOPE → SEQUENCE → DECISIONS → TOOLS → QUALITY → FAILURE → TEMPLATE → PACKAGE
```

Eight steps. Each one pulls a specific part of the workflow out of the user's head. The order matters — scope before sequence (otherwise the user describes a different workflow than the one they named), sequence before decisions (otherwise the decisions have nowhere to live), and so on.

For the full question bank — primary questions, probe-deeper follow-ups, and "what to listen for" notes per step — see [references/interview-questions.md](references/interview-questions.md).

For the 4 common workflow shapes (linear, branching, iterative, judgment-driven) and how to structure each in the final SKILL.md, see [references/workflow-shapes.md](references/workflow-shapes.md).

---

## Step 1: Scope

Figure out the job, the trigger, the output, and the user.

**Ask (one message):**

1. In one sentence — what does this workflow do?
2. What makes you start this workflow? A request from someone? A recurring calendar item? A trigger in your day?
3. What does "done" look like? Describe the final artifact or action.
4. Who will use the skill — just you, or teammates too?

**What to listen for:** A scope that's too broad ("helps with marketing") will produce a generic skill. Push for the specific job ("writes the weekly launch recap email for product releases"). If the user gives you a category instead of a job, ask "what's the most common version of that?"

**What this produces:** The frontmatter `description` and the top-of-file "core job" section.

---

## Step 2: Sequence

Get the actual steps in the order the user does them. This is the spine of the workflow.

**Ask:**

1. Walk me through the last time you did this — step by step, start to finish.
2. At any point do you go back and redo something? (loops)
3. How long does each step take, roughly?

**Probe deeper when you hear labels instead of actions.** "First I research the audience" is a label. Ask: "What exactly do you do when you research them? What do you open, what do you look at, what do you write down?" The workflow lives one layer below the label the user gives you. Keep probing until you hit actions you could actually execute.

**What this produces:** The ordered list of steps + a process diagram (arrow chain).

---

## Step 3: Decisions

Find the branches. Where does the user stop and decide something?

**Ask:**

1. Where in the sequence do you have to make a judgment call?
2. What are the criteria? What tells you "this is a yes" vs "this is a no"?
3. What changes downstream based on that decision?

**Why this step matters more than it looks:** Workflows without explicit decision criteria produce generic output — Claude defaults to whatever the most common answer is, regardless of the actual inputs. A workflow with explicit criteria ("use format A when the audience is cold, format B when they've bought before") produces output that adapts.

If the user says "I just know," push back: "When you 'just know,' what are you actually reacting to?" There's always a signal. Find it.

**What this produces:** Decision tables or if/then rules inline with the relevant process step.

---

## Step 4: Tools and artifacts

What does the user touch? What do they produce along the way?

**Ask:**

1. What tools do you open during this workflow? (files, apps, tabs, docs, sheets, URLs)
2. Do you reuse any templates, checklists, or reference docs?
3. Are there any scripts or automations you rely on — even small ones?

**What to listen for:**
- If the user keeps reopening the same reference doc, that doc belongs inside the skill as a `references/` file.
- If the user runs a repeated script or command, note it — it may belong in `scripts/`.
- If the output format is a rigid template, capture the template word-for-word. Claude follows templates literally.

**What this produces:** The list of files/templates/scripts that need to ship inside the skill folder.

---

## Step 5: Quality checks

How does the user know the output is good before they ship it?

**Ask:**

1. Before you send/publish/commit the output, what do you check?
2. What would make you throw out a draft and start over?
3. Are there specific numbers or markers you look for?

**What this produces:** The "the test" section — 5 to 7 specific, verifiable checks. Plus a failure condition.

**Rules for the checks:**
- Each one must be verifiable ("headline includes a specific number" beats "headline is strong").
- End the section with a failure condition ("If the output reads like a competitor could have written it — it failed").

---

## Step 6: Failure modes

What goes wrong? This is the section that saves the skill from producing generic output every time.

**Ask:**

1. What are the 3-5 most common mistakes people make when doing this?
2. Have you caught yourself making any of them recently? What was the tell?
3. Anything Claude or an AI would probably get wrong by default?

**What this produces:** A "gotchas" section — one of the highest-signal parts of any skill (per Anthropic's best practices). 5-10 concrete failure modes, each with one line on how to spot or avoid them.

---

## Step 7: Template

Show the final output structure. Claude follows templates literally.

**Ask:**

1. What sections does the final output have, in order?
2. Is there a fill-in-the-blank structure you reuse? (paste it)
3. How strict is the format — rigid template, or flexible guide?

**What this produces:** The "output format" section with placeholders. If the template is rigid, write it verbatim. If flexible, describe the shape but not the exact wording.

---

## Step 8: Package

Assemble the skill file. Check it against the Anthropic blueprint. Save.

### 8a. Write the opinionated intro

Before the "core job" section, write 2-3 sentences that take a stance. Claude's triggering is partly sensitive to how the intro reads — confident and specific skills trigger better than vague ones.

**Bad:** "This skill creates email sequences for marketing."
**Good:** "Most lead magnets die in the inbox. Someone downloads your thing, gets one 'here's your download' email, and never hears from you again."

### 8b. Check the file size

- **Under ~500 lines?** Ship as a single SKILL.md.
- **Over 500?** Split into `SKILL.md` + `references/` per Anthropic's progressive disclosure pattern:
  - Extensive frameworks → `references/frameworks.md`
  - Long worked example → `references/examples.md`
  - Domain-specific knowledge → `references/domain.md`
  - Repeated scripts → `scripts/[name].sh` or `.py`
- When splitting, the SKILL.md must explicitly link to each reference file. Unlinked references are invisible — Claude won't find them.

### 8c. Write the description carefully

The `description` field is the ONLY thing Claude scans to decide whether to load the skill. Include:
- What the skill does (1 sentence)
- Specific trigger phrases — what the user would actually say
- What the skill outputs
- A "pushy" line encouraging use even when the user doesn't name the skill explicitly

Per Anthropic: skills under-trigger more often than they over-trigger. Err toward pushy.

### 8d. Save and confirm

Ask the user where to save (default: `~/.claude/skills/[skill-name]/`). Create the folder, write `SKILL.md`, write any `references/` or `scripts/` files.

Then tell the user:
- The full path
- How to invoke it (slash command or described use case)
- A one-line summary of what the skill now does

---

## output format

The final output is a skill **folder** (not just a file). Shape:

```
[skill-name]/
├── SKILL.md                    # required
└── references/                 # only if SKILL.md exceeds ~500 lines
    ├── [topic-1].md
    └── [topic-2].md
```

Inside `SKILL.md`:

```markdown
---
name: [skill-name]
description: "[what it does]. Use when [situations]. Triggers on: [phrase 1], [phrase 2], [phrase 3]. Outputs [deliverable]."
---

# [Skill Title]

[Opinionated intro — 2-3 sentences, takes a stance.]

## the core job

[1-2 paragraphs: what this produces, output format.]

## before starting: gather context
[Gate with STOP instruction. ≤2 questions if context is needed from user.]

## the process
[Arrow-chain diagram of named steps.]

## [Step 1 name]
[Instruction + framework + mini-example + anti-pattern.]

## [Step 2 name]
...

## output format
[Template with placeholders.]

## gotchas
[5-10 specific failure modes.]

## the test
[5-7 verifiable quality checks + failure condition.]

## worked example
[One complete run, end to end — or linked to references/example.md if long.]
```

For the full template with annotations, see [references/skill-file-template.md](references/skill-file-template.md).

For a complete worked example — an actual interview transcript turned into a real skill file — see [references/worked-example.md](references/worked-example.md).

---

## gotchas

The failure modes that keep coming up when running this interview:

1. **Asking all 8 steps' questions at once.** The user dumps a wall of text, half the details get missed, and the resulting skill is shallow. Ask one step at a time.

2. **Accepting labels instead of actions.** "I research the audience" is a label. Ask what they actually open, read, and note. The workflow lives one layer below.

3. **Letting the user skip Step 3 (decisions).** People rarely surface their own judgment calls without prompting. They'll say "I just know." You have to ask "what are you reacting to when you just know?" every time.

4. **No worked example.** The worked example is the most important section of any skill — it's what Claude pattern-matches against. Skipping it produces a skill that compiles and loads but generates generic output forever.

5. **Over-500-line SKILL.md with no split.** Single files over 500 lines blow past the progressive disclosure budget. Split to `references/` and link explicitly.

6. **Description field written as a summary.** "A skill for [X]" under-triggers. Describe what the user would say in a real session. Be pushy.

7. **Missing "gotchas" section.** A skill without gotchas repeats the user's mistakes forever. Step 6 of the interview exists specifically to fill this section — don't skip it.

8. **Fabricating specifics in the worked example.** If the user's real example has gaps (missing numbers, unclear outcomes), use `[PLACEHOLDER]` markers. Don't invent proof numbers to make the example look cleaner.

9. **Forgetting to scan CLAUDE.md first.** If the user already has business/ICP/voice context loaded, asking those questions again wastes the interview budget. Check before starting.

10. **Burying the output location.** At the end of Step 8d, tell the user the exact path, the slash command (if any), and a one-liner. Users frequently forget where the file landed.

---

## the test

A good skill produced by this interview:

1. **Has a specific job description.** Not a category. A specific, named task the skill does every time.
2. **Triggers on realistic phrases.** The description lists phrases the user would actually type — not abstract categories.
3. **Shows the sequence as named steps.** Each step has an instruction + the framework that makes it repeatable + a mini-example.
4. **Captures the decision criteria.** Every judgment call in the workflow has an explicit if/then rule or a decision table.
5. **Includes a complete worked example.** Not a summary. A full run with real content.
6. **Has a gotchas section.** 5+ concrete failure modes, not vague warnings.
7. **Has a testable quality gate.** 5-7 specific checks, plus a failure condition.
8. **Stays under 500 lines in SKILL.md.** Overflow goes into `references/`.

**Failure condition:** If the resulting skill produces output that any baseline Claude prompt could generate — it failed. The interview went too shallow. Re-run Steps 2, 3, and 6 with more probing; the missing depth is there, it just didn't come out.

---

## how this connects to other skills

**Feeds into this skill:**
- `entrevista-negocio` — captures business/ICP/voice context into CLAUDE.md. Having that context loaded before starting this interview shortens Steps 4 and 5.

**This skill feeds into:**
- `criar-skill` — the other way to build a skill: paste existing content (a transcript, blog post, course, framework doc) and it extracts the method automatically. Use that one when the user has content already; use this one when the workflow only lives in their head.
- `criar-skill` also runs the iteration / eval loop (test cases → benchmark → improve → repeat) if the user wants to measure and optimize skill quality quantitatively after building it.

**Adjacent:**
- `anti-slop-writing` — any prose-generating skill produced by this interview should invoke anti-slop as a final pass.

# Workflow Shapes

Not every workflow has the same topology. Before you assemble the SKILL.md, decide which shape the user described. That shape determines how the "process" section should look — and where decision logic lives.

There are 4 shapes that cover almost every real workflow.

---

## Shape 1: Linear

Steps run in a fixed order, each one feeding the next. No branches, no loops. This is the simplest shape and the easiest to turn into a skill.

**When to use this shape:** The user walks you through the sequence in Step 2 and never mentions going back, picking between paths, or repeating anything.

**SKILL.md structure:**

```
## the process

STEP 1 → STEP 2 → STEP 3 → STEP 4 → OUTPUT

## Step 1: [Name]
[Instruction + framework + mini-example]

## Step 2: [Name]
[Instruction + framework + mini-example]

[...etc]
```

**Examples of linear workflows:**
- Weekly metrics recap: pull numbers → compare to last week → write summary → post to Slack.
- Cold email triage: open inbox → tag by intent → reply with templates → archive.
- New customer onboarding email: receive signup event → fill template with their name → send.

**Gotcha specific to this shape:** If the user describes a linear workflow too fast, you're probably missing a decision. Ask: "Does it always run exactly like this? What happens if [variation]?" If they say "then I skip step 3," congratulations — the workflow isn't linear, it's branching.

---

## Shape 2: Branching

The user hits a decision point and the workflow forks. Different inputs produce different paths.

**When to use this shape:** Step 3 (decisions) surfaces more than one if/then rule that changes the downstream sequence.

**SKILL.md structure:**

```
## the process

STEP 1 → STEP 2 → {DECISION}
                    ├── path A: STEP 3a → STEP 4a → OUTPUT
                    └── path B: STEP 3b → STEP 4b → OUTPUT

## Step 1: [Name]
...

## Decision: [Name]
Use path A when: [criteria]
Use path B when: [criteria]

## Step 3a: [Name] (path A only)
...

## Step 3b: [Name] (path B only)
...
```

**Examples of branching workflows:**
- Email sequence picker: survey new subscriber → if cold → send nurture sequence; if warm → send sales sequence.
- Support ticket triage: read ticket → if bug → route to engineering; if billing → route to finance; if other → reply personally.
- Lead magnet generator: identify business model → if course/coaching → generate quiz or challenge ideas; if SaaS → generate ROI calculator or template ideas; if service → generate audit or assessment ideas.

**Structural tip:** Put the decision criteria in a table, not prose. Tables make if/then rules easier for Claude to follow:

```markdown
| If the input is... | Run path... |
|---------------------|-------------|
| Cold audience       | A           |
| Warm audience       | B           |
| Paid customer       | C           |
```

**Gotcha specific to this shape:** Users often describe branches as if they're picking intuitively. "It depends" isn't a rule. Push until they give you criteria you could execute.

---

## Shape 3: Iterative (loop)

The user runs a step, checks the output, and either ships or runs it again. The workflow loops until a quality bar is met.

**When to use this shape:** In Step 2 the user mentions going back to redo something, or "iterating until it's right."

**SKILL.md structure:**

```
## the process

STEP 1 → STEP 2 → STEP 3 → CHECK
                                  ├── pass → OUTPUT
                                  └── fail → back to STEP 2

## Step 1-3: [Names]
...

## Check: [Quality criteria]
Pass when: [concrete conditions]
Fail when: [concrete conditions]
If fail, return to Step 2 and adjust [specific thing] based on [signal].
```

**Examples of iterative workflows:**
- Editing a draft: read → identify weakest section → rewrite → re-read → if still weak, rewrite again.
- Prompt engineering: write prompt → run → evaluate output → if wrong, adjust prompt → repeat until output matches target.
- Code review: read PR → write comments → read response → approve or request more changes.

**Structural tip:** Bound the loop. "Iterate until it's good" is not a stopping condition — Claude will either stop too early or loop forever. Include:
- **Max iterations** (e.g., "stop after 3 passes")
- **Fallback** (e.g., "if still failing after 3 passes, flag to user")

**Gotcha specific to this shape:** Iterative workflows blow up token budgets fast. Each loop re-reads the whole output. If the loop is long, consider whether each iteration really needs full context, or just the diff from the previous iteration.

---

## Shape 4: Judgment-driven

Every step involves a judgment call, and the workflow is more about pattern-matching than executing a fixed sequence. Creative and strategic workflows usually live here.

**When to use this shape:** Step 2 produces a sequence, but Step 3 reveals that every single step has a judgment call — the workflow is really a series of decisions with execution attached.

**SKILL.md structure:**

Don't force a linear flow. Instead, organize by the framework the user uses to think about the task:

```
## the process

The workflow runs on a framework, not a fixed sequence. Apply the framework to the input:

## Framework: [Name]

Dimension 1: [What the user evaluates]
Dimension 2: [What the user evaluates]
Dimension 3: [What the user evaluates]

For each dimension, [action/decision].

## [Supporting concept 1]
## [Supporting concept 2]
```

**Examples of judgment-driven workflows:**
- Positioning angles: look at product → generate 5 angles → score each against ICP, novelty, believability → pick top 2.
- Editing voice: read draft → evaluate against voice rules → rewrite each violation → check rhythm and specificity.
- Creative direction: brief in → brainstorm against proposition types → apply novelty techniques → stress-test for surprise + shareability.

**Structural tip:** Shift weight from "sequence" to "framework." The SKILL.md should make the framework the centerpiece. Include 3-5 dimensions the user scores, with concrete rules for each.

**Gotcha specific to this shape:** These are the hardest workflows to turn into skills. The user's judgment is often compressed expertise built over years, and breaking it down into explicit criteria is painful. Budget more interview time — especially on Step 3 (decisions) — because this shape is 80% decisions and 20% execution.

---

## Picking the right shape — quick decision tree

```
Does the workflow run the same way every time?
├── YES → Linear
└── NO → Does the input determine which path runs?
    ├── YES → Branching
    └── NO → Does the user repeat steps until a quality bar is met?
        ├── YES → Iterative
        └── NO → Judgment-driven (every step has a decision)
```

If you're not sure, default to **Branching**. It's the most forgiving shape — a linear workflow is just a branching workflow with one path, and an iterative workflow is a branching workflow where one path loops back. Starting with branching gives you room to simplify later.

---

## Mixing shapes

Real workflows often combine shapes. That's fine. A workflow might be:

- **Linear overall, with one branching decision in the middle.** Still describe it as linear, but put the branch as a decision inside the relevant step.
- **Iterative with branches inside each iteration.** Describe the outer loop first, then the branches as steps within the loop.
- **Judgment-driven with a linear packaging step at the end.** Describe the judgment framework as the core, then add the linear packaging as Steps X, Y, Z at the bottom.

Don't force a pure shape when the workflow is genuinely hybrid. Users know their workflows better than the taxonomy does.

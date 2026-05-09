---
name: escrever-artigo
description: "Write long-form X/Twitter articles — tactical tutorials and breakdowns, not threads or single posts. Use when someone wants to turn a method, tool, or update into a walkthrough their audience can use in 15 minutes. Triggers on: write an X article, Twitter article, long-form X post, long-form for X, write a tutorial for X, breakdown for X, article about [tool/method] for Twitter/X. Use this skill even when the user doesn't say 'X article' — if they're writing a step-by-step walkthrough with copy-paste material intended for X/Twitter, this is the right tool. Reads the user's voice, audience, and CTA from CLAUDE.md or the project's `Context/` folder before writing. Outputs a publish-ready article with hook, numbered steps, copy-paste blocks, inline CTAs, and a hard closer."
---

# Article Writer (X/Twitter)

Most X articles die because they read like blog posts that accidentally ended up on Twitter. Dense paragraphs, no numbered steps, no copy-paste material, a "conclusion" that tells the reader what they just read.

The X articles that get passed around feel like a smart friend texted you a walkthrough. Numbered steps. Exact prompts you can copy. An analogy that makes the concept click. A direct "go do this right now" at the end.

This skill writes that.

---

## the core job

Produce a **publish-ready X/Twitter article** that:

- Opens with a hook that pays off in 2-4 sentences
- Walks the reader through an exact process they can copy
- Includes at least one copy-paste block (prompt, command, template)
- Lands with a direct push to take action
- Sounds like the user wrote it, not a content machine

**Output:** Full article in plain markdown, ready to paste into X's article editor.

---

## before starting: gather context

**STOP. Do not write until context is in hand. Cap questions at 2 max.**

### Step A: Gather context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan for:
   - **Voice** — tone, do/don't rules, sample sentences. The article must read like the user wrote it.
   - **Audience / ICP** — who the reader is, what they want, their vocabulary.
   - **Brand + CTA** — name, newsletter link, product, free asset they give away. Goes into the P.S. blocks.
2. **If missing, check the project folder** for `Context/voice.md`, `Context/icp.md`, `Context/business.md`. Read whichever exist.
3. **If voice is still missing:** flag it — "Voice samples are missing. I'll write in a neutral direct tone; paste 3-5 sentences in your voice to get a true match."

### Step B: Confirm the brief (≤2 questions, combined)

Skip anything context already covers. Combine into at most 2 questions:

1. **Topic + skeleton** — "What's the article about, and is this a Tutorial (here's how to set up / build X) or a Breakdown (here's what's new + what to do about it)?"
2. **Personal result or news hook** — "Do you have a specific result, number, or recent news that anchors this? (e.g. 'I went from X to Y in Z weeks' or '[Tool] just dropped [feature]')"

Never ask more than 2 questions. If the user's prompt already answered one, ask only what's missing.

---

## the process

```
PICK SKELETON → HOOK → BODY → COPY-PASTE → CTA → CLOSER → VOICE PASS → SHIP
```

The skeleton picks itself based on Step B answers. The hook is written first and stress-tested before anything else. Everything after follows the skeleton.

---

## Step 1: Pick the skeleton

Two skeletons cover almost every X article. Pick one.

### Skeleton A: The Tutorial

For "here's how to set up / build / do this exact thing" articles.

```
HOOK → Why it matters → What it does → What the output looks like →
How to use it → How to set it up (numbered steps) → Closer
```

### Skeleton B: The Breakdown

For "here's what changed and what to do about it" articles.

```
HOOK → Problem 1 (what's new → how it works → what to do with results) →
Problem 2 → Problem 3 → How to get started → Closer
```

For the detailed structure of each skeleton, section-by-section rules, and worked micro-examples, see [references/skeletons.md](references/skeletons.md).

---

## Step 2: Write the hook (first, always)

The hook is 2-4 sentences. It does one of three things:

| Type | Pattern | When to use |
|------|---------|-------------|
| **Personal result** | "I [specific action] [timeframe] and [concrete outcome]" | Tutorial with your own before/after |
| **News + gap** | "[Product/Feature] just dropped and most people missed it." | Breakdown of a recent release |
| **Direct value promise** | "The best [audience] all have the same secret weapon: [thing]." | Tutorial teaching a widespread-but-unknown method |

**Rules:**
- 2-4 sentences max. If it's 5+, cut.
- State the benefit in concrete terms.
- Make the reader feel they're about to get something usable TODAY.
- Never open with a rhetorical question, life story, "In this article," or suspense building.

**Stress test:** Read the hook alone. Would someone scroll past? If yes, rewrite before continuing.

---

## Step 3: Fill the body

Apply the chosen skeleton. Section-by-section rules live in [references/skeletons.md](references/skeletons.md). Two universal rules apply across both skeletons:

### Numbered steps, not bullets

Every "how to" section uses numbered steps. Each step:

- Starts with an imperative verb (Open, Click, Copy, Paste, Type, Set, Tell)
- Has 1-3 sentences under it, not a paragraph
- Includes an exact command/prompt in a code block when applicable
- Anticipates where people get stuck — add the fix inline

Example:
```
3. Paste this prompt into Claude:

"Write a landing page hero for [OFFER]. Audience: [ICP]. 
Tone: [VOICE]. Include a specific number result in the headline."

Swap the bracketed placeholders for your real values. 
Claude will complain if you leave them blank — that's fine, it means it's working.
```

### Copy-paste blocks are mandatory

Every X article must give the reader something they can literally copy. Use code blocks (```) for anything copy-pasteable. Introduce with one line: "Here's the exact prompt:" or "Copy this command:". After the block, tell them what to customize with `[PLACEHOLDER]` markers.

---

## Step 4: Add the CTAs (inline, P.S.-format)

Insert 1-2 mid-article CTAs and 1 closing CTA. Pull the exact CTA copy and URL from the business/brand context in CLAUDE.md (newsletter link, free offer, etc.). Format them as P.S. blocks so they feel like a friendly aside, not an ad break.

### Mid-article CTA (40-60% mark)

Pattern:
```
P.S. If you want [specific value promise], [get them / join here / sign up]: [URL]
```

### Closing CTA (end of article)

Pattern:
```
P.S. If you want more [specific content type]...
[specific promise + optional bonus]: [URL]
```

If no CTA exists in the business context, ask the user once: "Any newsletter or free asset URL you want to include?" If they say no, skip the P.S. blocks entirely — don't fabricate a URL.

---

## Step 5: Write the closer

Every article ends with a direct push to take action. No soft landings.

**Pattern:** [Direct instruction] + [urgency or payoff in one sentence]

**Good closers:**
- "Go set it up right now while you're still thinking about it. 15 minutes and you're in."
- "Pick your worst-performing X and run it. Come back to something that actually works."
- "Open a new tab, paste the prompt, see what happens."

**Bad closers (do not use):**
- "I hope you found this helpful"
- Summarizing the article
- Ending on a rhetorical question
- Fading out ("Anyway…")

---

## Step 6: Run the voice pass

Before shipping, check every section against the voice rules. The rules below are the critical subset — full list in [references/voice-rules.md](references/voice-rules.md).

### Fatal violations (cut immediately if found)

1. **Em dashes (—).** Zero. None. Use commas, periods, colons, semicolons, or parentheses.
2. **"Isn't X / Is Y" pattern.** All variations banned: "This isn't X. This is Y." / "Not X. Y." / "Less X, more Y." / "Everyone focuses on X. The actual thing is Y." Detection test: if a passage reduces to "thing A no, thing B yes" — kill it. Just state B directly.
3. **Dead closers.** "Let that sink in" / "Read that again" / "Full stop" / "This changes everything."
4. **Engagement bait.** "Are you paying attention?" / rhetorical questions as hooks.
5. **AI cringe.** "10x your productivity" / "Unlock/Harness/Leverage" / "Supercharge your workflow."
6. **Hollow intensifiers.** "Absolutely" / "Literally" / "Insane/Wild/Crazy" / "Game-changer."
7. **Staccato lists.** "No X. No Y. No Z." fragment patterns.
8. **Dramatic reveal setups.** "But here's where it gets clever:" / "Here's the kicker:"

### Required (must be present)

- **Feynman rule.** Any technical term gets a plain-language explanation in the same sentence. "state management changes, the code that controls how data moves through the app" — not "state management changes."
- **Flair.** Minimum 2 per article of: creative analogy, process compression, wry observation, vivid "imagine this," playful comparison, honest reaction, parenthetical aside, micro-narrative, self-deprecating flash, coined term.
- **Parenthetical asides.** 2-4 per piece. Real personality. Never put periods inside parentheses.
- **Rhythm.** 1-3 sentences per paragraph. Alternate explanation paragraphs with action steps. After dense sections, drop a short punchy line ("That's it." / "You're in.") to let the reader breathe.

---

## Step 7: Ship

Output the full article in markdown. Structure:

```markdown
[Hook — 2-4 sentences]

[Body per skeleton]

P.S. [Mid-article CTA]

[More body]

[Closer]

P.S. [Closing CTA]
```

No preamble from the skill ("Here's your article..."). Just the article itself, ready to paste.

---

## output format

The output is the article. Plain markdown. Ready to paste into X.

If anything from the business context is missing (testimonial names, specific numbers, product URLs), mark them `[PLACEHOLDER — needs real value]` so the user can see exactly what to fill in. Never fabricate.

---

## gotchas

The failure modes to catch before shipping:

1. **Writing the hook last.** Hooks wander when you write them after the body. Write the hook first, stress-test it, then commit.
2. **Bullet points instead of numbered steps.** Bullets read as "list of ideas." Numbers read as "exact order, do this then this." X articles need numbers.
3. **No copy-paste block.** The reader came for something to copy. No copy-paste = no reason to share. Minimum one per article.
4. **Copying the reader article's voice.** The reference article ([references/reference-article.md](references/reference-article.md)) is a structural study, not a voice template. Pull patterns (stacked analogies, origin story, results breakdown) — do NOT pull phrases or rhythms. Voice comes from the user's CLAUDE.md, not the reference.
5. **Banned patterns slipping in.** The "isn't X, is Y" construction is the single most common voice violation. Run the detection test on every sentence that contains "isn't" or "not" — if it reduces to "A no, B yes," rewrite.
6. **Em dashes.** They sneak in during "polish" rewrites. Final scan should specifically look for — and replace with , or . or :.
7. **Fabricated CTA URLs.** If the business context doesn't have a newsletter or free asset, skip the P.S. blocks. Don't invent "[name]@newsletter.com".
8. **Closer that summarizes.** "So in summary..." is dead. The closer is a kick in the butt to go do the thing. One direct instruction + urgency.
9. **Sections that explain instead of show.** When explaining a method, the "what the output looks like" section should show a real example (even a short one) before the steps. Readers trust examples more than descriptions.
10. **Tutorial with no personal grounding.** The hook's "personal result" pattern only works if there's a real personal result. If the user hasn't done the thing themselves, use News + Gap or Direct Value Promise instead.

---

## the test

Before shipping, verify each:

1. **Hook earns the second sentence.** Reader would keep reading after line 1.
2. **Numbered steps, not bullets** in every "how to" section.
3. **At least one copy-paste block** with a clear `[PLACEHOLDER]` marker.
4. **2+ pieces of flair** (analogy, aside, coined term, wry observation, etc.) across the article.
5. **Zero em dashes.** Full-text scan confirms.
6. **Zero "isn't X, is Y" constructions.** Run the detection test.
7. **Feynman passes** — every technical term has a plain-language gloss.
8. **Closer is a direct instruction**, not a summary.
9. **CTAs present** (or confirmed skipped because no URL exists).
10. **Reads like the user wrote it.** Compare one paragraph to a sample from their voice context. Match rhythm and word choice.

**Failure condition:** If any banned pattern appears or the article reads like a generic AI newsletter — it failed. Return to Step 6 and rewrite the flagged sections.

---

## how this connects to other skills

**Feeds into this skill:**
- `entrevista-negocio` — captures voice, ICP, brand + CTA into CLAUDE.md. Having that loaded makes Steps A-B trivial.
- `pesquisa-keywords` — surfaces topic ideas and the exact language the ICP uses.
- `afiar-ideia` — sharpens the angle before drafting.

**This skill feeds into:**
- `humanizar-texto` — run as a final voice pass before posting.
- `reaproveitar-conteudo` / `vibe2-content-atomizer` — turn the article into LinkedIn, newsletter, thread, and YouTube variants.

**Adjacent:**
- `post-longo-x` — for shorter long-form posts (500-3000 chars) rather than full articles.
- `escrever-newsletter` — for email newsletters; different structure, different energy (more personal, fewer numbered steps).

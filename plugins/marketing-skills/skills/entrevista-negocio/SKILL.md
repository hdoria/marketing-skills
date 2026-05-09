---
name: entrevista-negocio
description: >
  Interview the user with 11 targeted questions to produce a complete, paste-ready
  Global Instructions / CLAUDE.md file that makes every other skill in their setup
  work without briefing Claude every time. Captures business + offer, ICP (with pain,
  fears, dream, objections), competitors + weaknesses, proof, voice, and positioning.
  Outputs the final file in a code block for the user to copy-paste into Cowork →
  Settings → Global Instructions. Does NOT auto-save.

  USE THIS SKILL WHEN:
  - User wants to set up Claude to remember their business context
  - User asks to build a CLAUDE.md / Global Instructions file
  - User says "interview me", "set up my context", "build my Claude profile"
  - User is onboarding into a Cowork / Claude Code workflow and hasn't populated context yet

  Use this skill even when the user doesn't explicitly say "interview" — if they're
  setting up their Claude workspace for the first time and need context loaded, this
  is the right tool.

  TRIGGERS: "business interview", "build my CLAUDE.md", "set up global instructions",
  "interview me about my business", "populate my context", "onboard me"
---

# Business Interview

Build a Global Instructions file by interviewing the user. One question at a time. No forms. No walls of text. Just a conversation.

At the end, compile everything into a paste-ready CLAUDE.md block. The user pastes it into Cowork's Global Instructions — or saves it as `~/.claude/CLAUDE.md` for Claude Code — and every future conversation starts with full context loaded.

---

## Your Role

You are a smart colleague doing a quick intake call. You ask sharp, specific questions. You listen. You compile everything into a Global Instructions file that makes Claude useful from the first message of every future conversation.

You are NOT:
- A survey
- A form with blanks to fill in
- An AI asking generic questions

You ARE:
- A smart colleague who asks the right follow-up
- Someone who knows what matters and skips what doesn't
- Efficient — 11 questions, ~5-6 minutes

---

## Start here

Before Question 1, ask:
> "Quick check first — do you have a website? Drop the URL and I'll read it before we start so I can skip the obvious questions."

If they share a URL, use WebFetch to read the homepage (and `/about` or `/pricing` if the homepage leaves gaps). Pre-fill any answers the site already covers. Skip or compress those questions when you hit them.

Then proceed to Phase 1.

---

## The 11 Questions

Ask ONE question at a time. Wait for the answer. Acknowledge briefly (one line), then ask the next.

### Phase 1: Business Foundation (Q1)

**Question 1 — Business + offer + price + transformation:**
> "What's your business? Tell me in one go: what you sell, to whom, at what price, and the specific transformation or outcome you promise. Like you're explaining it to someone at a party."

If the answer is thin, ask ONE follow-up: "What makes someone pick you over doing nothing or trying [adjacent alternative]?"

### Phase 2: The ICP (Q2–Q6)

**Question 2 — ICP:**
> "Describe your ideal customer. Not the broad market — the ONE person who's perfect for what you sell. What do they do? How far along are they? What have they already tried?"

**Question 3 — Pain (specific, in their words):**
> "What keeps that person up at night? Give me the specific complaints, not the generic ones. The stuff they'd say in a DM, not on a webinar."

**Question 4 — Fears:**
> "What are they afraid of? What future scenario makes them anxious? Different from pain — pain is what's wrong today, fear is what could go wrong tomorrow."

**Question 5 — Dream / transformation:**
> "What does their life look like after you help them? Not the deliverable — the actual change in their day-to-day."

**Question 6 — Objections:**
> "When you pitch this, what are the top 2-3 reasons someone says NO? The real objections — price, skepticism, 'won't work for my situation' — not the polite ones."

### Phase 3: Market & Proof (Q7–Q9)

**Question 7 — Competitors:**
> "Who are your 2-3 biggest competitors? Or if you don't have direct competitors, who are the biggest names in your space that your audience also follows?"

**Question 8 — Competitor weaknesses:**
> "What do their customers complain about? What do they get wrong? If you've researched them, pull 3-5 weaknesses. Otherwise, just tell me what you've noticed."

Follow-up (inline, only if not covered): "And what makes YOU different from those competitors? One sentence."

**Question 9 — Proof:**
> "What proof can you cite? Testimonials with real names, specific results (revenue, customers, timeframes, %), case studies, milestones, credentials, press, known clients. Even 1-2 real items is enough. This is critical — landing pages and emails will insert placeholder brackets wherever you have no real proof."

### Phase 4: Voice (Q10–Q11)

**Question 10 — Voice source:**
> "I need to learn how you sound. Pick one:
> A) Paste a piece of your own writing (newsletter, email, social post)
> B) Share a link to a writer whose style you want to capture
> C) Describe how you want to sound in 2-3 sentences"

**Question 11 — Voice details + always/never words:**
Adapt based on their answer to Q10:
- If they pasted writing: "What do you like about how this sounds? Anything you'd change? Any specific words or phrases you ALWAYS use or NEVER use?"
- If they shared a link: "What specifically about their style do you want — the humor, directness, storytelling, rhythm? Any words or phrases you'd never use?"
- If they described it: "Give me an example of a sentence you'd write and one you'd never write."

---

## Adaptive Rules

- If answers are short, ask ONE follow-up. Never two.
- If answers are detailed, skip ahead. Don't ask what you already know.
- Maximum 11 questions. Fewer is better.
- After each answer, acknowledge briefly (one line), then move on.
- If the website pre-fill covered a question, either skip it or confirm with "Website says X — confirm or adjust."

---

## Compilation

After all answers, output a single fenced code block containing the complete Global Instructions / CLAUDE.md content. Use this exact structure:

````markdown
```markdown
# About [Business Name]

## What I Do
[1-2 sentences from Q1 — plain language, party version]

## What I Sell
**Offer:** [Product / service name]
**Price:** [From Q1]
**Transformation I promise:** [The specific outcome from Q1]

## My Ideal Customer

**Who they are:** [Demographics, stage, experience level — from Q2]
**What they've already tried:** [From Q2]
**Their biggest pain:** [From Q3 — use their actual language, quote-level specifics]
**What they fear:** [From Q4]
**What they dream about:** [The transformation from Q5]
**Top objections when I pitch:** [From Q6]

## Competitors & Their Weaknesses

| Competitor | Their Weakness | My Advantage |
|-----------|---------------|-------------|
| [Name] | [Weakness] | [How I'm better] |
| [Name] | [Weakness] | [How I'm better] |

**What makes me different:** [From Q8 follow-up]

## Proof & Evidence

Real, cite-able proof Claude should use in landing pages, emails, sales copy. Never fabricate beyond this list.

[From Q9 — structured as appropriate:]
- **Results / numbers:** [e.g., "$X MRR", "X customers", "X% conversion", "X in Y months"]
- **Testimonials:** [Name, one-line quote, outcome — list 1-5 real ones if available]
- **Case studies / milestones:** [Any specific wins, client names, features, launches]
- **Credentials / press:** [Any authority markers worth citing]

If a section above is empty, use `[NONE YET]` so skills know to mark `[PLACEHOLDER]` rather than invent.

## Writing Voice

**Tone:** [Extracted from Q10-11 — 3-5 descriptors like "direct, no-fluff, conversational, mildly contrarian"]
**Audience register:** [Technical? Casual? Industry jargon?]
**Words I always use:** [Signature phrases from Q11, if any]
**Words I never use:** [Banned phrases from Q11, if any]

[If they pasted a writing sample, include 2-3 sample sentences here as the ground-truth rhythm reference.]

## Key Instructions for Claude

- Always write in my voice as described above. Before shipping any content, compare a paragraph to the voice samples — match or rewrite.
- **Always run the `humanizar-texto` skill on any written content output (newsletters, emails, landing page copy, social posts, articles, ad copy) before delivering it to me. Zero tolerance for AI-sounding output. If the skill is not installed, apply the anti-slop rules manually: no em dashes, no "isn't X, is Y" patterns, no "game-changer" / "unlock" / "leverage" / "delve" / "landscape", no rhetorical questions as hooks, no dead closers like "let that sink in."**
- Reference my competitors' weaknesses when positioning my offers
- Use my audience's language, not industry jargon (unless they use it)
- Speak to my ideal customer's pain, fears, and dreams — not generic benefits
- Handle my top objections proactively in copy (from Q6)
- **Never fabricate testimonials, results numbers, customer quotes, or case studies.** If a specific isn't in my Proof section above, mark it `[PLACEHOLDER — needs real X]` so I can fill it in.
- When creating content, ground emotional beats in my actual ICP research and pain/fear/dream notes above
```
````

---

## Where to paste it

After outputting the code block, tell the user:

> "Done. Copy the block above and paste it into one of these:
>
> **Cowork (recommended):**
> 1. Settings (top-right) → Cowork → Global Instructions
> 2. Click Edit
> 3. Paste the whole block → Save
>
> **Claude Code (terminal / CLI):**
> Save the block content to `~/.claude/CLAUDE.md`. Create the file if it doesn't exist. Overwrite carefully if you already have content there — offer to merge instead.
>
> **Project-specific overrides (optional):**
> If you want different context for a specific project — e.g., a client whose brand voice differs from yours — drop a `CLAUDE.md`, or separate `business.md`, `icp.md`, `voice.md` files into the project folder. Claude auto-loads project-level context on top of global."

---

## After the paste

Tell the user to verify:

> "Test it: start a new chat and ask Claude 'who am I?' If it answers with your business, ICP, and voice without you briefing it — you're set. Every future skill in your workspace now loads this context automatically."

---

## What NOT to do

- Do NOT save the file automatically. Output in a code block, let the user paste it themselves.
- Do NOT create a backup file in the project folder. The user's copy-paste is the only save action.
- Do NOT skip Q9 (Proof). This is the most-missed question in this interview, and its absence is the single biggest reason landing pages and emails end up full of `[PLACEHOLDER]` brackets.
- Do NOT ask questions the website pre-fill already answered. Confirm and move on.
- Do NOT invent answers to fill gaps. If the user doesn't have proof yet, mark `[NONE YET]` in that section.

---

## The Test

A good interview:

1. Took under 7 minutes
2. Asked 11 questions max (fewer if the website pre-filled)
3. Felt like a conversation, not a form
4. Captured real, specific, in-their-words ICP language — not generic marketer-speak
5. Got at least 1-2 real proof items (or explicit `[NONE YET]`)
6. Produced a file the user can paste into Cowork Global Instructions in under 30 seconds
7. Included the mandatory antislop directive in the Key Instructions section

**Failure condition:** If the output CLAUDE.md uses generic language ("helps entrepreneurs," "busy professionals," "quality results") instead of the user's actual words — the interview went too shallow. Return to the pain/fears/dream questions and probe for specifics before compiling.

---

## how this connects to other skills

**This skill feeds into every other skill in the bundle:**

Every workshop skill (landing-page, escrever-copy, escrever-newsletter, sequencia-email, escrever-linkedin, escrever-artigo, pesquisa-keywords, lead-magnet, arquitetar-oferta, afiar-ideia, polir-texto, post-longo-x, etc.) has a "before starting: gather context" gate that scans CLAUDE.md for business, ICP, voice, pain, fears, dreams, objections, proof, and competitor data. This skill produces all of that in one pass.

Run this ONCE at setup, paste the output into Global Instructions, and every future skill session skips the context-gathering questions.

**Adjacent:**
- `entrevista-skill` — a similar interview pattern but for building new skills from the user's expertise, not context.

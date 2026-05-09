# Worked Example — Interview Transcript → Resulting SKILL.md

A complete run of this interview, from opening question to final packaged skill. Use this as a shape reference when running your own interview.

The example below captures a fictional user named "Sam" — a solo product marketer at a mid-sized SaaS — who wants to turn their weekly "customer voice digest" workflow into a skill.

---

## The opening question

> **Interviewer:** What's the one task you want to capture? In plain language, one sentence.
>
> **Sam:** Every Friday I go through our support tickets, sales call notes, and Intercom conversations from the week and pull out customer language we should use in marketing copy.

---

## Step 1 — Scope

> **Interviewer:** Great. Four quick questions:
> 1. In one sentence — what does this workflow do?
> 2. What makes you start it? (recurring calendar, request, something else?)
> 3. What does "done" look like?
> 4. Who'll use the skill — just you, or teammates too?
>
> **Sam:**
> 1. It produces a weekly "customer voice digest" — direct quotes and patterns from customer conversations, categorized for the copywriting and product teams to use.
> 2. It's on my calendar every Friday at 2pm. Block for 90 minutes.
> 3. Done = a Notion page with 4 sections: Top 3 recurring objections, Top 3 desired outcomes, 5-8 verbatim quotes tagged by theme, one "quote of the week" we can use in ads.
> 4. Me and two copywriters on the team. They read it, they don't run it.

**Captured:**

- `description` triggers: "weekly customer voice digest," "pull customer quotes from tickets," "voice of customer report"
- Output format: Notion page with 4 named sections
- Trigger: calendar-based, every Friday
- Users: the workflow runner + 2 downstream readers

---

## Step 2 — Sequence

> **Interviewer:** Walk me through the last time you did this — step by step.
>
> **Sam:** OK so I open the Zendesk dashboard and filter tickets from the past 7 days. Then I open the Gong library and pull up calls from that same window. Then I...
>
> **Interviewer:** Hold on — "open Zendesk and filter tickets." What do you actually do once the tickets are filtered? Read every one?
>
> **Sam:** No, I sort by word count descending — long tickets are usually where the good stuff is. I read the top 20. Then I paste any good sentence into a scratchpad doc.
>
> **Interviewer:** What makes a sentence "good"?
>
> **Sam:** Has to sound like the customer, not like me. If it uses their own phrasing for a pain point or a desire, it goes in. Generic complaints like "this is broken" get skipped.
>
> **Interviewer:** Got it. Keep going.
>
> **Sam:** Then Gong — I watch the first 5 minutes of every call. That's where the "problem statement" usually comes out. Transcript view, I highlight any line where the prospect says "we're trying to..." or "the issue is..." Paste to scratchpad.
>
> Then I open Intercom — I search the week's chats for specific words: "frustrated," "wish," "can't," "why." Usually finds 10-20 hits. Good quotes go in.
>
> Once the scratchpad has 30-50 raw quotes, I open the Notion template. I group quotes by theme — usually 4-6 themes surface. I pick the top 3 objections and top 3 desired outcomes. I pick the best 5-8 verbatim quotes tagged by theme. Finally I pick one "quote of the week" — the most vivid one, usually short.

**Probe deeper triggered twice** (on "open Zendesk," on "good sentence"). In both cases, the deeper answer was the actual workflow detail.

**Captured sequence:**

```
ZENDESK → GONG → INTERCOM → SCRATCHPAD → THEME → NOTION PAGE
```

**Step-level detail:**

| Step | What | Time |
|------|------|------|
| 1. Zendesk pass | Filter 7 days, sort by word count, read top 20, extract quotes | 15 min |
| 2. Gong pass | Last 7 days, watch first 5 min of each, highlight "we're trying to..." | 25 min |
| 3. Intercom pass | Search week for keywords (frustrated/wish/can't/why), extract | 15 min |
| 4. Scratchpad | Paste raw quotes, aim for 30-50 | (rolling) |
| 5. Theme grouping | Group quotes by theme, identify top 3 objections + top 3 outcomes | 15 min |
| 6. Notion page | Fill template: 4 sections + quote of the week | 15 min |

---

## Step 3 — Decisions

> **Interviewer:** Where in the sequence do you make judgment calls?
>
> **Sam:** Mostly when I decide what's a "good" quote. Like I said, it has to sound like the customer. But also:
> - Objections are things they said NO or "not yet" because of. Desired outcomes are things they said YES or "if only" about. If a quote is both, it's actually about a missing feature — I route it to product, not marketing.
> - Quote of the week: it has to be vivid AND specific to one persona. If it sounds like "anyone could've said this," skip it.
> - Themes: if I only find 1-2 quotes on a theme, I don't include that theme. Needs at least 3 quotes to be a pattern.
>
> **Interviewer:** What if a quote doesn't clearly fit one of those buckets?
>
> **Sam:** I tag it "uncategorized" in the scratchpad and come back at the end. If there are 5+ uncategorized quotes, that often means there's a new theme emerging — I'll add a 7th theme or flag it for the product team.

**Captured decision rules:**

| Decision | Criteria |
|----------|----------|
| Include a quote? | Customer voice (not paraphrase) + specific to a pain or desire, not generic |
| Objection vs outcome? | "NO because..." → objection. "YES if..." or "wish I had..." → outcome. Both? → product feature, route separately |
| Include a theme? | ≥3 quotes on that theme |
| Quote of the week? | Vivid + specific to one persona (not generic) |
| Emerging theme alert? | 5+ uncategorized quotes = new pattern, flag separately |

---

## Step 4 — Tools and artifacts

> **Interviewer:** What tools do you open? Any templates or scripts?
>
> **Sam:** Zendesk, Gong, Intercom, Notion, plus a Google Doc scratchpad. The Notion page has a template — I literally duplicate last week's and clear the content. It's called "VOC Digest Template" in our workspace.
>
> No scripts. But I do have a saved filter in Zendesk ("past 7 days, sorted by word count desc") and a saved search in Intercom for the four keywords.

**Captured artifacts:**

- **Reference files to bundle:** The Notion template structure (can be captured as markdown).
- **No scripts** needed, but the saved filters/searches should be documented so Claude can reproduce them.
- **External tools** the skill needs awareness of: Zendesk, Gong, Intercom, Notion. Skill will prompt user to paste content (since API access is out of scope for a v1).

---

## Step 5 — Quality checks

> **Interviewer:** Before you publish the digest, what do you check?
>
> **Sam:**
> - Every quote is in direct-speech form. No "the customer was frustrated that..." Only "I was so frustrated that..."
> - Every theme has at least 3 quotes under it.
> - Quote of the week is under 30 words.
> - At least one quote is negative (objection) — if the whole digest is positive outcomes, I missed something.
> - Every quote has the source (Zendesk ticket #, Gong call, or Intercom chat) — so if copy uses it, we can verify.
>
> **Interviewer:** What would make you throw it out and restart?
>
> **Sam:** If I only got 10 or fewer total quotes. That usually means I rushed one of the three sources. Below 20 total, I go back and do another pass on whichever source I skimmed.

**Captured test:**

1. Every quote is in direct-speech voice (no paraphrase)
2. Every theme has ≥3 quotes
3. Quote of the week is ≤30 words
4. At least one negative quote appears
5. Every quote has a source tag (ticket/call/chat ID)
6. Total quote count is ≥20

**Failure condition:** If total quotes <20 — the digest failed. Return to whichever source was under-sampled and run another pass.

---

## Step 6 — Failure modes

> **Interviewer:** Common mistakes?
>
> **Sam:**
> 1. Paraphrasing instead of copying verbatim. It's tempting when you remember the gist but not the exact words. If it's paraphrased, it's useless — the whole point is *their* language.
> 2. Picking quotes that sound good but came from 1 person. A "theme" with 1 quote is just one person's opinion.
> 3. Skipping Gong because it takes longest. Gong has the best quotes because prospects aren't typing — they're thinking out loud. Skipping it hollows out the digest.
> 4. Missing the negative. Our marketing team uses these quotes too literally — if everything is positive, they write copy that sounds like our customers have no problems, which reads as fake.
> 5. Letting "quote of the week" drift into generic. The vivid, specific ones always outperform the polished ones.
>
> **Interviewer:** Anything Claude would probably get wrong by default?
>
> **Sam:** Probably smoothing out the language. Customers say "it was hella annoying." Claude's instinct is to write "users found the experience frustrating." No. Keep the voice.

**Captured gotchas:** 6 concrete failure modes, all specific and actionable.

---

## Step 7 — Template

> **Interviewer:** What's the final Notion page structure?
>
> **Sam:**
>
> ```
> # VOC Digest — Week of [Date]
>
> ## Top 3 Objections
> 1. [Theme name]
>    > "[Verbatim quote]" — [source]
>    > "[Verbatim quote]" — [source]
>    > "[Verbatim quote]" — [source]
> 2. ...
> 3. ...
>
> ## Top 3 Desired Outcomes
> 1. [Theme name]
>    > "[Verbatim quote]" — [source]
>    > "[Verbatim quote]" — [source]
>    > "[Verbatim quote]" — [source]
> 2. ...
> 3. ...
>
> ## Quote Bank (5-8 tagged by theme)
> - **[Theme tag]:** "[Quote]" — [source]
> - **[Theme tag]:** "[Quote]" — [source]
> - ...
>
> ## Quote of the Week
> > "[Vivid, specific quote, ≤30 words]"
> > — [Persona], [source]
> ```

**Captured:** Exact template, verbatim.

---

## Step 8 — Package

**8a. Opinionated intro drafted:**

> "Most customer voice reports die because they're paraphrased. Someone skims 50 tickets, summarizes in their own words, and hands marketing a doc that sounds exactly like any other marketing doc. The quotes that actually convert are the ones customers actually said — verbatim, with the rough edges intact."

**8b. Size check:** Estimated ~280 lines for SKILL.md + inline template. No references/ split needed.

**8c. Description:**

> "Generate a weekly customer voice digest from support tickets, sales calls, and chat transcripts — extracting verbatim customer language organized by theme. Use when a product marketer, PMM, or copywriter needs to pull 'voice of customer' data for marketing copy, positioning, or product feedback. Triggers on: customer voice digest, voice of customer report, extract customer quotes, VOC digest, pull quotes from tickets. Use this skill even when the user doesn't say 'VOC' — if they want to aggregate what customers have been saying this week for marketing use, this is the right tool. Outputs a Notion-ready markdown page with Top 3 Objections, Top 3 Desired Outcomes, a tagged quote bank, and one Quote of the Week."

**8d. Save location:** User chose `~/.claude/skills/voc-digest/`.

---

## Final SKILL.md (excerpt)

The generated skill file — shortened here to the key sections. Full file lives at the saved path.

```markdown
---
name: voc-digest
description: "Generate a weekly customer voice digest from support tickets, sales calls, and chat transcripts — extracting verbatim customer language organized by theme. Use when a product marketer, PMM, or copywriter needs to pull 'voice of customer' data for marketing copy, positioning, or product feedback. Triggers on: customer voice digest, voice of customer report, extract customer quotes, VOC digest, pull quotes from tickets. Use this skill even when the user doesn't say 'VOC' — if they want to aggregate what customers have been saying this week for marketing use, this is the right tool. Outputs a Notion-ready markdown page with Top 3 Objections, Top 3 Desired Outcomes, a tagged quote bank, and one Quote of the Week."
---

# VOC Digest Builder

Most customer voice reports die because they're paraphrased. Someone skims 50 tickets, summarizes in their own words, and hands marketing a doc that sounds exactly like any other marketing doc. The quotes that actually convert are the ones customers actually said — verbatim, with the rough edges intact.

This skill runs the weekly extraction across three sources, groups by theme, applies inclusion rules, and ships a Notion-ready digest.

---

## the core job

Produce a weekly VOC digest with 4 sections: Top 3 Objections, Top 3 Desired Outcomes, a tagged quote bank of 5-8 verbatim quotes, and one Quote of the Week.

**Output:** A markdown document in the exact template below, ready to paste into Notion.

---

## before starting: gather context

**STOP. Do not produce a digest until the raw material is in hand. Cap questions at 2 max.**

### Step A: Get the raw material

Ask the user to paste content from each source:
1. **Zendesk tickets** — past 7 days, sorted by word count desc, top 20
2. **Gong call transcripts** — past 7 days, first 5 minutes of each
3. **Intercom chats** — past 7 days, searching for "frustrated," "wish," "can't," "why"

### Step B: Confirm the week (≤1 question if needed)

Ask: "What week are we covering? (date range)" — only if not obvious from context.

---

## the process

```
EXTRACT (3 sources) → SCRATCHPAD → THEME → TEMPLATE → CHECK → SHIP
```

---

## Step 1: Extract

From each source, pull any sentence that:
- Uses the customer's own phrasing (NOT paraphrase)
- Names a specific pain, objection, or desired outcome
- Is NOT generic ("this is broken" = skip)

Keep source tags (ticket ID, call ID, chat ID) on every quote.

### Framework: the "keep or skip" rule

| Keep if the quote... | Skip if the quote... |
|----------------------|----------------------|
| Uses customer's own words | Is a paraphrase or summary |
| Names specific pain or desire | Is generic or vague |
| Has texture (emotion, detail) | Is neutral or transactional |

### Anti-pattern
Paraphrasing. If you can't quote it verbatim, leave it out.

---

## Step 2: Scratchpad

Collect 30-50 raw quotes across all three sources before theming.

If total is <20, the extraction missed a source. Go back.

---

## Step 3: Theme

Group quotes by theme. Rules:

- A theme needs ≥3 quotes to qualify
- Objections = "NO because..." or "not yet because..."
- Desired outcomes = "wish I had..." or "YES if..."
- Feature requests (both pain AND asked-for solution) go to product, not the digest

If 5+ quotes end up uncategorized, that's an emerging theme. Flag it separately.

---

## Step 4: Template fill

Apply the exact template [...full template inline...]

---

## Step 5: Check

Before shipping, verify:

1. Every quote is in direct-speech voice (no paraphrase)
2. Every theme has ≥3 quotes
3. Quote of the week is ≤30 words
4. At least one negative quote appears
5. Every quote has a source tag
6. Total quote count is ≥20

**Failure condition:** If total quotes <20 — return to Step 1 and re-extract from the under-sampled source.

---

## output format

[Exact template from Step 7 of interview, verbatim]

---

## gotchas

1. **Paraphrasing instead of copying verbatim.** The whole point is *their* language. If you can't quote it exactly, leave it out.
2. **Themes with only 1-2 quotes.** That's one person's opinion, not a pattern. Need 3+ per theme.
3. **Skipping Gong because it's slow.** Gong has the best quotes because prospects think out loud. Skipping it hollows out the digest.
4. **All-positive digest.** If every quote is a desired outcome, you missed something. At least one negative required.
5. **Polished "quote of the week."** Vivid and specific beats polished. Let the rough edges show.
6. **Smoothing customer language.** "Hella annoying" stays "hella annoying." Don't translate to "frustrating."

---

## the test

1. Every quote is in direct-speech voice
2. Every theme has ≥3 quotes
3. Quote of the week is ≤30 words
4. At least one negative quote
5. Every quote has a source tag
6. Total quote count ≥20

**Failure condition:** Total quotes <20 — return to Step 1.

---

## worked example

[One complete fictional run of the workflow, with extracted quotes, themed sections, and final output.]
```

---

## What to notice about this run

1. **Probing happened 3 times** (Step 2 twice, Step 5 once). Each probe surfaced a detail that would've been missing otherwise — the word-count sort, the "customer voice" criterion, the ≥20 threshold.
2. **Judgment calls were made explicit.** Sam's original answer was "I pick what's good." The probe extracted the actual if/then criteria.
3. **The worked example in the final skill uses Sam's real examples.** Nothing was fabricated — everything came from the interview.
4. **The SKILL.md ended up ~280 lines.** No references/ split needed. But if the template had been more complex or the worked example longer, it would've split naturally.
5. **The description is "pushy."** Includes the "Use this skill even when the user doesn't say 'VOC'" line so the skill triggers on adjacent phrasings.

That's the full shape of an interview run. Use this as the pattern when running your own.

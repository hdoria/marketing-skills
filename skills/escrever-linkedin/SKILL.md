---
name: escrever-linkedin
description: >
  Repurpose YouTube videos, blog articles, guides, or raw insights into high-performing LinkedIn posts
  that sound like the user wrote them. STEP-BY-STEP, interactive process — never output a complete
  LinkedIn post immediately. Each step presents options, waits for the user to pick, then progresses.
  Reads voice, ICP, and offer context from CLAUDE.md or the project's `Context/` folder; asks the
  user to fill gaps if context is thin.

  USE THIS SKILL WHEN:
  - User shares a YouTube link and wants a LinkedIn post
  - User shares a blog article URL and wants a LinkedIn post
  - User provides an insight, idea, or document and wants a LinkedIn post
  - User mentions "LinkedIn post", "repurpose for LinkedIn", "turn this into a LinkedIn post"
  - User says "LinkedIn content", "write a post", "create a post"
  - User pastes a transcript and wants LinkedIn content
  - User asks to create social content from a video, article, or idea

  Use this skill even when the user doesn't explicitly say "LinkedIn" — if they share source
  material (transcript, article, notes) and want a social post that walks readers through an
  insight or tutorial, this is the right tool.

  TRIGGERS: "LinkedIn post", "LinkedIn content", "repurpose", "write a post", "post about",
  "turn this into a post", "create a LinkedIn post", "LinkedIn from YouTube", "LinkedIn from blog"
---

# LinkedIn Writer

You are the user's LinkedIn content strategist. Your job: take source material (YouTube videos, blog articles, guides, or raw insights) and walk the user through a structured, collaborative process to create a LinkedIn post that sounds authentically like them.

This is an **iterative, step-by-step process**. You never skip steps or output a finished post without going through each stage. At most steps, you present multiple options (typically 10) so the user can choose the direction.

The reason this process exists: great LinkedIn posts aren't just summaries. They're strategically crafted pieces with a clear audience outcome, the right structural framework, and a hook that stops the scroll. Rushing to a finished post skips the thinking that makes a post perform.

---

## before starting: gather context

**STOP. Do not begin the process until voice, ICP, and offer context are in hand. Cap questions at 2 max.**

### Step A: Scan context (fast)

1. **Check CLAUDE.md first.** Claude auto-loads `~/.claude/CLAUDE.md` and any project-level `CLAUDE.md`. Scan what's loaded for three things:
   - **Voice** — tone, do/don't rules, signature phrases, sample sentences. The post must sound like the user wrote it.
   - **ICP** — who the audience is, their pain, their phrases. Every outcome and hook must land for THIS audience.
   - **Offer / business** — what the user sells, their positioning, any newsletter or community for CTAs. Step 5 uses this for optional CTAs.
2. **If missing, check the project folder** for `Context/voice.md`, `Context/icp.md`, `Context/business.md` (or similar). Read whichever exist.
3. **Check for post samples.** If the user has previous LinkedIn posts saved anywhere obvious (e.g., `Context/linkedin-examples.md`, a `posts/` folder), read them — they're the best voice reference there is.

### Step B: Ask ≤2 questions to fill gaps

Only ask about what context didn't cover. Combine into AT MOST 2 questions. Priority order:

1. **Voice + post samples** — "I don't see voice context. Can you paste 3-5 of your previous LinkedIn posts so I can match your voice?" (This is the single most important input. If the user has no previous posts, ask them to describe their tone in 1-2 sentences + paste 3-5 sentences in their voice from anywhere.)
2. **ICP + offer** — "Who's the audience for this post in one line, and what (if anything) are you selling that a CTA could point to?"

Skip both questions if CLAUDE.md already covered them. Never ask more than 2.

If the user has no offer, that's fine — skip CTAs in Step 5. Never fabricate.

---

## the process

```
SCAN CONTEXT → SOURCE INTAKE → ANALYZE → 10 OUTCOMES → 4 FRAMEWORKS → 10 HOOKS → WRITE → ITERATE
```

Seven steps after context gathering. Wait for the user to choose at each decision point before moving on.

| Step | What happens | User chooses from |
|---|---|---|
| 0 | Get source material | — |
| 1 | Analyze content internally | — |
| 2 | Suggest audience outcomes | 10 options |
| 3 | Suggest writing frameworks | 4 frameworks with skeletons |
| 4 | Suggest hooks | 10 options |
| 5 | Write the post | Artifact for iteration |

**Golden rule:** Never skip a step. Never combine steps. Never output a finished post before Step 5. The process exists because each decision builds on the last.

---

## Step 0: Source Intake

Figure out what the source material is and get the full content.

**Priority: use provided data first.** The user will typically paste a transcript, article text, notes, or other content directly. Do NOT try to scrape or fetch external data if the user has already given you the content. Only reach out to external sources when the user gives you a URL without accompanying text.

### When the user provides content directly (most common)

- Read and acknowledge the content
- Give a brief 1-2 sentence summary of what it covers
- Move on — no need to fetch anything

### When the user provides just an insight or idea

- Acknowledge the idea and summarize it back to confirm understanding
- This is valid input — not everything needs a source document

### When the user provides only a URL (no text content)

Follow this priority order:

**For YouTube links:**
1. **Apify MCP (preferred)** — if available:
   ```
   Call tool: call-actor
   Parameters: {
     "actorId": "topaz_sharingan/Youtube-Transcript-Scraper-1",
     "input": { "url": "<youtube-url>" }
   }
   ```
   Then retrieve results with `get-actor-output` or `get-dataset-items`.
2. **Fallback** — if Apify is not available, ask the user to paste the transcript.

**For blog/article links:**
1. **Apify MCP (preferred)** — if available:
   ```
   Call tool: call-actor
   Parameters: {
     "actorId": "apify/web-scraper",
     "input": { "startUrls": [{ "url": "<article-url>" }] }
   }
   ```
2. **WebFetch fallback** — use the WebFetch tool to grab the page.
3. **Manual fallback** — ask the user to paste the article text.

**Never scrape LinkedIn profiles or posts.** If the user mentions LinkedIn content as a source, ask them to paste the text directly.

### Confirm source material

After getting the content, give a brief 1-2 sentence summary and confirm before moving to Step 1.

---

## Step 1: Content Analysis

Before suggesting outcomes, analyze the source material internally. Identify:
- The core themes and ideas
- Specific stories, data points, or examples that stand out
- Angles that could resonate with the ICP from your gathered context
- Any personal experiences or unique perspectives in the material

Don't present this analysis to the user in detail — use it to inform Step 2. Just let them know you've analyzed and you're ready to suggest outcomes.

---

## Step 2: Define Main Outcome for the Audience

The purpose of this step: decide *what the reader should take away from this post*. Every good LinkedIn post has a clear outcome — it changes how they think, feel, or act. Source material often contains multiple possible angles, and choosing the right one is what separates a forgettable post from one that resonates.

Use the ICP context you gathered (voice.md / CLAUDE.md / user-provided ICP) to shape these outcomes.

**Present 10 options to the user.** Each option:
- **Main outcome** (1 sentence): what the reader walks away thinking, feeling, or doing
- **Angle** (1 sentence): the specific lens or approach to get there
- **Secondary outcome** (optional, 1 sentence): an additional benefit the reader gets

Format clearly numbered 1-10. Make them genuinely different — don't rephrase the same idea 10 ways. Pull from different themes in the source material, different audience segments, and different emotional triggers (fear, ambition, permission, curiosity, practical execution).

**One post = one idea with depth.** When the user picks a main outcome plus secondaries, weave the secondaries in as subtle undertones — not standalone sections. The post should hammer the main outcome with depth. Trying to give equal weight to 4-5 ideas turns a punchy LinkedIn post into a shallow blog post.

**Wait for the user to choose before moving on.**

---

## Step 3: Define Writing Framework

Present the four frameworks below with a brief description of *how this specific post would flow* under each. The point is NOT to write the post — it's to show how the structure would organize the ideas so the user can pick the right one.

For each framework, write 3-5 bullet points describing what each section of the post would cover for this specific topic and outcome. Skeleton, not draft.

### The Four Frameworks

**PAS — Problem, Agitation, Solution**
Best for: posts where the audience has a clear pain point that needs to be surfaced and intensified before offering resolution. Works well when the reader might not fully realize the depth of their problem.

**AIDA — Attention, Interest, Desire, Action**
Best for: posts that need to build momentum from curiosity to action. Works well for announcing something, sharing a discovery, or when you want the reader to take a specific step.

**CPF — Context, Problem, Framework**
Best for: posts where you need to set the scene first. Works when the topic requires background or when the problem only makes sense in a specific context. Good for more educational, nuanced posts.

**BAB — Before, After, Bridge**
Best for: transformation stories. Paint where the reader is now, show where they could be, bridge the gap. Works brilliantly for personal stories and case studies.

**Present all four as options.** Describe what the post structure would look like for the chosen outcome. Skeleton bullets only.

Pull style cues from [references/style-patterns.md](references/style-patterns.md) — match the framework to the style patterns that fit the user's voice. If the user's voice is direct and contrarian, PAS or BAB usually hits harder than AIDA. If the voice is educational and thoughtful, CPF or AIDA fits.

**Wait for the user to choose before moving on.**

---

## Step 4: Define the Hook

**Before this step, read [references/hook-templates.md](references/hook-templates.md) thoroughly.** It has 80+ hook templates organized by category with psychological triggers. This is the most important reference for this step.

The hook is the single most important element of a LinkedIn post. It determines whether people keep reading or scroll past. On LinkedIn, only the first ~2 lines are visible before "see more" — the hook must earn that click.

**Brevity is everything.** Great hooks are SHORT — often under 15 words for the first line. They hit hard and stop the scroll. If a hook needs a paragraph to land, it's not a hook.

**Present exactly 10 hook options.** Each hook:
- Short and punchy — 1-2 lines max
- Stays focused on the main outcome chosen in Step 2 (every hook serves the same core idea, just from different angles)
- Ready to use as-is — no leftover `[BRACKETS]`

**How to use hook-templates.md — critical:**

The templates are fill-in-the-blank structures with placeholders like `[owned asset]`, `[desirable outcome]`. When presenting hooks:
1. Pick a template
2. Show the original template structure so the user can see which one you're using
3. Fill in the brackets with specifics from the source material and the user's context
4. The result should follow the template's exact sentence structure — not just be "loosely inspired"

For example, if the template is:
```
I [achieved desirable outcome] in just [short time frame].
I also [additional related outcome].
```

Then the hook should literally follow that structure:
```
[Concrete result from user's actual experience] in just [specific timeframe].
It also [real additional outcome].
```

Do NOT paraphrase the template into something "vaguely similar." The templates work because their specific structures are psychologically proven. Use them literally.

When selecting templates, match to:
- The **outcome** defined in Step 2
- The **framework** chosen in Step 3
- The **ICP's** pain points and desires (from context)
- The **post type** (insight, tutorial, story, success share, contrarian take)

Hooks should feel like the user wrote them — pattern-interrupting, no fluff, specific. Never leave generic placeholders — every hook should be ready to publish.

**Wait for the user to choose before moving on.**

---

## Step 5: Write the Post

**Before writing, MUST re-read [references/style-patterns.md](references/style-patterns.md) — even if you read it earlier.** Earlier reads inform strategy; this read is about absorbing the structural rhythm right before you write. If you skip this re-read, the post will drift into generic AI rhythm.

**Also re-scan the user's voice context.** Pull up whatever voice samples, CLAUDE.md rules, or previous post examples you gathered. Your job is to match THAT voice — not the style-patterns defaults where the user's voice differs.

Now write the full LinkedIn post. **Open it as an artifact** (create an `.md` file) so the user can see it and iterate with you.

### The Hook-to-Body Connection

This is where posts most commonly fail. The hook and the body must flow as one continuous thought — not two pieces stitched together.

The hook delivers the "what." The very next line should be the reader's natural next thought. Ask: "If someone just read this hook out loud, what would I naturally say next?"

**Common mistakes to avoid:**
- Re-explaining the hook in different words (reader already read it — move forward)
- Abruptly jumping to a different topic ("Great hook about X... anyway, here's Y")
- Starting the body with backstory when the hook already set up the story

See style-patterns.md section 6 for the flow pattern with an example.

### Writing Rules — Style Match

These rules apply on top of the user's voice. Details and examples are in [references/style-patterns.md](references/style-patterns.md) — the summary:

**Sentence length and rhythm (the #1 AI tell if violated):**
- Average sentence: 7-12 words. 20+ word sentences get broken up.
- Every new thought gets its own line — no exceptions.
- Fragments are good when they land.

**Structure & formatting:**
- 1-2 sentences per paragraph, then a line break
- Arrow bullets (`↳` or `➝`), never `-` or `•`
- Bold Unicode (`𝗕𝗼𝗹𝗱`) sparingly for section headers within the post
- 150-300 words total (LinkedIn sweet spot)
- End with a soft CTA or question
- Optional: comment-based engagement hook ("Comment [X] to get [Y]") — only if the user has a real resource to offer (from offer context)

**Tone & voice:**
- Match the user's voice context
- Direct, confident, never hedging
- Conversational — like telling a smart friend what happened
- "I" and "you" freely
- Vulnerability and real experience where natural — from the user's actual history, not invented
- No corporate jargon or buzzwords

**Flow:**
- Each line is the logical next thought
- Transitions are invisible — if you need a "Now let's talk about..." header, you're covering too many ideas
- Standalone transition words work sparingly: "Why?" / "The result?" / "Here's what happened:"

**What NOT to do:**
- Don't use hashtags in the post body (3-5 at the very bottom, separated by a line, if at all)
- Don't use emojis excessively (1-2 max, only at the end or CTA if they add something)
- Don't start with "I'm excited to share..." or any LinkedIn cliché
- Don't write walls of text
- Don't sound like AI — no "In today's fast-paced world," no "Let's dive in," no "game-changer," no "landscape"
- Don't over-explain — trust the reader's intelligence
- Don't use regular bullet points
- Don't cram multiple ideas into explicit sections — one idea with depth, secondaries as undertones
- Don't bolt the body onto the hook — they must flow as one continuous piece
- Don't fabricate numbers, testimonials, or personal stories the user hasn't provided. If a claim needs a number and the context doesn't have one, use `[PLACEHOLDER — needs real number]`.

### After Writing

Present the post in an artifact. Then ask:
- How does this feel? Want to adjust tone, length, or emphasis?
- Should we sharpen any section?
- Want to try a different hook from the ones we explored?

Be ready to iterate. The first draft is a starting point.

---

## gotchas

The failure modes to catch before delivering:

1. **Skipping the context gate.** If you start Step 0 before scanning CLAUDE.md and asking the ≤2 gap questions, every later step is guessing at voice. The post will sound generic.
2. **Asking more than 2 context questions.** The gate is ≤2. If the user has to answer 5 questions before seeing options, they bail. Combine — voice+samples in one question, ICP+offer in the other.
3. **Skipping steps to "save time."** Every step feeds the next. Jumping from Step 0 to Step 5 produces a generic summary post. The process is the product.
4. **10 outcomes that are all the same idea.** Step 2 fails when all 10 options are rephrased versions of one angle. Pull from different themes, segments, and emotional triggers.
5. **Hooks that paraphrase the template.** Hook templates work because their exact sentence shapes are proven. "Loosely inspired" hooks lose the psychological effect. Follow the structure literally.
6. **Bolting the body onto the hook.** The most common post failure. Read hook and line 2 aloud — if line 2 is a restatement of the hook, or jumps topic, rewrite.
7. **Walls of text.** Any paragraph over 2 sentences in the final post is a structural failure. Break it up.
8. **Fabricating numbers, testimonials, or stories.** If the user's context doesn't have the specific, use `[PLACEHOLDER — needs real X]`. Invented specifics destroy trust.
9. **AI-cliché openers.** "In today's fast-paced world," "Let's dive in," "I'm excited to share" — all instant credibility killers.
10. **Finishing without the iterate offer.** The first draft is rarely final. Always ask after writing: feel right? sharpen? try a different hook?

---

## the test

Before delivering the final post, verify:

1. **Context was gathered** — voice, ICP, offer either from CLAUDE.md or ≤2 user questions.
2. **All 5 decision steps ran** — source, analysis, 10 outcomes picked, 4 frameworks picked from, 10 hooks picked from.
3. **Hook is under 15 words (first line)** and pattern-interrupting.
4. **Hook and body flow as one thought** — line 2 extends the hook, doesn't restate or jump.
5. **Sentence rhythm matches style-patterns.md** — average 7-12 words, every thought on its own line.
6. **Arrow bullets used (↳ or ➝)** — no `-` or `•`.
7. **150-300 words total.**
8. **Voice matches the user's samples** — read one paragraph alongside a user voice sample. Match or miss?
9. **No fabricated specifics** — every number, name, and story came from the user's context.
10. **No AI clichés** — scan for "In today's," "Let's dive in," "game-changer," "landscape," "unlock," "harness."

**Failure condition:** If the post reads like a generic AI summary of the source — it failed. Return to Step 5 and pull harder from the user's voice samples. If voice samples are thin, go back to the context gate and ask for more.

---

## how this connects to other skills

**Feeds into this skill:**
- `entrevista-negocio` — captures voice, ICP, offer into CLAUDE.md. Having that loaded makes the context gate trivial.
- `afiar-ideia` — sharpens the angle before drafting the 10 outcomes.

**This skill feeds into:**
- `humanizar-texto` — optional final voice pass before posting.
- `reaproveitar-conteudo` / `vibe2-content-atomizer` — turn one LinkedIn post into a thread, newsletter, tweet, and YouTube short.

**Adjacent:**
- `post-longo-x` — for longer-form X/Twitter posts with different structural patterns.
- `escrever-newsletter` — for email newsletters (different energy, more personal, fewer numbered steps).
- `escrever-artigo` — for long-form X/Twitter articles (tutorials and breakdowns).

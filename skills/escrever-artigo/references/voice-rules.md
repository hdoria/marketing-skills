# Voice Rules (Full)

The complete voice guardrails for X/Twitter articles. SKILL.md covers the critical subset; this file covers everything, plus the "humanity layer" that makes an article sound human.

Load this during Step 6 (voice pass).

---

## Part 1: Fatal violations

Any of these kill the article. Scan every draft before shipping.

### Em dashes: absolute zero

Never use the em dash character (—) anywhere in the article. Not in prose, not in lists, not in CTAs. Period.

Replace with:
- Comma — for parenthetical asides with no emphasis shift
- Period — for a hard stop
- Colon — when the second clause explains the first
- Semicolon — when joining two independent clauses (use sparingly)
- Parentheses — for actual asides

Detection tip: Em dashes hide in "polish" rewrites. After every edit pass, do one specific search for `—` and replace.

### The "Isn't X / Is Y" pattern: fatal

All variations banned:
- "This isn't X. This is Y."
- "Not X. Y."
- "Forget X. This is Y."
- "Less X, more Y."
- "The constraint has nothing to do with X. It's Y."
- "It's less about X and more about Y."
- "X isn't the hard part. Y is."
- "Everyone focuses on X. The actual thing is Y."
- "This is no longer X. This is Y."

**Detection test:** If a passage reduces to "[thing A] no, [thing B] yes" — it's this pattern. Cut it. Just state B directly.

**Why this matters:** The pattern is an AI tell. It creates fake contrast that does no real work. A confident writer states the thing. The AI dresses it up with a negated strawman first.

**Bad:**
> This isn't just a prompt. This is a full workflow.

**Good:**
> This is a full workflow. The prompt is one piece of it.

### Generic insider claims

"Here's the part nobody's talking about" / "What nobody tells you" / "The thing everyone misses" — all banned. These promise insider knowledge and deliver common knowledge. They make the reader trust you less, not more.

Replace with the actual insight, stated directly.

### Dead closers

Cut all of these:
- "Let that sink in"
- "Read that again"
- "Full stop"
- "This changes everything"
- "Game over"
- "The end"

They're designed to make ordinary claims feel profound. They do the opposite.

### Engagement bait

- "Are you paying attention?"
- "Still with me?"
- "Did you catch that?"
- "Most people don't understand this..."
- Rhetorical questions used as hooks or transitions

### Hollow intensifiers

- "Absolutely"
- "Literally" (when not literal)
- "Insane" / "Wild" / "Crazy" / "Mind-blowing"
- "Game-changer" / "Revolutionary"
- "Next-level" / "Cutting-edge"

These are filler. Remove them and the sentence almost always gets stronger.

### AI cringe phrases

- "10x your productivity" / "10x your [anything]"
- "Unlock your potential" / "Unlock [anything]"
- "Harness the power of [anything]"
- "Leverage [anything]" (use "use")
- "Supercharge your workflow"
- "Transform your [anything]"
- "Seamless integration"
- "Robust solution"
- "Streamline your process"

### Staccato fragment lists

- "No X. No Y. No Z."
- "Not this. Not that. Not the other."

Rapid-fire fragments signal "AI is trying to sound punchy." Replace with a real sentence.

### Negation runway

- "Not a wireframe. Not a suggestion. A page."
- "Not a list. Not a guide. A system."

Three-part escalating negations land like a movie trailer narrator. Cut the first two clauses, keep the last as a regular sentence.

### Dramatic reveal setups

- "But here's where it gets clever:"
- "Here's the kicker:"
- "Plot twist:"
- "And here's the thing:"
- "But wait, there's more:"

Cut the setup. Just state the thing.

---

## Part 2: Soft bans

These aren't fatal but weaken the article. Fix when you see them.

- Starting multiple consecutive sentences with the same word
- Rhetorical questions inside paragraphs (used for emphasis rather than genuine questions)
- Corporate verbs: "improved," "enhanced," "facilitated," "optimized," "enabled"
- Passive voice where active works
- Weasel words: "quite," "rather," "somewhat," "perhaps"

---

## Part 3: Required — the humanity layer

The article must sound human. These elements are not optional.

### Conversational hedges

When genuinely thinking through something, use:
- "Kinda"
- "I feel like"
- "Probably"
- "I'm not totally sure but"
- "Honestly"
- "tbh"

Hedges coexist with declarative boldness on real takes. You can be confident about your method and hedge about whether one edge case applies.

**Good:**
> The autoresearch method works on anything you can score. I'm not totally sure how it holds up on creative work where "score" is vibes, but for anything with a rubric it's solid.

### Sentence fragments (used right)

Fragments that complete a thought in a punchy way are fine. Fragments that stack into staccato lists are not.

**Fine:**
> Then he tested it. And it worked.

**Not fine:**
> No setup. No training. No onboarding.

### Parenthetical asides (signature move)

2-4 per article. Real personality bleeding through. Never put periods inside parentheses.

**Three types:**

**Editorial commentary:**
> which, fine, nobody actually needs yet, but it's cool

**Self-aware humor:**
> it took me 4 hours, which is longer than just doing it manually, but that's not the point

**Honest reactions:**
> and I say that as someone who's been burned by AI demos before

### Flair moments

Minimum 2 per article. Pick from:

- **Creative analogy** — "Think of it like teaching a new hire vs hiring a contractor"
- **Process compression** — "Open the file, paste the prompt, close the tab. Done."
- **Wry observation** — "which, sure, is technically what the docs say, but nobody does that"
- **Vivid "imagine this"** — "Imagine a version of you that never checks email before 10am"
- **Playful comparison** — "It's less Swiss Army knife, more one-trick pony that does the trick really well"
- **Honest reaction** — "I read it three times before I understood it. Which is unusual for me"
- **Micro-narrative** — 2-3 sentence story that illustrates the point
- **Absurdly specific detail** — "Last Tuesday at 2am, I ran this for the 14th time"
- **Self-deprecating flash** — "which, fair, is the kind of over-engineering I usually make fun of"
- **Coined term** — name a concept the reader doesn't have a name for yet ("the staircase of credibility")

### The Feynman rule

Every technical term gets a plain-language gloss in the same sentence. Never assume the reader knows jargon. Never talk down.

**Good:**
> state management changes, the code that controls how data moves through the app

**Good:**
> autoresearch is just running the same skill over and over, scoring each run, and keeping changes that improved the score

**Bad:**
> state management changes (left unexplained)

**Bad:**
> As you know, state management is... (talking down)

### Rhythm rules

- 1-3 sentences per paragraph. Default is 1-2.
- Alternate explanation paragraphs with action steps/code blocks.
- After dense sections, drop a short punchy line to let the reader breathe: "That's it." / "You're in." / "Easy."
- Never stack more than 3 short paragraphs without a visual break (list, code block, header).

---

## Part 4: Voice self-check (run before finishing)

Eight-question check. Answer honestly. Any NO = rewrite the flagged section.

1. Could a generic AI newsletter have written this? If yes, rewrite.
2. Do the first 2-3 sentences make the reader feel something (curiosity, recognition, surprise)?
3. At least one creative analogy or personality moment present?
4. Sounds like a smart friend, not a blog post?
5. No banned patterns (scan every sentence)?
6. Zero em dashes (—)?
7. No fabricated credentials or numbers?
8. All jargon explained inline (Feynman rule)?

---

## Part 5: When to break a rule

The rules above are defaults, not commandments. Sometimes the right move is to break one on purpose.

**You can break a rule when:**
- Breaking it is clearly funnier or more vivid than following it
- Breaking it lands a specific point the rule-compliant version can't land
- The user's voice context explicitly calls for it (e.g., voice.md says "I use em dashes in my casual posts")

**You cannot break a rule when:**
- You're tired of the constraint
- You "kinda feel like" it would be better
- The rule feels too strict
- You want to sound smart

Rule-breaking is a choice with a reason. Rule-breaking by accident is a voice failure.

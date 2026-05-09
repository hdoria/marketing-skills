# Worked Example — Hook Writing for a Real Topic

Complete run of the skill on a realistic scenario: a founder wants to hook a long-form post about why AI SDR tools will collapse in 2026.

---

## Step 0 — Context gathering

```
User: "write me a hook for my post about why AI SDRs won't work"

Claude: STOP — before I write, I need 5 things confirmed:

1. Topic / source material — paste the post, the argument, or the URL.
2. The angle — what's the specific take?
3. Audience — who's this for?
4. Content type — how-to, critique, case study, data, prediction, cultural?
5. Emotional goal — shock, intrigue, FOMO, discovery, authority, validation?
```

User answers:

```
1. Topic: AI SDR tools (Clay, Apollo AI, Artisan, etc.)
2. Angle: They'll all collapse in 2026 because every SaaS adds the same AI SDR features as a checkbox. The standalone tools lose their moat.
3. Audience: B2B SaaS founders and RevOps leaders on X.
4. Content type: Market prediction / takedown.
5. Emotional goal: Shock + authority — "I saw this coming before you did."
```

---

## Step 1 — Read the pattern library

Claude skims `references/hook-examples.md` for patterns matching:
- Content type: prediction / takedown
- Emotional goal: shock, authority

Candidate patterns:

- **The Ominous Four Words** — ultra-short foreboding opener
- **The Contrarian Takedown** — "X is a scam" / "X is dying"
- **Insider Rumor / Industry Shift** — "the [category] is dying"
- **Annual Predictions** — numbered bold claims about a year
- **Bold Claim + Timeline Forecast** — prediction with a date
- **Shocking Statistic Lead** — if there's a number to anchor

Shortlist: Contrarian Takedown, Industry Shift, Annual Predictions, Bold Claim + Timeline, Ominous Four Words.

---

## Step 2 — Match and draft 5 variations

### Option 1 — Contrarian Takedown ("The [Category] is Dying")

```
Every AI SDR tool will be dead by 2026.

Not because they don't work. Because every SaaS will ship the same features natively and the standalone tools lose their only moat.

Here's how it plays out:
🧵
```

### Option 2 — Annual Prediction

```
2026 B2B prediction: The AI SDR category collapses.

Clay, Apollo AI, Artisan — every standalone AI SDR tool loses 70% of its market when HubSpot, Salesforce, and Pipedrive add the same features as a free checkbox.

The ones still standing in 12 months will look nothing like today.
🧵
```

### Option 3 — Ominous Four Words

```
The moat just closed.

Every AI SDR tool you paid $2k/month for in 2025 is about to become a feature toggle inside the CRM you already own.

Here's what that means for your stack — and what I'd build instead.
🧵
```

### Option 4 — Bold Claim + Timeline

```
By Q4 2026, half of today's AI SDR tools will be out of business.

Clay will survive. Apollo will survive. The 40+ copycat startups? Dead — because Salesforce just added the same features to every plan.

The winners from here are the ones nobody's watching.
🧵
```

### Option 5 — Insider Rumor / Industry Shift

```
Quiet signal most B2B founders missed this week:

HubSpot shipped AI SDR features natively. Salesforce announced the same thing 10 days ago. Pipedrive is next.

The standalone AI SDR category has ~12 months.
🧵
```

---

## Step 3 — Pressure-test

| Checklist item | Opt 1 | Opt 2 | Opt 3 | Opt 4 | Opt 5 |
|----------------|-------|-------|-------|-------|-------|
| Stops scroll in <2s | ✓ | ✓ | ✓ | ✓ | ✓ |
| Specific curiosity | ✓ | ✓ | ✓ | ✓ | ✓ |
| Bold defensible claim | ✓ | ✓ | ✓ | ✓ | ✓ |
| Concrete details | ✓ | ✓ (names tools) | weaker | ✓ (names tools + Q4) | ✓ (names 3 CRMs) |
| First sentence strongest | ✓ | ✓ | ✓ | ✓ | weaker |
| No filler / hedges | ✓ | ✓ | ✓ | ✓ | ✓ |
| Pattern from library | ✓ | ✓ | ✓ | ✓ | ✓ |
| Passes "so what?" | ✓ | ✓ | ✓ | ✓ | ✓ |

All 5 ship. Slight edits: Option 3's hook is strong but the body tease is vaguer than the others. Option 5's opener "Quiet signal..." is softer than the others — OK for a different audience but weaker for shock goal.

---

## Step 4 — Recommendation

**Recommended: Option 4 (Bold Claim + Timeline).**

Why: the audience is B2B SaaS founders who respond to specific, datable predictions over general takedowns. "By Q4 2026, half of today's AI SDR tools will be out of business" names a date AND a scale in 12 words. The body tease ("Clay will survive... 40+ copycat startups dead") gives concrete names on both sides of the bet, which founders screenshot and re-share. Shock goal hit with authority backing.

Backup: Option 2 if the user wants to lean harder into the predictions-list format for thread structure.

---

## Notes for Claude running this skill

- Don't stop at 3 options if the topic clearly has 5 strong patterns. But don't force 5 if only 3 really fit.
- When patterns stack (e.g., Contrarian + Timeline), that's fine — just name both patterns in the label.
- The user's voice always wins over the pattern's original phrasing. Adapt the template to their voice, don't paste the creator's line as-is.
- Always include the recommendation. Users want a verdict, not a menu.

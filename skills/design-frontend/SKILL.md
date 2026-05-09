---
name: design-frontend
description: "Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks to build web components, pages, artifacts, posters, or applications (examples include websites, landing pages, dashboards, React components, HTML/CSS layouts, or when styling/beautifying any web UI). Triggers on: build me a landing page, create a website, design a dashboard, make this look better, style this page, build a UI for X. Generates creative, polished code and UI design that avoids generic AI aesthetics."
---

# Frontend Design

Most AI-generated interfaces look the same. Purple gradients, Inter font, rounded cards on white backgrounds. You've seen it a thousand times. It's the visual equivalent of "In today's fast-paced world."

This skill builds frontend interfaces that look like a human designer made them — distinctive, opinionated, and built with real working code.

---

## the core job

Produce **working frontend code** (HTML/CSS/JS, React, Vue, etc.) that is:
- Production-grade and functional
- Visually striking and memorable
- Cohesive with a clear aesthetic point-of-view
- Meticulously refined in every detail

**Output:** Complete, working code files ready to open in a browser or deploy.

---

## before starting: gather context

**STOP. Do not write any code until all context fields below are confirmed with the user. Ask for any missing fields before proceeding. Even if the user gives a vague request like "build me a landing page," you must clarify these fields first.**

1. **What are you building?** — Component, page, full app? What does it need to do? (determines scope and tech)
2. **Who is it for?** — Audience and purpose. A dashboard for developers looks different from a landing page for a yoga studio. (drives the aesthetic)
3. **What's the vibe?** — Pick a direction: brutally minimal, maximalist chaos, retro-futuristic, organic/natural, luxury/refined, playful/toy-like, editorial/magazine, brutalist/raw, art deco/geometric, soft/pastel, industrial/utilitarian — or something else entirely. (sets the tone for every decision)
4. **Technical constraints?** — Framework preference (plain HTML, React, Vue), must-have features, performance requirements, accessibility needs. (prevents rework)
5. **Any references?** — Websites, screenshots, brands, moods they like. "I want it to feel like Apple" is useful info. (calibrates expectations)

---

## the process

```
DIRECTION → PALETTE → STRUCTURE → BUILD → REFINE → DELIVER
```

---

## Step 1: Commit to a direction

Before writing a single line of CSS, choose a bold aesthetic direction and commit to it fully.

**Ask yourself:**
- **Purpose**: What problem does this interface solve? Who uses it?
- **Tone**: Pick an extreme from the vibe options. Not "clean and modern" — that's not a direction, that's a default.
- **Differentiation**: What's the one thing someone will remember about this design?

**CRITICAL**: Bold maximalism and refined minimalism both work — the key is intentionality, not intensity. Choose a clear conceptual direction and execute it with precision.

**Anti-pattern:** Don't default to "clean, modern, minimal" every time. That's not a design decision. That's the absence of one.

---

## Step 2: Choose the palette

Every design decision flows from the palette — colors, fonts, spacing philosophy.

### Typography
Choose fonts that are beautiful, unique, and interesting. Pair a distinctive display font with a refined body font.

**NEVER use:** Arial, Inter, Roboto, system fonts, or any generic stack. These are the default of defaults.

**DO use:** Google Fonts, Adobe Fonts, or self-hosted fonts that match the aesthetic. A serif heading font with a sans body. A monospace display font for a tech vibe. Something unexpected.

### Color & Theme
Commit to a cohesive palette. Use CSS variables for consistency.

**Rule:** Dominant colors with sharp accents outperform timid, evenly-distributed palettes. Pick a strong background, a text color, and one accent. That's enough to start.

**NEVER use:** Purple gradients on white backgrounds, the default blue link color unmodified, or any palette that looks like a Bootstrap template.

### Spacing
Decide upfront: generous whitespace or controlled density? Both work. Mixing them doesn't.

---

## Step 3: Build the structure

Plan the layout before building components.

### Spatial Composition
Think beyond centered-content-in-a-container:
- Unexpected layouts
- Asymmetry
- Overlap
- Diagonal flow
- Grid-breaking elements
- Generous negative space OR controlled density

### Component Architecture
- Break the page into logical sections
- Each section has a clear purpose
- Plan the responsive behavior upfront (not as an afterthought)

**Anti-pattern:** Don't build a standard hero → features → testimonials → CTA layout unless the user specifically asks for it. That's a template, not a design.

---

## Step 4: Build with craft

Write the actual code. This is where the aesthetic vision meets implementation.

### Motion & Animation
- Use animations for effects and micro-interactions
- Prioritize CSS-only solutions for HTML projects
- Use Motion library for React when available
- Focus on high-impact moments: one well-orchestrated page load with staggered reveals (animation-delay) creates more delight than scattered micro-interactions
- Use scroll-triggering and hover states that surprise

### Backgrounds & Visual Details
Create atmosphere and depth rather than defaulting to solid colors:
- Gradient meshes
- Noise textures
- Geometric patterns
- Layered transparencies
- Dramatic shadows
- Decorative borders
- Custom cursors
- Grain overlays

### Code Quality
- Production-grade: no placeholder content, no TODO comments
- Accessible: proper semantic HTML, ARIA labels, keyboard navigation
- Responsive: works on mobile, tablet, desktop
- Performant: optimized images, minimal JS, efficient CSS

---

## Step 5: Refine the details

The difference between good and great is in the details nobody consciously notices but everyone feels.

**Refinement checklist:**
- [ ] Typography: line heights, letter spacing, font sizes feel balanced
- [ ] Colors: contrast ratios pass WCAG AA (4.5:1 for text)
- [ ] Hover states: every interactive element has a considered hover effect
- [ ] Focus states: keyboard users can navigate with visible focus rings
- [ ] Transitions: state changes are smooth (200-300ms)
- [ ] Loading: content doesn't jump around as it loads
- [ ] Scroll: scroll behavior feels intentional (scroll-margin-top on anchors)
- [ ] Selection: custom ::selection color that matches the palette
- [ ] prefers-reduced-motion: animations respect user preferences
- [ ] Mobile: touch targets are 44px minimum, text is readable without zooming

---

## Step 6: Deliver

Present the finished code with context.

**Output format:**
```
## [Project Name]

**Direction:** [The aesthetic chosen and why]
**Tech:** [Framework/stack used]
**Fonts:** [Display + Body fonts]
**Palette:** [Primary, secondary, accent colors]

[Complete working code]

**Design decisions:**
- [Key choice 1 and why]
- [Key choice 2 and why]
- [Key choice 3 and why]
```

---

## the rules

**Match implementation complexity to the aesthetic vision.** Maximalist designs need elaborate code with extensive animations and effects. Minimalist or refined designs need restraint, precision, and careful attention to spacing, typography, and subtle details. Elegance comes from executing the vision well.

**NEVER converge on common choices across builds.** Vary between light and dark themes, different fonts, different aesthetics. No two designs should look related unless the user asks for consistency.

**Interpret creatively.** Make unexpected choices that feel genuinely designed for the context. Claude is capable of extraordinary creative work. Don't hold back.

---

## the test

A good frontend build:

1. **Has a clear point-of-view** — Someone can describe the aesthetic in 2-3 words. If it just looks "clean and modern," it has no point-of-view.
2. **Avoids the AI look** — No Inter font, no purple gradients, no rounded-card-on-white-background defaults. If it looks like every other AI-generated UI, it failed.
3. **Works on every screen** — Responsive isn't optional. Test at 375px, 768px, and 1440px minimum.
4. **Sweats the details** — Hover states, focus rings, transitions, scroll behavior, selection color. The small things separate craft from code.
5. **Runs clean** — No console errors, no layout shifts, no broken images, no placeholder text left behind.
6. **Matches the brief** — The user's vibe and purpose are reflected in every choice. A playful kids' app shouldn't look like a banking dashboard.

If someone opens the page and says "oh, that's nice" with genuine surprise — it worked.

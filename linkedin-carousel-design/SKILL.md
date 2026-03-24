---
name: linkedin-carousel-design
description: Design and generate LinkedIn carousel posts (PDF document posts) for Tejinder Singh's AI expertise brand. Use this skill whenever the user asks to create a carousel, design slides, build a LinkedIn PDF post, make a swipeable post, create carousel content, or mentions "carousel", "slides", "LinkedIn PDF", "document post", or "swipeable post". Also trigger when the user asks to convert any post content into visual carousel format, or wants to batch-produce carousels for their 100-post LinkedIn series. This skill covers the complete pipeline — content structure, visual design system, HTML rendering, PDF export, and quality checks.
---

# LinkedIn Carousel Design System — Tejinder Singh

This is the master design skill for creating LinkedIn carousel posts that people actually SHARE — not just save and forget.

---

## THE THREE RULES THAT OVERRIDE EVERYTHING

Before reading a single design spec, internalize these. They are the reason this skill exists:

**Rule 1: People share what makes THEM look smart — not what makes YOU look smart.**
A carousel that teaches someone "how to use Perplexity" gets saved. A carousel that says "Your company is bleeding money on tools your intern could replace" gets shared — because the person sharing it looks like the smart one who found it. Every carousel must pass this test: "If someone reposts this, what does it say about THEM to their network?"

**Rule 2: The design must be recognizable before readable.**
If someone scrolling at speed can't tell it's a Tejinder Singh carousel before reading a single word, the design has failed. This means owning a visual signature so distinctive that copying it would feel like plagiarism. The dark+serif+accent template that every AI influencer uses is a costume, not a brand.

**Rule 3: Information doesn't travel. Emotion does.**
Nobody has ever reposted a step-by-step tutorial because the steps were well-numbered. They repost because the carousel made them feel something — called out, vindicated, challenged, surprised, or understood. Every carousel needs a moment of emotional friction.

---

## PART 1: THE VISUAL IDENTITY

### Why We're Breaking From the Dark Template

The "dark background + editorial serif + single accent color + grain texture" look was pioneered by Ruben Hassid and a few others in 2023-2024. By 2026, it has been copied by thousands of AI creators. It signals "AI content" — not "Tejinder Singh." Using it makes you invisible in the exact category you're trying to own.

The new direction: **Warm, high-contrast, signature-color-led.** Not cold and dark. Not clinical and techy. Warm, human, and unmistakably yours.

### The Signature Color: Deep Saffron

```
SIGNATURE:             #E85D04   (deep saffron — warm, bold, unique in the AI space)
```

Why saffron: Every AI carousel uses pink, yellow, electric blue, or neon green as their accent. Nobody owns warm orange-saffron. It's bold without being aggressive. It reads as confident and approachable — which is exactly how Tejinder should feel. And it's deeply tied to South Asian identity without being overt about it. When someone sees this color in their feed, they'll learn to associate it with one person.

### Full Color System

```
── DARK MODE (Primary — 70% of carousels) ──────────────────
BACKGROUND:            #141218   (deep ink — warm undertone, NOT cool black)
SIGNATURE:             #E85D04   (deep saffron — THE brand color)
SIGNATURE LIGHT:       #F4A261   (warm amber — secondary accent, used sparingly)
PRIMARY TEXT:           #EEEBE4   (warm cream — softer than white)
SECONDARY TEXT:         #9B978E   (warm grey — body copy, descriptions)
TERTIARY TEXT:          #5C5852   (dim warm — page numbers, fine print)
SURFACE:               #1E1B24   (card/panel backgrounds — subtle lift from bg)
DIVIDERS:              #2A2630   (barely-there structure lines)

── LIGHT MODE (30% of carousels — for variety) ─────────────
BACKGROUND:            #FAF7F2   (warm paper — not sterile white)
SIGNATURE:             #D4520A   (deeper saffron on light — maintains punch)
PRIMARY TEXT:           #1A1814   (warm near-black)
SECONDARY TEXT:         #5C5852   (warm mid-grey)
SURFACE:               #F0EDE6   (subtle card lift)
DIVIDERS:              #E0DCD4
```

**Rules:**
- Alternate between dark and light mode across posts (roughly 70/30). This prevents visual fatigue AND makes each post feel fresh while staying on-brand. The signature saffron works on both
- Saffron is used on the ONE most important element per slide. Never two things. If everything glows, nothing glows
- No pure black (#000) or pure white (#FFF) anywhere — the warm undertones are what make this feel human and premium
- No gradients, no glows, no shadows. Flat, confident, editorial

### Typography System

```
DISPLAY / HEADLINES:   Sora — Bold or ExtraBold (700/800)
                       Modern geometric sans-serif. Clean but has character.
                       Wider letterforms than typical sans — feels confident, not cramped.
                       Size: 38–56px depending on word count

BODY / DESCRIPTIONS:   Sora — Regular or Medium (400/500)
                       Same family as headlines — creates cohesion.
                       Size: 16–20px. Line-height: 1.45

LABELS / EYEBROWS:     Sora — SemiBold (600)
                       All-caps. Letter-spacing: 2–4px.
                       Size: 11–13px

ACCENT / HANDWRITTEN:  Caveat — Bold (700)
                       THE secret weapon. A handwritten font used for:
                       → Annotations ("this is the part everyone skips")
                       → Emotional beats ("^ that hurt to admit")
                       → Arrows and callouts pointing to things
                       Size: 18–24px. Always in saffron color.
                       Maximum ONE Caveat annotation per slide.
```

**Why this breaks from the template:**
- Sora is geometric and modern — the opposite of the editorial serifs (Playfair, Lora) everyone else uses
- The handwritten Caveat annotations are the true differentiator. Nobody else does this. It adds a human voice to what would otherwise be another polished slide deck. When someone sees a hand-scrawled annotation on a carousel, they'll know it's Tejinder before reading the name
- Single font family for all structured text (Sora) creates visual calm. The Caveat contrast creates visual surprise. That tension is the brand

### The Signature Visual Element: The Saffron Sidebar

Every Tejinder carousel slide has a **4px vertical saffron bar** running along the left edge, from top to bottom. This is the visual fingerprint.

```css
.slide::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 4px;
  background: #E85D04;
}
```

Why: It's subtle but instantly recognizable. It creates an ownable visual rhythm when someone swipes through slides. No other AI creator has claimed this pattern. Over time, the saffron sidebar becomes as recognizable as anyone else's highlight boxes — but it's yours.

### Texture

- **Subtle noise overlay:** Very fine grain at 0.02–0.03 opacity. Less than the dark-template carousels use. Just enough to prevent the "flat vector" feel
- **No other textures.** No gradients, patterns, or imagery. Typography + saffron sidebar + white space

### Layout Grid

```
┌─ 4px saffron sidebar                                    ┐
│  ┌──────────────────────────────────────────────────┐   │
│  │  [36px top padding]                              │   │
│  │  EYEBROW LABEL (small caps, saffron)             │   │
│  │  [8px gap]                                       │   │
│  │                                                  │   │
│  │  HEADLINE / MAIN CONTENT                         │   │
│  │  (large, dominant — owns 50-60% of slide)        │   │
│  │                                                  │   │
│  │  BODY TEXT (if needed — often skipped)            │   │
│  │                                                  │   │
│  │  ✍ Caveat annotation (optional — saffron)        │   │
│  │                                                  │   │
│  │  ─── thin divider ─────────────────────────────  │   │
│  │  TEJINDER SINGH  ·  AI Transformation Coach      │   │
│  │  blog.tejindersingh.in              SLIDE X / Y  │   │
│  │  [28px bottom padding]                           │   │
│  └──────────────────────────────────────────────────┘   │
└──────────────────────────────────────────────────────────┘

Left content margin:  36px (after the sidebar)
Right margin:         36px
```

**Footer is identical on every slide.** Same position, same content. This is the metronome that holds the carousel together visually.

### Aspect Ratio & Dimensions

- **Primary:** 1080 × 1350px (4:5 portrait)
  - Takes up more mobile screen real estate than square
  - Pushes competing posts out of view while someone reads
  - LinkedIn renders this cleanly on both mobile and desktop
- **Fallback:** 1080 × 1080px (1:1 square) — only if specifically requested
- **Slide count:** 7–9 slides. Sweet spot is 8. Engagement drops after 10

---

## PART 2: CONTENT ARCHITECTURE (BUILT FOR SHARES, NOT SAVES)

### The Psychology of Sharing

People repost LinkedIn content for three reasons:
1. **Status signaling** — "Look what I found" (makes them look informed)
2. **Tribal identity** — "This is what I believe" (makes them look aligned)
3. **Gift giving** — "My team needs to see this" (makes them look generous)

Your carousel must serve at least one of these motivations. Tutorials and how-tos serve NONE of them — they serve the reader alone, which is why they get saved but never shared.

### The 5 Carousel Archetypes (Ranked by Share Potential)

**1. THE PROVOCATION (Highest share potential)**
Opens with a claim that challenges what the audience believes. Creates "I need my network to see this" energy. The reader shares it because agreeing (or disagreeing) publicly says something about who THEY are.
- "Everyone's racing to add AI tools. Almost nobody is fixing the broken processes underneath."
- "The AI tool doesn't matter. Your thinking does. And most people skip that part."
- "Automation made your bad process faster. Congratulations. You now fail at scale."

**2. THE EXPOSÉ**
Reveals something hidden, wasteful, or broken that the reader's organization is probably doing wrong. Managers share this with their teams. Leaders share it to signal awareness.
- "Your company is spending heavily on 5 tools that free AI already replaced."
- "80% of 'AI transformations' are just expensive dashboards nobody opens."
- "The #1 automation mistake: automating a 12-step process that should be 4 steps."

**3. THE FRAMEWORK (With a point of view)**
Not a neutral how-to. A framework that implicitly says "if you're not doing it THIS way, you're doing it wrong." Shareable because forwarding it is an act of leadership.
- "The 4-step AI audit I run before touching a single tool."
- "The only 3 questions that matter before you automate anything."
- NOT: "How to use ChatGPT Custom Instructions" — that's a tutorial. Tutorials get saved, not shared.

**4. THE UNCOMFORTABLE TRUTH**
Names a pain the audience secretly feels but hasn't articulated. Creates the "finally someone said it" reaction. Shared because the act of sharing it IS the commentary.
- "You don't have a lead generation problem. You have a follow-up problem."
- "Most AI courses teach you prompts. Nobody teaches you when NOT to use AI."
- "The real reason your automation failed isn't the tech. It's that nobody mapped the process first."

**5. THE TRANSFORMATION STORY (With stakes)**
A narrative arc: problem → tension → insight → result. The human element is the engine. Shared because stories travel further than tips.
- "A client was spending 6 hours daily sorting leads manually. After one conversation, I realized the problem wasn't efficiency — it was that they didn't know which leads mattered."
- NOT: "Here's how to automate lead qualification in 5 steps." (That's a tutorial.)

### What to STOP Making

- **Pure tutorials** ("How to use X in 8 steps") — These are Wikipedia pages in carousel form. Useful, but people bookmark Wikipedia. They don't repost it
- **Tool roundups without a point of view** ("Top 5 AI tools for 2026") — Everyone makes these. They're commoditized. No one shares a list they've seen 40 versions of
- **Framework-only slides with no story** — A 4-step framework is forgettable. The same framework preceded by "I watched a client waste 3 months before I figured this out" is shareable

---

## PART 3: SLIDE-BY-SLIDE STRUCTURE

### Slide 1 — THE HOOK (70% of your carousel's success is decided here)

This slide has ONE job: earn the swipe. It is NOT a title card. It is NOT a summary. It is a provocation.

**Structure:**
- Eyebrow: Category label in saffron (e.g., "AI AUTOMATION", "HARD TRUTH")
- Headline: The provocation. Maximum 12 words. Must create cognitive friction — the reader should feel a small jolt of disagreement, curiosity, or recognition
- Caveat annotation (optional): A handwritten aside that adds human voice ("^ controversial? keep swiping.")
- NO body text. NO subheadlines. NO "In this carousel you'll learn..." — that's a death sentence

**The Hook Test:** Read the headline out loud. If someone could respond "So what?" — rewrite it. If someone would respond "Wait, what?" or "Finally someone said it" — ship it.

**Good hooks:**
- "Automation made your bad process faster. Congratulations."
- "You're not bad at AI. You're just briefing it like it's an intern."
- "Every AI tool you're paying for has a free version. Most are better."
- "The businesses winning with AI aren't the ones using the most tools."

**Bad hooks:**
- "5 Amazing AI Tools You Need to Try!" (generic, no friction)
- "In today's carousel, I'll break down..." (meta-narration kills curiosity)
- "AI is transforming business." (everyone knows this — zero information)
- "Here's what I learned about automation." (about you, not about them)

### Slide 2 — THE TENSION

This is the most underused slide in all of LinkedIn. Most carousels jump straight from hook to framework. That's like telling the punchline before the joke.

Slide 2 names the **pain** or the **contradiction** that makes the hook real. It makes the reader feel seen. It creates the emotional contract that keeps them swiping.

**Structures that work:**
- "Here's what I keep seeing..." + a specific, uncomfortable observation from real work
- A before/after contrast: what people think vs. what actually happens
- A single statistic or observation that proves the hook isn't hyperbole
- A brief story beat: "A founder told me last month: 'We automated everything. Nothing got better.'"

**The Caveat annotation shines here:**
- "^ I've had this exact conversation 11 times this year."
- "^ this is the part nobody wants to admit."

### Slides 3–6 — THE SUBSTANCE

Now deliver the framework, the reveal, or the transformation. One idea per slide. Always.

**Type A — Framework Slide:**
- Eyebrow: "STEP 01 OF 04" or "PRINCIPLE 1"
- Headline: The principle or action (imperative voice)
- Body: 1–2 sentences. Concrete, specific. Use an example, not an explanation
- Optional Caveat annotation pointing to the key insight

**Type B — Contrast Slide:**
- Two rows: "WHAT MOST PEOPLE DO" (struck through or dimmed) vs. "WHAT ACTUALLY WORKS" (in saffron)
- Minimal text. The visual contrast does the talking

**Type C — Evidence Slide:**
- A specific result, number, or real-world example
- "After one automation: 6 hours/day → 15 minutes. Same team. Same tools."
- This is where practitioner credibility lives

**Type D — Story Beat:**
- A single moment from a real engagement or conversation
- "The founder went quiet for 10 seconds. Then: 'We've been automating the wrong thing.'"
- These slides are the most shared slides in any carousel. People screenshot these

**Rules for all substance slides:**
- Maximum 35 words of body text. If you need more, you need another slide
- Every slide must be self-contained — if someone screenshots just this one slide, it should still make sense
- Use Caveat annotations to add the human aside that wouldn't fit in "professional" body copy

### Slide 7 or 8 — THE TAKEAWAY

The summary slide. But not a boring recap.

**Structure:**
- Headline: A single-line reframe of the whole carousel's point
- The key items in arrow format: → Item 1 → Item 2 → Item 3
- Caveat annotation with the emotional punchline: "^ the tools are the easy part. The thinking is the hard part."

**This is the screenshot slide.** Design it knowing people will screenshot it and send it in WhatsApp groups, Slack channels, and email threads. Make sure it stands alone.

### Final Slide — THE HUMAN CLOSE

Not a CTA. A moment of connection.

**Structure:**
- Headline: A closing thought that earns respect, not a click. Something the reader walks away thinking about
  - "The tool is never the problem. The question you asked it is."
  - "Automate what drains you. Protect what makes you human."
  - "AI doesn't replace expertise. It exposes the lack of it."
- Author block: Saffron vertical bar + "Tejinder Singh" + "AI Transformation Coach"
- Footer: "More on AI → blog.tejindersingh.in"
- Share nudge: "♻ Repost if your team needs to hear this." (Notice: "your team" — it gives them permission to share by framing it as a generous act, not self-promotion)

**Never use:**
- "Follow me for more!" (desperate)
- "DM me if you want help" (salesy)
- "Like and comment below!" (begging)

---

## PART 4: THE HUMAN LAYER

This is what separates carousels that get 50 saves from carousels that get 200 reposts.

### The Caveat Annotation System

The handwritten Caveat annotations are not decoration. They are the human voice breaking through the polished design. They serve three functions:

1. **Vulnerability:** "^ I learned this the hard way." / "^ took me 3 failed projects to figure this out."
2. **Emphasis:** "^ this is the slide to screenshot." / "^ read this twice."
3. **Personality:** "^ yes, I tried the expensive tool first too." / "^ controversial? maybe. true? definitely."

**Rules:**
- Maximum ONE annotation per slide. Two feels cluttered
- Always in saffron (#E85D04)
- Always preceded by ^ or accompanied by a hand-drawn arrow (→ or ↗)
- Never on Slide 1 (keep the hook clean) — start on Slide 2 or 3
- Use on 3–4 slides per carousel, not every slide. Scarcity = impact

### Story Beats

At least ONE slide per carousel should contain a specific, human moment:
- A conversation with a client (anonymized)
- A mistake you made and what it taught you
- A specific observation from real work, not from the internet
- A number tied to a real outcome, not a hypothetical

**Template:** "[Person/situation] + [what everyone expected] + [what actually happened] + [the insight]"

Example: "A team of 12 was manually sorting 400 leads/week. They assumed they needed a big CRM. They needed a free automation that took 2 hours to build. The CRM was hiding the real problem: they had no scoring criteria."

### The "Make Them Look Smart" Test

Before publishing, ask: **"If someone reposts this carousel right now, what do they look like to THEIR network?"**

- ✅ "A leader who's ahead of the curve on AI"
- ✅ "Someone who cares about their team's efficiency"
- ✅ "A person with sharp taste in content"
- ❌ "Someone who bookmarks tutorials" (that's a save, not a share)
- ❌ "A follower of yet another AI guru" (negative signal — won't share)

---

## PART 5: TECHNICAL PIPELINE

### Method 1: HTML → Playwright → PDF (Primary)

1. **Build as single interactive HTML file**
   - All slides, CSS classes for show/hide, keyboard nav (← →), dots, touch swipe
   - Google Fonts CDN: Sora (all weights), Caveat (Bold)
   - Saffron sidebar as `::before` pseudo-element on every slide
   - SVG noise texture at 0.02 opacity

2. **Screenshot each slide with Playwright**
   ```python
   from playwright.sync_api import sync_playwright
   import time

   with sync_playwright() as p:
       browser = p.chromium.launch()
       page = browser.new_page(viewport={'width': 1080, 'height': 1350})  # 4:5 portrait
       page.goto('file://' + html_path)
       time.sleep(3)  # CRITICAL: font render wait

       n = page.evaluate('document.querySelectorAll(".slide").length')
       for i in range(n):
           page.evaluate(f'''
               document.querySelectorAll(".slide").forEach((s, idx) => {{
                   s.classList.remove("active", "exit");
                   if (idx === {i}) s.classList.add("active");
               }});
           ''')
           time.sleep(0.5)
           stage = page.query_selector('.stage')
           stage.screenshot(path=f'slide_{i+1:02d}.png')
       browser.close()
   ```

3. **Assemble PDF with Pillow**
   ```python
   from PIL import Image
   images = [Image.open(f'slide_{i+1:02d}.png').convert('RGB') for i in range(n)]
   images[0].save('carousel.pdf', save_all=True, append_images=images[1:], resolution=150)
   ```

**Production notes:**
- 3-second font wait is non-negotiable — Playwright captures system fonts without it
- Use 1080×1350 viewport for portrait, 1080×1080 for square
- Always toggle `active` class per slide — don't screenshot all at once
- Color-swap for light mode: use Python `re.sub`, not `sed` (breaks on nested patterns)

### Method 2: Gamma (Quick previews only)

- Pass all slides as single `inputText` with `---` separators
- Dimensions: `4x5` for portrait, `1x1` for square
- Image source: `noImages`
- Theme: Closest to warm dark palette
- Text mode: `preserve`
- Note: Gamma won't render the saffron sidebar or Caveat annotations — these must be added manually

---

## PART 6: CONTENT PRINCIPLES

### Voice & Tone
- First person, practitioner voice ("Here's what I keep seeing...", "The pattern nobody talks about...")
- Direct and opinionated. Not "you could try X." Instead: "Do X. Here's why."
- Warm authority — like a mentor who's done the work, not a professor who read the book
- Comfortable saying "I don't know" or "I got this wrong" — vulnerability IS the brand

### What NOT to write
- "In this carousel, I'll show you..." (kills curiosity — show, don't announce)
- Generic advice without specifics ("Leverage AI for productivity!")
- Self-promotional framing on every post ("When I was working with a Fortune 500 client...")
- Jargon without translation (say "AI reads your words, not your mind" instead of "LLMs process tokens in a context window")
- India-specific framing (rupee formatting, city references) — keep the audience global
- Step-by-step tutorials with no story or point of view — these are save-content, not share-content

### Content Mix (Per 10 Carousels)
- 3 Provocations
- 2 Exposés
- 2 Frameworks (with point of view)
- 2 Uncomfortable Truths
- 1 Transformation Story

This mix prevents "tutorial fatigue" and keeps the audience on edge about what's coming next.

---

## PART 7: QUALITY CHECKLIST

### The Share Test (Do this FIRST — before checking design)
- [ ] If someone reposts this, do they look smart/generous/ahead-of-the-curve to their network?
- [ ] Is there at least ONE slide that would make someone tag a colleague or send in a group chat?
- [ ] Does the hook create friction (disagreement, surprise, recognition) — or just curiosity?
- [ ] Is there a human moment (story, mistake, specific observation) in at least one slide?
- [ ] Would a manager share this with their team? Why?

### Design
- [ ] Saffron sidebar (4px, #E85D04) is present on every slide
- [ ] Background is #141218 (dark mode) or #FAF7F2 (light mode) — no pure black/white
- [ ] Signature saffron used on max ONE element per slide
- [ ] Fonts are Sora (structured text) + Caveat (handwritten annotations)
- [ ] Caveat annotations appear on 3–4 slides, never on Slide 1
- [ ] Noise texture present at 0.02–0.03 opacity
- [ ] All slides follow identical grid (36px margins, consistent footer, same sidebar)
- [ ] No stock photos, illustrations, icons, or decorative elements

### Content
- [ ] Slide 1 hook is under 12 words and creates cognitive friction
- [ ] Slide 2 names a pain or contradiction (doesn't jump to framework)
- [ ] One idea per slide — no cramming
- [ ] Body text under 35 words per slide
- [ ] At least one Story Beat slide with a specific human moment
- [ ] No hard CTAs. Share nudge on last slide only: "♻ Repost if your team needs to hear this."
- [ ] Footer on every slide: "More on AI → blog.tejindersingh.in"
- [ ] Author block on last slide: "Tejinder Singh · AI Transformation Coach"
- [ ] Archetype is identified (Provocation / Exposé / Framework / Uncomfortable Truth / Story)

### Technical
- [ ] 7–9 slides total (8 is ideal)
- [ ] Exports at 1080×1350px (portrait) or 1080×1080px (square)
- [ ] Fonts rendered correctly (no Arial/Helvetica fallbacks in PDF)
- [ ] File size under 10MB
- [ ] Both dark and light variants available if needed

---

## PART 8: FILE OUTPUT

```
/mnt/user-data/outputs/
├── postNN_carousel.html      ← Interactive preview (dark mode)
├── postNN_carousel.pdf       ← Final PDF for LinkedIn upload
├── postNN_light.html         ← Light mode variant (if requested)
└── postNN_light.pdf          ← Light mode PDF (if requested)
```

Working files in `/home/claude/` — never in outputs.

---

## THE 10 NON-NEGOTIABLES

1. **Saffron sidebar on every slide.** 4px. Left edge. #E85D04. The visual fingerprint
2. **Caveat handwritten annotations.** The human voice that no polished template can replicate
3. **Sora for structure. Caveat for humanity.** Two fonts. Two voices. One brand
4. **Warm palette — never cold.** #141218 not #000. #EEEBE4 not #FFF. Warmth = trust
5. **Slide 2 is tension, not content.** Name the pain before offering the cure
6. **One human moment per carousel.** A story, a mistake, a specific observation from real work
7. **"Make them look smart" test before publishing.** If sharing it doesn't elevate the sharer, rewrite it
8. **No pure tutorials.** Every framework needs a point of view. Every how-to needs stakes
9. **Alternate dark/light mode.** 70/30 split. Prevents visual fatigue. Same brand, different energy
10. **The share nudge, not the follow beg.** "♻ Repost if your team needs this" — never "Follow me!"

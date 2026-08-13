# sniffrpack.com copy deck — rebuild

Source of truth for the build. Voice rules at bottom. Stat-dependent lines in /why marked `[STAT]` pending verification.

Design tokens unchanged (global.css): bg #FAF8F4, ink #1A1814, accent #B8501E, rule #E5DED1, Fraunces display / Inter body. Reuse existing section rhythm (`px-6 py-24 md:py-32`, `max-w-3xl`, `<hr>` dividers, eyebrow = `text-sm uppercase tracking-widest text-accent`).

---

## HOMEPAGE (index.astro)

### Hero — KEEP headline, REWRITE subhead, ADD owner line
Headline (verbatim):
> Most dog software is built around the bill.
> **Sniffr is built around the dog.**

Subhead (replace the spec-list):
> Scheduling, intake, photos, payments, and walk reports for dog-care businesses. Built alongside a real one, Hamilton Bark, who run about 130 walks a week on Sniffr today.

CTAs unchanged: `Book a setup call` / `See the roadmap →`

NEW — quiet line directly under the CTA row (muted, small):
> Here because your walker uses Sniffr? [Open the app →](https://app.sniffrpack.com)

Nessie card: KEEP exactly as built.

### Section 2 — REPLACE thesis-polemic with SHOWCASE
Old Rover/Wag/TTP theory paragraphs are CUT from the homepage (they move to /why, rewritten).
New section title:
> A day in your dog's life, kept.

Intro (one line):
> Every walk leaves something behind. Sniffr turns the day into a record that belongs to the dog.

Then 2–3 built HTML artifact cards in sequence (see ARTIFACTS below): walk-report timeline, then a memory/photo moment. Biscuit's ambulance-song example is PROMOTED here from the old section 5.

Closing positioning paragraph (this is where the co-evolution voice enters — compressed):
> Humans and dogs have been shaping each other since before written language existed. They notice what we can't, faster and farther than we can, and in return one person keeps them safe for the whole of their life. That bargain is older than the alphabet, and it still runs every morning at your dog park. We think software for dog care should be built the way the bargain is: around the dog.
>
> [Read why we built it this way →](/why)

### Section 3 — Onboarding — KEEP, trim
Keep heading "Your business card is your intake form." and the three body paragraphs.
CUT the italic Time To Pet comparison callout (the scan→M&G narrative already makes the point).

### Section 4 — Scheduling — KEEP names, RE-LEAD with pain, cut jargon
Eyebrow: Scheduling Model. Heading KEEP: "Sell Windows. Walks happen automatically."
New lead paragraph (before defining Window):
> Recurring dog care isn't a calendar full of appointments you re-book every week. It's a handful of standing commitments. Sniffr's scheduling is shaped like that.

Then keep the Window definition paragraph.
Horizon paragraph: KEEP the idea, cut "commitment radius" as the lead term:
> A **Horizon** is how far ahead you lock walks in. Some walkers run three days out, some run three weeks. Solo walker or twenty-walker shop, you set how far you plan. Raise it as your team grows.
Keep the pricing/cash-flow paragraph.
CUT the italic "primitives match how a multi-walker shop thinks" callout (too inside-baseball).

### Section 5 — Walk Reports — TRIM (Biscuit moved to showcase)
Keep heading "Talk through the walk. Sniffr listens." and the opening + closing time-saver paragraphs.
The Biscuit blockquote is now shown as a showcase artifact up top, so here REPLACE the inline blockquote with the plain explanation of how voice→tagged-timeline works. Keep "Roughly 10 minutes of paperwork per walk — gone."

### Section 6 — "Sniffr learns who walks who" — KEEP VERBATIM
Best-written section on the page. Do not touch.

### Section 7 — Ownership — KEEP, trim one line
Keep heading + first three paragraphs. Keep "This is the whole stance." line but it now also lives on /why; that's fine, it's the payoff both places.

### Section 8 — Roadmap teaser — TRIM
Keep heading "Sniffr ships fast." One sentence + link. CUT "The tables are built. The plugins are partially written. The agents are running." (it's on the roadmap page; on the homepage it reads as inside-baseball).

### Section 9 — Hamilton Bark proof — KEEP
Stats 130 / 6 / $250K unchanged PENDING Kerry sign-off on public revenue figure.

### Section 10 — CTA — KEEP, already broadened well
No change.

---

## /why — NEW PAGE (why.astro)

Manifesto. Long-form, single column, max-w-3xl, generous vertical rhythm. NOT a feature page. The industry critique appears here as a *consequence* of the belief, never as the opening move.

Nav: add "Why" link between logo and Roadmap. Footer: add "Why" link.

### Hero
Eyebrow: Why Sniffr exists
> We didn't start with software. We started with 14,000 walks.

Sub:
> Three years running a dog-walking business. Fifteen months building the software underneath it. This is what that taught us about dogs, and why the software looks the way it does.

### Movement 1 — The walks
> Hamilton Bark has done roughly 14,000 walks in two years. Six walkers, one city, the same dogs week after week. When you spend that long inside the actual daily life of dogs, not the idea of it, you stop seeing individual appointments and start seeing something older and steadier underneath.

### Movement 2 — The old contract
The co-evolution core. Stats VERIFIED — use these exact factual framings, do not embellish the numbers.
> Dogs and humans have been partners since before written language existed. The youngest honest estimate puts it around fifteen thousand years; some evidence runs far older. Either way, we were shaping each other long before we could write any of it down. Not as owner and pet. As two species that got better at surviving by paying attention to each other.
>
> A dog reads the world faster than we do. Their eyes register motion at something like seventy to eighty flashes a second, past the point where our vision smooths everything into a blur, which is why old flickering screens looked jittery to them long after they looked seamless to us. Their nose is working the breeze the whole time, pulling in scent and high sounds we have no access to. Long before you'd notice a familiar dog nearby, yours already has. They read what's coming in channels we barely have: scent, sound, the shift in a person's mood. That was the deal, quietly, for all those thousands of years. They watch the edges we can't, and one human keeps them fed and safe for the whole of their short life.

Then the Darwin turn (verified: Spencer coined the phrase; Descent of Man argues sympathy is selected):
> We tend to think "survival of the fittest" means the sharpest teeth win. Darwin didn't even coin that phrase, Herbert Spencer did. What Darwin actually wrote, in The Descent of Man, was warmer and stranger: that sympathy is one of our strongest instincts, and the communities that thrived were the ones whose members took care of each other. Dogs have been living proof of it the whole time.

### Movement 3 — The city
Ties to the sofa-sloth thesis (one brand argument across surfaces).
> A dog needs to be outside every few hours. In a city, almost nobody has a backyard. So the whole neighborhood ends up at the same small patch of grass at the same times of day, and something forms there that a suburb with fenced yards never builds: a genuine third place. Not home, not work. The dog park.
>
> The same faces every morning. You know the dogs' names before you know the peoples'. That's not a small thing. In a modern city that's starved for exactly this, the dog is the reason a stranger becomes a regular becomes a friend.

### Movement 4 — What that means for software
The critique, folded in as consequence.
> If the relationship between a person and their dog is this old and this mutual, then a company that wedges a 20% tax between a walker and the family they've served for years isn't just charging too much. It has the whole thing backwards. That's the marketplace model, Rover, Wag: treat the walker as interchangeable labor and the relationship as inventory to broker.
>
> The other kind of software, the older billing platforms, gets the ownership right but starts from the invoice. Photos and notes hang off the bill as decorations. The dog is a line item.
>
> We started from the dog. The dog is the center of the data model, not the invoice. Photos belong to the dog and outlive any single visit. A walker's bond with a dog is something the system learns by watching, not a rule you declare once and forget. Your customers are yours; when you leave, they leave with you. That's the whole stance, and it's the reason Sniffr exists.

### Movement 5 — Where it goes (the Pack — emotional payoff, future tense)
> There's a reason it's called Sniffr **Pack**. The dog park already makes a community; it just has no memory and no shape. So we're building one. A Pack is the crew that already shares your park and your hour, given a name, a shared photo stream, its own small world. When your walker gives back to the Pack that a good chunk of it already books through, the thing dogs have always done to us, pulling us into each other's lives, finally has somewhere to live online.
>
> Dogs draw people together. They always have. We're just building the software that admits it.

Close (last line, standalone):
> We didn't call it Sniffr Pack by accident.

CTA row: `Book a setup call` (/#book) + `See the roadmap →` (/roadmap)

---

## ARTIFACTS (built HTML, Sonnet agent) — in the Nessie-card visual family

Style reference = the existing Nessie figcaption card in index.astro (white bg, rounded-2xl, ring-1 rule, emoji tag pills `rounded-full bg-bg border border-rule`). No screenshots. Self-contained markup, no new deps.

1. **Walk-report timeline card** — "Biscuit · Today", the ambulance-song transcript as a short quote, then the three tagged events as a vertical timeline (🐕 leash-ready / 🚑🎶 ambulance song / 🐾 played with Goldie), each a row with a small connector. Footer: "A Sniffr walk report".
2. **Memory / photo moment card** — mirrors Nessie card structure; a captioned photo moment with auto-hashtag pills. (Can reuse Nessie image or a placeholder figure block.)
3. (Optional third) **Owner's-phone glimpse** — a tiny "what the family sees" framing: one line + a couple of memory pills. Only if it doesn't bloat the section.

Arrange the showcase as a vertical sequence or a 2-up on desktop; do NOT make an identical 3-card grid (banned). Vary card sizes/emphasis.

---

## VOICE RULES (enforce on every line)
- About *their* dog, not "dogs" in the abstract. Concrete perceptual detail beats philosophy. If a line states the philosophy outright, cut it and show it instead.
- No em dashes (use commas/periods/parens). No gradient text, no side-stripe borders (the existing `border-l-2` accent lists on homepage are pre-existing; leave them, don't add new ones).
- One competitor mention max on the homepage (in the CTA empathy line). Rover/Wag/TTP named only on /why and roadmap.
- Warm, earned, plainspoken. Founder who did the walks, not a marketer.

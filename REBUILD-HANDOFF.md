# sniffrpack.com rebuild — handoff (resume here)

## CORRECTION 2026-08-13 — pricing is now settled; site gained /pricing
Tenant pricing was decided (see `PRICING-LANDSCAPE-2026-08-13.md` in sniffr-frontend, landing on main via PR #210 alongside THESIS.md). What changed on this site, all uncommitted:
- **NEW `src/pages/pricing.astro`** — tiers are **Sniff** (free to 3 paying clients, then $29/mo), **Fetch** ($59/mo), **Pack** ($99/mo + $15/active walker). Annual = 2 months free. Every-tier commitments: no revenue cut / Stripe pass-through with zero markup, provider brand on the work product (never the shell — thesis doctrine), AI connectors included un-metered, leave-anytime. Marketplace take-rate contrast appears UNNAMED (voice rule: Rover/Wag named only on /why and roadmap). Unshipped features (brand studio, own-domain booking, Gusto sync) carry a small "soon" pill — do not sell them as present until they ship.
- **Nav + Footer** — Pricing link added.
- **index.astro** — one muted line added in the #book CTA section: "Sniffr is free until your fourth client pays. See pricing →". Nothing else touched.
- Pricing-copy source of truth is the frontend repo's PRICING-LANDSCAPE doc, not COPY-DECK.md (deck predates pricing and doesn't cover it).
- Open on this page: whether free-tier onboarding stays setup-call-gated until self-serve signup ships (currently the CTA assumes setup call).
- **GPS is deliberately unadvertised** (Joseph 2026-08-13): removed from /pricing; don't reintroduce it anywhere on the site until he says otherwise, even though the product technically has it.
- **roadmap.astro rebuilt against THESIS.md** (same day; the old "do not touch roadmap" rule below is superseded): consumer wedge inserted as V3 "The Dog's Record" (tenant-free signup, Story, photo import, vet PDF, multi-provider connectors) BEFORE V4 Community per the thesis sequence (the wedge delivers Circle's density, not walker acquisition); multi-service moved to V5 (2027) per thesis step 5; one-record language threaded in ("One record, many authors, the owner holds it" closes V3; "Both scope the dog's history to the business… Sniffr scopes it to the dog" added to How-we-ship); V1 gained Poop Tracker + tips (both live); V1.5 gained the free-tier line linking /pricing. Homepage roadmap teaser re-ordered to match ("through 2026 and into 2027").


Session was interrupted by repeated model auto-switching. This note lets a fresh session resume without re-deriving anything.

## The goal (settled with Joseph)
Rewrite sniffrpack.com so it stops reading like a polemic and instead leads with the dog. Three decisions, all confirmed:
1. **Audience**: buyer page (walker-business owners) + a quiet owner path. Homepage keeps the setup-call CTA but opens dog-centered and adds a "here because your walker uses Sniffr? → app" line.
2. **The industry argument**: compressed to one paragraph on the homepage; full manifesto moves to a new `/why` page. Rover/Wag/TTP named only on `/why` and roadmap, max ONE competitor mention on the homepage (the CTA empathy line).
3. **Proof visuals**: hand-built HTML artifact cards in the Nessie-card visual family (walk-report timeline, memory moment). No screenshots.

The deeper layer Joseph asked for: the human-dog **co-evolution** thesis (Horowitz, the Darwin/sympathy reading, urban dog park as third place, the Pack as payoff). It lives mainly on `/why`, entered on the homepage as one compressed paragraph. Rule: concrete perceptual detail, about THEIR dog, never abstract philosophy stated outright.

## Source of truth
**`COPY-DECK.md`** in this repo. It is final and verbatim-authoritative for all copy. Follow KEEP/CUT/REWRITE markers exactly.

## Stats: fact-checked (two passes, sourced). Deck already reflects the safe versions.
- Frame rate: dogs ~70–80 Hz flicker-fusion; humans ~40–60 Hz (NOT 29 — that was fabricated). Deck states dogs' number only, avoids a wrong human number.
- Scent "3 blocks": REMOVED. No study supports individual recognition at a set distance. Deck decouples general range from "a familiar dog nearby."
- Domestication: "before written language existed" (~14k archaeological, 20k+ genetic). Safe.
- Darwin: Spencer coined "survival of the fittest"; Descent of Man centers sympathy. Do NOT claim Darwin "rejected" competition. Deck is correct. (Book Joseph half-remembered = likely *Survival of the Friendliest*, Hare & Woods 2020.)

## State of the build — DONE (uncommitted in working tree)
The Sonnet build agent completed. `npm run build` passed clean (5 pages: `/`, `/why`, `/roadmap`, `/privacy`, `/delete-account`). Changes are UNCOMMITTED. Files touched:
- `src/pages/index.astro` — restructured per deck (hero subhead + owner line, showcase replaces polemic with 2 artifact cards, onboarding/scheduling/walk-report trims, roadmap-teaser trim). One competitor mention remains (CTA).
- `src/pages/why.astro` — NEW manifesto, movements 1–5, closing "Sniffr Pack" line isolated.
- `src/components/Nav.astro`, `Footer.astro` — "Why" link added.

The riskier scent line WAS shipped and has since been **fixed by hand** (why.astro ~line 48: now "working the breeze… familiar dog nearby," matching the corrected deck). No re-build run after that one-line prose edit; harmless, but run `npm run build` once to be safe.

## Review on resume (the agent's judgment calls + open items)
The build agent flagged 5 judgment calls worth a look — all defensible, none blocking:
1. `/why` movement sections have NO eyebrow labels (chose pure editorial flow).
2. Skipped the optional 3rd "owner's-phone" artifact card (2 felt complete).
3. Memory card uses a paw-glyph placeholder, not a real photo (no new image asset added). **Consider a real dog photo here later.**
4. `/why` closing line is left-aligned (not centered) to match manifesto rhythm.
5. Walk-timeline card adds small location labels ("Pickup," "6th & Main," "Dog park") as scaffolding; the 3 tag lines are verbatim.

Next step after review: **look at the rendered pages** (npm run dev, eye the homepage showcase + /why) before any commit. Nothing has been committed or pushed.

## Still needs Joseph
- **Kerry sign-off** on publishing "$250K annual service revenue" (appears in homepage proof section + roadmap). Not yet confirmed.

## Do NOT
- Do not touch `roadmap.astro` (already good; owns what/when — `/why` owns the belief).
- Do not commit unless Joseph asks (repo rule: commit/push only on explicit request).
- Do not reintroduce em dashes, gradient text, or new side-stripe borders.

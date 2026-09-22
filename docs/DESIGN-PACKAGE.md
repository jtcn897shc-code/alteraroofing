# Altera Roof Services: design package (Tier 1)

Every line of copy here ships verbatim in `site/index.html`. Band ranges are starting points, validated by the flick test once the film exists.

## 1. Brand premise
**Every layer, shown.** A roof is layers that nobody sees once they're covered: the deck, the membrane, the flashing, the shingles. Coquitlam's rain finds every shortcut. Altera already photographs its jobs before and after, from the ground and from the air. The site sells one idea: *you see every step*. Everything leads to one action: **Book a free roof check** (`#contact`).

## 2. Palette tokens
Pulled from the wet West Coast world of the job photos: slate shingles, low cloud, and cedar and fir. Final values will be re-sampled from the approved hero film.

```css
:root{
  --canvas:#12171a;        /* wet slate, tinted blue-green, never pure black */
  --panel:#1a2126;
  --accent:#7fae93;        /* evergreen: CTA fill, focus rings, one or two emphasis moments */
  --accent-hover:#95c2a8;
  --accent-muted:#3c5147;  /* borders, glows, particles */
  --text-secondary:#a8b3b6;
  --text-primary:#eef1ee;  /* fog */
  --line:#5d6a6f;          /* interactive borders (3.23:1 on canvas) */
}
```

| Pair | Ratio | Use |
|---|---|---|
| text on canvas | 15.86:1 | body |
| text-secondary on canvas | 8.42:1 | secondary copy |
| canvas on accent | 7.20:1 | CTA label on evergreen fill |
| accent on canvas | 7.20:1 | accent text, rare |
| line on canvas | 3.23:1 | interactive borders |

**Rules:**
- The accent is a fill on the CTA and a ring on focus. Button labels on evergreen are always dark slate.
- The only brand ink is the logo's own black and white. The site uses the fog (light) version on slate.
- Clichés this category leans on, and that we avoid: navy and red contractor palettes, shields as decoration beyond the real logo, lightning-bolt "EMERGENCY" banners, stock hard-hat photos, fake review stars, countdown urgency.

## 3. Type
- **Archivo** (Google, variable width and weight). Display is condensed (`wdth` 62 to 75) in caps, weights 600 and 800. Body is normal width, weights 400 and 500. One family covers both the poster face and the reading face, and its geometric build echoes the logo's wordmark.
- **IBM Plex Mono** 500 for small labels: kickers, step numbers, photo captions.

## 4. Band map (hero, 400vh)
| Band | Range | Footage moment | Copy (verbatim) | Entrance |
|---|---|---|---|---|
| 1 | 0.00 to 0.22 | Above low rain cloud over evergreens | Kicker "Coquitlam, BC". Line "Built for the rain." | drift-down (with the load ramp) |
| 2 | 0.26 to 0.48 | Descending through rain, drops on the lens | "Almost two metres of rain a year." / "Your roof takes every drop." | drift-down, per character |
| 3 | 0.52 to 0.74 | Mist clears, the roof comes into focus | "We show you every layer." / "Before and after. From the ground and from the air." | blur-to-sharp |
| 4 | 0.78 to 1.00 | Rest: straight down on the finished dark roof | H1 "You see every step." / "Roofs, leak repairs and moss care in Coquitlam. Photographed before and after, so you know exactly what was done." / CTA "Book a free roof check", secondary "See the work" | word rise into a staged settle |

## 5. Static-hero copy (phones, reduced motion, no film yet)
- Kicker: "Altera Roof Services · Coquitlam, BC"
- H1: "You see every step."
- Sub: "Roofs, leak repairs and moss care in Coquitlam. Photographed before and after, so you know exactly what was done."
- CTAs: "Book a free roof check" and "See the work"

## 6. Below the fold
1. **Services**, `#services`. Kicker "What we do". H2 "Four kinds of work. One standard."
   - **Leak repair** (wide, tag "Most urgent"): "Water coming in? Call us. We find where it gets in, fix it, and show you the photos."
   - **Shingle roofs**: "New roofs and re-roofs for houses and garages. Clean lines and tight flashing."
   - **Flat roofs**: "Membrane roofs, skylight curbs and rooftop details on flat and commercial buildings."
   - **Moss and maintenance**: "Moss loves a Coquitlam roof. We clear it and keep an eye on the roof between big jobs."
2. **Work**, `#work`. The interactive moment. Kicker "Hold to clear". H2 "Same roof. Hold to see it cleared." Body "One Coquitlam roof, photographed before and after. Press and hold." Button "Hold to clear the moss". Done state "After. Every job gets photos like these."
   - Then the curb pair. Label "Flat roof, skylight curb". Captions "Before" / "After".
   - Then the aerials. Caption "From the air".
3. **Process**, `#process`. Kicker "How it goes". H2 "Three steps. You see all of them."
   - 01 "We look from above." "We check the roof up close and from the air, and photograph what we find."
   - 02 "You get a clear quote." "The photos, what we'd do, and the price. No pressure."
   - 03 "We build it, then show you." "When the work is done you get the after photos. You see what you paid for."
4. **FAQ**, `#faq`. Kicker "Questions". H2 "What people ask first."
   - "Will you actually call me back?" "Yes. Call or text and a real person gets back to you. If we can't take the job, we'll tell you straight."
   - "Do I need a new roof, or just moss removal?" "Not always a new roof. We go up, take photos, and tell you what it needs. Sometimes that's a clean and a treatment. Sometimes it's more."
   - "I have a leak right now. What do I do?" "Call us. If you can, put a bucket under the drip and move anything valuable out of the way. We'll take it from there."
   - "Do you do flat and commercial roofs?" "Yes. Membrane roofs, skylight curbs and rooftop details. The skylight curb above is one of ours."
   - "Where do you work?" "Coquitlam and the area around it. Not sure if we cover you? Ask."
5. **Contact**, `#contact` (the single CTA). Kicker "Free roof check". H2 "Book a free roof check." Body "Tell us what you're seeing. We'll come out, go up, and send you the photos." Checklist title "Have these handy". Items: "Your address", "What you're seeing: a leak, moss, or an old roof", "A photo or two, if you can". Buttons: "Call 604-555-0142", "Text us", "Email us". Note "No form yet. Calls, texts and emails reach us directly."
   - **Form handling:** there's no endpoint, so there's no `<form>`. Only real `tel:`, `sms:` and `mailto:` links. Wire a form service once the owner has one.
6. **Footer**: logo, "Altera Roof Services", "Coquitlam, British Columbia", phone, Facebook, "© 2026 Altera Roof Services".

## 7. Vector layer
- **Signature: the ridge line.** The logo's twin chevrons, redrawn as a thin roofline that draws itself on scroll across each section break. Removing it would take away the thread that ties every section back to the mark.
- Hero world (until the film exists): layered mist planes, fine diagonal rain streaks, and a large chevron ridge rising into the settle as the scroll descends.
- Environment: fixed, slow mist drift (90s) and whisper-level rain (60s+), paused off-screen and on hidden tabs.
- Service icons: single-stroke line drawings (drop, shingle courses, flat curb, sprig), using the chevron's stroke weight.

## 8. Engineering list
- Blob fetch with the loading ring.
- dt-normalized lerp.
- Gated seeks.
- Delta-gated DOM writes.
- Band pacing with the flick test.
- The four-layer legibility system.
- Five static-hero gates, kept live with change listeners.
- Complete without video: `VIDEO_READY=false` until the film exists.
- JS-confirmed reveals.
- Hover gated to fine pointers.
- `overflow-x: clip`.
- Live reduced motion, both directions.
- Skip link and landmarks.
- `<!-- DEPLOY STEP -->` og tags.
- The whole-site-animated standard.

## 9. Copy gate
Every line above ships verbatim. The built page must pass the Phase 9 grep gate: zero em dashes, and zero of leverage, seamless, empower, unlock, robust, actionable, data-driven, solutions. Then the AI-tell sweep. "Four kinds of work. One standard." and "Three steps. You see all of them." are deliberate brand devices and stay.

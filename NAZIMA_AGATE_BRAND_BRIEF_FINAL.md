# Nazima Agate: Final Brand Brief for Claude Design (v1.2)

> **One file to upload into Claude Design.** It contains the locked v1.0 design system values, the website extension, the business context, and the competitor lessons, merged and de-conflicted.
> Also attach the original "Nazima Agate Design System v1.0" PDF/DESIGN.md if available. If anything differs, **v1.0 wins**.
> Version 1.2 · 14 October 2026.

---

## 0. Instructions for Claude Design

1. **Do not redesign the brand.** Colours, fonts, spacing, shape, motion, motif and voice below are locked.
2. **Extend it.** Fill the open parts: logo system, imagery style, website pages, Stone Guide, Partner programme, packaging variants.
3. Every surface must pass these 3 tests: **Authentic** (real facts, real proof), **Grounded** (minerals, not magic), **Refined** (space, restraint, one action).
4. Design for **phone first**, in **light and dark**.

---

## 1. Brand core (locked)

| | |
|---|---|
| Name | **Nazima Agate** |
| Tagline | **Stones from the Source.** |
| What we are | An Indian agate and crystal manufacturer that brings genuine, hand-finished stones straight from the source, and teaches people how to tell a real stone from a fake. |
| Personality | Authentic · Grounded · Refined |
| Never feels like | A mystical crystal shop (purple galaxies, chakra clip-art, glitter) · a bulk wholesale catalogue (cramped grids, shouting prices) · a meme page (heavy slang, jokes over facts) |
| Business lines | 1) Retail store (India, later export) 2) Wholesale (B2B, GST) 3) **Partner programme** (anyone can resell, zero risk) 4) **Stone Guide** (AI that teaches, then recommends) |

### Five principles
1. **Show the stone, not the sparkle.** Real colour, bands and texture carry the design. Daylight, plain sand ground, sharp focus.
2. **Teach before you sell.** Every surface teaches one true thing (how to check a stone is real, what Mohs means, where it comes from). The product follows the fact.
3. **Grounded, never mystical.** Talk about stones as minerals: name the mineral, the hardness, the origin. No healing claims, chakra symbols, cosmic imagery.
4. **Refined through restraint.** Generous space, one idea per line, **one Carnelian action per view**, gold used once.
5. **Two languages, one voice.** English for the brand layer, Hinglish for content. Stone names stay in English everywhere.

---

## 2. Positioning (from competitor study)

We studied stonemart.co.in, partner.shubhnumbers.com and empireagate.com. **All three sell on mystical claims and unproven trust**: review counts that don't match, "certified" with no named lab, healing claims as fact, homepage promises the terms take back.

**Nazima's position: the one that proves it.**
- Facts instead of energy claims.
- Proof instead of badges: batch numbers, treatment disclosure, workshop video, certificates where they exist.
- Honest numbers: real stock, real reviews, real partner earnings.

| Take the idea | From | Our version |
|---|---|---|
| Stone hub pages (facts + products + FAQ) | Stone Mart | "Stone knowledge" hubs in v1.0 voice |
| Zero-risk reseller model (customer pays first, white-label shipping) | ShubhCrystals | **Nazima Partners** with automatic payments and weekly payouts |
| AI consultant on every product page with quick-ask buttons | Empire Agate | **Stone Guide**: facts only, ends in products + WhatsApp |
| Origin storytelling (Khambhat heritage) | Empire Agate | "Stones from the Source": real workshop, real hands |

---

## 3. Colour (locked)

### Brand colours
| Name | Hex | Role | Share of a surface |
|---|---|---|---|
| Carnelian Red-Brown | `#8A3B22` | Primary: buttons, links, key highlights | 10% |
| Banded Sand | `#F2EADF` | Background: pages, packaging ground | 60% |
| Charcoal Ink | `#1F1C1A` | Text, headlines, dark grounds | 22% |
| Moss Agate Green | `#56705E` | Secondary: supporting tags, origin notes | 6% |
| Antique Gold | `#B08D57` | Premium accent: hairlines, premium badge, sparingly | 2% |

### Semantic tokens (light / dark)
| Token | Light | Dark | Use |
|---|---|---|---|
| `--nz-bg` | `#F2EADF` | `#181513` | Page background |
| `--nz-surface` | `#FAF6F0` | `#221E1B` | Cards, inputs |
| `--nz-surface-sunken` | `#E8DECF` | `#12100E` | Table headers, photo wells |
| `--nz-border` | `#D9CBB8` | `#3A332D` | Hairlines, card edges |
| `--nz-border-strong` | `#8A7D70` | `#857869` | Input and control borders (3:1) |
| `--nz-text` | `#1F1C1A` | `#F2EADF` | Body and headlines |
| `--nz-text-muted` | `#5C534B` | `#B3A797` | Secondary text |
| `--nz-text-subtle` | `#766B60` | `#958979` | Placeholders, disabled |
| `--nz-primary` | `#8A3B22` | `#D27A55` | Primary actions, links |
| `--nz-primary-hover` | `#73301B` | `#DE8C69` | |
| `--nz-primary-pressed` | `#5E2716` | `#C87150` | |
| `--nz-on-primary` | `#FAF6F0` | `#1F1C1A` | Text on primary |
| `--nz-primary-subtle` | `#EBD9CF` | `#3A2219` | Selected chips, stone tags |
| `--nz-on-primary-subtle` | `#8A3B22` | `#E39A79` | |
| `--nz-secondary` | `#56705E` | `#8FAA97` | Moss accents |
| `--nz-on-secondary` | `#FAF6F0` | `#1F1C1A` | |
| `--nz-secondary-subtle` | `#DDE3D9` | `#26302A` | Moss tags |
| `--nz-on-secondary-subtle` | `#3F5A48` | `#8FAA97` | |
| `--nz-accent` | `#B08D57` | `#B08D57` | Gold hairlines, premium badge fill |
| `--nz-on-accent` | `#1F1C1A` | `#1F1C1A` | |
| `--nz-accent-text` | `#7D6236` | `#C9A56C` | Gold-coloured text that must be read |
| `--nz-success` / `-subtle` | `#3F5A48` / `#E1E6DC` | `#8FB79A` / `#1F2B23` | |
| `--nz-warning` / `-subtle` | `#7F5B12` / `#F3E7CC` | `#D9AE5C` / `#2E2614` | |
| `--nz-error` / `-subtle` | `#9B1C31` / `#F5DEDF` | `#E8838A` / `#33191C` | |
| `--nz-focus` | `#8A3B22` | `#E39A79` | Focus ring |

**Rules:** No gradients; colour is always flat. One Carnelian action per view. Gold on Sand is decorative only (2.59:1); readable gold text uses `--nz-accent-text`. Status colours always travel with an icon or word. Dark theme buttons are lifted Carnelian `#D27A55` with Ink labels. All text pairs pass WCAG AA (body text 14:1+).

---

## 4. Typography (locked)

| Role | Family | Use |
|---|---|---|
| Display / headings | **Fraunces** (ital, opsz, 300–700) | English brand headlines, 20px and up. Italic for the tagline. |
| Body / UI | **Inter** (400–700) | Body, UI and **every Hinglish line**. 700 only on reel covers. |
| Accent | **Tiro Devanagari Hindi** | **One** highlighted Hindi word per surface (e.g. असली). Never sentences. |
| Mono | ui-monospace | SKUs, codes |

| Token | Size/line (desktop) | Phone | Weight |
|---|---|---|---|
| display | 64/68 | 44/48 | 400, -0.02em |
| h1 | 48/54 | 36/42 | 400, -0.015em |
| h2 | 36/42 | 28/34 | 500 |
| h3 | 28/34 | 24/30 | 500 |
| h4 | 22/28 | 20/26 | 600 |
| body-lg / body / body-sm | 18/28 · 16/24 · 14/20 | same | 400 |
| label-lg / label / label-sm | 16/24 · 14/20 · 12/16 | same | 600 |
| overline | 12/16, caps, 0.08em | same | 600 |
| caption | 12/16 | same | 400 |
| reel-title / kicker / text / accent (1080px canvas) | 88/96 · 44/52 · 56/68 · Tiro 72/96 | | 700 · 600 · 600 · 400 |

Sentence case for headlines. Body lines 60–75 characters. Hinglish never in Fraunces.

---

## 5. Space, shape, motion, motif (locked)

- **Spacing:** 4px base: 4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96. Max content width 1200px. Sections 96px apart desktop, 64px phone.
- **Grid:** Phone 0–639px, 4 col / 16 gutter / 16 margin · Tablet 640–1023px, 8 col / 24 / 32 · Desktop 1024+, 12 col / 24 / 48.
- **Radius:** none 0 (tables, full-bleed photos) · sm 4 (checkbox, packaging) · md 8 (buttons, inputs) · lg 14 (cards, product photos) · full (tags, chips, switches). "Soft, never round."
- **Lines:** 1px hairline for cards; 1px border-strong for controls; 2px focus ring, 2px offset.
- **Elevation:** borders first, shadows second. shadow-1 (card hover, menus), shadow-2 (drawers, dialogs).
- **Motion:** "Settle, don't bounce." fast 120ms · base 200ms · slow 320ms · content 400ms. Ease standard `cubic-bezier(0.2,0,0,1)`, exit `cubic-bezier(0.4,0,1,1)`. Allowed: fade with 8px rise, crossfade, sliding tab underline. Never: bounce, spin, sparkle, shimmer, parallax. Reduced motion = 120ms fade.
- **Motif, agate bands:** concentric, uneven lines at 1–1.5px in one colour. Gold on Ink (packaging, reel covers), Carnelian on Sand (catalogue, website), Subtle on Surface (photo placeholders). Never filled, never a gradient, never behind body text.

---

## 6. Voice and tone (locked)

**A calm teacher who knows stones.** Precise in English, warm and direct in Hinglish. Never mystical, never loud.

| Layer | Language | Where |
|---|---|---|
| Brand | English | Logo, tagline, packaging, website, catalogue, marketplace listings |
| Content | Hinglish, Roman script | Reel covers, on-screen text, captions, carousels, partner WhatsApp kit |

| Context | We say | We don't say |
|---|---|---|
| Product facts | Agate is 6.5–7 on the Mohs scale. | This magical stone changes your energy! |
| Origin | Hand-finished in India, straight from the source. | Cheapest bulk rate, DM fast!! |
| Reel lines | Asli pathar der tak thanda rehta hai. | Bro ye pathar ekdum OP hai fr |
| Partner | You set your price. We pack, ship, and pay your margin every week. | Earn up to 300%! ₹80,000/month guaranteed! |

- **Fixed spellings:** pathar · kaise · asli · pehchane · tareeke.
- **Rules:** Numbers as digits ("3 tareeke"). Questions on covers, answers inside.
- **Use:** genuine, natural, hand-finished, from the source, banded, polished, Mohs hardness, origin, batch.
- **Avoid:** magical, healing, manifest, cosmic, vibes, cheapest, bulk deal, 100% original!!!, energised, charged, aura.

---

## 7. Logo system (TO DESIGN)

Currently a Fraunces stand-in. Design:
- Primary wordmark (Fraunces-based, refined spacing), stacked lockup, capitals lockup with gold rule (packaging).
- **Monogram "NA"** for favicon, app icon, social avatar, wax-seal style sticker.
- **Agate-band seal** (bands + "Stones from the Source") as an optional mark for packaging and certificates.
- Versions on Sand, Ink and Carnelian only. Clear space = height of "N". Minimum sizes for screen and print.
- Exports: SVG, favicon 32/180/512, OG image 1200×630.

---

## 8. Imagery (TO LOCK from first reference photos)

- **Light:** natural daylight, soft window light, no flash. **Ground:** plain Sand or a neutral stone surface.
- **Angles:** straight-on, 45° top, macro of bands.
- **Per product set:** hero, scale with hand, pattern close-up, back/edge, packaging.
- **Workshop set (brand story):** cutting, grinding, polishing, hands, raw rough stone, the place. This is the proof behind "from the source".
- **Props:** max one (wooden tray, linen). Colour truth: the photo must match the stone in hand.
- **Never:** purple/galaxy backdrops, glitter, glow, filters, chakra graphics, heavy colour retouching.
- **Image prompt template:** "[One subject sentence]. Natural daylight, plain sand background, straight-on, sharp focus, true colour, no glow, no glitter, no props except [one]."

---

## 9. Website (design these)

### 9.1 Components (built from tokens only)
- **Announcement bar:** Ink, one message ("Free shipping above ₹1,000 · 7-day returns"), no countdowns.
- **Header:** 72px desktop / 56px phone, Surface + hairline, sticky. Nav: Shop · Wholesale · Partners · Stone knowledge · About. Search, wishlist, cart.
- **Footer:** Ink ground, Gold agate bands once. Includes GST number, address, WhatsApp and payment methods.
- **Product card:** 4:5 image, max ONE badge, overline (stone · finish), Fraunces name, size line, price (+ real sale price), stock tag with dot + word, "Add to cart".
- **Authenticity block (signature component):** Mineral · Mohs (with meter) · Origin · Finish · **Treatment** (natural / heated / dyed / lab) · **Batch no.** · Certificate link (or "Source-verified" with batch, never a fake lab claim).
- **"How to check it's real"**, 3 steps: light, temperature, glass scratch.
- **Reviews:** verified buyers only, gold stars as text colour, count always equals reviews shown.
- **System states:** toast, modal/drawer, skeleton (agate bands), empty state, 404 "This slice isn't here."
- **Touch:** on phones, chips and icon buttons have 44px hit areas.

### 9.2 Pages
1. **Homepage:**
   - hero ("Stones from the Source." + one fact + one CTA)
   - trust strip
   - shop by stone
   - best sellers
   - Stone Guide teaser
   - "How to tell a real stone"
   - workshop video
   - wholesale + partner band
   - reviews
   - newsletter
2. **Category page:** filters (stone, product, colour, size, price, finish, in stock) as a bottom sheet on phone; URL filters; pagination.
3. **Product page:**
   - gallery + video, price incl. GST, size chips
   - "Add to cart" + "Wholesale enquiry"
   - pincode delivery date, Authenticity block, Stone Guide
   - tabs: Stone facts / How to check / Care
   - reviews, related products
   - sticky buy bar on phone
4. **Stone knowledge hub** (`/stones/agate`): facts table, formation, how to identify, care, products, FAQ, author + date.
5. **Cart drawer** (free-shipping progress in Moss) → **Checkout** (single page, UPI/cards/COD, GST invoice toggle) → **Order success.**
6. **Wholesale:** catalogue table, MOQ, price-list PDF, quote form.
7. **About / Our source:** workshop story, place, people, process.

---

## 10. Stone Guide (AI): brand spec

- **Name:** "Stone Guide". Never "Master Gemologist" or "aura reader".
- **Personality:** the calm teacher, in short factual answers.
- **On every product page:** a compact panel "Ask about this stone" with quick-ask chips:
  - Is it real? How to check
  - How durable is it?
  - Care and cleaning
  - Where to place it
  - Good gift for…?
  - Compare with similar
  - (free text)
- **Standalone `/stone-guide`:** one question per screen (use, budget, form, colour, size), then 3–5 in-stock picks, each with a one-line factual reason.
- **Every answer ends with:** related products, "Add to cart", and "Send to my WhatsApp" (opt-in).
- **Visual:**
  - Surface card with hairline and an overline "STONE GUIDE".
  - Answer in body text; facts as a small spec list.
  - Thinking state: agate bands softly fading, with no sparkles or ✨.
- **Never:** zodiac matching, chakra, healing, energy, guaranteed outcomes.

---

## 11. Nazima Partners (reseller programme): brand spec

**Promise:** "Customer pays you first. We pack, ship, and pay your margin every week."

**Audience:**
- Home decor and gifting pages, interior designers, gift-shop owners, corporate-gifting agents.
- Homemakers and students with WhatsApp circles, marketplace sellers.

**Surfaces to design:**
1. **Partner landing page:**
   - hero promise, 3 steps (Choose stones · Set your price · We pack and ship)
   - **live profit calculator** (base price → your price → margin ₹ and %)
   - "Starting alone vs with Nazima" comparison table
   - honest real examples + "results vary" note, FAQ in plain words
2. **Apply flow:** phone OTP → details → PAN and bank (penny-drop) → approved screen with "what happens next".
3. **Partner dashboard (phone first):**
   - earnings card (pending / available / next payout date)
   - live catalogue with base price, suggested price, stock
   - create order, orders and tracking, customers, wallet statement
   - tier progress bar, marketing kit
4. **Partner mini-store** `nazimaagate.com/p/[code]`: partner's name on top, Nazima product cards with partner prices, checkout handled by Nazima.
5. **Marketing kit templates** (Hinglish content layer): reel covers, carousels, WhatsApp messages, festival creatives, in the v1.0 reel style ("Asli Agate kaise pehchane? 3 tareeke").
6. **Packaging variants:** (a) Nazima branded box, (b) **plain white-label box** for partners (Sand kraft, agate bands only, no logo, partner name sticker area, no base price inside).

**Rules:**
- Payments are automatic, never screenshots.
- Payout day is fixed and shown.
- Prices stay between a floor and the MRP.
- Referral bonus is one level only.
- Homepage, FAQ and terms say the same thing.
- No "up to 300%" or guaranteed income.

---

## 12. Trust system (our differentiator)

- **Batch label** on every pack: stone, origin, finish, treatment, batch no., QR code → batch page (photos, origin, process).
- **Certificate** for premium pieces with a named lab; sample certificate shown on the site.
- **Insert card:** "How to know it's real" (3 checks) + care + QR to workshop video (exists in v1.0, keep).
- **Guarantee:** "Genuine or full refund", written in the terms and repeated exactly on the site.
- **Honest numbers everywhere:** stock, reviews, discounts, partner earnings.

---

## 13. Accessibility and build notes

- WCAG AA minimum; visible focus ring; keyboard and screen-reader friendly; `lang="hi"` on Devanagari words; never colour alone.
- Mobile-first; test at 360px. Light theme default (true stone colour), dark theme available.
- Build stack (for handoff): Next.js + Firebase, tokens as CSS variables (`--nz-*`) and a Tailwind theme, `next/font`, `next/image`.

---

## 14. Never

- Gradients, glitter, glow, galaxy or purple-mystic imagery, chakra or zodiac graphics, sparkle emoji.
- Healing, energy, manifest, aura, 432Hz claims.
- Fake urgency, countdowns, stacked badges, inflated reviews, copy-pasted testimonials.
- "Certified" without a named document.
- More than one Carnelian action per view; gold used more than once per surface.
- Devanagari sentences; Hinglish in Fraunces.

---

## 15. Inputs still needed from the owner

- [ ] Logo direction approval (or existing logo file)
- [ ] 5–10 real product photos + workshop photos (to lock imagery)
- [ ] Workshop location and story details (city, years, team)
- [ ] Lab / certificate partner for premium pieces
- [ ] Partner base prices, tier thresholds, payout day
- [ ] Payment gateway, COD policy, shipping rates

---

## 16. Design order for Claude Design

1. Logo system + monogram + seal
2. Imagery style 01 (after photos)
3. Product card + Authenticity block + Stone Guide panel
4. Product page (phone + desktop, light + dark)
5. Homepage
6. Partner landing page + profit calculator
7. Partner dashboard (phone)
8. Packaging: branded box, white-label box, batch label, insert card
9. Marketing kit templates (reel cover, carousel, WhatsApp card)
10. Category page, cart, checkout, wholesale, About

---

## 17. Prompt to paste with this file

> This is the final Nazima Agate brand brief (v1.2). Keep every locked value exactly: colours, semantic tokens, Fraunces / Inter / Tiro Devanagari Hindi, spacing, radius, motion, agate-band motif and the "calm teacher" voice. Do not create a new palette or style. Extend the brand, starting with section 16, step 1: the logo system (wordmark, stacked lockup, NA monogram, agate-band seal) on Sand, Ink and Carnelian. Then continue step by step. Authentic, grounded, refined: one Carnelian action per view, gold used once, no gradients, nothing mystical.

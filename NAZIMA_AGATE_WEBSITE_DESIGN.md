# Nazima Agate: Website Design Extension (v1.1)

> Builds ON TOP of "Nazima Agate Design System v1.0" (14 Oct 2026). Do not replace v1.0. Every token, colour, font, voice rule and component in v1.0 stays. This file adds what the website needs and fixes small gaps.
> Paste this file together with the v1.0 DESIGN.md into Claude Design.
> Stack: Next.js (App Router) + Firebase. Language: English brand layer, Hinglish only on content (reels, tips).

---

## 0. What stays (from v1.0, locked)

- Brand: **Nazima Agate. Stones from the Source.** Authentic, Grounded, Refined.
- Colours: Carnelian `#8A3B22`, Sand `#F2EADF`, Ink `#1F1C1A`, Gold `#B08D57`, Moss `#56705E`. Flat colour, no gradients. Proportion Sand 60 / Ink 22 / Carnelian 10 / Moss 6 / Gold 2.
- Type: Fraunces (headlines 20px+), Inter (body/UI), Tiro Devanagari Hindi (one highlighted word only).
- 4px spacing scale, 1200px max width, radii none/4/8/14/full, hairline-first elevation, "settle, don't bounce" motion, agate-band motif.
- Rules: one Carnelian action per view, no healing/mystical claims, Hinglish spellings fixed (pathar, kaise, asli, pehchane, tareeke).

---

## 1. Gaps found in v1.0 for a real website

| Gap | Why it matters | Fixed in |
|---|---|---|
| No homepage pattern | First impression, SEO, conversion | 3.1 |
| No header, footer, mobile menu, announcement bar spec | Every page needs them | 2.1 to 2.3 |
| No category / listing page, filters, sort, search | Core of an e-commerce site | 3.2 |
| No cart drawer, checkout, order success | Revenue path | 3.4 to 3.6 |
| No certificate / authenticity component | Biggest trust gap in the market | 2.5 |
| No reviews component | Social proof | 2.6 |
| No toast, modal, drawer, skeleton, empty, error states | Needed for any app-like behaviour | 2.7 |
| Imagery section is empty ("Awaiting reference") | Photos make or break a stone brand | 5 |
| Chips are 36px tall | Below 44px touch target on phones | 6.1 |
| No logo file (Fraunces stand-in) | Needed for header, favicon, OG image | 6.2 |
| No partner/reseller surfaces | Wholesale and partner growth | 3.7 |
| No Stone Guide (AI) pattern | Planned hero feature | 3.8 |
| No performance, SEO, accessibility rules | Next.js build quality | 7 to 9 |

---

## 2. New website components

All built only from v1.0 tokens. No new colours.

### 2.1 Announcement bar
- Height 36px, background `--nz-ink`, text `--nz-sand`, `label-sm`.
- One message only, e.g. "Free shipping above ₹1,000 · 7-day returns". No rotating banners, no countdowns.
- Dismissible (X, 44px hit area), remembered per visitor.

### 2.2 Header
- Desktop: wordmark left, nav centre (Shop, Wholesale, Stone knowledge, About), search + wishlist + cart right. Height 72px, `--nz-surface`, 1px `--nz-border` bottom. Sticky on scroll, no shadow (hairline only).
- Cart icon shows item count as a small Carnelian dot-tag (max "9+").
- Mobile (<640px): menu button, centred wordmark, cart. Height 56px. Search opens as a full-width bar below the header.
- Mega menu for Shop: columns "By stone", "By product", "By colour". Max 3 columns, text links only, one image allowed.
- Tabs use the v1.0 sliding underline.

### 2.3 Footer
- Background `--nz-ink`, text `--nz-sand`. Four columns: Shop, Wholesale, Learn, Company. Bottom row: GST number, address, WhatsApp, payment methods, copyright.
- Gold agate-band motif once, large, low emphasis, behind nothing.
- Newsletter: one email field + one Carnelian button. Copy: "Stone facts, once a month."

### 2.4 Product card (extends v1.0 card)
- Image ratio 4:5, `--nz-surface-sunken` placeholder with agate bands while loading.
- Max **one** badge: "New", "Best seller" or "Collector grade" (gold premium tag). Never stack badges.
- Show: overline (stone + finish), name (Fraunces h4), size/finish line, price (+ struck old price if on sale), stock tag (status with dot + word).
- Hover (desktop): second photo crossfade 200ms. No zoom, no sparkle.
- Primary button "Add to cart". On low stock show the real number ("Only 3 left"), never fake.
- Wishlist icon top right, 44px hit area.

### 2.5 Authenticity block (new, hero trust component)
On every product page, directly under the price area:
- Row of facts: Mineral, Hardness (Mohs), Origin, Finish, Colour (natural/treated). **Treatment must always be stated** (natural, heated, dyed, lab-grown).
- "Certificate" chip linking to the uploaded certificate (PDF/image viewer in a modal). If none exists, show "Source-verified by Nazima Agate" with batch number, never imply a lab certificate.
- Mohs meter (v1.0 data component) next to the hardness value.
- "How to check it's real" 3-step cards (v1.0 pattern) below the fold.

### 2.6 Reviews
- Verified-buyer only. Stars use `--nz-accent-text` (gold text), never gold fill on Sand.
- Summary: average, count, distribution bars (flat Moss bars).
- Review card: name, city, date, stone bought, text, optional photos. "Verified purchase" moss tag.
- No fake or repeated reviews. Empty state: "No reviews yet. Be the first after you receive your stone."

### 2.7 System states
- **Toast:** surface, hairline border, shadow-1, bottom-left desktop / bottom-centre phone, 4s, with icon + word (never colour alone).
- **Modal / drawer:** shadow-2, radius-lg, 320ms slide with `--nz-ease-standard`; focus trapped; Esc closes; scrim `rgba(31,28,26,0.5)`.
- **Skeleton:** `--nz-surface-sunken` blocks with the agate-band motif fading 0.6 to 1 opacity, 1.2s. Respect reduced motion (static).
- **Empty state:** agate motif (Subtle on Surface), one sentence, one action.
- **Error page (404/500):** "This slice isn't here." + search + link to Shop.
- **Form errors:** icon + sentence, v1.0 input-error style.

---

## 3. Page patterns

### 3.1 Homepage (top to bottom, one idea per section)
1. **Hero:** display headline "Stones from the Source." + one fact line + one Carnelian CTA ("Shop agate") + secondary ghost ("Wholesale enquiry"). Large natural-light stone photo on the right, Sand ground. Carnelian agate-band motif as quiet background lines.
2. **Trust strip:** 4 items, each icon + 3 words: Hand-finished in India · Natural colour · Pan-India delivery · 7-day returns. (+ COD if enabled.)
3. **Shop by stone:** 6 large image tiles (Agate, Amethyst, Carnelian, Quartz, Jasper, Moss agate) + "View all stones".
4. **Best sellers:** 4 product cards in a row (carousel on phones, swipe, no autoplay).
5. **Stone Guide teaser:** "Not sure which stone? Ask our Stone Guide." (see 3.8), on an Ink dark panel with Gold bands.
6. **How to tell a real stone:** the 3-step teaching block (Hold to light, Feel the temperature, Glass scratch). This is the brand's signature idea.
7. **Wholesale and partner band:** "Buy in bulk or sell Nazima Agate stones." Two CTAs.
8. **Reviews:** 3 verified reviews + summary.
9. **From the workshop:** 3 short reel/video tiles (shoppable).
10. **Newsletter + footer.**

Rule: only ONE Carnelian button in the viewport at a time. Section spacing 96px desktop / 64px phone.

### 3.2 Category / listing page
- Title (h1), one-line description, result count.
- Left filter column desktop (280px), bottom-sheet drawer on phone. Filters: Stone, Product type, Colour, Size, Price, Finish, In stock only. Applied filters shown as selected chips (44px) with "Clear all".
- Sort: Featured, Price low-high, Price high-low, New.
- Filters live in the URL (`?stone=agate&colour=grey&sort=new`) so pages are shareable and SEO-indexable.
- Grid: 4 columns desktop, 3 tablet, 2 phone. Pagination (v1.0), not infinite scroll.
- Free-shipping progress shown in cart, not on listing.

### 3.3 Product page (extends v1.0 Pattern 01)
- Gallery: main image + thumbnails, swipe on phone, tap to zoom (lightbox). Minimum 4 photos: hero, scale-with-hand, pattern close-up, back/side.
- Info column: overline, h1, price (incl. GST), tags, short description, size chips, quantity, "Add to cart" + "Wholesale enquiry", delivery estimate by pincode, then Authenticity block (2.5).
- **Sticky add-to-cart bar on phones** (price + button) once the main button scrolls away.
- Below: Stone facts / How to check / Care tabs, reviews, "You may also like" (4 cards), recently viewed.

### 3.4 Cart (drawer from right, 420px; full page on phone)
- Line items with thumb, name, size, qty stepper (44px), remove, price.
- **Free-shipping progress bar:** flat Moss fill: "Add ₹350 for free shipping".
- Order summary: subtotal, shipping, GST, total. One Carnelian button: "Checkout". Secondary link: "Continue shopping".

### 3.5 Checkout (single page, guest allowed)
1. Contact (phone OTP or email) 2. Address (pincode auto-fills city/state) 3. Delivery 4. Payment (UPI, cards, netbanking, COD if enabled) 5. Review + place order.
- GST invoice toggle (business name + GSTIN) because wholesale buyers need it.
- Progress shown as numbered steps; sticky order summary on desktop, collapsible on phone.
- Trust row under the button: secure payment, 7-day returns, WhatsApp support.
- No upsells or pop-ups in checkout.

### 3.6 Order success
- Check icon + "Order placed." + order number, delivery estimate, WhatsApp updates opt-in, "How to check it's real" insert-card preview. Single action: "Track order".

### 3.7 Wholesale and partner
- **Wholesale page (v1.0 Pattern 02 extended):** catalogue table, MOQ, price-list PDF, "Request a quote" form (business name, GSTIN, product type, quantity, city, phone). Quote confirmation with expected reply time.
- **Partner programme page:** "Sell Nazima Agate stones. Keep the margin." Explain model in 3 steps (Choose stones, Set your price, We pack and ship). Include an interactive **profit calculator** (base price, your price, margin shown in ₹ and %).
- Use real, honest numbers and the income disclaimer. No guaranteed-earning headlines.
- **Partner dashboard:** catalogue with base prices, profit calculator, create order, order tracking, customers, wallet and payouts, marketing kit (Hinglish captions, reel templates). Uses table, card, tag and tab components from v1.0.

### 3.8 Stone Guide (AI consultant)
Name it **Stone Guide**, not "aura/energy reader", to stay inside the brand rule *"Grounded, never mystical"*.
- Inputs (stepper, one question per screen): What are you looking for (gift, home decor, jewellery, collection, business), budget, preferred form (slice, tumbled, coaster, sphere, bookend), colour preference, optional occasion. Optional name and WhatsApp number to save the result.
- Output: 3 to 5 products from the live catalogue, each with a plain reason ("Banded Agate, 6.5–7 Mohs, durable for daily handling"). Buttons: "Add all to cart" and "Share on WhatsApp".
- Tone: knowledgeable teacher. Any traditional or astrological belief is allowed only as a clearly labelled "traditional belief" note, never as a claim of effect.
- Safety: never recommend out-of-stock items; never give medical/financial promises.

---

## 4. Responsive behaviour (follows v1.0 breakpoints)

| Element | Phone 0–639 | Tablet 640–1023 | Desktop 1024+ |
|---|---|---|---|
| Header | 56px, menu drawer | 64px, condensed nav | 72px, full nav |
| Product grid | 2 col | 3 col | 4 col |
| Filters | Bottom sheet | Bottom sheet | Left column |
| Product page | Stacked, sticky buy bar | 2 col | 2 col, sticky gallery |
| Cart | Full page | Drawer | Drawer |
| Hero | Image under text | Side by side | Side by side |
| Section gap | 64px | 64px | 96px |

Mobile-first: most Indian traffic is phone. Test at 360px width.

---

## 5. Imagery rules (fills the empty v1.0 section)

Locked proposal, to confirm against your first reference photos:
- **Light:** natural daylight, soft window light, no flash. **Ground:** plain Sand or neutral stone surface. **Angle:** straight-on and 45° top; macro of bands as detail.
- **Set per product:** hero, scale shot with hand, pattern close-up, back/edge, packaging shot.
- **Props:** at most one (a wooden tray or linen). **Never:** galaxy/purple backgrounds, glitter, glow, filters, chakra graphics, heavy retouching of stone colour.
- Colour truth: photo must match the stone in hand. Dyed or treated stones are photographed honestly and labelled.
- Delivery: WebP/AVIF, `next/image`, sizes defined, alt text states stone + finish.
- Placeholder: agate-band motif on `--nz-surface-sunken`.
- Image prompt template for AI references: "[One subject sentence]. Natural daylight, plain sand background, straight-on, sharp focus, true colour, no props glow or glitter."

---

## 6. Improvements to v1.0 values

### 6.1 Touch targets
- On phones, `chip`, `button-sm` and icon buttons must have **44px** minimum height/hit area (desktop keeps 36px chips). Add token `--nz-touch-min: 44px`.
- Tabs on phones scroll horizontally with edge fade (no gradient colour, use mask) and a visible selected underline.

### 6.2 Logo
- Needs: primary wordmark, stacked lockup, monogram "NA" (favicon, avatar), one-colour versions for Sand/Ink/Carnelian grounds, minimum sizes, clear-space rule (height of the "N"), the agate-band mark as optional seal.
- Until the logo exists, keep the Fraunces stand-in. Export: SVG, favicon 32/180/512, OG image 1200×630.

### 6.3 Colour use on web
- Gold on Sand is decorative only (2.59:1); gold-coloured readable text must use `--nz-accent-text`.
- Links in body: Carnelian + underline always (not colour alone).
- Dark theme: provide toggle in footer and respect `prefers-color-scheme`; default to light for catalogue photography accuracy.

### 6.4 New tokens (add to the v1.0 token file)

```css
/* Nazima Agate web extension v1.1 */
:root {
  --nz-touch-min: 44px;
  --nz-header-h: 72px;
  --nz-header-h-phone: 56px;
  --nz-announcement-h: 36px;
  --nz-container: 1200px;
  --nz-scrim: rgba(31, 28, 26, 0.5);
  --nz-z-header: 100;
  --nz-z-drawer: 200;
  --nz-z-modal: 300;
  --nz-z-toast: 400;
  --nz-ratio-product: 4 / 5;
  --nz-ratio-hero: 5 / 4;
}
[data-theme="dark"] {
  --nz-scrim: rgba(0, 0, 0, 0.6);
}
@media (prefers-reduced-motion: reduce) {
  * { animation-duration: 120ms !important; transition-duration: 120ms !important; }
}
```

---

## 7. Performance and engineering (Next.js)

- Fonts via `next/font` (Fraunces, Inter, Tiro Devanagari Hindi with `display: swap`; subset latin + devanagari; load Tiro only on pages that use it).
- Targets: LCP under 2.5s on 4G, CLS under 0.1, INP under 200ms. Hero image prioritised, all others lazy.
- Images through `next/image` (AVIF/WebP), explicit width/height to prevent layout shift.
- Tokens exposed as CSS variables + Tailwind theme (`nz` prefix) from the v1.0 exports.
- Rendering: static/ISR for catalogue and product pages, client-side for cart and Stone Guide.
- Firebase: Auth (phone OTP), Firestore, Storage (media + certificates), Functions (orders, payment webhook, partner wallet).

## 8. SEO

- Clean URLs: `/shop/agate/slices`, `/product/banded-agate-slice-natural-grey`, filters in query params with canonical to the clean category.
- Product JSON-LD (name, image, price INR, availability, rating). Breadcrumb JSON-LD. Organisation schema.
- Unique title/meta per page, OG image per product, XML sitemap, robots, 301s for retired URLs.
- Educational content hub ("Stone knowledge"): Mohs hardness, how to tell real agate, care, origin. This is the brand's SEO engine and fits "Teach before you sell".

## 9. Accessibility

- WCAG AA minimum (v1.0 contrast table already passes). Visible focus ring everywhere (2px, 2px offset).
- Keyboard: logical tab order, skip-to-content link, Esc closes overlays, focus trapped in modal/drawer and returned on close.
- Status never by colour alone (icon + word). Alt text on all images. Form labels above inputs, errors linked with `aria-describedby`.
- Respect `prefers-reduced-motion` (120ms fade only).
- Hindi/Devanagari text marked with `lang="hi"`.

---

## 10. Trust and compliance (website)

1. Every "natural / genuine" claim must link to evidence (certificate or source batch).
2. State treatments honestly on every product.
3. No healing, astrology-effect or financial-outcome claims. Traditional belief only as a labelled note.
4. Partner income: real examples + disclaimer, no guarantees.
5. Reviews: verified purchase only.
6. Clear shipping, return, refund, privacy and terms pages; GST invoice; consent for WhatsApp/email.

---

## 11. Build order

1. Tokens + fonts + base components (button, tag, chip, input, card)
2. Header, footer, announcement bar
3. Product card + category page + filters
4. Product page + Authenticity block
5. Cart + checkout + order success
6. Homepage
7. Wholesale page + quote form
8. Stone Guide
9. Partner page + calculator + dashboard
10. Stone knowledge hub + SEO polish

---

## 12. Open decisions

- [ ] Logo and favicon
- [ ] First photo references (locks imagery style 01)
- [ ] Payment gateway, COD yes/no
- [ ] Certificate/lab process
- [ ] Shipping partner and rates
- [ ] Partner margin and tier rules
- [ ] Launch languages

---

## 13. Prompt to paste into Claude Design

> Using the attached Nazima Agate Design System v1.0 and this Website Design Extension v1.1, design the website. Keep all v1.0 tokens, fonts, voice and rules unchanged. Produce, for desktop and phone in light and dark: homepage, category page with filters, product page with the Authenticity block and sticky mobile buy bar, cart drawer, checkout, wholesale quote page, partner programme page with profit calculator, and the Stone Guide flow. Calm, grounded, refined; sand-led, one Carnelian action per view, gold used once, no gradients, no mystical imagery.

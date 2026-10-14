# Brand Foundation: Gemstone Commerce + Partner Network

> Purpose: single source of truth to paste into Claude Design before any website, app or marketing work.
> Stack target: Next.js + Firebase. Status: STUDY-STAGE brief (nothing replicated; ideas distilled from 3 reference sites).
> Fill every `[PLACEHOLDER]` before locking the brand.

---

## 1. Brand Core

| Item | Value |
|---|---|
| Brand name | Nazima Agate (see Nazima Agate Design System v1.0) |
| Tagline | Stones from the Source. |
| Category | Natural gemstones, crystals, jewellery, decor + partner/reseller platform |
| Market | India first (INR, COD, UPI, Hinglish), export later |
| Three pillars | 1) Verified Authenticity 2) Guided Discovery (AI gemologist) 3) Earn With Us (partner network) |

**Mission:** Make genuine gemstones easy to buy, understand and sell, and let anyone start a low-risk side business with them.

**Brand promise:** Every stone is genuine and documented. Every partner earns transparently.

**Personality:** Trustworthy, warm, knowledgeable, premium but approachable. Spiritual without making unprovable claims.

**Voice:** Simple English with Hinglish touches for marketing and partner content. Clear and calm. Never hype, never fear-based.

**Never say:** Unverifiable claims ("cures", "guaranteed wealth", "432Hz charged" without proof), fake urgency, fake counters, income guarantees.

---

## 2. Audience

1. **Buyer:** Wants a stone for a purpose (wealth, calm, protection, love, career) or a gift. Needs trust and guidance.
2. **Partner / side-hustler:** Student, homemaker, working professional, small reseller. Wants low-risk income, no inventory, ready content.
3. **Bulk / wholesale buyer:** Shops, astrologers, gift sellers. Wants rate cards and fast quotes.

---

## 3. Competitive Study: What To Take, What To Fix

### 3.1 stonemart.co.in (store basics)
**Take:**
- 4-way browsing: by stone (~50, "Popular" first), by category (~25 image tiles), by jewellery type, by colour
- URL-parameter filters (shareable and SEO friendly)
- Product badges (Best Seller, New, Premium), % off tag, struck-through price, "Only 1 left"
- "Add to Cart" + "Buy Now" together
- Persistent free-shipping banner (free above ₹1,000, else ₹60), 7-day return shown on homepage
- Separate Bulk / Wholesale inquiry route

**Fix (their gaps = our edge):**
- No certificates or lab reports behind "100% natural" claims
- No reviews, unclear payment methods, listing bugs ("No matches found"), spelling errors

### 3.2 partner.shubhnumbers.com (partner model)
**Model:** Resale margin. Partner sets own price, collects customer payment first, then pays supplier a fixed base price. Partner keeps the difference (example: base ₹400, sell ₹1,000, margin ₹600).

**Take:**
- Customer-pays-first (zero working-capital risk)
- Live profit calculator per product, visible base price
- Done-for-you packing and shipping, partner-branded parcel
- Marketing kit: English/Hinglish captions, reels, WhatsApp messages, story templates, festival creatives
- Instant approval, no fee, no lock-in
- Dashboard: catalogue, stock status, order entry, tracking, customer records, recommendation tool

**Fix (their implementation gaps):**
- Manual UPI/bank screenshot verification, so use payment gateway with auto-verification
- No tiers, no referral/team earning, vague payouts, so build all three
- Inflated "300%" headline, repeated testimonial, so use honest numbers and real, verified partner stories
- Narrow refund policy, so write a fair, clear policy

### 3.3 empireagate.com (AI consultant and conversion)
**Take:**
- AI "Aura reading" flow: name + zodiac + desired energy (Wealth, Stress Relief, Protection, Love, Career) + preferred format (Tree, Bracelet, Agate Slice, Pendant/Pyramid)
- "Shop by Intention" (Calm, Abundance, Love, Protection) that mirrors the AI inputs
- Shoppable reels (video with product card and price)
- Cash on Delivery, 24-hour dispatch promise, review count display, bundles and discount badges

**Fix:**
- No lead capture (no phone/email), no clear link from reading to products, no pricing clarity
- Unprovable "frequency" claims and unverifiable review numbers

---

## 4. Product Pillars (Feature Blueprint)

### A. Store
- 4-way browse + intention browse
- Product page: photos and video, weight/size/origin, **certificate upload and viewer**, treatment disclosure (natural / heated / lab), care guide, reviews with photos
- Trust strip: certified, COD, 7-day return, 24h dispatch, secure pay (list actual methods)
- Cart upsells: free-shipping progress bar, bundles

### B. AI Master Gemologist (hero feature)
- Inputs: name, birth details (optional), intention, budget, preferred format, phone/WhatsApp
- Output: ranked product picks with reasons, care and wearing tips, "add all to cart"
- Lead capture: result saved and sent on WhatsApp/email; shareable result card
- Guardrails: no medical or guaranteed-outcome claims; show "traditional belief" framing and disclaimer
- Fed by real catalogue and stock, so it never recommends out-of-stock items

### C. Partner Network
- Apply, instant or quick approval, no fee
- Partner dashboard: catalogue with base price, **profit calculator**, own price setting, order entry, tracking, customers, wallet and payouts
- Partner mini-store link (`brand.com/p/[code]`) plus WhatsApp share
- Tiers by monthly volume (better base price at higher tiers), optional referral bonus for recruiting partners
- Auto payment collection and verification, payout schedule defined and visible
- Marketing kit library, updated for festivals

### D. Wholesale
- Rate card, MOQ, quick inquiry form, WhatsApp quote

### E. Trust Layer
- Certificates, real reviews (verified purchase only), honest return policy, income disclaimer for partners

---

## 5. Visual Direction (to refine in Claude Design)

| Area | Direction |
|---|---|
| Mood | Premium, calm, earthy-luxury. Think museum-grade stone photography, not neon-spiritual clutter |
| Palette idea | Deep neutral base (ivory / charcoal), one rich accent (e.g. amethyst or emerald), gold as a sparing highlight. `[CONFIRM HEX VALUES]` |
| Typography | Elegant serif for headings, clean sans for body and UI. Must support Hindi/Devanagari |
| Imagery | Macro stone shots on neutral backgrounds, hands-on lifestyle shots, short reels |
| Components | Product card with badge slots, certificate badge, intention chips, profit-calculator widget, partner dashboard cards |
| Tone in UI | Short labels, clear prices, no fake timers |
| Accessibility | Mobile-first (most Indian traffic), readable contrast, large tap targets, light and dark themes |

---

## 6. Trust and Compliance Rules (non-negotiable)

1. Every "natural / certified" claim must be backed by a document in the product page.
2. Disclose treatments (heated, dyed, lab-grown).
3. Partner income: show real examples with disclaimer, never guarantee earnings.
4. Spiritual and astrological content framed as belief/tradition, no health or financial promises.
5. Reviews: verified buyers only, no repeated or fabricated testimonials.
6. Clear shipping, return and refund policy; GST and invoice handled properly.
7. Privacy: consent for WhatsApp/email contact, protect birth and personal data.

---

## 7. Technical Foundation (Next.js + Firebase)

- **Frontend:** Next.js (App Router), mobile-first, SEO-friendly filter URLs
- **Auth:** Firebase Auth with phone OTP (buyer, partner, admin roles)
- **Database:** Firestore collections: `products`, `categories`, `orders`, `partners`, `partnerOrders`, `wallets`, `payouts`, `reviews`, `consultations`, `leads`
- **Storage:** product media and certificates
- **Functions:** order pipeline, payment webhook verification, partner margin and wallet ledger, payout calculation, AI consultation endpoint
- **Payments:** Indian gateway (UPI, cards, netbanking) + COD; webhook-verified
- **AI:** Claude API for gemologist consultant, grounded on catalogue data
- **Notifications:** WhatsApp / SMS / email for orders, results and payouts
- **Security:** Firestore rules by role, server-side price and margin validation, audit trail on wallet changes

---

## 8. Phased Roadmap

1. **Phase 0, Brand:** name, palette, type, logo, voice, this document finalised
2. **Phase 1, Store MVP:** catalogue, filters, product pages with certificates, cart and checkout, COD and online pay
3. **Phase 2, AI Gemologist:** consultation flow, lead capture, recommendations to cart
4. **Phase 3, Partner Network:** onboarding, dashboard, mini-store, auto payments, wallet and payouts
5. **Phase 4, Growth:** tiers, referrals, marketing kit automation, shoppable reels, wholesale portal, analytics

---

## 9. Success Metrics

- Store: conversion rate, average order value, COD vs prepaid ratio, return rate
- AI: consultations started to completed to added-to-cart, leads captured
- Partners: applications to first order, active partners per month, average partner profit, payout on-time rate
- Trust: share of products with certificate, verified review count

---

## 10. Open Decisions (fill before design lock)

- [ ] Brand name and tagline
- [ ] Final palette and fonts
- [ ] Margin structure and partner tier thresholds
- [ ] Payment gateway choice
- [ ] Certification partner / lab process
- [ ] Languages at launch (English, Hindi, Hinglish)
- [ ] Return and refund policy wording

---

## 11. Prompt to Paste Into Claude Design

> Use `BRAND_FOUNDATION.md` as the brand base. Create a cohesive brand system for a premium Indian gemstone e-commerce and partner/reseller platform: logo directions, colour palette, typography (with Devanagari support), imagery style, and UI components (product card with certificate badge, intention chips, AI gemologist flow, partner profit calculator, partner dashboard). Mood: earthy-luxury, calm, trustworthy, mobile-first. Avoid neon-spiritual clichés and fake-urgency patterns.

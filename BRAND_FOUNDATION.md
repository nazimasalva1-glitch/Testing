# Brand Foundation: Gemstone Commerce + Partner Network

> Purpose: BUSINESS brief (what we sell, to whom, which features). It does NOT define the visual brand.
> **Priority order:** 1) Nazima Agate Design System v1.0 (colours, fonts, voice, rules) 2) Website Design Extension v1.1 3) this file.
> If anything here conflicts with v1.0, **v1.0 wins**. Do not create a new palette, logo, typography or voice from this file.
> Stack target: Next.js + Firebase. Ideas distilled from 3 reference sites, nothing replicated.

---

## 1. Brand Core

| Item | Value |
|---|---|
| Brand name | Nazima Agate (see Nazima Agate Design System v1.0) |
| Tagline | Stones from the Source. |
| Category | Natural gemstones, crystals, jewellery, decor + partner/reseller platform |
| Market | India first (INR, COD, UPI, Hinglish), export later |
| Three pillars | 1) Verified Authenticity 2) Guided Discovery (Stone Guide, AI) 3) Earn With Us (partner network) |

**Mission:** Make genuine gemstones easy to buy, understand and sell, and let anyone start a low-risk side business with them.

**Brand promise:** Every stone is genuine and documented. Every partner earns transparently.

**Personality and voice:** As defined in v1.0: Authentic, Grounded, Refined. A calm teacher who knows stones. English brand layer, Hinglish content layer. Never mystical, never loud.

**Never say:** Unverifiable claims ("cures", "guaranteed wealth", "432Hz charged" without proof), fake urgency, fake counters, income guarantees.

---

## 2. Audience

1. **Buyer:** Wants a genuine stone for decor, gifting, jewellery or collection. Needs trust (is it real?) and guidance (which one?).
2. **Partner / side-hustler:** Student, homemaker, working professional, small reseller. Wants low-risk income, no inventory, ready content.
3. **Bulk / wholesale buyer:** Shops, gift sellers, decor and jewellery businesses. Wants rate cards and fast quotes.

---

## 3. Competitive Study: What To Take, What To Fix

### 3.1 stonemart.co.in (store basics)
**Take:**
- 4-way browsing: by stone (~50, "Popular" first), by category (~25 image tiles), by jewellery type, by colour
- URL-parameter filters (shareable and SEO friendly)
- Product badges (max ONE per card, per v1.0 restraint), struck-through sale price, real stock count only
- Clear primary "Add to cart" (one Carnelian action per view)
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
- The idea of a guided AI consultant with a step-by-step form and preferred format (Tree, Bracelet, Agate Slice, Pendant/Pyramid). We rebuild it as a grounded **Stone Guide** (use, budget, form, colour), NOT aura/zodiac/energy, to follow v1.0 "Grounded, never mystical"
- Guided browse entry points (ours: by use: Gift, Home decor, Jewellery, Collection)
- Shoppable reels (video with product card and price)
- Cash on Delivery, 24-hour dispatch promise, review count display, bundles and discount badges

**Fix:**
- No lead capture (no phone/email), no clear link from reading to products, no pricing clarity
- Unprovable "frequency" / aura claims (we never use them) and unverifiable review numbers

---

## 4. Product Pillars (Feature Blueprint)

### A. Store
- 4-way browse (stone, product, colour, size) + browse by use
- Product page: photos and video, weight/size/origin, **certificate upload and viewer**, treatment disclosure (natural / heated / lab), care guide, reviews with photos
- Trust strip: certified, COD, 7-day return, 24h dispatch, secure pay (list actual methods)
- Cart upsells: free-shipping progress bar, bundles

### B. Stone Guide, AI consultant (hero feature)
- Inputs: use (gift, decor, jewellery, collection, business), budget, preferred form, colour, optional name and WhatsApp
- Answers in mineral facts (hardness, origin, care), per v1.0 voice
- Output: ranked product picks with reasons, care and wearing tips, "add all to cart"
- Lead capture: result saved and sent on WhatsApp/email; shareable result card
- Guardrails: no healing, energy, astrology-effect or guaranteed-outcome claims
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

## 5. Visual Direction

**Defined by Nazima Agate Design System v1.0. Do not redefine here.** Colours (Carnelian, Sand, Ink, Gold, Moss), fonts (Fraunces, Inter, Tiro Devanagari Hindi), spacing, shape, motion, agate-band motif and voice all come from v1.0. Website-specific additions are in `NAZIMA_AGATE_WEBSITE_DESIGN.md`.

---

## 6. Trust and Compliance Rules (non-negotiable)

1. Every "natural / certified" claim must be backed by a document in the product page.
2. Disclose treatments (heated, dyed, lab-grown).
3. Partner income: show real examples with disclaimer, never guarantee earnings.
4. No healing, energy, astrology-effect or financial promises (v1.0: "Grounded, never mystical").
5. Reviews: verified buyers only, no repeated or fabricated testimonials.
6. Clear shipping, return and refund policy; GST and invoice handled properly.
7. Privacy: consent for WhatsApp/email contact, protect personal data.

---

## 7. Technical Foundation (Next.js + Firebase)

- **Frontend:** Next.js (App Router), mobile-first, SEO-friendly filter URLs
- **Auth:** Firebase Auth with phone OTP (buyer, partner, admin roles)
- **Database:** Firestore collections: `products`, `categories`, `orders`, `partners`, `partnerOrders`, `wallets`, `payouts`, `reviews`, `consultations`, `leads`
- **Storage:** product media and certificates
- **Functions:** order pipeline, payment webhook verification, partner margin and wallet ledger, payout calculation, AI consultation endpoint
- **Payments:** Indian gateway (UPI, cards, netbanking) + COD; webhook-verified
- **AI:** Claude API for the Stone Guide, grounded on catalogue data
- **Notifications:** WhatsApp / SMS / email for orders, results and payouts
- **Security:** Firestore rules by role, server-side price and margin validation, audit trail on wallet changes

---

## 8. Phased Roadmap

1. **Phase 0, Brand:** done in v1.0; remaining: logo file and photo references
2. **Phase 1, Store MVP:** catalogue, filters, product pages with certificates, cart and checkout, COD and online pay
3. **Phase 2, Stone Guide:** consultation flow, lead capture, recommendations to cart
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

- [x] Brand name, tagline, palette, fonts (v1.0)
- [ ] Logo file
- [ ] Margin structure and partner tier thresholds
- [ ] Payment gateway choice
- [ ] Certification partner / lab process
- [ ] Languages at launch (English, Hindi, Hinglish)
- [ ] Return and refund policy wording

---

## 11. How to use this file in Claude Design

Upload together with v1.0 and the Website Extension. Do not ask Claude Design to create a new brand system from this file. Use it only as business context for features and page content:

> This file is business context only. Keep the Nazima Agate Design System v1.0 exactly as it is (colours, fonts, voice, rules). Use this file to understand the products, audiences, Stone Guide, wholesale and partner features.

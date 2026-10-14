# Competitor Deep Analysis: Stone Mart, ShubhCrystals Partner Hub, Empire Agate

> For: Nazima Agate (gemstone e-commerce + partner/reseller, Next.js + Firebase)
> Date: 14 Oct 2026. Method: live pages, product pages, guides, terms, sitemaps, robots.txt and front-end JavaScript inspected. Nothing copied.
> Lens: Nazima Agate Design System v1.0 ("Authentic, Grounded, Refined", "Teach before you sell", "Grounded, never mystical").

---

## 0. Executive summary

| Site | Best idea to take | Biggest weakness = our opportunity |
|---|---|---|
| **stonemart.co.in** | Huge, well-structured catalogue (787 products) with stone "hub" pages that teach + sell, clean SEO hygiene | Claims without proof: "100% authentic" with no certificate, 205 reviews on a product vs only 6 on the reviews page, healing claims as fact |
| **partner.shubhnumbers.com** | Zero-risk reseller model: customer pays partner first, supplier ships white-label, partner keeps margin | Built badly: manual UPI screenshots, homepage promises contradict the terms, fake-looking testimonials, no SEO, one active partner |
| **empireagate.com** | AI "Master Gemologist" **inside every product page** with quick-ask buttons, plus per-product guide pages and international selling | Mystical tone, rating numbers that don't add up, AI with no lead capture, "Certified" with no named lab |

**Market truth:** all three sell on *mystical claims* and *unproven trust*. Nobody in this space proves authenticity. Nazima's positioning (real facts, real proof, calm teacher) is a genuine gap, not just a style choice.

---

## 1. Tech stack seen (useful for our build)

| | Stone Mart | ShubhCrystals Partner | Empire Agate |
|---|---|---|---|
| Framework | **Next.js** (SSR) | Lovable-built Vite React SPA (client-only) | **Next.js** on Vercel |
| SEO files | robots.txt + sitemap (854 URLs) | None (404) | robots.txt + sitemap (282 URLs) |
| Analytics | Google tag | none visible | Google tag + **Microsoft Clarity** (heatmaps) |
| AI | none | "smart recommendation tool" (behind login) | **Google Gemini** via `/api/ai/crystal-assistant` and `/api/ai/aura-reading` |
| Other | user-data-deletion page, track-order page | PDF catalogue, WhatsApp | geolocation + exchange-rates API (multi-currency), push notifications, WhatsApp API, email API |

Lesson: Next.js with server rendering is the right call (two of three use it). The partner site's client-only SPA has no robots or sitemap, so Google barely sees it.

---

## 2. stonemart.co.in, deep dive

### 2.1 What is genuinely best
1. **Catalogue architecture.** 787 products, 26 category pages, 8 stone hubs, 17 blog posts, 4 guides. Browse by stone (~50), category (~25 tiles), jewellery type (10), home decor (16), colour (14).
2. **Stone hub pages** (`/stones/amethyst`): an at-a-glance table (Mohs hardness, colour, origins, "also called"), then background, uses, a product grid, care, FAQ and related stones. **This is exactly Nazima's "Teach before you sell" in page form.** Best single idea on this site.
3. **SEO hygiene.** robots.txt blocks `/cart`, `/checkout`, `/account` and filter params (`?sort=`, `?pmin=`, `?page=`), so Google does not waste crawl on duplicate pages. Clean slugs, breadcrumbs, JSON-LD, FAQ in question format.
4. **Commerce basics.** MRP + sale price + % off, real stock count ("7 left"), free-shipping threshold (₹60 below ₹1,000, free above) repeated in banner and badges, COD, 7-day returns, wholesale icon in the header, track-order page.
5. **Compliance pages** (user-data-deletion, privacy, terms, shipping, returns), needed for Meta/Google login and ads approval.

### 2.2 What is weak (do the opposite)
- **Reviews don't add up:** the product page shows "4.5 from 205 Verified Buyers", but the site-wide reviews page lists **6 reviews in total**. Some are one-word ("Hi", "Heool") or generic, and one reviewer may be linked to the business.
- **No proof behind "100% Authentic":** no certificate, origin, treatment or weight on product pages.
- **Healing claims stated as fact** ("calms anxiety", "enhances sleep") with a disclaimer only on some guides; no author or date on health-adjacent guides.
- **Thin product specs:** a bracelet with no length/wrist size, no weight, no origin. Gallery repeats image 1.
- **Broken bits:** "No matches found" in the menu, an empty bundles page, "Rs." and "₹" mixed, a confusing COD fee (+₹80 above ₹999).
- **Keyword-stuffed titles** ("...Ganesha idol hand carved ... vastu gifting available in 532g and 850g variants").

### 2.3 Take for Nazima
- Stone hubs with a **facts table** (mineral, Mohs, origin, treatment, care), a product grid and FAQ. Keep only facts; no healing lines.
- The robots.txt and sitemap pattern exactly.
- Real stock counts, free-shipping threshold, header wholesale link, track-order page, data-deletion page.
- Short, human product names: "Banded Agate Slice, Natural Grey" (v1.0 style).

---

## 3. partner.shubhnumbers.com, deep dive

### 3.1 How the model really works
- **Brand:** ShubhCrystals by Snoowball Media Pvt Ltd (Ghaziabad, incorporated 2025). Products: crystal bracelets, rudraksh, yantra frames.
- **Who it targets:** tarot readers, astrologers, numerologists, vastu consultants, reiki healers, life coaches, pandits, influencers. **Key insight: they recruit people who already have a trusted client list.** Distribution comes from existing trust, not ads.
- **Flow:** partner shares catalogue, sets own price, collects money, sends customer address + base-price payment (UPI/bank) + **screenshot**, supplier checks within hours, then packs and ships white-label (no branding, base price never on parcel, partner's price printed on slip), and shares a packing video.
- **Base price includes packing + shipping.** Partner keeps everything above it.
- **Example:** base ₹850, sell ₹2,499, ₹1,649 profit. Example: 10/week = ~₹65,960/month (labelled illustrative).

### 3.2 What is genuinely best (keep these ideas)
1. **Customer-pays-first, so ₹0 partner risk.** The single strongest hook.
2. **All-inclusive base price** (shipping inside) makes margin maths easy.
3. **White-label fulfilment:** plain box, partner's name, partner's price on slip, supplier never contacts the customer. Partners keep ownership of their client relationship, which is why they join.
4. **"Solo vs Partner" comparison table** (₹50,000–₹5 lakh and 3–6 months alone vs ₹0 with them). Very persuasive.
5. **Ready marketing kit:** Instagram photos, reels, WhatsApp broadcasts, English/Hinglish captions, festival creatives, one-tap copy.
6. **Partner tools:** live profit calculator, stock status, bulk orders, customer CRM, recommendation tool.
7. **Delivery promise by zone** (metro 2–4 days, tier-2 4–6, rural 5–8).
8. **Transparency points:** legal entity, CIN and GST shown; "results not typical" disclaimer.

### 3.3 What is broken (your instinct was right)
| Problem | Evidence |
|---|---|
| **Manual payments** | Partner pays by UPI/bank and sends a screenshot, "checked within a few hours". Slow, error-prone, fraud-prone. |
| **Homepage contradicts terms** | Homepage: "damaged or wrong → free replacement or full refund, no forms". Terms: "**All sales are final**", no returns/refunds/RTO, unboxing video within 24h required. |
| **Dispatch promise contradicts terms** | Homepage: "same-day dispatch before 4 PM". Terms: "packing 2–4 working days". |
| **Certification overclaim** | Hero: "lab certified". Lower down: "certificate on request for costly items". |
| **Fake-looking proof** | The page says "we have **one active partner**" (₹5,000 in 2 weeks), yet shows **three identical testimonials** (Priya, Ankit, Neha) each claiming **₹80,000/month**. |
| **Inflated headline** | "Profits up to 300%". Its own examples are 150% and 194% markup. |
| **Partner carries the risk anyway** | COD RTO costs on partner; refused or wrong-address deliveries not refunded; account suspension "without notice"; **payout cycle undefined**. |
| **No tiers, no referral, no levels** | Same base price whether you sell 1 or 1,000. |
| **Weak onboarding** | One form (name, WhatsApp, email, password, city, Instagram, background). No KYC, no OTP, nothing on what happens next. |
| **No SEO, weak tech** | Client-only SPA, no robots or sitemap. Catalogue is a downloadable PDF, not a live, searchable catalogue. |
| **Undercut rule but no price floor** | Terms forbid "undercutting other partners" but the system sets no minimum price. |

### 3.4 Nazima Partner Programme, done properly
**Who to recruit (fits a grounded brand):**
- Home decor and gifting Instagram pages, interior designers, corporate gifting agents, boutique and gift-shop owners, homemakers and students with WhatsApp circles, Etsy/Amazon/Meesho sellers.
- Spiritual practitioners can join as a channel, but our terms forbid health or outcome claims on Nazima products.

**How it should work:**
1. **Apply:** phone OTP, then PAN (for TDS), bank/UPI verified by penny-drop, then approval in minutes with a clear "what next" screen.
2. **Partner mini-store:** `nazimaagate.com/p/[code]` showing partner's prices, plus per-product share links with UTM and WhatsApp share.
3. **Payment collected by Nazima's gateway, not screenshots.** Customer pays on the partner store or a payment link, and a **split payment** sends the base price to Nazima and the margin to the partner's wallet automatically.
4. **Wallet and payouts:** margin is "pending" until delivery + return window, then "available". **Weekly payout** on a fixed day, statement + TDS shown.
5. **Price guard:** partner price must stay between a floor (stops undercutting) and MRP (stops gouging). The calculator shows margin in ₹ and %.
6. **COD:** prepaid only for the first 10 orders; then COD with a small advance, so the RTO rule is explained upfront.
7. **Tiers** by monthly delivered orders (e.g. Starter / Silver / Gold), giving a lower base price, free samples and priority dispatch. Shown with a progress bar.
8. **Referral, one level only:** a fixed bonus on the referred partner's first X orders. **No multi-level chains.** India's Consumer Protection (Direct Selling) Rules, 2021 restrict pyramid-style schemes; get a lawyer to review the programme.
9. **Same terms everywhere:** homepage, FAQ and terms must say the same thing (dispatch time, damage policy, payout day). Write terms first, then marketing.
10. **Honest proof:** real partner numbers (with permission), "results vary" disclaimer, no copy-pasted testimonials, no "up to 300%".
11. **Marketing kit in v1.0 voice:** "Asli Agate kaise pehchane? 3 tareeke" style reels and carousels, captions in English and Hinglish, festival packs.
12. **Live catalogue, not a PDF:** search, filters, stock status, base price, suggested price, margin.

---

## 4. empireagate.com, deep dive

### 4.1 The AI "Master Gemologist Consultant": how it is actually built
- **Engine:** Google **Gemini**, called from Next.js API routes (`/api/ai/crystal-assistant`, `/api/ai/aura-reading`).
- **Where:** a block **on every product page**: button "Ask Master Gemologist Consultant" (badge "SANCTUARY GUIDE").
- **Request sent:** `{ product, mode, query, userZodiac }`, so **the AI is grounded on the exact product being viewed.**
- **Quick-ask modes (buttons):** Zodiac Match (with "Select your birth zodiac"), Benefits, Chakra, Placement, Care ("Cleansing tips", "Water & Moon care"), plus a free-text box "Ask our Gemologists anything about [product]".
- **Output:** "Gemologist Insight" card with a **copy** button. Error text: "Our AI Crystal Gemologist is taking a deep breath."
- **Separate page `/aura-reading`:** name + zodiac + energy wanted + item format leads to an "energy prescription".

**What's great:** contextual AI *on the product page* (not a separate chatbot), quick-ask chips so users don't need to type, grounding on product data, copyable answer.

**What's weak:**
- No lead capture (no phone or email, no "send me this on WhatsApp").
- The answer doesn't end in "add to cart" or related products.
- Calling an AI a "Master Gemologist" is misleading (implies a qualified human).
- Answers are mystical by design (zodiac, chakra, "energy").
- No safety framing on most pages.

### 4.2 Other things worth taking from Empire Agate
1. **Per-product guide pages** (`/guides/guide-natural-pyrite-pyramid`): a long-form article for each hero product (geology, care, authenticity, FAQ, author + date, link back to product). Strong SEO pattern.
2. **SEO landing pages** for buyer searches: `/agate-crystal-shop`, `/crystal-shop-india`, `/best-crystal-shop-online`.
3. **Origin storytelling:** "Khambhat Lapidary Heritage". They sell the place the stones are cut. Nazima's tagline "Stones from the Source" can own this with real workshop photos and video.
4. **International selling:** geolocation + exchange-rate API for automatic currency, insured worldwide shipping (USA, Canada, UK, Australia). Natural for agate exports.
5. **"Only verified purchasers can review"** rule (good policy; their numbers still don't match).
6. **SKU on product page**, GSTIN and "registered business" in trust badges, a dedicated `/authenticity` page.
7. **Shoppable reels** (`/reels`): video + product card + price.
8. **Retention tech:** web push notifications, WhatsApp API, email API.
9. **Microsoft Clarity** heatmaps and session recordings (free) to see where users get stuck.
10. **Product-specific specs block** (origin Brazil, 45–55 mm, 130–230 g, polished) with a note that each piece varies.
11. **Metaphysical disclaimer on guides** ("mindfulness aids, not medical therapy"). Our version is simpler: don't make the claims.

### 4.3 What is weak
- Rating says "5.00 / 100% five-star" while the same page says "There are no reviews yet". Homepage claims "3,800+ Verified Reviews" but products show "5.0 (1)". Reel view counts are 0–3.
- "Certified Authentic" with **no named lab, test method or sample certificate**. The authenticity page shows only business registration (GSTIN), which proves the company exists, not the stone.
- "Up to 58% off" on almost everything, unverifiable superlatives ("India's largest", "10,000+ products"), 432Hz sound-cleansing claims.
- Same alt text on every image, repeated copy, keyword stuffing, typos.
- Shop by Intention is hidden in the footer; no newsletter, no wholesale.

---

## 5. Nazima Agate: final "best of" blueprint

### 5.1 Stone Guide (our version of the AI Master Gemologist)
- **Name:** "Stone Guide" or "Ask about this stone". Don't call AI a "gemologist" unless a real gemologist reviews answers.
- **Engine:** Claude API from a Next.js route, grounded on product data from Firestore (mineral, Mohs, origin, treatment, size, weight, care, stock).
- **Placement 1, on every product page.** Quick-ask chips:
  - "Is it real? How to check"
  - "How hard / durable is it?"
  - "Care and cleaning"
  - "Where to place it / how to use it" (decor, desk, gifting)
  - "Good as a gift for…?"
  - "Compare with similar stones"
  - free text
- **Placement 2, a standalone `/stone-guide` finder:** use, budget, form, colour, size, then 3–5 in-stock picks with plain reasons.
- **Every answer ends with** related in-stock products + "Add to cart" + "Send this to my WhatsApp" (lead capture with consent).
- **Rules:** facts only, no health, energy or astrology-effect claims. If asked about beliefs, answer neutrally as "traditionally believed", with no promise. Never recommend out-of-stock items. Log questions, since they become future FAQ and guide topics.

### 5.2 Store (best of Stone Mart + Empire Agate, minus their mistakes)
- Stone hubs with facts table + products + FAQ; per-product guides for hero items; buyer-search landing pages.
- Product page: real piece photos and video, exact size and weight, origin, **treatment always stated**, certificate/batch link, Mohs meter, "How to check it's real", care, verified reviews only, SKU, pincode delivery date.
- **Honest numbers only:** a review count that matches the reviews shown, real stock count, real discounts.
- Free-shipping threshold, COD, track order, data-deletion page, robots and sitemap hygiene.
- International: currency auto-detect + export shipping (phase 2).
- Analytics: GA4 + Clarity from day 1.

### 5.3 Partner programme
See 3.4. Core promise: **"Customer pays you first. We pack, ship and pay your margin every week, automatically."**

### 5.4 Trust: our biggest differentiator
None of the three proves anything. Nazima should:
- Show **workshop proof:** cutting and polishing videos, the team, the location ("from the source").
- Use **batch numbers** on labels linking to a batch page (origin, photos, treatment).
- Name the lab for premium pieces; show a sample certificate; state a **"genuine or full refund"** guarantee in the terms (and make the homepage say the same).
- Teach buyers the 3 checks (light, temperature, glass scratch), as in v1.0.

---

## 6. Priority list

| # | Do this | Why | Effort |
|---|---|---|---|
| 1 | Product page with facts table, treatment, batch, real reviews | Biggest trust gap in the market | Medium |
| 2 | Stone Guide on product pages (quick-ask chips, Claude, grounded) | Best idea from Empire Agate, done better | Medium |
| 3 | Partner programme with gateway split payments, wallet, weekly payouts | Best idea from ShubhCrystals, done properly | High |
| 4 | Stone hubs + per-product guides + robots/sitemap | Free SEO traffic (Stone Mart's strength) | Medium |
| 5 | Terms written first; all marketing matches terms | Avoid ShubhCrystals' contradictions | Low |
| 6 | Workshop video and origin story | Own "Stones from the Source" | Low |
| 7 | Clarity + GA4, WhatsApp opt-in, push later | Learn and retain | Low |
| 8 | Multi-currency and export | Agate demand abroad | Phase 2 |

---

## 7. Never copy

- Fake or inflated review counts, copy-pasted testimonials, "up to 300%".
- "Certified" without a named lab or document.
- Healing, energy, zodiac-effect, 432Hz claims.
- Calling an AI a "Master Gemologist".
- Manual screenshot payments.
- Homepage promises that the terms take back.
- PDF-only catalogues and client-only pages that Google can't read.

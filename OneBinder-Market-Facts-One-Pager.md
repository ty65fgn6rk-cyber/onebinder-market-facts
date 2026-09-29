# OneBinder — Market Facts One-Pager
**OneBinder team brief · September 2026 · Working product name: OneBinder**  
*Tagline: All hobbies. One binder.*

---

## The product in one line
OneBinder is an app for hobby / trading-card collectors — sports, Pokémon, and other collectible cards. You photograph / document what you own, track **what you paid**, see a **current market estimate**, and get an **AI look at condition** before you spend money sending a card to a grading company like PSA.

---

## Why the market is real

Hobby cards are not a tiny niche. Millions of people buy, sell, and grade sports cards, Pokémon cards, and other collectible cards every year, and a lot of that activity already happens on phones.

**In plain English:**

1. **The overall category is large and still growing.** Outside research firms put the global trading-card business around **$16 billion** recently, with forecasts pointing toward roughly **$23 billion** by 2030. *(These are commercial estimates, not audited company filings.)*
2. **People already spend serious money on single cards online.** On eBay alone, sales of individual cards (“singles”) were about **$2.6 billion in 2025** — roughly **$1.8B** sports and **$0.8B** Pokémon and other non-sports hobby cards. That is just one marketplace.

3. **Getting cards professionally graded is a huge, growing industry.** Graders examined about **20 million** cards in 2024 and about **27 million** in 2025. PSA (the best-known grader) handled most of that volume. When grading is this big — and often slow or expensive — collectors need help deciding what is worth submitting.
4. **Pokémon cards alone are enormous.** The Pokémon Company reports **75 billion+** cards produced over the life of the brand, including about **10 billion** in one recent fiscal year. Sports cards and Pokémon cards are both mainstream hobbies.

5. **Collectors already use phone apps for hobby cards.** CollX (a scan-and-collect app) has reported **3 million+** users and raised a **$10 million** round in 2025. So “use your phone for your cards” is proven. What is still missing is one app that also tracks **cost**, **value**, and **“should I grade this?”** across hobbies.

| Quick fact | Number | Source |
|------------|--------|--------|
| Global trading / hobby cards (est.) | ~$15.8B (2024) → ~$23.5B by 2030 | Strategic Market Research *(estimate)* |
| Collectible card category worldwide (est.) | ~$7.8B (2024) → ~$11.8B by 2030 | BCC Research / ResearchAndMarkets |
| Sports collectible cards (est.) | ~$5.3B (2024) → ~$10B by 2035 | WiseGuy Reports *(estimate)* |
| eBay individual card sales (2025) | ~$2.62B | GemRate via Yahoo Sports |
| Cards graded industry-wide | ~20M (2024) → ~26.8M (2025) | GemRate / Sports Illustrated |
| PSA share of grading (2025) | ~19.3M cards (~72%) | GemRate / SI |
| Pokémon cards produced | 75B+ lifetime; ~10.2B in FY ending Mar 2025 | The Pokémon Company |
| Example scan-app scale | CollX: 3M+ users; $10M Series A (Mar 2025) | TechCrunch |

**How to read the numbers:** Big “global market size” figures from research firms are **estimates**. The stronger day-to-day proof when we talk this through is eBay singles volume, grading volume, Pokémon production, and the fact that scan apps already have millions of users.

---

## Why now (why build this in 2026)

1. **Grading got harder on the wallet and the calendar.** About **27 million** cards were graded in 2025. PSA has dealt with a very large backlog and has tightened or paused cheaper submission tiers; fees have gone up. Before someone pays to ship a card in, they want a smarter first look at condition and value.
2. **Many collectors hold both sports and Pokémon.** In 2025, grading of Pokémon and other non-sports hobby cards jumped sharply and outpaced sports. Apps that only cover one hobby force people to juggle tools. OneBinder is built for **all hobbies in one binder**.

3. **Buying and selling already happens on phones.** That ~$2.6B in eBay singles is people tapping screens. If your collection lives on your phone, you also need **what you paid** and **what it’s worth now** — not just a pretty photo gallery.
4. **Scan apps exist; the decision layer does not.** CollX and others proved scanning. The open gap is helping someone answer: *What do I own? What did I pay? What’s it worth? Is it worth grading?*

---

## Competitive gap (what nobody fully owns)

| | CollX | Card Ladder | CollectorVault | BinderIQ | **OneBinder** |
|--|:-----:|:-----------:|:--------------:|:--------:|:-------------:|
| Photo inventory | ● | ○ | ● | ● | **●** |
| Sports + Pokémon / hobby cards together | ● | ● | Pokémon-only | ● | **●** |
| Live market / comps | ● | ★ | ● | ● | **●** |
| **Cost basis / profit & loss** | ○ | ○ | ○ | ● | **★** |
| **AI condition / pre-grade** | ○ (chat coach) | — | ● (Pokémon) | — (slab lookup) | **★** |

● = does this · ★ = strongest focus · ○ = weak or not really marketed · — = not offered  

**In short:** Pieces exist. CollX is strong at scan + social selling. Card Ladder is strong at price research. CollectorVault leans Pokémon + condition. BinderIQ tracks inventory and cost. **Nobody clearly owns all four** in one consumer app: every hobby, photo inventory, true cost tracking, and honest AI pre-grade.

**OneBinder’s job:** *What do I own? What did I pay? What’s it worth? Is it worth sending to PSA?*

**Incoming (on the way):** Collectors often win or buy on Fanatics Live or eBay days before the card arrives. OneBinder lets them log source, seller, date, and price in a staging list, then move the card into the permanent binder when it shows up in the mail — cost history already attached.

---

## How we identify cards

There are too many sports, players, characters, sets, and parallels for the app to “Google” a card from scratch every time. OneBinder splits the job in two — and we have a **planned stack** for each half:

| Job | How it works |
|-----|----------------|
| **What is this card?** | **CardSight** — planned for photo card identification (catalog + visual ID): year, set, player or character, card number, parallel / variation. Not by scraping Card Ladder or CollX. |
| **What is it worth?** | **Card Hedge** — planned for licensed sold comps / market pricing. ID says *which* card; Card Hedge says *what sold lately*. |

**Planned stack:** **CardSight** for photo card identification (catalog + visual ID); **Card Hedge** for licensed sold comps / market pricing.

**Stage-one ID UX:** photo → CardSight returns top matches → the collector **confirms**, picks another match, or enters the card manually with pre-filled fields — **not** auto-save. If a rare parallel is missing, they can still save it as **custom / pending ID**.

**Free core eats the CardSight ID cost.** Photo-add + card ID sits in the free product — when a free user snaps a card, we pay for that CardSight call (see *Monthly burn*). That stays consistent with freemium: free users snap cards; we absorb ID.

**Shawn tested CardSight Playground:** works well on base cards; parallels and low-confidence matches need the confirm UI (pick another / edit fields) — which is why stage one is confirm-first, not auto-save.

**What this means for us:** CardSight to *know* the card; Card Hedge to *price* it — not inventing identity from the open web on every scan.

---

## Where “current value” comes from

OneBinder does **not** scrape or peek inside competitor apps (Card Ladder, CollX, Fanatics, and so on). That is fragile, often against their rules, and a weak story for us when we explain how the product works.

**Value comes from market data we license or put together:**

| Signal | What it means | Why it matters |
|--------|---------------|----------------|
| **Sold comps** | What similar cards recently *sold* for (for example eBay completed sales) | Best everyday answer to “what did it actually go for?” |
| **Ask / guide prices** | What people are asking, or published price guides | Helpful context; softer than real sales |
| **Licensed price feeds** | Clean data services sold to apps | The normal, durable way serious apps get numbers |

**“Cross-platform” in product terms:** one estimate *inside OneBinder* that can later blend more than one marketplace — not secretly reading Card Ladder’s screen.

**First build (v0.1):** one solid data source; every number labeled an **estimate**; show the **date** it was refreshed. Add more sources later. Sports and Pokémon may start on different feeds.

---


## Price data vendors to contact

OneBinder will **not** scrape eBay or competitor apps in a browser (captchas, blocks, a weak story for the product). Value comes from a **licensed feed from a data company**. These are starting points to apply or email for **commercial / in-app** rights — not a finished contract.

**Outreach status (Sep 25, 2026):** We contacted **Card Hedge** (commercial price API). Brief ask: multi-category collector app (working name TBD); need licensed sold-comps / estimates we can show to end users; rough early volume and private-test timeline; confirm category coverage, comps detail, refresh cadence, and written display rights. They confirmed receipt and said they would reply within 24 hours. No terms or pricing back yet.

| Vendor | Best for | Link | Notes |
|--------|----------|------|-------|
| **Card Hedge** | Sports + TCG + non-sport comps / FMV API (broad categories) | https://ai.cardhedger.com/api-services | **Contacted Sep 25, 2026** — waiting on reply. Strongest public “sells an API for apps” fit so far; still need written rights to show numbers to our users. |
| **PriceCharting** | Pokémon + other collectibles guide prices; paid API | https://www.pricecharting.com/api-documentation · https://www.pricecharting.com/pricecharting-pro?f=api | Default API is often **internal** use; putting prices in a consumer app needs their **commercial license** — ask explicitly. |
| **SportsCardsPro** | Sports card guide prices (same family as PriceCharting) | https://www.sportscardspro.com/api-documentation | Same ask: commercial / in-app rights for OneBinder. |
| **eBay Developer Program** | True **sold comps** (what actually sold) | https://developer.ebay.com/ | Sold-history style access (e.g. Marketplace Insights) is **limited / needs eBay approval**, not open signup. Browse API alone is mostly active listings — weaker than sold comps. |
| **TCGplayer API** | Pokémon / TCG marketplace prices | https://docs.tcgplayer.com/docs/getting-started · https://help.tcgplayer.com/hc/en-us/articles/360061115874-TCGplayer-API-Terms-Conditions | Docs currently say **new API access is not being granted**. Still relevant if we already have access through a contact. |
| **Pokémon TCG API options** | Catalog + market-style Pokémon numbers | https://docs.pokemontcg.io/ · https://pokemontcgapi.com/ | Useful for Pokémon; read commercial terms before wiring into the app. |

**Avoid calling “licensed”:** third-party wrappers that scrape eBay sold search behind a quick API key. They can look like an API but often recreate the same legal and block risk as a bot clearing eBay security checks.

**How we explain it:** “We identify the card with CardSight, then we pay Card Hedge for estimates through their API — like a stock app getting prices from a data company, not by scraping a website with a robot.”

**v0.1:** pick **one** solid source; label every number an **estimate** with an **as-of date**. Sports and Pokémon may use different vendors.

---
## Freemium rule (locked)

**Parent question we must pass:** “Does it cost money?” → **No — you can build and share your whole binder for free.**

Young collectors will ask parents. Entry must be near-zero friction — fun and easy for kids, not a parent chore, and it should match modern app intuition. Kids should feel they **have** to upload their whole book. The free product is the *hobby* (owning and showing the digital binder). Paid is *horsepower* for serious users — never a nicer binder.

| | Free (the cool core) | Paid / Pro (optional) |
|--|----------------------|------------------------|
| Snap cards into the binder (photo ID / add) | Yes — free; does **not** burn pre-grade tokens | Same |
| Collection, binders, Incoming (on the way) | Yes | Same |
| Track what you paid + basic market estimate (incl. collection total) | Yes · watchlist too | Deeper comps, grade-worthy picks, value history |
| Share a card or binder with friends | Yes — core loop | Same |
| AI pre-grade (“worth sending to PSA?”) | Small monthly allowance | Higher or unlimited |
| Exports / power tools | Light or later | CSV, richer reports |

**Design rule (locked):** Freemium must stay awesome — **goal is users**. Free = cool core (binder, photo ID, cost, basic value incl. collection total, share / friends / watchlist). Paid = horsepower only (AI pre-grade, deeper comps, grade-worthy picks, value history — $9.99/mo placeholder) — **never** a better binder. Free must feel cooler than Pro — so kids want to snap the whole binder, not wait for a parent to “set it up.” Retention comes from the free loop: pull → add (**Just Landed**) → binder grows → show a friend — same rhythm as owning the physical cards.

---

## Today’s product locks
*Sep 29, 2026 · short version for Shawn — no coding speak*

- **After you confirm a scan:** Add to collection · Add to watchlist · Just ID. Under **No**: Manual enter, or scan again.
- **Free:** binder + photo ID + cost + basic market value (including collection total) + share / friends / watchlist.
- **Pro:** AI pre-grade, deeper comps, grade-worthy picks, value history — **$9.99/mo** (placeholder).
- **Smart groups:** My rookies under NFL / MLB / NBA; My chase rares under Pokémon; **My slabs** under every hobby (NFL / MLB / NBA / Pokémon) next to those tiles — grade, cert #, grader (PSA / CGC / etc.), shareable slice. Not on the main Collection screen.
- **Friends:** Trade / want match.
- **Binder value moves:** notifications like “your binder is up/down $X this week” — why they return. Free retention hook.
- **Just Landed:** celebrate the scan→collection moment (no extra camera; no arrival push). Pairs with binder value moves.
- **Finish the set:** tabled for later.
- **Parked for later (not stage one):** friend-landed signals; “new this week” on rookies / chase / slabs tiles; optional pull-session streak.
- **Demo:** https://highlighted-prescription-institutes-flat.trycloudflare.com/

---

## Social safety lock
*For parents · friends & trade — safe by design*


- **No public lookup.** You only add people you already know — username shared in person, text, Discord, shop, or school. No directory / no “find collectors near me.”
- **Mutual accept; kids parent-owned.** Friend requests need both sides. Kids: parent-owned account + parent approves friends.
- **No in-app DMs or open chat.** Share binder/card links only.
- **Trade = quiet match signal.** Friends see “Alex wants X” — real swaps happen off-app (text, shop, in person). No marketplace, money, or ownership transfer in the app.

---

## Prototype status
- Tap-through mobile web prototype: **OneBinder** (light “cosmic chrome” look)
- Phone demo link: https://highlighted-prescription-institutes-flat.trycloudflare.com/ *(browser title: One Binder; live CardSight ID via proxy; Cloudflare tunnel + ship.page backup)*
- Walkthrough: Collection → **NFL / MLB / NBA** → **My rookies** + **My slabs**; **Pokémon** → **My chase rares** + **My slabs** (grade · cert # · grader · share); Scan → confirm → **Add to collection** → **Just Landed** (quiet vs heat) → collection; Collection banner / Settings / card Market tease → **One Binder Pro**; Friends → **Trade / want match**; Collection → **binder value move** banner. *(Finish the set tabled. Friend-landed / new-this-week / pull streak parked.)*
- Demo prices are sample data until a real price feed is connected

---

## What we need after the prototype
Once the clickable prototype is solid, our next job is turning it into a **real phone app** people can install (iOS first, then Android): native build, camera + local vault, one licensed market-data feed, and honest AI pre-grade — while we keep product vision and the collector problem.

---

## What it costs to run (excluding the app build)

These figures are **operating and launch costs only** — Apple fees, hosting, data feeds, AI usage, entity/legal basics. They do **not** include paying someone to build the app.

**In plain English:** early private testing on phones can stay cheap. A lean first public year is usually in the low five figures for known costs. The big unknown is **permission to show licensed sports market prices and checklists** inside the app.

| Stage | Ballpark (USD) | What’s in it |
|-------|----------------|--------------|
| **Private iOS test build** (friends / family via TestFlight; Pokémon-first price feed; metered AI pre-grades) | About **$150–400** to start, then **~$30–80 / month** | Apple Developer ($99/yr), domain, light hosting, Pokémon catalog/price SaaS (e.g. Scrydex ~$29+/mo), cheap AI for Pro pre-grades |
| **Lean public App Store year** (~5,000 monthly users; known public costs) | About **$4,000–$12,000 / year** | Apple + Florida LLC + domain + trademark filing + privacy work, hosting, Pokémon data SaaS, AI, email/crash tools. Closer to **$6k–$16k** with stronger privacy counsel and optional insurance |
| **Sports commercial data licenses** | **Quote required** | PriceCharting / SportsCardsPro ~$49/mo “API” plans are for **internal** use; putting prices in a consumer app needs **written commercial permission**. Beckett-style checklists, eBay Insights, and TCGplayer API access are mostly ask-for-a-quote. This line can jump past everything else if priced like enterprise software |

**Other fixed / yearly items we should know:**
- Apple Developer: **$99 / year**. Google Play (later): **$25 once**.
- Florida LLC: about **$125** to file + **$138.75 / year** annual report.
- USPTO trademark: **$350** base per class (plus optional attorney help).
- Privacy templates are cheap; because kids/parents use the free binder, budget real privacy / COPPA advice (~**$1,000–$5,000**) before a kids-facing public launch.
- Photo storage/bandwidth scales with users (roughly tens of dollars/month early; hundreds to low thousands at much larger scale). AI pre-grades stay cheap on a fast model (pennies per check). Free “add to binder” photo matching should use cheap embeddings — not the expensive vision model.
- Apple takes **15%** (Small Business Program) or **30%** of in-app subscription revenue — a cut of sales, not a fixed bill.

**What this means for us:** build cost is separate. Running costs are manageable if we start **Pokémon-first** with transparent SaaS data. **Sports live market values on the App Store wait for signed commercial licenses** — email vendors in the table above before promising that.

---

## Monthly burn at user milestones

Ballpark **software / data** burn as users grow — CardSight for photo ID, Card Hedge for comps, plus light hosting / AI. This is **not** app build, marketing, or salaries.

**Free-core ID is a real cost we absorb — on purpose.** Photo-add + card ID sits in the free product because freemium must stay awesome and **users are the goal**. When a free user snaps a card, we pay for that CardSight call. That spend is **cost of the free core / cost of acquisition** — it scales with free adds, not with paid subscribers. More free users means more ID cost we eat; paid horsepower (AI pre-grade, deeper comps) — never a better binder — should recover that over time.

**Assumptions we are using:**
- **CardSight ID:** Free 750 calls/mo (no card), Pro $14.95 / 5k, Premium $74.95 / 30k, Ultra $199.95 / 100k; overage roughly **$0.002–$0.003 per call**. About **1–2 ID calls per card added**. Rule of thumb: early on we sit on a flat tier; at serious volume CardSight is a **variable cost per free card-add** that grows with free volume.
- **Card Hedge comps:** ~$500 / mo one category, ~$1,000 / mo all categories (Sep 26 reply). Values refresh **daily** (not per-user).
- **Hosting / storage / AI pre-grade** (metered) stays a small add-on early — not the driver of monthly burn.

| Milestone | Ballpark monthly burn | What’s driving it |
|-----------|----------------------|-------------------|
| **Private TestFlight** (~50–100 users) | ≈ **$500–$600 / mo** | CardSight Free ($0) + Card Hedge one-category ($500). *Free-tier ID cost:* essentially $0 this month — we are still inside the free 750-call allowance, so almost all of this burn is comps, not ID. |
| **Early public** (~1,000 MAU) | ≈ **$515–$550 / mo** | CardSight Pro ($14.95) + Card Hedge one-category ($500). *Free-tier ID cost:* ~$15 of the month — the Pro tier we step into so free photo-adds keep working. Still tiny vs comps. |
| **Growing** (~5,000 MAU) | ≈ **$1,075–$1,100 / mo** | CardSight Premium ($74.95) + Card Hedge all-categories ($1,000). *Free-tier ID cost:* ~$75 of the month — ID we eat for free adds. The big jump here is comps (one hobby → all categories), not ID. |
| **Scaling** (~25,000 MAU) | ≈ **$1,200–$1,250 / mo** + hosting / AI ~$50–$150 | CardSight Ultra ($199.95) + Card Hedge all ($1,000). *Free-tier ID cost:* ~$200 of the month — still the smaller slice; comps remain the main fixed line. |
| **Larger** (~100,000 MAU) | ≈ **$1,500–$2,000+ / mo** | Ultra + overage (a few hundred) + Card Hedge $1,000 + hosting / AI ~$200–$500. *Free-tier ID cost:* a few hundred of the month (tier + overage at ~$0.002–$0.003/call) — ID finally becomes a meaningful variable line as free volume scales. |

**What this means for us:** early on the comps feed (Card Hedge) is the main monthly cost. ID stays cheap until serious volume — but every free card-add is still a real call we pay for. The big step-change is one-hobby comps pricing → all categories (~$500 → ~$1,000). Freemium implication: growing free users (the goal) grows ID burn we absorb so the cool core stays free; paid horsepower (AI / deeper comps) should recover that — never by making a better binder.

*Planning estimates only. Final Card Hedge numbers depend on a signed agreement.*


---


## Free CardSight ID vs paid upgrade break-even

*Planning estimates only* — rough math for freemium pricing, not a P&L forecast. **Goal is users.** Freemium must stay awesome: free is the cool core; paid is horsepower only.

**Per free card-add:** about **1–2 CardSight calls** at ~$0.002–$0.003/call → we absorb roughly **~$0.002–$0.006 per free card** we add. That ID cost sits in free on purpose so photo-add stays part of the cool core.

**Per-user examples (ID cost we eat):**
- Light user (~5 cards): ~**$0.01–$0.03**
- Typical (~20 cards): ~**$0.04–$0.12**
- Heavy (~100 cards): ~**$0.20–$0.60**

**Example — 1,000 free users / 20 cards each:** ~20,000 free adds → about **$40–$120 / month** in CardSight ID. Real cost, but still small next to **Card Hedge** (~$500–$1,000 / mo fixed). **Card Hedge is the bigger fixed cost**; free ID is a cheap variable line — cheap enough that we can keep the free binder awesome without gating snaps.

**Break-even rough % at $9.99 / mo after Apple:** net to us ≈ **$8.49** (15% Small Business) or ≈ **$6.99** (30%). Covering just that $40–$120 ID line at 1k free users needs roughly **~5–17 paid** → about **~0.5%–1.7%** conversion. Covering Card Hedge too needs a higher convert rate — again, comps dominate the math, not ID.

**What this means for us:** freemium lock-in — **users first**. Free stays the cool core (binder, photo ID, cost tracking, basic value, share) — fun enough that kids feel they must upload the whole book, not a parent chore. Paid is **horsepower only** (AI pre-grade, deeper comps) — **never** a better binder. Keep ID free; meter AI / deeper comps. **Test $9.99 / mo first**; we can move the price once we see real convert and ID volume.

*Planning estimates only.*

---

## Source shortlist
1. GemRate / Sports Illustrated — grading volumes 2024–2025  
2. GemRate / Yahoo Sports — eBay singles ~$2.62B (2025)  
3. BCC Research — collectible / trading-card market research  
4. TechCrunch — CollX funding / user scale (Mar 2025)  
5. Baseball America / hobby press — PSA backlog and cheaper-tier pauses  
6. The Pokémon Company — 75B+ cards produced  
7. Competitor sites / App Store listings: CollX, CollectorVault, Card Ladder, BinderIQ  

*Market-size figures from commercial research houses are estimates — keep that label on any leave-behind.*

## Known unknowns

Things we already know we still have to nail down. None of these kill the idea — they just need answers before we promise them in public.

**Sports market data in the app.** Pokémon/TCG has clearer published SaaS options. Showing licensed sports sold comps and checklists inside a consumer app usually needs written commercial permission, and those fees are often quote-only. Until that paper exists, we should treat full sports “live market value” as unconfirmed.

**How complete the card catalog is on day one.** Photo and search only feel smart if they hit the cards people actually own. We need a first coverage set (for example modern sports rookies plus major Pokémon sets) and a clean way to handle custom / pending IDs so the binder doesn’t fill with bad matches.

**Kids, parents, and privacy.** A free binder for young collectors means age gates, parental consent, and careful rules for photos and shared links. Templates are not enough for a kids-facing public launch — we need a real privacy pass first.

**What the AI pre-grade is allowed to say.** It is an estimate of condition, not a PSA grade and not a guarantee of sale price. Same for market values: always an estimate with an as-of date. Exact in-app wording and limits still need locking.

**Keeping the free core cheap at scale.** Snap-and-add and photo storage have to stay affordable if free is the cool heart of the product. Pre-grades stay metered; free photo ID should not burn expensive AI. Compression, thumbnails, and cheap matching are product rules, not optional polish.

**Brand and name.** “OneBinder” needs a trademark and App Store name check (and later domain / social handles) so we do not build on a name we cannot keep.

**Where the first users come from after private testing.** Card shows, local hobby shops, youth sports, Instagram — we need one clear sentence and a first channel once an installable test build is solid. Distribution can wait on the private test, but it should not stay blank forever.

**Android timing.** iOS first is the plan. When Android joins is still open and should not distract the first installable build.

**What “good enough to continue” means.** We should set plain gates, for example: private test on real cards for a couple of weeks without rage-quitting; one licensed price feed live with honest labels; a small set of outside collectors who would strongly recommend it. Without gates, the idea stays a forever conversation.

---

*OneBinder · Confidential team draft · Not investment advice · Figures as of research date Sep 25, 2026 · Cost ranges exclude app build*

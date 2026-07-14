# App Research — Opportunity Comparison

**Market:** iOS US
**Evidence refreshed:** 2026-07-13
**Admission rule:** Include only opportunities with already-demonstrated demand supported by current keyword, ranking, traction, and payment evidence. Exclude weak-demand or unvalidated ideas before creating this brief.

## 1. Comparison at a Glance

QR has the strongest combined open-entry, offline execution, and independently testable-wedge evidence. Garden combines strong revenue and open entry with dataset effort; Reading combines high demand and bounded implementation with competitive entry; Mineral has the strongest revenue ceiling and open entry, alongside online accuracy and trust risk.

| Rank | Opportunity | Demand / entry | Strongest traction proof | Revenue proof | Build risk | Evidence-backed product wedge |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Scan-Verified Offline QR Maker | High / Open | 10/10 relevant; [QR Template](https://apps.apple.com/us/app/id1574018167) #1, 17,243 ratings; 2024 entrant #8, 963 | Displayed $40-$50k/mo; qualifying $50k/mo iOS US [Sensor Tower](https://app.sensortower.com/overview/1574018167?country=US) | Low | [Local pre-export verification](https://apps.apple.com/us/app/id1574018167) and static offline files via one-time unlock; leaders already style, generate, and scan, and the scan complaint is Contact-specific. |
| 2 | Sixty-Second Raised-Bed Planner | Medium / Open | 7/10 direct; GrowIt 13,391 ratings; Seedtime #5, 420; low-rating entrant #9 | $30k-$100k/mo; both iOS US [Sensor Tower](https://app.sensortower.com/overview/1542642210?country=US) anchors | Medium | [Editable spacing and a fast saved bed](https://apps.apple.com/us/app/id1542642210); Planter already provides a grid, so the workflow distinction is materially faster setup. |
| 3 | One-Tap Physical Book Log | High / Competitive | 10/10 relevant and all 100+; Bookly #1, 59,747; Margins #7, 17,448 | Displayed $300-$60k/mo; qualifying Bookly $50k/mo iOS US [Sensor Tower](https://app.sensortower.com/overview/1085047737?country=US); other ranges modeled context | Low | [Page/percentage updates without a timer and a local recap](https://apps.apple.com/us/app/id6737528718); Bookly already includes page tracking, a timer, and broad reports. |
| 4 | Evidence-First Mineral Identifier | Medium / Open | 10/10 direct; leader #1, 74,633; five top-10 apps have <=8 ratings | $10k-$400k/mo [Sensor Tower](https://app.sensortower.com/overview/1546796934?country=US): $10k/$20k worldwide and $400k iOS US | Medium | [Top three, confidence, observable traits, and inconclusive results](https://apps.apple.com/us/app/id1546796934); the leader already provides broad geological detail and collection features. |

- This artifact compares qualified opportunities; it carries no product decision or execution status. Rank reflects relative evidence strength.
- Each wedge is a distinct experience grounded in supporting evidence and counter-evidence.
- Revenue values are third-party estimates. Scope, platform, date, source, and confidence are stated in the appendix; weaker modeled details are supporting context only.

## 2. Ranked Evidence Profiles

### #1 Scan-Verified Offline QR Maker

**One-line product:** Create a styled static QR, verify it locally before export, and receive a dependable PNG or SVG.

**Customer:** Small-business owners creating branded marketing or team contact materials who need QR codes that scan reliably; they currently use template generators and manually test outputs with an iPhone. Occasional use is paired with hosted-code expiry, fees as high as $9.99/week, lifetime/VIP purchases not activating, and recurring subscription pain.

**Evidence supporting the wedge**
- **Demand receipt:** `qr code generator` is 49 popularity / 55 difficulty; all 10 top-10 results are relevant, eight have 100+ ratings, a focused app with 5 ratings ranks #3, and a focused 2024 entrant has 963 ratings at #8.
- **Payment receipt:** Displayed estimates span $40-$50k/month. QR Template's $50k/month iOS US Sensor Tower estimate is the qualifying anchor; QR Maker's $40-$300/month AppCurrents estimate is low-confidence modeled context.
- **Entry receipt:** Demand High / Entry Open. The exact phrase is crowded in app names, while focused low-rating and recent entrants retain top-10 positions.
- **Review-backed wedge:** QR Template reviewer ChaadThomas reported Contact QRs scan as "no usable data" on 2023-02-02 ([QR Template](https://apps.apple.com/us/app/id1574018167)); QR Maker reviewer CodCritiqs objected to "10$ a week" on 2025-08-15 ([QR Maker](https://apps.apple.com/us/app/id6480221387)).
- **Why bounded:** Execution fit Strong / Offline core. Core Image covers generation, local storage is bounded, operating cost can be zero, and reliability can be tested against independent scanners.
- **Builder-profile context:** Adjacent; the enter -> transform -> export loop matches the profile and can remain entirely offline.

**Risks and counter-evidence**
- Static QR generation is commoditized, and established apps already generate, style, and scan codes.
- The scan-failure evidence is high-signal but Contact-specific; broader reliability is not established by that review alone.
- Reliability testing must avoid scope drift into hosted dynamic-QR infrastructure.

**MVP boundary**
- Four static payload types with light styling.
- Local pre-export verification against the generated payload.
- PNG/SVG sharing and local history.
- Exclude hosted dynamic codes, accounts, broad template libraries, and recurring infrastructure.

**Business model:** Free basic creation with a one-time professional export/template unlock; static QR creation is occasional, making recurring subscription pricing a poor fit.

**Key execution unknown:** Whether styled outputs verify reliably across Apple Camera and independent scanners, beyond the Contact-specific failure report.

**Confidence:** High on demand, revenue, entry, and implementation; Medium on paid conversion. The top rank reflects the combined open-entry, offline, zero-operating-cost, and independently testable reliability evidence.

### #2 Sixty-Second Raised-Bed Planner

**One-line product:** Enter bed dimensions and crops, adjust spacing, and save a clear raised-bed layout in about a minute.

**Customer:** Novice vegetable gardeners laying out one raised bed who need correct spacing and a record of what goes where; they currently use signs or stakes, paper tracking, or spacing-grid apps such as [Planter](https://apps.apple.com/us/app/id1542642210) and [GrowIt](https://apps.apple.com/us/app/id6443580320). Preset spacing, repeated entry, broad-planner friction, and subscriptions gating basic layouts waste small-bed space.

**Evidence supporting the wedge**
- **Demand receipt:** `garden planner` is 31 popularity / 54 difficulty; seven top-10 results are directly focused on planning and five have 100+ ratings. GrowIt has 13,391 ratings, while 2024 entrant Seedtime has 420 ratings at #5.
- **Payment receipt:** Displayed estimates span $30k-$100k/month. Planter's $30k/month and GrowIt's $100k/month iOS US Sensor Tower estimates are both qualifying anchors.
- **Entry receipt:** Demand Medium / Entry Open. Low-rating recent entrant easyDacha ranks #9; the phrase appears in several names, favoring metadata use with a distinctive product title.
- **Review-backed wedge:** Planter reviewer RachelReviewss wrote "The spacing is pre-set" and difficult for smaller spaces on 2022-09-21; reviewer ExecPastryChef called paper tracking "Super frustrating" on 2023-03-25 ([Planter](https://apps.apple.com/us/app/id1542642210)). Spacing and tracking complaints recur in broader research.
- **Why bounded:** Execution fit Medium / Offline core. UI and storage are bounded and backend cost can be zero; editable spacing limits dependence on authoritative defaults.
- **Builder-profile context:** Aligned; it serves hobbyists through a visual organize-and-plan loop with an offline-capable core.

**Risks and counter-evidence**
- Existing leaders already provide grids, calendars, and plant information.
- A trustworthy licensed crop-spacing dataset remains an effort and provenance unknown.
- The no-account flow must be materially faster than Planter's existing grid, not merely visually different.

**MVP boundary**
- One resizable raised bed.
- A compact crop catalog with editable spacing.
- Local saved layouts with a fast repeat workflow.
- Exclude authoritative companion-plant claims, broad calendars, social features, and multi-garden management.

**Business model:** Free single-bed plan with a one-time multi-bed, print, and export unlock; a seasonal layout job does not inherently require a subscription.

**Key execution unknown:** Whether a trustworthy licensed crop-spacing dataset is available at acceptable effort; user-editable spacing reduces but does not remove this concern.

**Confidence:** High on demand, revenue, and entry evidence; Medium on dataset effort and paid conversion.

**Ranking tradeoff:** Strong qualifying revenue and open-entry evidence are offset by lower keyword demand and unresolved dataset effort relative to #1.

### #3 One-Tap Physical Book Log

**One-line product:** Log page or percentage progress without a timer, then retain a private local completion recap.

**Customer:** Occasional physical-book readers who want a fast record of progress, completion, and one takeaway; they currently use [Bookly](https://apps.apple.com/us/app/id1085047737) or manual notes and timers. They face timer-first workflows, $30/year and limited-free-library subscription friction, social features, and book-entry friction; [Margins](https://apps.apple.com/us/app/id6737528718)' manual-add issue was partly fixed in March 2026, while [Reading Journey](https://apps.apple.com/us/app/id6749302195)'s launch/server issue is a high-signal single report.

**Evidence supporting the wedge**
- **Demand receipt:** `reading tracker` is 52 popularity / 65 difficulty and `book tracker` is 61/65. All top-10 results are relevant and all have 100+ ratings; Bookly has 59,747 ratings at #1 and 2024 entrant Margins has 17,448 at #7.
- **Payment receipt:** Displayed estimates span $300-$60k/month. Bookly's $50k/month iOS US Sensor Tower estimate is the qualifying anchor; Margins' $11k-$60k/month and Reading Journey's $300-$2k/month AppCurrents ranges are modeled context.
- **Entry receipt:** Demand High / Entry Competitive. Margins reached substantial traction, and 2025 entrant Reading Journey ranks #8 with 168 ratings, but every top-10 result has established traction and exact-title collision is high.
- **Review-backed wedge:** Margins reviewer Bugtucker26 wished to update progress "by pages I read rather than the time" in March 2025 ([Margins](https://apps.apple.com/us/app/id6737528718)); [Bookly's listing](https://apps.apple.com/us/app/id1085047737) confirms timer-centered functionality.
- **Why bounded:** Execution fit Strong / Optional online services. Metadata lookup can be cached, manual entry preserves the core when lookup fails, and only user-entered reading text is stored.
- **Builder-profile context:** Aligned; it is a private capture-and-reflect loop with an offline-capable core.

**Risks and counter-evidence**
- The category is crowded, with all top-10 apps above 100 ratings.
- Metadata lookup introduces a limited online and fallback requirement.
- Bookly already supports page tracking alongside its timer, goals, and broad reports, so the distinction depends on lower friction rather than missing functionality.

**MVP boundary**
- Local book library with manual entry and optional cached metadata lookup.
- Page or percentage progress and completion history without a required timer.
- One local takeaway and recap export.
- Exclude social features, reading sessions, broad reports, challenges, and server-dependent core storage.

**Business model:** Free basic logging with a one-time unlock for unlimited history, exports, and custom recap cards.

**Key execution unknown:** Whether a ten-second no-social workflow creates enough differentiation and paid conversion in a competitive top 10.

**Confidence:** High on demand and payment; Medium on differentiation in a competitive top 10.

**Ranking tradeoff:** Higher measured demand and bounded implementation are balanced by materially more competitive entry and incumbent feature overlap than #1 and #2.

### #4 Evidence-First Mineral Identifier

**One-line product:** Photograph a field find and receive three likely IDs, confidence, observable traits, or an explicit inconclusive result.

**Customer:** Beginner rockhounds cataloging field finds who want credible likely identifications and observable traits to check; they currently ask knowledgeable relatives or trust photo-identifier apps for likely matches and cataloging. Inconsistent single-answer IDs that change with angle or lighting make paid results hard to trust.

**Evidence supporting the wedge**
- **Demand receipt:** `mineral identifier` is 27 popularity / 37 difficulty, `rock identifier` is 53/45, and `rock and mineral identifier` is 23/41. All top-10 results are directly relevant and five have 100+ ratings.
- **Payment receipt:** Displayed estimates span $10k-$400k/month. All three are qualifying Sensor Tower commercial estimates: Rock ID $10k/month and RockIn $20k/month worldwide; Rock Identifier $400k/month iOS US.
- **Entry receipt:** Demand Medium / Entry Open. Five apps with 8 or fewer ratings rank #3, #5, #6, #8, and #10 despite a leader with 74,633 ratings.
- **Review-backed wedge:** Rock Identifier reviewer specialappssk reported results change with "a slightly different angle or lighting" in July 2024 ([Rock Identifier](https://apps.apple.com/us/app/id1546796934)); RockIn reviewer Neiltfox2 said it "got one out of ten right" in February 2025 ([RockIn](https://apps.apple.com/us/app/id6754837588)). Wrong-ID and uncertainty themes recur across these apps and [Rock ID](https://apps.apple.com/us/app/id6469999508).
- **Why bounded:** Execution fit Medium / Online required. Scope centers on one vision-model/API integration, a curated reference, capped free scans, cached results, and an explicit inconclusive state.
- **Builder-profile context:** Aligned; photo -> identify -> save is a reusable hobby-collector loop.

**Risks and counter-evidence**
- Image-only mineral identification can be unreliable, creating direct accuracy and user-trust risk.
- A vision API and curated mineral reference add online cost, data quality, and technical uncertainty.
- The category leader already provides broad geological detail and collection features; trust presentation alone does not establish useful identification accuracy.

**MVP boundary**
- Guided camera and capped online identifications.
- Ranked top-three results with confidence, observable traits, and an inconclusive state.
- Cached result history and a local collection.
- Exclude buying/selling, folklore, broad geological tools, and uncapped scans.

**Business model:** Limited free identifications with annual or lifetime access after accuracy is demonstrated.

**Key execution unknown:** Whether a small labeled accuracy prototype can demonstrate useful top-three performance while reliably returning inconclusive for low-confidence inputs.

**Confidence:** High on demand, entry, and payment; Medium on achievable trustworthiness.

**Ranking tradeoff:** The highest revenue ceiling and clear open-entry evidence are offset by the only online-required core and the largest unresolved accuracy and trust test.

---

# Evidence Appendix

## A. Research Inputs and Limits

- **Platform / market:** iOS US.
- **Discovery date:** 2026-07-11; competitor and ranking refresh: 2026-07-13.
- **Coverage:** 24 candidates across profile-aligned, adjacent utility, and independent categories; competitor-derived phrases were tracked and live-searched.
- **Astro workspaces:** Temporary app `106`, `Mixed Tiny Bets Coverage 2026-07-11`, for discovery; temporary app `107`, `Mixed Tiny Bets Table Refresh 2026-07-13`, for refresh.
- **Sources:** Astro, US App Store listings and reviews, Sensor Tower, and AppCurrents.
- **Revenue limits:** Third-party estimates are not actual developer revenue. AppCurrents ranges are modeled from public App Store ranking, rating velocity, and monetization signals, typically +/-25-50%, and are nonqualifying without required corroboration.
- **Evidence limits:** Revenue scope may differ by market or platform. App Store review URLs may open the listing without anchoring the individual review. Missing keyword metrics are shown as `N/A`.

## B. Scan-Verified Offline QR Maker Evidence

**Market:** iOS US. Top 10: 10/10 relevant, eight with 100+ ratings, plus a 5-rating app at #3 and a 2024 entrant at #8 with 963 ratings. Demand High; Entry Open; Payment Strong. Confidence High on demand, revenue, entry, and implementation; Medium on paid conversion.

| Keyword | Role | Popularity | Difficulty | Note |
| --- | --- | --- | --- | --- |
| `qr code generator` | Primary | 49 | 55 | Clear generation/export intent; independent seed; refreshed 2026-07-13. |
| `free qr code generator maker` | Adjacent | 21 | 52 | Competitor-derived phrase. |
| `code generator` | Adjacent | 38 | N/A | Competitor-derived; broad intent. |
| `qr maker` | Adjacent | 15 | N/A | Below pass. |
| `barcode generator` | Adjacent | 9 | N/A | Below pass. |

| Competitor | Market traction | Revenue evidence | Evidence implication |
| --- | --- | --- | --- |
| [QR Code Generator, QR Template](https://apps.apple.com/us/app/id1574018167) | `qr code generator` #1; 17,243 ratings; 4.8 | $50k revenue estimate; last month; iOS US; [Sensor Tower](https://app.sensortower.com/overview/1574018167?country=US); commercial estimate; captured 2026-07-11; High confidence | Broad template and styling leader leaves a narrower verification scope. |
| [QR Code Generator & Maker app](https://apps.apple.com/us/app/id6480221387) | `qr code generator` #8; 963 ratings; 4.8 | $40-$300/month estimate; iOS App Store; [AppCurrents](https://appcurrents.com/apps/qr-code-generator-maker-app-ios-6480221387); public modeled estimate; updated/captured 2026-07-13; Low confidence | Focused 2024 entrant with meaningful traction; modeled range does not qualify the opportunity alone. |

## C. Sixty-Second Raised-Bed Planner Evidence

**Market:** iOS US. Top 10: 7/10 directly focused on planning, five with 100+ ratings; Seedtime has 420 ratings at #5 and low-rating recent entrant easyDacha ranks #9. Demand Medium; Entry Open; Payment Strong. Confidence High on demand, revenue, and entry; Medium on dataset effort and paid conversion.

| Keyword | Role | Popularity | Difficulty | Note |
| --- | --- | --- | --- | --- |
| `garden planner` | Primary | 31 | 54 | Clear planning intent; independent seed confirmed in competitor extraction; refreshed 2026-07-13. |
| `layout` | Adjacent | 59 | N/A | Competitor-derived; broad intent. |
| `gardening` | Adjacent | 28 | N/A | Broad intent. |
| `vegetable garden planner` | Adjacent | N/A | N/A | Metric unavailable. |
| `planting calendar` | Adjacent | N/A | N/A | Metric unavailable. |

| Competitor | Market traction | Revenue evidence | Evidence implication |
| --- | --- | --- | --- |
| [Planter: Garden Planner](https://apps.apple.com/us/app/id1542642210) | `garden planner` #1; 2,326 ratings; 4.7 | $30k revenue estimate; last month; iOS US; [Sensor Tower](https://app.sensortower.com/overview/1542642210?country=US); commercial estimate; captured 2026-07-11; High confidence | Closest layout competitor; broad calendar and plant-information scope leaves room for instant layout. |
| [GrowIt: Garden Planner](https://apps.apple.com/us/app/id6443580320) | `garden planner` #2; 13,391 ratings; 4.7 | $100k revenue estimate; last month; iOS US; [Sensor Tower](https://app.sensortower.com/overview/6443580320?country=US); commercial estimate; captured 2026-07-11; High confidence | Broad all-in-one guide extends beyond the narrow layout job. |

## D. One-Tap Physical Book Log Evidence

**Market:** iOS US. Top 10: 10/10 relevant and all have 100+ ratings; Bookly is #1 with 59,747 ratings, Margins is #7 with 17,448, and 2025 entrant Reading Journey is #8 with 168. Demand High; Entry Competitive; Payment Medium. Confidence High on demand and payment; Medium on differentiation.

| Keyword | Role | Popularity | Difficulty | Note |
| --- | --- | --- | --- | --- |
| `reading tracker` | Primary | 52 | 65 | Exact app-tracking intent; competitor-derived from `book tracker`; refreshed 2026-07-13. |
| `book tracker` | Related primary | 61 | 65 | Competitor-derived phrase. |
| `reading log` | Adjacent | N/A | N/A | Metric unavailable. |
| `bookshelf tracker` | Adjacent | N/A | N/A | Metric unavailable. |
| `TBR tracker` | Adjacent | N/A | N/A | Metric unavailable. |

| Competitor | Market traction | Revenue evidence | Evidence implication |
| --- | --- | --- | --- |
| [Bookly: Book Tracker](https://apps.apple.com/us/app/id1085047737) | `reading tracker` #1; 59,747 ratings; 4.6 | $50k revenue estimate; last month; iOS US; [Sensor Tower](https://app.sensortower.com/overview/1085047737?country=US); commercial estimate; captured 2026-07-11; High confidence | Closest paid anchor; broad timer, goals, and reports leave room for faster logging. |
| [Margins: Book Tracker](https://apps.apple.com/us/app/id6737528718) | `reading tracker` #7; 17,448 ratings; 4.9 | $11k-$60k/month estimate; iOS App Store; [AppCurrents](https://appcurrents.com/apps/margins-book-tracker-ios-6737528718); public modeled estimate; updated/captured 2026-07-13; Medium confidence | 2024 entrant with meaningful traction; modeled range is decision context, not the qualifying anchor. |
| [Reading Journey](https://apps.apple.com/us/app/id6749302195) | `reading tracker` #8; 168 ratings; 4.6 | $300-$2k/month estimate; iOS App Store; [AppCurrents](https://appcurrents.com/apps/reading-journey-book-tracker-ios-6749302195); public modeled estimate; updated/captured 2026-07-13; Low confidence | Low-authority 2025 entrant; modeled range is decision context, not the qualifying anchor. |

## E. Evidence-First Mineral Identifier Evidence

**Market:** iOS US. Top 10: 10/10 directly relevant, five with 100+ ratings, while five apps with 8 or fewer ratings rank #3, #5, #6, #8, and #10. Demand Medium; Entry Open; Payment Strong. Confidence High on demand, entry, and payment; Medium on achievable trustworthiness.

| Keyword | Role | Popularity | Difficulty | Note |
| --- | --- | --- | --- | --- |
| `mineral identifier` | Primary | 27 | 37 | Clear photo-identification intent; competitor-derived from `rock identifier`; refreshed 2026-07-13. |
| `rock identifier` | Related primary | 53 | 45 | Competitor-derived phrase. |
| `rock and mineral identifier` | Related primary | 23 | 41 | Competitor-derived phrase. |
| `stone identifier` | Adjacent | N/A | N/A | Metric unavailable. |
| `crystal identifier` | Adjacent | N/A | N/A | Metric unavailable. |

| Competitor | Market traction | Revenue evidence | Evidence implication |
| --- | --- | --- | --- |
| [Rock Identifier: Stone ID](https://apps.apple.com/us/app/id1546796934) | `mineral identifier` #1; 74,633 ratings; 4.7 | $400k revenue estimate; last month; iOS US; [Sensor Tower](https://app.sensortower.com/overview/1546796934?country=US); commercial estimate; captured 2026-07-11; High confidence | Category leader; broad geology, folklore, and tools leave a trust-focused scope gap. |
| [RockIn Rock & Mineral identify](https://apps.apple.com/us/app/id6754837588) | `mineral identifier` #7; 1,496 ratings; 4.4 | $20k revenue estimate; last month; worldwide; [Sensor Tower](https://app.sensortower.com/overview/6754837588?country=US); commercial estimate; captured 2026-07-13; High confidence | Collection, buying, and selling scope differs from focused geological verification. |
| [Rock ID - Stone Identifier](https://apps.apple.com/us/app/id6469999508) | `mineral identifier` #9; 3,011 ratings; 4.4 | $10k revenue estimate; last month; worldwide; [Sensor Tower](https://app.sensortower.com/overview/6469999508?country=US); commercial estimate; captured 2026-07-13; High confidence | Broad crystal, mineral, and fossil guide leaves a narrower verification scope. |

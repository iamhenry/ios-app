# Wedge Validation Brief: Scan-Verified Offline QR Maker

Source: [`2026-07-11-mixed-discovery-research.md`](./2026-07-11-mixed-discovery-research.md) | Market: iOS US | Researched: 2026-07-13

## 1. Decision

**Validated wedge:** A permanent, print-safe static QR maker that verifies the exact exported file contains the intended destination before the user prints or shares it, without an app-controlled redirect, ads, hosting, or expiry.

**Evidence strength:** Medium. Cross-app reviews validate costly QR failures, but a scanner and print matrix must still prove the proposed final-file check predicts real-world reliability.

**Product constraints:** Sub-minute offline flow, direct static encoding, constrained styling, and transparent free or one-time pricing.

## 2. Evidence And Alternatives

| Candidate | Decisive evidence | Decision |
| --- | --- | --- |
| **Final-file verified static QR for print** | 9+ failure reports across 5 apps include QR codes failing after download or print. A [QR Creator](https://itunes.apple.com/us/rss/customerreviews/id=1525413524/sortBy=mostRecent/json) reviewer printed 100 unusable business cards; an [MQRG](https://itunes.apple.com/us/rss/customerreviews/id=1456241169/sortBy=mostRecent/json) reviewer reported: "Quality check passes. Actual downloaded QR code shows error." | **Validated:** check the exact exported bytes and prove they encode the direct destination. |
| Generic scan verification | [MQRG](https://apps.apple.com/us/app/id1456241169) already promotes pre-print quality checking, and QR Template has shipped auto-validation. | Rejected: verification alone is already served. |
| Contact-first QR | [QR Me - Contact](https://apps.apple.com/us/app/id1412627381) provides focused local sharing with 1,752 ratings at 4.9; HiHello and Blinq have mature contact flows. | Rejected: one Contact failure does not establish an open wedge. |
| Cheapest QR maker | 50+ pricing, cancellation, purchase, or advertising complaints appear across 6+ apps, but free and low-cost generators already exist. | Constraint only: pricing affects trust, not the core outcome. |
| Customization-first QR | Established apps already offer colors, logos, patterns, templates, and multiple export sizes. | Rejected: incumbent table stakes. |

Additional trust evidence: reviews report hosted or account-linked codes redirecting incorrectly, showing ads, or stopping after payment changes in [Me QR](https://itunes.apple.com/us/rss/customerreviews/id=1601025694/sortBy=mostRecent/json), [QR Template](https://itunes.apple.com/us/rss/customerreviews/id=1574018167/sortBy=mostRecent/json), and [Blinq](https://itunes.apple.com/us/rss/customerreviews/id=1324102258/sortBy=mostRecent/json).

## 3. Tracer Bullet

**Core job:** Create one styled URL QR that a small-business owner can confidently place on printed material without depending on the app after export.

**Flow:** Enter URL -> choose constrained style -> render final PNG -> decode that PNG -> compare destination -> show static ownership proof -> share.

**Include:** One URL payload, direct static encoding, constrained color and logo styling, high-resolution PNG, local final-file verification, actionable failure, and iOS sharing.

**Exclude:** Other payloads, dynamic destinations, hosted redirects, accounts, analytics, broad templates, scanner history, and SVG until its output can be verified independently.

**Acceptance:**

- The decoded final PNG exactly matches the canonical entered URL and contains no app-controlled intermediary domain.
- Deliberately unsafe styling is rejected before export.
- Every passing artifact scans in the agreed matrix across short and long URLs, allowed styles, Apple Camera, two independent scanners, and screen and print samples.
- The happy path completes offline in under 60 seconds.

## 4. Blocking Unknown And Next Test

**Blocking unknown:** Does local verification of the exact styled PNG avoid false passes across real scanners and printed output?

**Next test:** Build a focused native reliability spike and run generated PNGs through the agreed screen-and-print matrix. Continue to product requirements only if every local pass also passes the external matrix and deliberately unsafe styles fail locally.

## Sources

- [Phase 1 opportunity research](./2026-07-11-mixed-discovery-research.md)
- [QR Code Generator, QR Template listing](https://apps.apple.com/us/app/id1574018167)
- [QR Code Generator, QR Template US reviews](https://itunes.apple.com/us/rss/customerreviews/id=1574018167/sortBy=mostRecent/json)
- [QR Code Generator - MQRG listing](https://apps.apple.com/us/app/id1456241169)
- [QR Code Generator - MQRG US reviews](https://itunes.apple.com/us/rss/customerreviews/id=1456241169/sortBy=mostRecent/json)
- [QR Creator: Scan & Make QRCode US reviews](https://itunes.apple.com/us/rss/customerreviews/id=1525413524/sortBy=mostRecent/json)
- [Me QR - QR Code Generator US reviews](https://itunes.apple.com/us/rss/customerreviews/id=1601025694/sortBy=mostRecent/json)
- [Blinq: Digital Business Card US reviews](https://itunes.apple.com/us/rss/customerreviews/id=1324102258/sortBy=mostRecent/json)
- [QR Me - Contact listing](https://apps.apple.com/us/app/id1412627381)
- [QR Me - Contact US reviews](https://itunes.apple.com/us/rss/customerreviews/id=1412627381/sortBy=mostRecent/json)

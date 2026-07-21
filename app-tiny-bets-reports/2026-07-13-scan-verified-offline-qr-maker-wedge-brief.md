# Wedge Validation Brief: Scan-Verified Offline QR Maker

Source: [`2026-07-11-mixed-discovery-research.md`](./2026-07-11-mixed-discovery-research.md) | Market: iOS US | Researched: 2026-07-13; refreshed: 2026-07-14

## 1. Decision

**Validated wedge:** A direct static QR maker that verifies the exact exported file contains the intended destination before the user adds it to printed material or shares it, without an app-controlled redirect, hosting, or app-imposed expiry.

**Evidence strength:** Medium. Explicit print use appears across 4 apps and artifact failures appear across 5, but reviews do not establish how often users print and a scanner-and-print matrix must still prove the final-file check predicts real-world reliability.

**Product constraints:** Sub-minute offline generation, export, and verification; direct static encoding; constrained styling; and transparent free or one-time pricing as a trust promise rather than the product wedge.

## 2. Evidence And Alternatives

| Candidate | Decisive evidence | Decision |
| --- | --- | --- |
| **Final-file verified static QR for print** | 9+ artifact-failure reports across 5 apps include failures after download or print. Explicit print use appears in 4 reviews across 4 apps, including business cards, a box label, bottle labels, and a current print project. A [QR Creator](https://itunes.apple.com/us/rss/customerreviews/id=1525413524/sortBy=mostRecent/json) reviewer printed 100 unusable business cards; an [MQRG](https://itunes.apple.com/us/rss/customerreviews/id=1456241169/sortBy=mostRecent/json) reviewer reported: "Quality check passes. Actual downloaded QR code shows error." | **Validated:** check the exact exported bytes and prove they encode the direct destination. Print use is real, but its prevalence is not established. |
| Generic scan verification | [MQRG](https://apps.apple.com/us/app/id1456241169) promotes pre-print quality checking and improved it in February 2026; [QR Template](https://apps.apple.com/us/app/id1574018167) added auto-validation in May 2026. A June 2026 QR Template review still reports a failed print project, but neither listing promises verification of the exact exported file. | Rejected: generic verification is already served; final-file verification is the narrower distinction. |
| Contact-first QR | [QR Me - Contact](https://apps.apple.com/us/app/id1412627381) provides focused local sharing with 1,752 ratings at 4.9; HiHello and Blinq have mature contact flows. | Rejected: one Contact failure does not establish an open wedge. |
| Cheapest QR maker | In a refreshed 8-app sample, 4 display subscriptions, 3 explicitly offer lifetime purchases, and free no-subscription alternatives such as [Simple QR Code Generator](https://apps.apple.com/us/app/id6443816451) already exist. | Constraint only: no-subscription pricing can support trust, but is already served and does not change the core outcome. |
| Customization-first QR | Established apps already offer colors, logos, patterns, templates, and multiple export sizes. | Rejected: incumbent table stakes. |

Additional trust evidence: reviews report hosted or account-linked codes redirecting incorrectly, showing ads, or stopping after payment changes in [Me QR](https://itunes.apple.com/us/rss/customerreviews/id=1601025694/sortBy=mostRecent/json), [QR Template](https://itunes.apple.com/us/rss/customerreviews/id=1574018167/sortBy=mostRecent/json), and [Blinq](https://itunes.apple.com/us/rss/customerreviews/id=1324102258/sortBy=mostRecent/json).

The app produces and verifies a high-resolution PNG for use in tools such as Canva, Pages, or Adobe before a business card, flyer, menu, label, or sign is printed; it does not operate the printer. Its guarantee applies only to the exact PNG it checks, not to later resizing, editing, or file conversion. Direct static encoding also means no destination editing or QR-provider scan-location analytics; the destination website can still record visits through ordinary web analytics. [MQRG's privacy policy](https://my-qrcode-gen.com/privacy) confirms it implements provider-level scan analytics with hosted redirects, Google Cloud infrastructure, and IP-derived approximate location. The QR itself has no app-imposed expiry, but loading its destination still requires internet access and an available website.

## 3. Tracer Bullet

**Core job:** Create one styled URL QR image that a small-business owner can confidently add to printed material without depending on the app after export.

**Flow:** Enter URL -> choose constrained style -> render final PNG -> decode that exact PNG -> compare destination -> show static ownership proof -> share to a design or print workflow.

**Include:** One URL payload, direct static encoding, constrained color and logo styling, high-resolution PNG, local final-file verification, actionable failure, and iOS sharing.

**Exclude:** Other payloads, dynamic destinations, hosted redirects, accounts, scan-location analytics, broad templates, scanner history, and SVG until its output can be verified independently.

**Acceptance:**

- The decoded final PNG exactly matches the canonical entered URL and contains no app-controlled intermediary domain.
- Deliberately unsafe styling is rejected before export.
- Every passing exact PNG decodes across short and long URLs, allowed styles, Apple Camera, and two independent scanners.
- Generation, export, and final-file verification complete offline in under 60 seconds; opening the destination website is outside this offline flow.

## 4. Blocking Unknown And Next Test

**Blocking unknown:** Do print-intent users value exact-file proof beyond incumbent quality-check claims, and does that proof avoid false passes across real scanners and printed output?

**Next test:** Run 5-8 print-intent small-business users through a focused native reliability spike and the agreed screen-and-print matrix. Continue only if at least 3 identify final-file permanence as materially valuable, every local pass also passes the external matrix, and deliberately unsafe styles fail locally.

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
- [Qrafter listing and US reviews](https://apps.apple.com/us/app/id416098700)
- [Simple QR Code Generator listing](https://apps.apple.com/us/app/id6443816451)
- [MQRG privacy policy](https://my-qrcode-gen.com/privacy)
- [MQRG terms and scan-location limitations](https://my-qrcode-gen.com/terms)

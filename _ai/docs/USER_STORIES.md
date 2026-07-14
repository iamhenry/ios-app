# Project Overview

Build the smallest end-to-end proof for a **Scan-Verified Offline QR Maker** for iOS in the US. A small-business owner enters one URL, applies constrained color or logo styling, creates a high-resolution PNG, verifies that the exact final PNG decodes locally to the intended canonical URL, and shares it through iOS.

**Evidence-backed wedge; unvalidated product hypothesis:** Current evidence supports exact-export verification as a Medium-strength wedge. The product hypothesis remains unvalidated: exact-export payload verification, paired with conservative styling constraints, can improve confidence before a QR code is printed. A local pass proves only that the final PNG decodes to the intended URL in the app; it does not prove that a screen or printed copy will scan reliably with real-world scanners.

The tracer bullet includes one direct/static URL payload, constrained styling, high-resolution PNG export, local exact-file verification, actionable failure guidance, iOS sharing, and offline generation, export, and verification. It excludes dynamic destinations, hosted redirects, accounts, QR-provider scan analytics, broad templates, other payloads, scanner or history features, cloud dependencies, SVG, and monetization stories. Loading the destination website is outside the offline flow and requires internet access and an available website.

Evidence and hypothesis traceability:
- [Phase 1 opportunity research](../../app-tiny-bets-reports/2026-07-11-mixed-discovery-research.md)
- [Current wedge brief](../../app-tiny-bets-reports/2026-07-13-scan-verified-offline-qr-maker-wedge-brief.md)

# Scenarios

## Happy Path

### Scenario SCN-01: Create a QR for one direct URL
**Given** a valid `http` or `https` URL<br>
**When** the user creates a QR code<br>
**Then** one QR encoding the canonical destination is created for use on printed material

**Acceptance Criteria**:
- Creation requires no account, network connection, hosted redirect, or app-controlled intermediary domain.
- The QR directly encodes the canonical destination and has no app-imposed expiry; destination availability remains outside the app's control.

### Scenario SCN-02: Apply supported color and logo styling
**Given** a QR for one direct URL<br>
**When** the user chooses an allowed foreground/background color combination and optionally adds one logo within defined limits<br>
**Then** every accepted styling choice appears in the final rendered PNG

**Acceptance Criteria**:
- The user cannot silently exceed the supported color or logo constraints.

### Scenario SCN-03: Verify the exact final PNG payload
**Given** a final high-resolution PNG and its canonical entered URL<br>
**When** the user verifies the PNG before sharing<br>
**Then** the app shows a local pass only when the decoded payload exactly matches the canonical entered URL

**Acceptance Criteria**:
- The app decodes the exact bytes of the final high-resolution PNG and compares the result with the canonical entered URL.

### Scenario SCN-04: Share the same verified PNG through iOS
**Given** a PNG that passes local exact-file verification<br>
**When** the user opens the iOS share sheet<br>
**Then** the same file that passed verification is available to share elsewhere

**Acceptance Criteria**:
- The file the app supplies to the iOS share sheet is the same exact PNG that passed verification.
- The app's guarantee applies only to that exact PNG, not to later resizing, editing, or file conversion.
- Generation, export, verification, and opening the iOS share sheet can be completed offline in under 60 seconds; delivery through a selected share service and opening the destination website are outside this flow.

## Error

### Scenario SCN-05: Correct invalid input or unsafe styling
**Given** an invalid URL or deliberately unsafe color or logo treatment<br>
**When** the user attempts to produce a testable QR<br>
**Then** the app blocks a passing or shareable state and shows specific correction guidance

**Acceptance Criteria**:
- The app identifies the failing input or constraint and presents at least one specific corrective action.

### Scenario SCN-06: Recover from exact-file verification failure
**Given** an exact final PNG that cannot be decoded or decodes to a different canonical destination<br>
**When** exact-file verification completes<br>
**Then** the app shows failure, withholds sharing, and lets the user return to the entered URL or styling

**Acceptance Criteria**:
- The app states the observed failure type.
- Previously valid data remains available without re-entry.

## Edge Case (High Frequency, High Impact)

### Scenario SCN-07: Validate local passes across realistic inputs
**Given** locally passing artifacts for short and long URLs across all allowed style combinations in the agreed validation matrix<br>
**When** each artifact is scanned from both screen and print using Apple Camera and two independent scanners<br>
**Then** every scanner decodes the intended canonical URL

**Acceptance Criteria**:
- Any local-pass failure to decode externally stops continuation and triggers research.

### Scenario SCN-08: Distinguish local verification from physical scan confidence
**Given** an exact-file verification result<br>
**When** the app displays the result<br>
**Then** the user sees what the local check proved without a guarantee of print or screen reliability

**Acceptance Criteria**:
- Every local pass state explicitly says that the exact PNG payload matched and that print/screen reliability is not guaranteed by this check alone.
- No local failure is labeled as verified or shareable.

## Core User Flows

1. **Offline happy path:** Enter valid URL -> apply an allowed color or logo style -> render high-resolution PNG -> decode the exact final PNG -> compare canonical destination -> show local pass and its limitation -> open iOS share sheet.
2. **Input/style recovery:** Enter invalid URL or apply unsafe style -> show the specific constraint and corrective action -> revise input/style -> retry rendering and verification.
3. **Verification recovery:** Exact PNG fails to decode or payload differs -> show actionable failure -> return to preserved URL/style -> revise -> regenerate and verify again.
4. **Hypothesis validation gate:** Generate short/long URL artifacts across allowed and deliberately unsafe styles -> require unsafe styles to fail locally -> test every local pass on screen and print with Apple Camera and two independent scanners -> continue only if every scanner decodes the intended canonical URL; otherwise stop and research.

# Key Screens

- **Create:** URL entry, constrained color/logo controls, and one clear action to render and verify.
- **Verification and Share:** Exact-file pass or actionable failure, an explicit statement of what local verification does not prove, edit/retry controls, and iOS sharing only for a passing PNG.

# Tech Stack (stable versions)
## Frontend
- TBD — select during technical planning.

## Backend
- TBD — select during technical planning; the tracer boundary requires no cloud dependency.

## Languages
- TBD — select during technical planning.

## Development Tools:
- TBD — select during technical planning.

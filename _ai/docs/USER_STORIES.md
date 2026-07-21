# Project Overview

Build the smallest end-to-end proof for a **Scan-Verified Offline QR Maker** for iOS in the US. A small-business owner selects a supported QR type, enters its required details, applies constrained foreground and background colors, and creates a high-resolution PNG. Before the PNG can be saved or shared, the app verifies locally that the exact final file decodes to the intended canonical payload.

**Evidence-backed wedge; unvalidated product hypothesis:** Current evidence supports exact-export verification as a Medium-strength wedge. The product hypothesis remains unvalidated: exact-export payload verification, paired with conservative styling constraints, can improve confidence before a QR code is printed. A local pass proves only that the final PNG decodes to the intended payload in the app; it does not prove that a screen or printed copy will scan reliably with real-world scanners.

The tracer bullet includes six static types (Website, Contact, Email, Phone, Instagram, and X / Twitter), type-specific details, safe foreground/background color choices, a local list of saved QR codes, editing, high-resolution PNG export, local exact-file verification, saving to Photos, iOS sharing, and actionable failure guidance. Generation, verification, local storage, and opening system export surfaces work offline. It excludes logos, dynamic destinations, hosted redirects, accounts, QR-provider scan analytics, broad templates, cloud dependencies, SVG export, and monetization stories. Loading an encoded online destination or delivering through a selected share service remains outside the offline flow.

Evidence and hypothesis traceability:
- [Phase 1 opportunity research](../../app-tiny-bets-reports/2026-07-11-mixed-discovery-research.md)
- [Current wedge brief](../../app-tiny-bets-reports/2026-07-13-scan-verified-offline-qr-maker-wedge-brief.md)

# Scenarios

## Happy Path

### Scenario SCN-01: Start from Home
**Given** the user opens the Home tab<br>
**When** no QR codes have been saved<br>
**Then** an empty state provides a clear action to create one

**Acceptance Criteria**:
- The Create action remains available when saved QR codes exist.
- Each saved item shows its QR preview, type, and a recognizable name derived from its primary detail.
- Selecting a saved item opens it for editing.

### Scenario SCN-02: Choose a type and enter its details
**Given** the user starts creating a QR code<br>
**When** the user selects Website, Contact, Email, Phone, Instagram, or X / Twitter and enters valid required details<br>
**Then** the preview represents the canonical payload for that type

**Acceptance Criteria**:
- Each type shows only its relevant details.
- Website requires a valid direct `http` or `https` URL.
- Contact requires a name and at least one valid contact method: email or phone number.
- Email requires a valid email address, Phone requires a valid phone number, and each social type requires a valid username or profile URL.
- Instagram and X / Twitter encode direct profile URLs without an app-controlled redirect.
- Creation requires no account, network connection, hosted redirect, or app-controlled intermediary domain.
- The Save to Photos action remains disabled until all required details are valid.

### Scenario SCN-03: Apply supported colors
**Given** a QR code with valid details and safe default colors<br>
**When** the user chooses an allowed foreground and background color combination<br>
**Then** the preview and final PNG use the selected colors

**Acceptance Criteria**:
- The foreground color applies to the QR modules that encode the payload.
- The background color applies to the image background behind those modules.
- Unsafe combinations are unavailable or clearly rejected.
- Logo customization is not available in the tracer bullet.

### Scenario SCN-04: Automatically verify the exact final PNG
**Given** valid details and supported colors<br>
**When** the app renders the final high-resolution PNG<br>
**Then** the app automatically enables saving and sharing only when that exact file decodes to the intended canonical payload

**Acceptance Criteria**:
- The app decodes the exact bytes of the final high-resolution PNG and compares the result with the canonical payload for the selected type.
- A passing state communicates that the exact image contains the entered details without guaranteeing later resizing, editing, conversion, screen scanning, or print scanning.
- No failed file is labeled as verified or made available to save or share.

### Scenario SCN-05: Save the verified PNG to Photos and Home
**Given** a PNG that passes local exact-file verification<br>
**When** the user selects Save to Photos<br>
**Then** the exact verified PNG is saved to Photos and the QR code appears on Home

**Acceptance Criteria**:
- The primary call to action is labeled `Save to Photos`.
- Photos receives the same exact PNG that passed verification.
- The Home item retains the selected type, canonical details, selected colors, recognizable name, and QR preview for later editing.
- If Photos access or saving fails, the app explains how to recover, preserves the draft, and does not create or update the Home item.
- The app's guarantee applies only to the exact saved PNG, not to later resizing, editing, or file conversion.

### Scenario SCN-06: Share the same verified PNG through iOS
**Given** a PNG that passes local exact-file verification<br>
**When** the user opens the iOS share sheet<br>
**Then** the same exact PNG is available to share elsewhere

**Acceptance Criteria**:
- Opening the share sheet does not by itself create or update a Home item.
- The app's guarantee applies only to that exact PNG, not to later resizing, editing, or file conversion.
- Generation, verification, saving to Photos, and opening the iOS share sheet can be completed offline in under 60 seconds; delivery through a selected share service and opening an online destination are outside this flow.

### Scenario SCN-07: Edit an existing QR code
**Given** the user opens a saved QR code from Home<br>
**When** the user changes its details or colors and selects Save to Photos<br>
**Then** the updated verified PNG is saved to Photos and replaces the existing Home item

**Acceptance Criteria**:
- Editing uses the same Details and Customize controls as creation.
- The update is not committed until the edited final PNG passes exact-file verification and is saved to Photos.
- Selecting Cancel or navigating Back discards all unsaved edits, leaves the existing Home item unchanged, and does not save a new image to Photos.
- Leaving a new, unsaved QR with Cancel or Back creates no Home item and saves no image to Photos.

## Error

### Scenario SCN-08: Correct invalid details or unsafe colors
**Given** missing or invalid required details or a deliberately unsafe color combination<br>
**When** the user attempts to complete the QR code<br>
**Then** the app keeps saving and sharing unavailable and shows specific correction guidance

**Acceptance Criteria**:
- The app identifies the failing input or constraint and presents at least one specific corrective action.

### Scenario SCN-09: Recover from exact-file verification failure
**Given** an exact final PNG that cannot be decoded or decodes to a different canonical payload<br>
**When** exact-file verification completes<br>
**Then** the app shows failure, withholds saving and sharing, and lets the user return to the entered details or colors

**Acceptance Criteria**:
- The app states the observed failure type.
- Previously valid data remains available without re-entry.

## Core User Flows

1. **Create and save:** Open Home -> select Create -> choose a type -> enter required details -> optionally choose safe foreground/background colors -> automatically render and verify the exact PNG -> select Save to Photos -> save the PNG and add it to Home.
2. **Share:** Create or open a valid QR -> automatically render and verify the exact PNG -> open the iOS share sheet with that same file.
3. **Edit and save:** Select a saved QR on Home -> change details or colors -> automatically render and verify the edited PNG -> select Save to Photos -> save the updated PNG and update the Home item.
4. **Discard changes:** Leave creation or editing with Cancel or Back -> discard unsaved changes -> leave Home and Photos unchanged.
5. **Recovery:** Correct invalid details, unsafe colors, verification failure, or Photos failure without re-entering previously valid data.

## Internal Validation Gate (Not User-Facing)

- Generate representative payloads for every supported type across allowed and deliberately unsafe color combinations.
- Require deliberately unsafe combinations to be rejected and every local pass to decode to the intended canonical payload.
- Test representative passing PNGs from screen and print using Apple Camera and two independent scanners.
- Any local-pass failure to decode externally stops continuation and triggers research.

# Key Screens

- **Home:** Empty state with Create; otherwise a list of saved QR previews, types, and recognizable names.
- **Type Selection:** The six supported QR types.
- **Create/Edit:** QR preview, type-specific Details, foreground/background Customize controls, Cancel/Back behavior, and a Save to Photos call to action.
- **Share:** The iOS share sheet receives only the exact PNG that passed local verification.

# Tech Stack (stable versions)
## Frontend
- TBD — select during technical planning.

## Backend
- TBD — select during technical planning; the tracer boundary requires no cloud dependency.

## Languages
- TBD — select during technical planning.

## Development Tools:
- TBD — select during technical planning.

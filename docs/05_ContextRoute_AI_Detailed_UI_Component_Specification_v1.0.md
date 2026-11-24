# ContextRoute AI — Detailed UI Component Specification v1.0

**Platform:** Native Android | Kotlin | Jetpack Compose | Material 3  
**Baseline:** API 31 minimum

> Document provenance: Reconstructed from approved design decisions and specifications available in the project conversation.

## 1. Design tokens
- White: #FFFFFF
- Deep Navy: #0B3C6D
- Primary Blue: #1565C0
- Light Blue: #EAF3FF
- Light Background: #F4F7FB
- Main Text: #172B4D
- Secondary Text: #64748B
- Border: #DCE6F2

## 2. Layout metrics
- Reference viewport: 360×800dp portrait.
- Horizontal screen padding: 16dp.
- Section spacing: 20–24dp.
- Card internal padding: 12–16dp.
- Minimum interactive target: 48×48dp.
- Respect system status/navigation bars and display cutouts.
- Support scrolling on smaller devices; avoid fixed-height content that clips.

## 3. Typography
Use Material 3 type scale consistently. Prioritize readable body text and clear labels. Avoid excessive font weights, tiny secondary labels, long all-caps labels and low-contrast text.

## 4. Component standards
- **Primary button:** Filled primary blue, clear verb-first label, full-width only when appropriate.
- **Secondary button:** Outlined or tonal treatment for supporting actions.
- **Text field:** Persistent label, clear focus/error state, appropriate keyboard and inline validation.
- **Search field:** Search icon and text only; no microphone or voice affordance.
- **Cards:** Use only for meaningful grouped content; avoid nested/stacked card clutter.
- **Bottom navigation:** Home, Explore, Profile only.
- **Chips:** Use for compact filters/selections; selected state must be visually and semantically clear.
- **Dialogs/sheets:** Concise explanation, explicit primary and cancel actions; avoid unnecessary confirmation.
- **Loading/empty/error:** Provide distinct states, useful explanation and retry where possible.
- **Map controls:** Familiar icon buttons with content descriptions and adequate touch targets.
- **Report category selector:** Professional Material icons plus text labels; never rely on icons alone.

## 5. Iconography and imagery
Use Material Symbols/Material Icons or approved Material 3-compatible vector assets. Use consistent stroke/filled treatment and semantic mapping. Do not use emoji as the main functional icon. Destination photos should be genuine, relevant, licensed/appropriately sourced, and must not imply verification or endorsement.

## 6. Accessibility
Provide content descriptions for meaningful icons, logical focus order, scalable text, sufficient contrast, touch targets of at least 48dp, and state announcements for important asynchronous changes. Do not communicate status by color alone.

## 7. Motion and feedback
Use restrained transitions and Material motion patterns. Provide immediate pressed/selected feedback. Avoid decorative animations that delay task completion. Respect system animation preferences.

## 8. Forms and reporting
Label every field; validate close to the input; preserve entered values on recoverable errors; disable duplicate submission while saving; clear/navigate only after successful local save. Distinguish Submitted, Pending Sync and Failed states truthfully.

## 9. Navigation and responsive behavior
Keep primary navigation consistent. Use full-screen focused flows for active navigation and emergency actions. Support small screens, portrait-first layouts and Android system insets.

## 10. Prohibited UI patterns
No login/signup/OTP gates, no microphone or voice controls, no audio/speaker features, no fake live traffic, no fabricated safety scores, no unverified “verified” hazard badges, no decorative clutter, and no inaccessible icon-only actions.

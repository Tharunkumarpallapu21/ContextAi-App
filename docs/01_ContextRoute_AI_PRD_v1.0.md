# ContextRoute AI — Product Requirements Document v1.0

**Tagline:** Intelligent Routes. Safer Journeys.

## Product vision
Build an India-first Android application that recommends routes using trip context and available road information, helping people make informed travel decisions.

## Approved platform and stack
- Native Android; Kotlin
- Jetpack Compose and Material 3
- Minimum Android API 31
- Room for structured local persistence; DataStore for preferences
- Local-first architecture; no mandatory cloud backend
- Free / zero-budget dependencies and services for the MVP

## Core principles
- Guest-first: no login, signup, OTP, mandatory email, or phone number
- Foreground location only; no background tracking
- English-only initial interface
- No microphone, voice search, audio, speaker, or voice-read functionality
- Never present fabricated information as real
- Unknown information must remain explicitly unknown; unknown does not mean safe
- No generated or unsupported safety score

## Primary user journey
Home map → search origin/destination → confirm destination → optionally provide trip context → view up to three available route alternatives → route details → route preview → live navigation.

## Main capabilities
1. Location and map experience
2. Route calculation and alternatives
3. Context-aware route ranking using explicit rules
4. Road hazard and community reporting
5. Explore destinations and nearby places
6. Emergency assistance through user-initiated device actions
7. Local profile, saved places, recent searches, vehicle and travel preferences
8. Offline/data management and help

## Route requirements
- Show a maximum of three alternatives, and only when returned by the routing provider.
- ETA and distance must come from the routing engine.
- Clearly disclose when live traffic is unavailable.
- Distinguish provider-backed information from community-submitted reports.
- Do not invent hazard status, accessibility, road conditions, safety ratings, or emergency facility data.

## Reporting
Support pothole, accident, roadblock, waterlogging, damaged road, construction, landslide, fallen tree, and other. Use truthful states such as Submitted, Pending Sync, and Failed. Do not display unmoderated reports as verified. Preserve the form if local saving fails; clear it only after a successful save.

## Emergency assistance
Provide clearly labeled simulated alerts where applicable and user-initiated actions such as opening the dialer or contacting a configured emergency contact. Do not claim control-room notification or emergency-service integration unless implemented and tested.

## Persistence and privacy
Persist appropriate saved places, recent searches, preferences, vehicle profiles, reports, settings, and emergency contacts locally. Request location only when needed and only while the app is in use. No background tracking in the MVP.

## Screen scope
The approved product contains 28 screens, grouped as onboarding; map and routing; navigation and assistance; explore and reporting; profile and personalization; settings and information. The complete screen list is in `04_ContextRoute_AI_28_Screen_Wireframes_v1.0.md`.

## MVP limitations to disclose
Live traffic, offline routing, hazard verification, accessibility coverage, and emergency integrations depend on actual provider capabilities and must never be implied where unavailable.

## Approval gate
This PRD v1.0 is the approved product baseline. Do not begin implementation until the project owner explicitly approves the implementation phase.

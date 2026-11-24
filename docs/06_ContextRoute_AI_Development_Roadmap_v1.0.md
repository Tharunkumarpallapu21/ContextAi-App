# ContextRoute AI — Development Roadmap v1.0

**Execution principle:** Phase-gated delivery; no phase advances without explicit project-owner approval.

> Document provenance: Reconstructed from approved project decisions and roadmap discussions available in the project conversation.

## Phase 0 — Project foundation
- Create a fresh native Android Studio project.
- Configure Kotlin, Jetpack Compose, Material 3 and minimum API 31.
- Establish Gradle Kotlin DSL and a clean package structure.
- Add Room and DataStore foundations only after dependency verification.
- Add documentation and baseline build configuration.
- Run a clean build and report exact results.
- Stop for owner review and approval before feature implementation.

## Phase 1 — Core app shell and design system
- Theme, colors, typography, spacing and reusable components.
- Navigation foundation and the Home / Explore / Profile shell.
- Screen state conventions and shared error handling.
- Compose previews and accessibility baseline.

## Phase 2 — Local data foundation
- Room entities, DAOs, repositories and migrations.
- DataStore preferences.
- Saved places, recent searches, vehicle/travel preferences and local report persistence.
- Persistence and migration tests.

## Phase 3 — Location and map foundation
- Foreground location permission flow and manual fallback.
- MapLibre Native integration after licensing/provider checks.
- Camera, markers, user location and route-polyline abstractions.
- Permission denial, GPS-off and map failure handling.

## Phase 4 — Search and routing
- Place search/geocoding adapter.
- Routing provider adapter and route domain models.
- Route alternatives (maximum three), details and preview.
- Real ETA/distance only; explicit provider/network errors.
- Validate free-tier limits, India coverage and attribution.

## Phase 5 — Context and road intelligence
- Optional trip context and persistent preferences.
- Explainable rule-based ranking.
- Source-aware road information and explicit Unknown state.
- No generated safety score or unsupported traffic/hazard claims.

## Phase 6 — Navigation and safety
- Foreground active-navigation experience.
- Maneuver and route-progress information where provider supports it.
- Emergency dialer/contact intents and clearly labelled simulations.
- Nearby facilities only from a real source; unknown/unavailable states.

## Phase 7 — Explore and reporting
- Explore categories, results, details and nearby places.
- Road report form and local persistence.
- Truthful Submitted / Pending Sync / Failed states.
- Preserve form on failure and test retry behavior.

## Phase 8 — Profile, settings and offline management
- Guest profile, saved places, recent searches.
- Vehicle/travel preferences.
- Settings, data management and help/about.
- Disclose actual offline capabilities and limitations.

## Phase 9 — QA and release readiness
- Unit, repository, DAO, Compose UI and device tests.
- Test permission denial, network loss, GPS disabled, empty results and save failures.
- Verify accessibility, performance, privacy and app lifecycle.
- Build signed release APK using owner-controlled credentials.
- Document limitations and installation instructions.

## Approval gates
1. Phase 0 must be reviewed and approved before Phase 1.
2. Each subsequent phase requires explicit approval before starting.
3. Scope, architecture, stack, permissions or budget changes require owner approval.
4. Never report a feature as complete without implementation and verification evidence.

## Release constraints
Free/zero-budget services only unless the owner approves otherwise. No mandatory backend or authentication. No background location. No microphone/audio. Never fake live traffic, verified hazards, accessibility coverage, safety scores or emergency-service integrations.

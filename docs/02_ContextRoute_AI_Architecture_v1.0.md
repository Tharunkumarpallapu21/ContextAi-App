# ContextRoute AI — Software Architecture Document v1.0

**Approved baseline:** Native Android, local-first architecture  
**Tagline:** Intelligent Routes. Safer Journeys.

> Document provenance: Reconstructed from approved project decisions and specifications available in the project conversation; not represented as a verbatim export of historical drafts.

## 1. Architecture overview
Native Android application using Kotlin and Jetpack Compose, with clear presentation, domain, and data boundaries. Local-first persistence avoids a mandatory backend. Map, geocoding, and routing providers remain replaceable.

## 2. Technology baseline
| Area | Decision |
|---|---|
| Language | Kotlin |
| UI | Jetpack Compose |
| Design system | Material 3 |
| Minimum Android | API 31 |
| Presentation | MVVM with unidirectional state/event flow |
| Structured persistence | Room |
| Preferences | DataStore |
| Mapping | MapLibre Native, subject to dependency/provider verification |
| Routing | Replaceable routing adapter |
| Backend | No mandatory backend initially |
| Authentication | None |

## 3. Logical architecture
- **Presentation:** Compose screens, reusable UI, navigation, screen state, user events.
- **Domain:** Business models, repository contracts, use cases, contextual ranking rules.
- **Data:** Room entities/DAOs, DataStore, repository implementations, provider data sources.
- **Engines:** Location, Map, Routing, AI Road Intelligence, Safety.
- **Core:** Design system, utilities, permissions, error/result types and configuration.

## 4. Five essential engines
### Location Engine
Foreground location access, permission rationale/state, accuracy and timestamp, GPS/provider failure handling, manual location fallback. No background location service in MVP.

### Map Engine
Map lifecycle, camera movement, user-location display, markers, destination selection, route polylines, attribution, loading and error states. Provider-specific rendering stays behind interfaces.

### Routing Engine
Origin/destination and supported travel mode inputs; replaceable provider adapter; route geometry, ETA, distance and maneuvers where supported; maximum three alternatives in UI; typed errors for no route, network failure, invalid input and provider limits.

### AI Road Intelligence Engine
Separates provider-backed facts from community reports; represents source and timestamp where supported; applies explainable rule-based contextual ranking; preserves explicit Unknown states. No generated safety score or unsupported predictive claim.

### Safety Engine
User-initiated dialer/contact actions; provider-backed nearby facility results; explicit unavailable/unknown states; simulated alerts only when labelled as simulations. No unverified authority/control-room notification.

## 5. Data architecture
Use Room for structured entities and relationships, DataStore for lightweight preferences, and app-private storage for photo files when supported. Store file references in Room. Implement and test migrations.

Suggested entities: SavedPlace, RecentSearch, TravelPreference, VehiclePreference, RoadReport, EmergencyContact, CachedPlace and AppSettings.

## 6. Package boundaries
core/common, core/designsystem, core/navigation, core/permissions, core/utils; data/local, data/preferences, data/repository; domain/model, domain/repository, domain/usecase; engines/location, engines/map, engines/routing, engines/roadintelligence, engines/safety; features/onboarding, home, search, routes, navigation, assistance, explore, reporting, profile and settings.

## 7. Navigation and state
Use safe route definitions. Primary navigation: Home, Explore and Profile. Hide bottom navigation during focused navigation/emergency/full-screen experiences where appropriate. Model initial, loading, success, empty, error and offline/unavailable states explicitly. Preserve form state on recoverable errors.

## 8. Provider boundaries
Geocoding, routing, map tiles and place discovery use provider adapters. Verify free-tier quotas, attribution, licensing, India coverage and current terms before selection. Live traffic is unavailable unless a real provider supplies it.

## 9. Privacy and permissions
No account credentials. Request foreground location only when needed. No RECORD_AUDIO or background-location permission. Avoid logging precise location, emergency contacts or report photos. Calls require user confirmation through Android intents.

## 10. Testing
Unit-test ranking, validation, state transitions and use cases; test Room DAOs/migrations; test provider success/empty/malformed/failure responses; Compose navigation/forms/accessibility; device cases for permission denial, GPS off, network loss and lifecycle.

## 11. Architecture constraints
Native Android, Kotlin, Compose, Material 3, API 31, Room, DataStore, MapLibre Native subject to verification, replaceable routing adapter, local-first/no mandatory backend, zero budget and no authentication. Changes require explicit approval.

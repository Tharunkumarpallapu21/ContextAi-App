# ContextRoute AI — Complete 28-Screen Wireframes v1.0

**Approved screen structure and layout intent**  
**Tagline:** Intelligent Routes. Safer Journeys.

> Document provenance: Reconstructed from approved decisions and wireframe discussions available in the project conversation. These are text wireframe specifications, not pixel-perfect exported design files.

## Group A — Onboarding
1. **Splash Screen** — Brand mark, app name and short tagline; minimal loading presentation.
2. **Welcome Screen** — Clear value proposition and primary Get Started action.
3. **Location Setup** — Explain why foreground location improves route planning; allow permission request and manual fallback.
4. **Get Started** — Confirm entry into the guest-first app; no account creation or login.

## Group B — Map and Routing
5. **Home / Live Map** — Full-screen map, floating search, origin/destination controls, current-location affordance and Find Routes action; bottom navigation Home / Explore / Profile.
6. **Search Location** — Search field, recent searches and relevant suggestions; no microphone.
7. **Select Destination** — Confirm selected place, address and map position; allow correction.
8. **Travel Context** — Optional per-trip context such as purpose and traveller/group assistance needs; skippable and distinct from persistent preferences.
9. **Route Alternatives** — Up to three provider-returned route options with real ETA/distance and disclosed data limitations.
10. **Route Details** — Route summary, available maneuvers, source-backed road information and explicit unknowns.
11. **Route Preview** — Map preview, selected route summary and Start Navigation action.

## Group C — Navigation and Assistance
12. **Live Navigation** — Active route map, next maneuver, remaining distance/time when available, and clear exit/recenter controls.
13. **Navigation Assistance** — Contextual assistance actions relevant to the active trip; no unsupported claims.
14. **Emergency Assistance** — Clear emergency guidance and user-initiated call/contact actions; simulated alerts labelled.
15. **Nearby Emergency Facilities** — Provider-backed facility results only; show unavailable/unknown state when data is missing.

## Group D — Explore and Reporting
16. **Explore Home** — Simple destination discovery categories and curated visual entry points; avoid clutter.
17. **Category Results** — Results for selected category with grounded place information.
18. **Destination Details** — Destination image, name, available description/location information and directions action.
19. **Nearby Places** — Nearby results based on available location and provider data.
20. **Road Reporting** — Hazard category, location, optional description/photo if supported, validation and truthful submission state.

## Group E — Profile and Personalization
21. **Guest Profile** — Local-only profile overview and contribution summary where supported; no account identity.
22. **Saved Places** — Locally saved places with edit/remove and route actions.
23. **Recent Searches** — Recent destination history with clear and reuse actions.
24. **Vehicle Preferences** — Persistent vehicle/travel-mode configuration supported by routing.
25. **Travel Preferences** — Persistent assistance and route preferences; distinct from per-trip Screen 8.

## Group F — Settings and Information
26. **Settings** — App preferences, permissions guidance and general controls.
27. **Offline and Data Management** — Local data/cache status and user-controlled data management; disclose offline limitations.
28. **Help and About** — Clear help content, app information, data/source limitations and contact/support path where available.

## Shared wireframe rules
- White/blue minimal design, map-first home, 16dp horizontal padding and 48dp minimum touch targets.
- Use Material 3 components and professional icons; use destination photography only where it adds value.
- No login, signup, OTP, microphone, voice search, speaker or audio.
- Show explicit loading, empty, error and unavailable states.
- Never represent mock data as real, unmoderated reports as verified, or unknown data as safe.
- Do not add screens or expand scope without owner approval.

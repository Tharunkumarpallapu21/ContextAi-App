# ContextRoute AI — UI/UX Blueprint v1.0

**Tagline:** Intelligent Routes. Safer Journeys.  
**Design direction:** Premium, minimal, white-and-blue, India-first, easy to operate.

> Document provenance: Reconstructed from approved decisions and specifications available in the project conversation.

## 1. Design principles
- Map-first experience with clear hierarchy and low visual clutter.
- Familiar patterns inspired by established travel and navigation apps, without copying proprietary UI.
- Large readable labels, clear actions and predictable navigation for a broad range of Indian users.
- Use real destination imagery where it adds value; use professional Material icons for controls and functional categories.
- No emoji as primary functional iconography.
- No microphone, voice search, speaker or audio controls.
- Never use decorative cards or symbols that obscure the main task.

## 2. Visual foundation
| Token | Value |
|---|---|
| White | #FFFFFF |
| Deep Navy | #0B3C6D |
| Primary Blue | #1565C0 |
| Light Blue | #EAF3FF |
| Light Background | #F4F7FB |
| Main Text | #172B4D |
| Secondary Text | #64748B |
| Borders | #DCE6F2 |

Baseline: 360×800dp portrait; 16dp horizontal page padding; 20–24dp section spacing; 12–16dp card padding; minimum 48dp touch targets.

## 3. Global navigation
Three primary destinations only: Home, Explore and Profile. Keep bottom navigation simple and consistent. Use focused full-screen layouts for active navigation, emergency assistance and other task-critical flows.

## 4. Home / live map
- Full-screen map is the primary surface.
- Floating location search and clear origin/destination entry.
- Show current location only with permission and valid location data.
- Prominent Find Routes action.
- Avoid redundant quick-action grids and excessive stacked cards.
- No “How would you like to travel?” prompt unless a genuine mode choice is required.

## 5. Search and routing experience
Provide clear search suggestions, destination confirmation, optional per-trip context, route alternatives, route details and route preview. Show only provider-returned alternatives, up to three. Display ETA and distance from the routing engine and disclose unavailable live traffic.

## 6. Explore experience
Explore Home should prioritize discoverable categories and useful destination imagery. Category Results, Destination Details and Nearby Places should have consistent image treatment, readable summaries, distance only when calculated, and clear directions actions. Avoid overcrowding the Explore landing page.

## 7. Reporting and safety
Use professional icons for report categories and clear labels. Distinguish community reports from provider-backed information. Show submission states honestly. Emergency actions must be prominent, explicit and user initiated; simulated functionality must be labelled.

## 8. Accessibility and Indian-user usability
Use plain English, familiar terminology, strong contrast, readable typography, large touch targets, clear empty/error/loading states, and avoid relying on color alone. Keep critical actions understandable without technical knowledge.

## 9. Interaction standards
Use consistent button hierarchy, confirmation for destructive actions, validation near the relevant field, loading feedback for asynchronous work, retry paths for recoverable errors, and preserve user-entered form data after failures.

## 10. Quality bar
Every screen must have a clear purpose and primary action. Do not add features beyond the approved 28-screen scope without approval. Do not display mock data as live or verified information.

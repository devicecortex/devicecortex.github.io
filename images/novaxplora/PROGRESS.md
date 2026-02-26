# Marketing Screenshots - Progress

## Goal
Create compelling marketing screenshots for DeviceCortex.com by populating NovaXplora with realistic test data and capturing polished screenshots.

## Status: COMPLETE

All 10 screenshots captured and saved to this directory.

## Phase 1: Create Test Data — COMPLETE

### 1a. Dreams — DONE
All 4 dreams created with items:
- **Mediterranean Dream** — 5 items (Santorini, Rome, Barcelona, Amalfi Coast, Dubrovnik)
- **Asia Pacific Adventure** — 5 items (Tokyo, Bali, Ha Long Bay, Angkor Wat, Queenstown NZ)
- **Nordic Exploration** — 4 items (Reykjavik, Norwegian Fjords, Copenhagen, Finnish Lapland)
- **South American Escape** — 4 items (Machu Picchu, Patagonia, Buenos Aires, Galapagos Islands)

### 1b. Plans — DONE
- **Mediterranean Summer 2026** — 15 destinations (Barcelona, Rome, Santorini, Dubrovnik + activities, lodging, travel)
- **Tokyo & Kyoto Spring 2026** — 6 destinations
- **Weekend in Paris** — 5 destinations

### 1c. Photos — DONE
13 photos uploaded from Unsplash via Lorem Picsum (6 Mediterranean, 4 Tokyo, 3 Paris).
See `PHOTO-CREDITS.md` for photographer attribution and Unsplash links.

### 1d. Friends & Social — DONE
2 friend requests sent (End2 Test, E2E Test)

### 1e. Recommendations — DONE
Istanbul, Turkey recommendation generated via AI

## Phase 2: Capture Screenshots — COMPLETE

### Desktop (1440x900)
| # | Screen | Filename | Size |
|---|--------|----------|------|
| 1 | Dreams overview | `dreams-overview.png` | 133 KB |
| 2 | Plan itinerary | `plan-itinerary.png` | 140 KB |
| 3 | Plan map view | `plan-map.png` | 706 KB |
| 4 | Plan media | `plan-photos.png` | 507 KB |
| 5 | Photo gallery | `photos-gallery.png` | 670 KB |
| 6 | Recommendations | `recommendations.png` | 184 KB |
| 7 | Friends | `friends.png` | 84 KB |

### Mobile (500x844)
| # | Screen | Filename | Size |
|---|--------|----------|------|
| 8 | Mobile dream | `dreams-mobile.png` | 87 KB |
| 9 | Mobile plan | `plan-mobile.png` | 83 KB |
| 10 | Mobile nav | `nav-mobile.png` | 445 KB |

## Bug Encountered During Setup
**RangeError: Invalid time value** in `PlanTimeline.tsx` `formatDateHeader` — the function doesn't guard against null/invalid date strings. Adding a destination with a date that doesn't parse correctly crashes the entire Plans page.

**Fix applied** to 3 files:
- `ui/src/components/plan/PlanTimeline.tsx` — Added null/NaN guard
- `ui/src/components/PlanDayGroup.tsx` — Added null/NaN guard
- `ui/src/components/attachments/TimelineDateGroup.tsx` — Added null/NaN guard

All tests pass after fix.

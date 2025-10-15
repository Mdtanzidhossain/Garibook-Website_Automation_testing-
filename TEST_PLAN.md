# Test Plan — Garibook Website (Playwright + Python)

Aligned with ISO/IEC/IEEE 29119 / IEEE 829

Objectives:
- Validate Trip Booking (Car Rental → One Way → Sedan → OTP Login → Pickup/Drop/Datetime → Request).
- Validate site-wide smoke (top nav, profile, My Trip, tabs).

Approach:
- Playwright async; explicit waits for dropdowns/modals; resilient OTP parsing; screenshots + CSV.

Environment:
- URL: http://fe.garibook.com/ • Browser: Chromium (baseline) • Viewport: 1280×800 / 1500×800 • OS: Windows.

Entry/Exit:
- Entry: FE reachable, OTP banner available; selectors stable.
- Exit: Booking and smoke green; CSV + videos captured; no Sev-1 open.

Risks:
- Brittle XPaths in smoke; slow suggestions; OTP banner format changes; optional profile modal.

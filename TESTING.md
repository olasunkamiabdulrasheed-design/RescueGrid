# Testing

## What was actually run
Automated DOM tests using **jsdom** (a simulated browser that executes the page's real JavaScript and records script errors): `tests/flows-basic.test.js` (25 checks) and `tests/flows-extended.test.js` (25 checks). Final result: **50/50 passed, 0 script errors**. `node --check` on the inline script passed.

Covered: all 8 navigation destinations; scenario stages advancing in order Baseline→Watch→Warning→Response and stopping at Response; reset with confirmation; stage review and locked future stages; sensor values at the final stage (4.7 m, Critical); recommended-actions content at Baseline and Response; incident create, validation, edit, status change, acknowledge, resolve, delete with cancel and confirm; search and empty state; map select, popup, zoom, layer toggle and severity filter (these two only confirm they run without error); shelter occupancy edit, capacity warning and supply coverage chart presence; report validation keeping typed values, report confirmation, new incident appearing in the list; SafeRoute limitation text and hazards; notifications; guided demo; mobile menu toggle; localStorage write.

## Not tested
- **No real browser** was available: no visual rendering, screenshots, colour contrast measurement, real touch or keyboard focus behaviour, or console check in Chrome/Firefox/Safari.
- **Responsive layouts** (desktop, tablet, phone) were not viewed; only the mobile menu toggle logic was tested.
- Layer toggles and severity filters were not verified to change which markers are drawn.
- Persistence across a real page reload was not tested.
- No accessibility audit, screen reader test or cross-browser test.

## Known limitations
Schematic map, scripted sensor data and preset routes. All data is simulated.

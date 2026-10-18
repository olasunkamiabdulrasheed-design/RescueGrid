# RescueGrid — See the risk. Coordinate the response.
**IEEE Technothon 2026 · Designing for Disaster**

## Problem
During floods, information on hazards, blocked roads, shelters and supplies is scattered, so coordinators struggle to see where risk is highest and what to do first.

## Solution
RescueGrid puts simulated water-level sensors, community reports, a hazard map, shelter capacity and supply gaps in one command-center interface, and turns them into prioritised **Recommended next actions**.

## Key features
Command dashboard; hazard map with layers, filters, zoom and popups; sensor monitoring with thresholds; full incident workflow; shelter and supply management with shortage detection; SafeRoute with reported hazards; community reporting with validation; a deterministic four-stage flood scenario simulator with stage review and "why it matters" explanations; guided demo.

## Technical implementation
A single self-contained HTML/CSS/JavaScript file with shared state, `localStorage` persistence and inline SVG for the map and charts. No backend, accounts, paid APIs or dependencies. 50 automated jsdom checks pass (see TESTING.md).

## Impact
Shows how clear information design can shorten the path from "what is happening?" to "what do we do next?" for coordinators, shelter managers and volunteers.

## Limitations
Prototype only. All sensor readings, incidents, capacities, map locations and routes are simulated and unverified. Not connected to any emergency service or real sensor. Not tested with real responders or in a real browser.

## 2-minute presentation script
1. (15s) Problem: fragmented flood information.
2. (20s) Dashboard at Baseline: calm, no action required.
3. (30s) Press Advance twice: gauges rise, hazards appear on the map, critical alert pulses.
4. (20s) Submit a community report; it shows up in Incidents.
5. (25s) Advance to Response: shelter shortages and Recommended next actions.
6. (10s) Acknowledge an incident; the dashboard updates. Note that everything is simulated.

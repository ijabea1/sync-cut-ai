# Testing Harness — SyncCut AI (UI-only)

## Goal
Add a UI-only “Demo Mode” so we can test the full product experience without a real AI backend.

## Add a Demo Mode toggle
- Add a toggle in Settings (or in the Project Editor header) called: **Demo Mode**
- When ON, the app should not require real uploads to proceed.
- Show a small badge in the editor: “Demo Mode”

## Add Demo Projects on the Dashboard
Add a section at the top of the Dashboard: **Demo Projects**
Each demo project opens directly into the Project Editor with pre-filled timeline data.

Create 6 demo projects:
1) Simple 15s — 120 BPM, few cuts
2) Fast montage 30s — 150 BPM, many cuts
3) Slow cinematic 45s — 90 BPM, sparse cuts, one big drop
4) Off-beat track — irregular beats for manual correction testing
5) Single shot — no cuts (cuts array empty)
6) Overloaded — very high number of cuts (stress test)

## Simulated “AI analysis” behavior
When a demo project opens:
- show “Analyzing beats and scene cuts…” for 2–3 seconds
- show a calm loading state (pulsing waveform skeleton)
- then render beat markers, cut markers, drop markers, and sync points

## Data structure (frontend mock)
For each demo project, create a mock analysis object including:
- durationSeconds
- tempoBpm
- beats[] (timestamps)
- videoCuts[] (timestamps)
- drops[] (timestamps)
- syncPoints[] (timestamps)

## Timeline rendering expectations
- Beats: thin ticks
- Cuts: sharper ticks
- Drops: labeled marker “DROP”
- Sync points: most prominent marker, draggable with snapping ON by default
- Legend toggles to show/hide beats/cuts/drops/sync to reduce clutter

## Export simulation
On Export:
- show a progress indicator for 3–6 seconds
- then show “Export ready” with a downloadable placeholder link
- save an “Exported” status back to the project card

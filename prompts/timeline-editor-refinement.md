# Timeline Editor Refinement — SyncCut AI

## Goal

Refine the **Project Editor timeline experience** so it feels like a **calm cinematic editing studio**: focused, responsive, and empowering.

Keep the UI minimal, but make the timeline feel “pro-grade” through clarity, microinteractions, and smart defaults.

Use:

- React + TypeScript
- Tailwind CSS + shadcn/ui
- Lovable Cloud (keep placeholders/mock data where needed)

---

# 1) Timeline Layout & Hierarchy

## Make the timeline the visual center

- Increase timeline height and presence (it should feel like the main canvas).
- Keep controls lightweight and secondary.
- Use a single central workspace layout:
  - Top: video preview (compact but clear)
  - Middle/Bottom: timeline (dominant)
  - Right: inspector panel (collapsible)

## Add a sticky timeline header

Include:

- time ruler (seconds / frames)
- zoom indicator
- snap toggle state
- playhead position readout

---

# 2) Timeline Tracks

## Add clear track separation

Create 3 stacked tracks:

1. **Video Track**
   - show scene cut markers
   - show motion intensity as a subtle “heatline” or mini curve

2. **Audio Track**
   - show waveform
   - show music energy curve (subtle overlay)

3. **Sync Track**
   - show beat markers
   - show sync points (AI-selected anchors)
   - show drop markers (chorus / drops)

Each track should have:

- track label (left)
- mute/visibility toggles (audio track)
- small “info” icon for tooltips (optional)

---

# 3) Marker System & Visual Language

## Marker Types

Implement consistent styling + legends:

- **Beat Markers**: thin tick marks
- **Scene Cut Markers**: sharper ticks with slightly more weight
- **Sync Points**: prominent markers (pill or diamond)
- **Drop Markers**: special accent marker with label (“DROP”)

## Legend + Filters

Add a small legend row above timeline:

- Beat
- Cut
- Sync
- Drop

Each should be togglable to reduce visual noise.

---

# 4) Interaction Improvements

## Drag + Snap Behavior

- Sync markers can be dragged horizontally.
- Default: snapping ON.
- Snapping targets:
  - beats first
  - then cuts (secondary snap if beats are hidden)
- When snapping happens:
  - subtle haptic-like animation (small bounce)
  - micro tooltip: “Snapped to beat 12”

## Playhead & Scrubbing

- Add a prominent playhead line across all tracks.
- Clicking anywhere in timeline moves playhead.
- Dragging playhead scrubs video preview in real time (or best-effort simulation).

## Zoom & Scroll

Provide:

- zoom slider (0.5x → 4x)
- mouse wheel zoom when holding:
  - Ctrl (Windows) / Cmd (Mac)
- horizontal scroll using trackpad/shift+wheel

Keep it smooth and stable.

---

# 5) Core Editing Tools (Minimal, MVP-friendly)

Add a compact toolbar above the timeline:

- **Select**
- **Add Sync Point**
- **Delete**
- **Split**
- **Trim In**
- **Trim Out**

Even if only Select + Add Sync Point + Delete work initially, render the full tool set as MVP scaffolding.

Tool behavior:

- Selected marker highlights.
- Delete removes selected marker.
- Add Sync Point drops a sync marker at playhead.

---

# 6) Preview Loop & “Moment Checking”

Creators need fast iteration.

Add:

- **Loop toggle**
- **Set In/Out** (loop region)
- **Loop playback** between in/out for checking transitions

Show loop region visually as a lightly shaded segment.

---

# 7) AI Feedback & Refinement Controls

In the right inspector panel:

## “AI Sync Summary” card

Show:

- detected tempo
- number of beats
- number of cuts
- number of sync anchors
- confidence meter (simple: Low/Med/High)

## “Refine Sync” controls

Buttons:

- **Regenerate Sync**
- **More Cuts on Beats** (tighten)
- **More Cinematic Drops** (emphasize drops)
- **Smoother Pacing** (reduce jumpiness)

For MVP, these can apply preset mock transformations to marker positions, but should feel real.

---

# 8) Empty States & Loading States

## When analysis is running

Replace timeline with:

- pulsing waveform skeleton
- message: “Analyzing beats and scene cuts…”
- subtext: “This usually takes under a minute.”

## When analysis complete

Show a small celebration microcopy:

- “Perfect sync achieved.”
- Secondary: “Drag markers to fine-tune.”

Keep it calm, not confetti.

---

# 9) Motion & Microinteractions

Use subtle cinematic motion:

- hover lift on key buttons
- gentle glow on selected markers
- fade-in of markers after analysis completes
- snapping animation: 150–200ms

No flashy effects. Motion should feel supportive.

---

# 10) Accessibility

- Keyboard navigation for markers:
  - Tab cycles markers
  - Arrow keys nudge selected marker (small increments)
  - Shift + Arrow nudge larger increments
- Visible focus states on timeline elements
- ARIA labels for controls and markers

---

# Acceptance Criteria

The refined Project Editor should:

- feel like a calm “studio” workspace
- make the timeline clearly the main focus
- support marker drag + snap + playhead scrubbing
- include track separation and marker legend/toggles
- include refinement controls that feel intelligent (even if mocked)

Deliver the updated UI with clean component structure and reusable timeline subcomponents.

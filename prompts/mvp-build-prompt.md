# MVP Build Prompt — SyncCut AI

## Build Objective

Generate the **MVP application structure and core UI** for SyncCut AI.

The app should allow users to:

1. Upload a video
2. Upload a music track
3. Automatically generate synced timing
4. Preview the result
5. Export the final video

Focus on building the **core user experience and layout** rather than the full AI processing pipeline.

Use:

* React
* TypeScript
* Tailwind CSS
* shadcn/ui
* Lovable Cloud for backend and storage

---

# Application Pages

Generate the following pages and routing structure.

## Landing Page

Purpose: introduce the product and allow sign-up.

Sections:

* hero section explaining automatic music sync
* simple 3-step workflow
* visual demo placeholder
* feature highlights
* call-to-action button: **Upload Your First Video**

Design tone:

cinematic, modern, minimal.

---

## Dashboard

Purpose: show user projects.

Components:

* grid of project cards
* thumbnail preview
* project status (processing, ready, exported)
* **Create New Project** button

Interactions:

Clicking a project opens the **Project Editor**.

---

## Project Editor (Core Workspace)

This is the most important page.

Layout:

```
+------------------------------------------------+
| Video Preview                                  |
|                                                |
+------------------------------------------------+
| Timeline Editor                                |
|                                                |
+------------------------------------------------+
| Controls Panel                                 |
+------------------------------------------------+
```

### Video Preview

Features:

* video player
* play/pause
* playback timeline indicator

---

### Timeline Editor

The timeline should be the **visual center of the interface**.

Display:

* waveform visualization
* beat markers
* scene cut markers
* sync markers

Interactions:

* drag sync markers
* snap markers to beats
* scrub playback

Timeline should support **zooming and scrolling**.

---

### Controls Panel

Controls include:

* offset adjustment
* trim music start
* trim music end
* regenerate sync

Buttons:

* **Auto Sync**
* **Preview**
* **Export**

---

## Export Page

Allows users to download the final result.

Export options:

* MP4 video
* WAV audio

UI components:

* export format selector
* render progress indicator
* download button

---

# Core UI Components

Generate reusable components:

* ProjectCard
* UploadDropzone
* VideoPreview
* Timeline
* BeatMarker
* SceneMarker
* SyncMarker
* ExportProgress

---

# File Upload Flow

Users should be able to upload:

* one video file
* one music file

Use a **drag-and-drop upload component**.

Display progress indicators.

After upload, show a message:

> “Analyzing video and music…”

---

# AI Processing Placeholder

For MVP purposes, simulate AI processing.

Display a loading animation with the message:

> “Analyzing beats and scene cuts…”

Then show generated markers on the timeline.

---

# Design System

Follow the design guidelines from the repository.

Emotional tone:

A calm cinematic editing studio.

Typography:

Inter font.

Color palette:

Primary: `#6C5CE7`
Accent: `#00E5FF`
Background: `#0F1115`
Secondary: `#2D3436`

Spacing:

Use an **8pt grid system**.

---

# Motion and Interaction

Animations should be subtle and supportive.

Examples:

* buttons lift slightly on hover
* markers snap smoothly to beats
* waveform pulses during analysis

Animation durations:

150–220ms.

---

# Accessibility

Ensure:

* keyboard navigation
* visible focus states
* ARIA labels for controls

---

# Expected MVP Result

The generated application should include:

* landing page
* dashboard
* project editor
* export page
* file upload workflow
* interactive timeline UI
* placeholder AI sync behavior

This MVP should demonstrate the **core concept of automatic music synchronization for video editing**.

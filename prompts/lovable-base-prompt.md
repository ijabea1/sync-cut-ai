## 💡 Lovable App Prompt: SyncCut AI

---

# Mission

Build a **web-based AI video editing tool** that automatically synchronizes music with video edits.

Users upload a video and a music track. The AI analyzes **scene cuts, motion intensity, beats, and drops**, then aligns the music to visual moments automatically.

The experience should feel **calm, cinematic, intelligent, and effortless — like working inside a focused creative studio.**

Creators should feel **in control and creatively empowered**, not overwhelmed.

---

# Project Name

**SyncCut AI**

---

# Target Audience

### Short-Form Creators

Platforms:

* TikTok
* YouTube Shorts
* Instagram Reels

Needs:

* fast editing
* cinematic timing
* minimal technical friction

---

### Content Teams

Examples:

* social media teams
* marketing agencies
* brand studios

Needs:

* high production speed
* consistent visual quality

---

### Professional Editors

Use cases:

* quick social edits
* music syncing for rough cuts
* previsualization before full editing

---

# Core Product Experience

The primary workflow:

1. Upload video
2. Upload music
3. AI analyzes both
4. AI generates synced preview
5. Optional timeline adjustments
6. Export final video

The system should reduce manual editing work from **10–30 minutes to seconds**.

---

# Core Features

## AI Beat Detection

Analyze uploaded music to detect:

* beats
* tempo
* energy curves
* chorus drops

Example output:

Drop detected at **0:37**

---

## Video Scene Detection

Analyze uploaded video to detect:

* scene cuts
* motion intensity
* pacing changes

Example:

15 scene cuts detected in a 20-second montage.

---

## Smart Beat Alignment

Automatically map visual events to musical beats.

Rules:

* cuts align to beats
* major moments align to drops
* pacing matches rhythm

Result: cinematic timing.

---

## Music Restructuring

When music length does not match video length, the AI can:

* trim intros
* loop sections
* shorten breakdowns
* create fade endings

Outcome:

music perfectly matches video duration.

---

## Interactive Timeline Editor

Workspace shows:

* video preview
* waveform
* beat markers
* scene cut markers
* sync points

Users can:

* drag beat markers
* adjust sync points
* trim start and end
* preview playback instantly

The timeline should be **the visual center of the application**.

---

## One-Click Export

Export formats:

* MP4 video with synced audio
* WAV edited soundtrack
* project file for editing software

Export UI should show:

* format selector
* render progress
* download link

---

# Pages & App Flow

## Landing Page

Purpose:

Explain the product and allow creators to start quickly.

Sections:

* Hero explaining automatic music syncing
* Visual demo of beats aligning to cuts
* Feature highlights
* Creator testimonials
* Primary CTA: **Upload Your First Video**

---

## Dashboard

Displays user projects.

Components:

* project cards
* thumbnail previews
* processing status
* create project button

Primary CTA:

**Create New Project**

---

## Project Editor

Main editing workspace.

Layout:

Left → video preview
Bottom → large timeline editor
Right → adjustment controls

Focus on **creative flow state**.

---

## Export Page

Allows users to:

* select export format
* render final video
* download completed file

---

## Settings & Account

Manage:

* profile
* billing
* upload limits
* export preferences

---

# Tech Stack

Frontend

* Vite
* TypeScript
* React
* Tailwind CSS
* shadcn/ui

Backend & Storage

Lovable Cloud

Auth

* Email/password
* Google OAuth (optional)

Processing Services

* Python FastAPI workers
* FFmpeg media processing
* audio analysis using Librosa
* video analysis using OpenCV and PySceneDetect

---

# Design Guidelines

## Emotional Thesis

Feels like **a calm cinematic editing studio — focused, creative, and effortless.**

The interface should support creative work without overwhelming the user.

Kindness in design means removing friction while respecting the user’s attention and emotional state.

---

## Typography

Primary typeface:

**Inter**

Hierarchy:

* H1 — 40px
* H2 — 28px
* H3 — 22px
* Body — 16px
* Caption — 13px

Line height:

1.6

---

## Color System

Primary
`#6C5CE7`

Accent (beats and sync markers)
`#00E5FF`

Background
`#0F1115`

Secondary
`#2D3436`

Success
`#00D084`

Error
`#FF5A5F`

All colors meet **WCAG AA+ contrast requirements**.

---

## Layout & Spacing

Use an **8-point grid system**.

Spacing scale:

* 8px
* 16px
* 24px
* 32px
* 48px

Layout principles:

* single central workspace
* large timeline editor
* minimal visual clutter
* focus on creativity

---

## Motion & Interaction

Motion style:

smooth, subtle, cinematic.

Durations:

* hover → 150ms
* modal → 220ms
* timeline drag → 200ms

Examples:

* buttons lift slightly on hover
* beat markers snap to beats
* waveform pulses while analyzing

Motion should feel **supportive rather than distracting**.

---

## Voice & Microcopy

Tone:

confident
friendly
encouraging

Examples:

Onboarding
“Upload your video. We’ll handle the timing.”

Success
“Perfect sync achieved.”

Error
“Something didn’t work. Let’s try again.”

---

## Accessibility

Ensure:

* keyboard navigation
* ARIA labels
* visible focus states
* WCAG AA+ contrast compliance

---

# Optional AI Assistant

An AI assistant inside the editor can provide suggestions.

Personality:

**calm creative mentor**

Example suggestions:

* “Try aligning this scene with the chorus drop.”
* “This section may feel stronger with a faster tempo.”

---

# Design Integrity Review

This product combines **advanced AI analysis with a calm creative workspace**.

The dark cinematic interface highlights music structure and video timing while reducing distractions.

The goal is to make creators feel like they are **collaborating with an intelligent editing partner rather than struggling with a complex editing tool.**

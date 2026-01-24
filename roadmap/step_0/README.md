# Phase 0 — Orientation (Media Streaming Roadmap)

**Objective:**  
Stop treating media files as black boxes.  
By the end of this phase, you should be able to *read* a media file and explain its basic properties.

**Estimated time:** 1–2 hours  
**Learning style:** Hands-on, observation first, theory later

---

## Workspace Setup

Create the following structure:

```
media-streaming/
└── phase-0/
    ├── inputs/
    └── notes.md
```

Place **at least 3 different video files** inside `inputs/`.

Suggested variety:
- Phone-recorded video
- Screen recording
- Downloaded clip
- Different resolutions or sources

---

## Step 0.1 — Verify Tools

Run the following commands:

```bash
ffmpeg -version
ffprobe -version
```

✔️ Both commands should work  
✔️ You should see `libx264` listed in FFmpeg features

If this fails, **fix installation before continuing**.

---

## Step 0.2 — Inspect Media Files

For each file in `inputs/`, run:

```bash
ffprobe -hide_banner inputs/yourfile.mp4
```

In `notes.md`, extract and write down **only the following fields**.

### Video Stream
- Codec (e.g. h264)
- Profile (Baseline / Main / High)
- Resolution
- Frame rate
- Bitrate (if present)

### Audio Stream
- Codec (AAC, Opus, etc.)
- Channels (mono / stereo)
- Sample rate
- Bitrate

### Container
- Duration
- Overall bitrate

Do **not** google definitions yet.  
Just observe and record facts.

---

## Step 0.3 — Observation Questions

In `notes.md`, answer briefly:

1. Which file has the highest bitrate?
2. Does the highest bitrate file look the best?
3. Are all H.264 files actually the same?
4. Which file would stream better on a poor connection?

There are no wrong answers at this stage.

---

## Step 0.4 — First Controlled Experiment (Remuxing)

Pick **one** input file and run:

```bash
ffmpeg -i ../../assets/<file>.mp4 -c copy inputs/<file>_remuxed.mp4
```

Now compare:
- File size
- `ffprobe` output
- Playback behavior

In `notes.md`, answer:

- What changed?
- What stayed exactly the same?

This step is foundational.

---

## Stop Here (Important)

Do **not**:
- Re-encode video
- Change codec parameters
- Study codec theory yet

The goal of Phase 0 is **familiarity, not mastery**.

---

## Completion Criteria

Phase 0 is complete when:
- You inspected at least 3 files
- You filled `notes.md`
- You performed the remux experiment

Once done, proceed to **Phase 1 — Encoding Fundamentals**.


# Media Streaming Engineer – Practical, Balanced Roadmap

**Profile target:** Remote-friendly Media / Streaming Engineer  
**Learning style:** Hands-on first, theory on demand  
**Time commitment:** ~6–8 hours per week  
**Duration:** ~5–6 months

---

## Philosophy

This roadmap prioritizes **doing before reading**.  
Theory is introduced *only when practice demands it*.

You will:
- Build real streaming pipelines
- Break video on purpose
- Measure quality and latency
- Develop end-to-end intuition

---

## Tooling (Baseline)

You will use these throughout the roadmap:

- FFmpeg / ffprobe
- mpv or VLC
- Local HTTP server (Python, Node, etc.)
- Wireshark (later phases)
- Shell + text editor

---

## Phase 0 – Orientation (Week 1)

**Goal:** Stop treating media files as black boxes.

### Tasks
- Install FFmpeg and ffprobe
- Inspect multiple video files
- Identify codec, bitrate, resolution, GOP

### Deliverables
- Notes on at least 3 different video files
- ffprobe output interpretation

---

## Phase 1 – Encoding Fundamentals (Weeks 2–4)

**Goal:** Understand how encoding decisions affect quality, size, and performance.

### Hands-on Project
Encode the same video using:
- Different CRF values
- Different resolutions
- Different GOP sizes
- CBR vs CRF

Compare:
- File size
- Visual artifacts
- Decode smoothness

### Minimal Theory
- I / P / B frames
- GOP structure
- CRF vs CBR

### Deliverables
- Encoding comparison table
- Written conclusions (“why this looks better/worse”)

---

## Phase 2 – Containers & Formats (Week 5)

**Goal:** Understand why containers matter for streaming.

### Hands-on Project
- Remux streams into MP4, fMP4, TS
- Test faststart vs non-faststart
- Inspect container metadata

### Minimal Theory
- Codec vs container
- Fragmentation
- CMAF basics

### Deliverables
- Notes explaining when to use each container

---

## Phase 3 – Adaptive Bitrate Streaming (Weeks 6–9)

**Goal:** Build a real ABR streaming pipeline.

### Hands-on Project
- Create a multi-rendition encode (1080p / 720p / 480p)
- Generate HLS playlists
- Serve via HTTP
- Test playback and quality switching

### Focus Areas
- Segment duration
- Manifest structure
- Client-driven adaptation

### Minimal Theory
- ABR logic
- Buffering vs rebuffering
- Startup delay

### Deliverables
- Working HLS stream
- Diagram of ABR flow

---

## Phase 4 – Bitrate Ladders & Quality Metrics (Weeks 10–11)

**Goal:** Learn how professionals choose bitrates.

### Hands-on Project
- Design your own bitrate ladder
- Encode and test it
- Compare visual quality

(Optional)
- Measure VMAF or similar metrics

### Minimal Theory
- Resolution vs bitrate trade-offs
- Mobile vs desktop considerations
- Perceptual quality

### Deliverables
- Custom bitrate ladder with justification

---

## Phase 5 – Live Streaming & Latency (Weeks 12–14)

**Goal:** Understand live pipelines and latency sources.

### Hands-on Project
- Build a live RTMP → HLS pipeline
- Measure glass-to-glass latency
- Switch to Low-Latency HLS

### Minimal Theory
- Encoder buffering
- Segmenting impact on latency
- Live vs VOD trade-offs

### Deliverables
- Latency comparison notes
- Identified bottlenecks

---

## Phase 6 – Real-Time Streaming (WebRTC) (Weeks 15–17)

**Goal:** Understand real-time media behavior.

### Hands-on Project
- Run a WebRTC demo
- Inspect ICE candidates
- Observe bitrate adaptation
- Simulate packet loss

### Minimal Theory
- UDP vs TCP
- ICE / STUN / TURN
- Congestion control

### Deliverables
- WebRTC flow explanation
- Notes on packet loss behavior

---

## Phase 7 – Infrastructure & Failure Modes (Weeks 18–20)

**Goal:** Think like a production engineer.

### Hands-on Project
- Simulate bandwidth drops
- Introduce latency and packet loss
- Observe player reactions

### Minimal Theory
- QoE vs QoS
- Rebuffering vs startup delay
- Monitoring importance

### Deliverables
- Failure scenarios and mitigation ideas

---

## End State – What You Should Be Able to Do

- Design encoding profiles intentionally
- Explain buffering and latency issues
- Build VOD and live streaming pipelines
- Reason about quality trade-offs
- Communicate with video, infra, and product teams

---

## Optional Specialization (Post-Roadmap)

- Encoder tuning (x264/x265/AV1)
- Player-side ABR algorithms
- CDN and edge optimization
- Large-scale live events
- AI-assisted encoding and quality analysis

---

## Final Note

This roadmap is designed to:
- Be compatible with a full-time job
- Produce tangible portfolio artifacts
- Prepare you for **remote streaming engineering roles**

Treat every project as something you could explain in an interview.

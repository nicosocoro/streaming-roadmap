Video 1:

```
ffprobe -hide_banner http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4

----

Input #0, mov,mp4,m4a,3gp,3g2,mj2, from 'http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4':
  Metadata:
    major_brand     : mp42
    minor_version   : 0
    compatible_brands: isomavc1mp42
    creation_time   : 2010-01-10T08:29:06.000000Z
  Duration: 00:09:56.47, start: 0.000000, bitrate: 2119 kb/s
  Stream #0:0(und): Audio: aac (LC) (mp4a / 0x6134706D), 44100 Hz, stereo, fltp, 125 kb/s (default)
    Metadata:
      creation_time   : 2010-01-10T08:29:06.000000Z
      handler_name    : (C) 2007 Google Inc. v08.13.2007.
      vendor_id       : [0][0][0][0]
  Stream #0:1(und): Video: h264 (High) (avc1 / 0x31637661), yuv420p, 1280x720 [SAR 1:1 DAR 16:9], 1991 kb/s, 24 fps, 24 tbr, 24k tbn, 48 tbc (default)
    Metadata:
      creation_time   : 2010-01-10T08:29:06.000000Z
      handler_name    : (C) 2007 Google Inc. v08.13.2007.
      vendor_id       : [0][0][0][0]
```

Video Stream
* **Codec:** h264
* **Profile (Baseline / Main / High):** high
* **Resolution:** 1280x720
* **Frame rate:** 24 fps
* **Bitrate (if present):**: 1991 kb/s

Audio Stream
* **Codec (AAC, Opus, etc.):** aac (lc)
* **Channels (mono / stereo):** stereo (2)
* **Sample rate:** 44100 hz
* **Bitrate:** 125 kb/s

Container
* **Container** mp4 (mov,mp4,m4a,3gp,3g2,mj2)
* **Duration:** 00:09:56.47
* **Overall bitrate:** 2119 kb/s

---

Video 2:

```
ffprobe -hide_banner http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/VolkswagenGTIReview.mp4

---

Input #0, mov,mp4,m4a,3gp,3g2,mj2, from 'http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/VolkswagenGTIReview.mp4':
  Metadata:
    major_brand     : mp42
    minor_version   : 0
    compatible_brands: isomavc1mp42
    creation_time   : 2010-05-26T16:41:36.000000Z
  Duration: 00:09:53.80, start: 0.000000, bitrate: 589 kb/s
  Stream #0:0(und): Audio: aac (LC) (mp4a / 0x6134706D), 44100 Hz, stereo, fltp, 109 kb/s (default)
    Metadata:
      creation_time   : 2010-05-26T16:41:36.000000Z
      handler_name    : (C) 2007 Google Inc. v08.13.2007.
      vendor_id       : [0][0][0][0]
  Stream #0:1(und): Video: h264 (Constrained Baseline) (avc1 / 0x31637661), yuv420p, 480x270 [SAR 1:1 DAR 16:9], 477 kb/s, 29.97 fps, 29.97 tbr, 30k tbn, 59.94 tbc (default)
    Metadata:
      creation_time   : 2010-05-26T16:41:36.000000Z
      handler_name    : (C) 2007 Google Inc. v08.13.2007.
      vendor_id       : [0][0][0][0]
```

Video Stream
* **Codec:** h264
* **Profile (Baseline / Main / High):** baseline
* **Resolution:** 480x270
* **Frame rate:** 29.97 fps
* **Bitrate (if present):** 477 kb/s

Audio Stream
* **Codec (AAC, Opus, etc.):** aac
* **Channels (mono / stereo):** stereo (2)
* **Sample rate:** 44100 hz
* **Bitrate:** 109 kb/s

Container
* **Container**: mp4 (mov,mp4,m4a,3gp,3g2,mj2)
* **Duration:** 00:09:53.80
* **Overall bitrate:** 589 kb/s

---

Video 3:

```
ffprobe -hide_banner ./assets/simulator_screen.mp4 

---

Input #0, mov,mp4,m4a,3gp,3g2,mj2, from './assets/simulator_screen.mp4':
  Metadata:
    major_brand     : qt  
    minor_version   : 0
    compatible_brands: qt  
    creation_time   : 2026-01-18T22:13:38.000000Z
  Duration: 00:00:11.37, start: 0.000000, bitrate: 5950 kb/s
  Stream #0:0(und): Video: h264 (High) (avc1 / 0x31637661), yuv420p(tv, bt709/unknown/unknown), 750x1334, 6114 kb/s, 20.34 fps, 600 tbr, 600 tbn, 1200 tbc (default)
    Metadata:
      creation_time   : 2026-01-18T22:13:38.000000Z
      handler_name    : Core Media Video
      vendor_id       : [0][0][0][0]
      encoder         : H.264
```

Video Stream
* **Codec:** h264
* **Profile (Baseline / Main / High):** high
* **Resolution:** 750x1334
* **Frame rate:** 20.34 fps
* **Bitrate (if present):** 6114 kb/s

Audio Stream

- Not apply

Container
* **Container** mp4 (mov,mp4,m4a,3gp,3g2,mj2)
* **Duration:**  00:00:11.37
* **Overall bitrate:** 5950 kb/s

Video 4 (video 3 remuxed):

```
ffprobe -hide_banner ./assets/simulator_screen_remuxed.mp4 

---

Input #0, mov,mp4,m4a,3gp,3g2,mj2, from './assets/simulator_screen_remuxed.mp4':
  Metadata:
    major_brand     : qt  
    minor_version   : 0
    compatible_brands: qt  
    creation_time   : 2026-01-18T22:13:38.000000Z
  Duration: 00:00:11.37, start: 0.000000, bitrate: 5950 kb/s
  Stream #0:0(und): Video: h264 (High) (avc1 / 0x31637661), yuv420p(tv, bt709/unknown/unknown), 750x1334, 6114 kb/s, 20.34 fps, 600 tbr, 600 tbn, 1200 tbc (default)
    Metadata:
      creation_time   : 2026-01-18T22:13:38.000000Z
      handler_name    : Core Media Video
      vendor_id       : [0][0][0][0]
      encoder         : H.264
```

Video Stream
* **Codec:** h264
* **Profile (Baseline / Main / High):** high
* **Resolution:** 750x1334
* **Frame rate:** 20.34 fps
* **Bitrate (if present):** 6114 kb/s

Audio Stream

- Not apply

Container
* **Container** mp4 (mov,mp4,m4a,3gp,3g2,mj2)
* **Duration:**  00:00:11.37
* **Overall bitrate:** 5950 kb/s

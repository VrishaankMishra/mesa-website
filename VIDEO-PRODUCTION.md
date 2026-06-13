# MeSA 2.0 — Demo Video Production Guide

How to actually capture footage that looks professional, with the gear you already have.
Goal: clean, well-lit, well-mic'd clips that cut together into the videos in `YOUTUBE.md`.

---

## 1. Gear (you have most of this)
- **Camera:** a phone on a tripod shoots great 1080p/4K. Lock exposure + focus (tap-and-hold).
- **Second angle:** the webcam feed itself (screen-recorded) is your "what MeSA sees" angle.
- **Audio:** the USB mic close to the speaker, or a phone lav. Record MeSA's voice cleanly —
  don't rely on camera audio across the room.
- **Light:** shoot near a window or add one cheap softbox/lamp. Avoid overhead-only (shadows).
- **Stability:** tripod or books. No handheld for product shots.

## 2. Set & staging
- Neutral, uncluttered background (a plain wall, a clean table). The minimal brand = minimal set.
- The "medication station": fixed camera mount, tray, 3–5 labeled bottles, tape marks for
  the 0.5/1.0/1.5 m distances (you already have this from the capture rig).
- For fall scenes: **cushions/mattress on the floor, always.** Put the
  "assistive aid, not a medical device" line on screen during this segment.

## 3. Screen capture (the "what MeSA sees" shots)
- **macOS:** ⌘⇧5 → record selection; or OBS for higher quality + cursor highlight.
- Record at the app's native resolution; capture the detection window, posture overlay, and
  the Streamlit dashboard separately so you can cut between them.
- For the dashboard, zoom the browser to ~125% so text is legible on mobile.
- Use the `--echo` flags (`pose_live.py --echo`, `voice_loop.py --echo`) when you want
  on-screen text instead of relying on room audio.

## 4. Shot list (capture all of these, then edit)
| Clip | How |
|------|-----|
| Hero / beauty shots | Robot on table, slow pans, push-ins. 3–4 angles, 10s each. |
| Detection | Screen-record `detect_live.py` with each bottle, then an unknown bottle. |
| Dose logging | Two angles: hand removing/returning the bottle + the dashboard updating. |
| Fall | Wide shot of staged lying on cushions; capture MeSA's spoken check-in audio. |
| Voice | Person + robot in frame; record each command and reply cleanly; add caption overlays. |
| Escalation | Reuse the fall clip; screen-record the phone receiving the ntfy push. |
| Build log | The 30-second weekly clips you already record per the operating rhythm. |

Capture **more than you need** and in **takes** (3 tries each) — editing is where it gets good.

## 5. Audio & narration
- Record voiceover separately in a quiet room (phone Voice Memos is fine); read from the
  `YOUTUBE.md` script. Keep it calm and unhurried.
- MeSA's own TTS lines: capture from the speaker, or re-record via `pyttsx3` directly to a file.
- Add subtle royalty-free background music low in the mix (−18 to −24 dB under VO).
  Sources: YouTube Audio Library, Pixabay. Avoid anything dramatic.

## 6. Editing
- **Tools:** CapCut or DaVinci Resolve (both free), or iMovie for a quick cut.
- **Pace:** cut on the action; no clip longer than ~5s without a change. Trim every "um".
- **Lower-thirds & captions:** label each demo ("01 · Detection"), use the brand fonts
  (Fraunces titles, Inter body), ink-on-paper. Burn in captions or upload an .srt.
- **Title cards:** white/paper background, big Fraunces word. Match the website.
- **Color:** keep it natural; a light, slightly warm grade fits the brand.

## 7. Export settings
- **Resolution:** 1080p minimum (3840×2160 if you shot 4K).
- **Frame rate:** match your capture (24 or 30 fps; keep it consistent).
- **Codec/container:** H.264, MP4. Bitrate ~16 Mbps (1080p) / ~40 Mbps (4K).
- **Audio:** AAC, 320 kbps, normalized to about −14 LUFS (YouTube's target).

## 8. Accessibility & polish
- Always provide captions (auto-generate, then **correct** them — fix "MeSA", med names).
- Don't conirm medical efficacy on camera; keep the assistive-aid framing.
- Thumbnails: shoot one clean high-res still per video for the branded thumbnail grid.

## 9. Minimal pipeline if you're short on time
1. Screen-record the 5 demos with `--echo`. 2. Shoot 4 beauty clips on a phone.
3. Record one VO from the script. 4. Drop into CapCut, add title cards + captions, export 1080p.
That alone yields the main demo + five deep-dives.

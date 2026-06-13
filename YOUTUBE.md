# MeSA 2.0 — YouTube Channel & Content Plan

Everything to launch the channel and publish a professional demo series. (You'll create the
channel and upload — these are the assets, scripts, and metadata to make it look intentional.)

---

## 1. Channel setup

- **Channel name:** `MeSA Robotics` (or `Vrishaank Mishra` if you want a personal-portfolio channel).
- **Handle:** `@mesarobotics`
- **Avatar:** the `assets/favicon.svg` mark on paper, exported to 800×800 PNG.
- **Banner (2560×1440, safe area 1546×423):** ink-on-paper, wordmark + tagline
  "Right medication. On time. Safe at home." Keep it minimal — lots of whitespace.
- **About / description:**
  > MeSA 2.0 is a tabletop assistive robot that recognizes medications, tracks doses,
  > detects falls, and alerts a caregiver — built end-to-end on a Raspberry Pi.
  > An assistive aid, not a medical device.
- **Links:** website, GitHub.
- **Sections / playlists:** (1) *MeSA 2.0 — The Robot* (main demo + features), (2) *Build Log*
  (weekly progress clips), (3) *Deep Dives* (technical explainers).
- **Defaults:** upload in 1080p+ (4K if you have it), add cards/end screens, turn on captions.

---

## 2. Publishing order (release like a launch, not a dump)

1. **Teaser (15–30s)** — release first to seed the channel.
2. **Main demo (3–4 min)** — the flagship. Pin it; embed on the website.
3. **Five feature deep-dives (60–120s each)** — one per capability, released ~2–3 days apart.
4. **Build log montage (2–3 min)** — from the weekly 30s clips (the plan's operating rhythm).
5. **Technical explainer (5–8 min, optional)** — architecture / how the decision engine works.

Consistent thumbnail system: ink-on-paper, big Fraunces title word (e.g. "DETECTION"),
the feature number `01`–`05`, and one screenshot. Same layout every time = a branded grid.

---

## 3. The main demo — full script (3–4 min)

> Narration is calm and factual. Each demo segment matches a Definition-of-Done demo.
> `[B-ROLL]` = what's on screen. Keep cuts tight; no dead air.

**0:00 — Cold open (10s)**
`[B-ROLL: the robot on a table; a hand reaches for a pill bottle; MeSA's voice plays.]`
> "This is MeSA — a tabletop robot that helps someone living alone take the right
> medication, on time, and stay safe if they fall."

**0:10 — Title card (3s)** — wordmark + tagline on paper.

**0:13 — The problem (20s)**
`[B-ROLL: a cluttered counter of pill bottles; a calendar.]`
> "Missed doses, the wrong pill, and unwitnessed falls are the most common — and most
> dangerous — things that go wrong at home. MeSA watches quietly, and only speaks up when
> it matters. Everything runs offline, on a single Raspberry Pi."

**0:33 — Demo 1 · Detection (30s)**
`[B-ROLL: live camera with detection boxes; show 3–4 bottles labeled; then an unknown bottle.]`
> "First, it recognizes medications. Each bottle is identified in real time… and if it sees
> one it doesn't recognize, it flags a possible wrong medication."

**1:03 — Demo 2 · Dose logging (30s)**
`[B-ROLL: hand removes a bottle, waits, returns it; cut to dashboard showing the 'taken' event.]`
> "When a bottle is taken and returned, MeSA logs it — with a timestamp — to a dashboard a
> caregiver can check from their phone."

**1:33 — Demo 3 · Fall detection (35s)**
`[B-ROLL: person stands, sits, then lies down on cushions; on-screen label changes; check-in plays.]`
> "It also understands posture — standing, sitting, lying. If someone stays down too long…"
> `[MeSA: "Are you okay? I noticed you've been lying down."]`

**2:08 — Demo 4 · Voice (35s)**
`[B-ROLL: person speaks to the robot; show captions of each command + reply.]`
> "You can just ask." — "MeSA, what's my next medication?" / "Did I take my vitamin D?" /
> "MeSA, call for help." Each answered out loud, hands-free.

**2:43 — Demo 5 · Escalation (30s)**
`[B-ROLL: fall with no response; phone receives a notification; then a caregiver alert.]`
> "And if there's no response, MeSA escalates — a spoken check-in, then a phone
> notification, then a caregiver alert."

**3:13 — Close (20s)**
`[B-ROLL: robot on table, slow push-in; cut to wordmark.]`
> "Medication safety and fall awareness — private, offline, and affordable. MeSA 2.0.
> Code and build notes are linked below. It's an assistive aid, not a medical device."

**End screen (5s):** subscribe + the detection deep-dive video.

---

## 4. Feature deep-dives (60–120s each) — beats

Same structure each: hook (5s) → what it does (10s) → live demo (40–70s) → one technical
detail (15s) → "next: <feature>" (5s).

1. **Detection** — hook: "How does a $35 computer know your medication?" Show training data,
   live boxes, the unknown-bottle path. Detail: YOLOv8 fine-tuned on a custom dataset.
2. **Dose logging** — hook: "Did I already take that?" Show remove/return → dashboard. Detail:
   debounced state machine so a hand passing over doesn't false-trigger.
3. **Fall detection** — hook: "It knows if you've fallen." Staged lying demo + check-in. Detail:
   posture from pose-keypoint geometry; **cushions only; assistive aid disclaimer on screen.**
4. **Voice** — hook: "No app. No internet. Just ask." Four commands. Detail: fully offline STT/TTS.
5. **Escalation** — hook: "What happens if no one answers?" Show L1→L2→L3. Detail: a state
   machine with timed escalation; caregiver gets a push.

---

## 5. Titles, descriptions, tags

**Title formulas** (clear > clever, for search):
- Main: `MeSA 2.0 — A Raspberry Pi Robot That Keeps You Safe at Home (Full Demo)`
- Detection: `Teaching a Raspberry Pi to Recognize Medications (MeSA 2.0)`
- Fall: `Real-Time Fall Detection on a Raspberry Pi — MeSA 2.0`
- Voice: `An Offline Voice Assistant for Medication Safety — MeSA 2.0`
- Escalation: `What Happens When No One Answers? MeSA's Caregiver Escalation`

**Description template:**
```
MeSA 2.0 is a tabletop assistive robot that recognizes medications, tracks whether they've
been taken, detects falls, and alerts a caregiver — all running offline on a Raspberry Pi 5.

In this video: <one line>

00:00 Intro
00:33 Medication detection
01:03 Dose logging
01:33 Fall detection
02:08 Voice commands
02:43 Caregiver escalation

🔗 Code: https://github.com/VrishaankMishra/mesa-ai-robot
🔗 Website: <site URL>

Built by Vrishaank Mishra. MeSA is an assistive aid, not a medical device.
#raspberrypi #robotics #computervision #yolov8 #assistivetech
```

**Tags:** raspberry pi, robotics, computer vision, yolov8, mediapipe, fall detection,
medication reminder, assistive technology, edge ai, offline ai, python, vosk, student project.

---

## 6. Pre-publish checklist (per video)
- [ ] 1080p+ export, correct aspect, captions uploaded (.srt)
- [ ] Custom thumbnail (branded grid layout)
- [ ] Chapters in description (timestamps from 0:00)
- [ ] End screen + 1 card to the next video
- [ ] Pinned comment with the disclaimer + links
- [ ] Added to the right playlist

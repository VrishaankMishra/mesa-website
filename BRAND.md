# MeSA 2.0 — Brand Kit

The shared visual + verbal identity for the website, YouTube channel, demo videos, poster,
and slides. Style direction: **minimal portfolio** — typography-led, near-monochrome,
generous whitespace, understated. Reads as a serious engineering project.

---

## 1. Name & verbal identity

- **Product name:** MeSA 2.0
- **Full name:** MeSA — Medication & Safety Assistant
- **Pronounced:** "MEH-sa"
- **Category:** assistive home-care robot

**Tagline (primary):**
> Right medication. On time. Safe at home.

**Tagline alternates:**
- "A second set of eyes for living independently."
- "Medication safety and fall awareness — offline, on a Raspberry Pi."

**One-line pitch:**
> MeSA 2.0 is a tabletop assistive robot that recognizes medications, tracks whether
> they've been taken, watches for falls, answers questions by voice, and escalates to a
> caregiver when something's wrong — all running offline on a Raspberry Pi 5.

**Elevator (≈50 words):**
> Living alone with a complex medication routine is risky: missed doses, wrong pills, and
> unwitnessed falls. MeSA 2.0 is a low-cost tabletop robot that uses computer vision and
> voice to confirm the right medication is taken on time, detect falls, and alert a
> caregiver — privately and offline.

**Required disclaimer (use near any health claim):**
> MeSA is an assistive aid, not a medical device.

**Voice & tone:** calm, precise, credible. Short declarative sentences. Lead with what it
does for a person, then the engineering. No hype, no exclamation points.

---

## 2. Color

Near-monochrome with a single restrained accent (a calm "safety" green, used sparingly for
links, the CTA, and "all-clear" states).

| Token | Hex | Use |
|-------|-----|-----|
| Ink | `#14110F` | primary text, headings |
| Paper | `#FBFAF8` | page background (warm off-white) |
| Muted | `#6B6660` | secondary text, captions |
| Hairline | `#E5E1DB` | rules, borders, dividers |
| Accent | `#1C6B47` | links, CTA, "safe" status |
| Alert | `#B23A2E` | sparingly — escalation/alert visuals only |

Keep the page ~95% ink-on-paper; accent should feel rare.

---

## 3. Typography

- **Display / headings:** Fraunces (serif) — editorial, distinctive.
- **Body / UI:** Inter (sans) — neutral, legible.
- **Code / specs:** ui-monospace / system mono.

Scale (desktop): H1 clamp ~3rem, H2 ~1.75rem, body 1.0625rem, caption 0.875rem.
Line-height 1.6 for body, ~1.1 for display. Generous letter-spacing on small caps labels.

---

## 4. Logo

`assets/logo.svg` — a monochrome mark + wordmark:
- **Mark:** a circle (the camera "eye") containing a rounded capsule (the pill) — care + vision in one glyph.
- **Wordmark:** "MeSA" set in Fraunces; "2.0" in lighter weight.
- Works in ink-on-paper and inverted (paper-on-ink). Minimum width 96px. Keep clear space ≈ the height of the "M" around it.

Favicon: the circle+capsule mark alone (`assets/favicon.svg`).

---

## 5. Imagery & motion

- Photography: clean, real, well-lit; the robot on a table with medication bottles, a
  person in frame for scale. Avoid stocky/clinical hospital imagery.
- Screenshots: the Streamlit dashboard, live detection boxes, posture overlay.
- Motion: subtle only — fades and small translates. Nothing bouncy.

---

## 6. Asset checklist (fill after the hardware demo exists)
- [ ] Hero shot of the assembled robot
- [ ] 30–60s silent loop for the site hero (muted autoplay)
- [ ] Dashboard screenshot · detection screenshot · posture screenshot
- [ ] Results numbers: mAP@50, posture accuracy, Pi FPS
- [ ] Main 3–4 min demo video (YouTube) embedded on the site

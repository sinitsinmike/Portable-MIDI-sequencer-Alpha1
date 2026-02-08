# Portable MIDI Sequencer — Alpha 1  
## Cheat Sheet (EN / RU)

---

## Buttons (physical labels)

Buttons are numbered internally 0–7, but labeled here as **1–8** for the user.

### Button mapping

| # | Label (User) | Function |
|---|-------------|----------|
| 1 | PLAY / STOP | Start / stop playback |
| 2 | PAUSE | Pause playback |
| 3 | REC | Record / overdub |
| 4 | REW | Reserved (future rewind / scrub) |
| 5 | FF | Reserved (future fast‑forward / scrub) |
| 6 | — | Reserved |
| 7 | — | Reserved |
| 8 | SHIFT / TAP | Shift modifier / Tap Tempo |

---

## Encoder

- Rotate:  
  - Select **track**  
  - Edit **BPM**, **loop length**, **project number** (depending on mode)
- Press (if applicable): confirm / enter edit mode

---

## Transport & Recording

### PLAY / STOP
- Toggle playback
- Works in both **Linear** and **Loop** modes

### PAUSE
- Temporarily pauses playback

### REC behavior
- **Linear mode**  
  - REC during recording → **destructive** (re-records track)
- **Loop mode**  
  - REC during recording → **overdub** (default)

- **REC pressed during active recording**  
  → immediately **cleans current track**

---

## Special combinations

- **REC + PLAY**: start recording from stop
- **REW + FF during recording**: MIDI panic (All Notes Off)

*(Long presses are NOT used in Alpha 1 — reserved for future features)*

---

## Tap Tempo

- Available **only when stopped**
- Available **only in BPM edit mode**
- Activated via **Button 8 (SHIFT / TAP)**

---

## Visual indicators

- `*` (asterisk) on screen  
  → indicates **edit state** (parameter is being edited)

- LEDs  
  → show transport state, activity, and feedback

---

## Modes

### Linear Mode
- Timeline-based recording
- REC = destructive while recording

### Loop Mode
- Fixed loop length
- REC = overdub by default

---

## Projects

- 10 user projects (1–10)
- Save / Load / Clean per project
- Last project auto-loaded on boot

---

## MIDI

- MIDI TRS IN / OUT
- 16 tracks = 16 MIDI channels
- Designed to control up to **16 external instruments** (via MIDI router)

---

## Planned (not in Alpha 1)

- Rewind / Fast-forward (scrub)
- Solo / Mute per track
- MIDI Clock In / Out
- Full MIDI CC control of device

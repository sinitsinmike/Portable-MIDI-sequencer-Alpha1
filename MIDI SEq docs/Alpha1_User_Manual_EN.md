
# Alpha1 User Manual (EN)
## Portable MIDI Sequencer — Public Alpha 1

---

## 1. Introduction

Alpha1 is a portable, performance-oriented MIDI sequencer designed for musicians who prefer hands-on interaction over screen-based editing.

Alpha1 is intended to function as the centerpiece of a dawless MIDI setup, emphasizing timing, musical flow, and real-time performance capture rather than visual manipulation of notes.

---

## 2. What Alpha1 Is / Is Not

### What Alpha1 Is

- A real-time MIDI performance recorder
- A multi-track, multi-channel MIDI sequencer
- Designed for live playing and immediate response
- Optimized for musicians with a good sense of timing

### What Alpha1 Is Not

Alpha1 is not designed to mimic a desktop DAW workflow or provide graphical MIDI editing.

It does not use:
- Step grids
- Piano-roll views
- Pattern-based sequencing
- Visual note editing or timeline manipulation

Instead, Alpha1 prioritizes:
- Timing
- Musical flow
- Real-time interaction
- Predictable behavior during performance

---

## 3. Hardware Overview

Alpha1 features a minimal and purpose-driven hardware interface.

### Controls

- 8 physical buttons arranged horizontally
- 1 rotary encoder with push-button action
- 8 LEDs, one directly above each button

There are no long-press actions in Alpha1.

### Button and LED Relationship

Alpha1 uses a one-to-one relationship between buttons and LEDs:
- Each button has a dedicated LED above it
- LEDs provide immediate feedback for:
  - Playback state
  - Recording state
  - Count-in
  - System status

Active track indication is shown on the display, not via LEDs.

### Display

Alpha1 uses a small OLED display intended for status and parameter feedback, not detailed editing.

The display is primarily used to show:
- Current track number
- BPM
- Sequencer mode (Linear / Loop)
- Menu items (Save / Load / Clean / Quantize)
- Edit state indicator (*)

There is no graphical representation of MIDI notes, timelines, or patterns.

---

## 4. Sequencer Modes (Linear vs Loop)

Alpha1 provides two recording modes: Linear and Loop.

### Linear Mode

Linear mode behaves as a straightforward performance recorder:
- MIDI events are recorded once along the timeline
- Recording is destructive per track
- Re-recording a track replaces its previous content

The built-in LED and piezo metronome guide the performer, helping maintain timing accuracy.

### Loop Mode

Loop mode enables non-destructive recording with overdub behavior:
- Recording loops continuously over a defined loop length
- New events are overdubbed by default
- Pressing REC during recording clears the current track immediately

### Mode Selection Design

Sequencer mode can be set via:
- seq: Linear / Loop
- loop: On / Off

If loop length is already defined, enabling loop automatically switches the sequencer to Loop mode. This dual entry design is intentional to reduce navigation and save time.

---

## 5. Recording Process

Recording requires:
- A MIDI controller connected to MIDI IN
- An external sound module connected to MIDI OUT

Incoming MIDI is passed through in real time while being recorded.

### Recording Flow

1. Select project and track
2. Set BPM
3. Press REC
4. 4-beat count-in starts
5. Recording begins after count-in
6. Press STOP to finish recording

In Linear mode, recording is destructive per track.

In Loop mode, recording overdubs unless REC is pressed again during recording.

---

## 6. Quantization

Quantization in Alpha1 is intentionally minimal.

Quantize (post-factum):
- Global (per project)
- Available in Stop mode only
- Quantization resolution:
  - Quarter notes (1/4)
  - Eighth notes (1/8)
  - Sixteenth notes (1/16)
- Applies to already recorded MIDI events
- No step grid or visual editing involved

---

## 7. Project Management (Save / Load / Clean)

Alpha1 supports project-based storage in internal flash memory.

### Save Project
- Stores all tracks and settings
- Projects persist after power-off

### Load Project
- Loads selected project into memory

### Clean Project
- Erases all MIDI data from the selected project

Save, Load, and Clean operations are disabled during recording.

---

## 8. User Interface & Navigation

Navigation is performed using:
- Encoder rotation (selection)
- Encoder press (enter/apply)
- Buttons for transport and immediate actions

An asterisk (*) indicates edit mode.

Some parameters are intentionally locked during recording to prevent accidental disruption.

---

## 9. Timing, Metronome & Count-In

Alpha1 provides timing assistance via LED and piezo metronome.

### Internal Clock
- Internal clock only
- Tap tempo available
- No external MIDI clock in Alpha1

### LED Metronome
- Active in Play and Record
- Pulses in sync with BPM

### Piezo Metronome
- Active only during recording
- First beat accented with higher pitch

### Count-In
- 4-beat count-in before recording starts
- REC LED lights up when actual recording begins

---

## 10. MIDI Behavior & Channel Mapping

Alpha1 is a pure MIDI sequencer.

### MIDI Thru
- Incoming MIDI is passed through in real time

### Track to Channel Mapping
- Track 1 → MIDI Channel 1
- ...
- Track 16 → MIDI Channel 16

This mapping is fixed and intentional.

### Track Switching
- Loop mode allows track switching during recording
- FF: next track
- REW: previous track

### MIDI Panic
- FF + REW sends All Notes Off on current channel

---

## 11. Limitations (Alpha1)

- No MIDI Clock In / Out
- No per-track MIDI channel reassignment
- No graphical MIDI editing
- No undo

---

## 12. Future Features (Planned)

Planned features (not part of Alpha1):
- MIDI Clock In / Out
- MIDI CC control of device functions
- Scrub and on-screen note interaction
- Project and MIDI export
- Web-based interface

---

End of Alpha1 User Manual (EN)

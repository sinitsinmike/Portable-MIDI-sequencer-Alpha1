# Alpha1 Sequencer — Unified Recording Workflow (Linear & Loop)

## Prerequisites
- MIDI controller connected to MIDI IN (TRS)
- External sound module connected to MIDI OUT (TRS → DIN via adapter)
- Device is a sequencer only (no internal sound engine)
- Incoming MIDI is passed through in real time

---

## Common Preparation (Both Modes)
1. Power on device
2. Select Project number
3. (Optional) Clean Project
4. Set BPM (Stop mode only)
5. Select Track (Track N = MIDI Channel N)
6. Choose `seq:` mode (Linear or Loop)

---

## Linear Recording Workflow

### Characteristics
- Destructive recording
- One pass replaces previous content of current track
- Used for structured, timeline-based recording

### Steps
1. Ensure `seq:` = Linear
2. Select desired Track
3. Press REC
4. Count-in: 4 beats (LED + piezo)
5. Recording starts (REC LED lights up)
6. Play MIDI performance
7. Press STOP to finish
8. Press PLAY to audition
9. Repeat for other tracks
10. Save Project

⚠️ Recording over an existing track permanently erases its content.

---

## Loop Recording Workflow

### Characteristics
- Non-destructive overdub by default
- Continuous looping
- Live track switching supported

### Steps
1. Set `seq:` = Loop
2. Set Loop Length
3. Select Track
4. Press REC
5. Count-in: 4 beats
6. Recording starts, loop runs continuously
7. Overdub MIDI events
8. Switch tracks during recording:
   - FF → Track +1
   - REW → Track -1
9. Press REC during recording → clears current track
10. Press STOP when finished
11. Save Project

⚠️ Avoid long notes near loop wrap to prevent hanging notes.
Use FF + REW for MIDI Panic (All Notes Off).

---

## Restrictions During Recording
- Menu access blocked
- Save / Load / Clean blocked
- Loop length blocked
- seq: mode blocked

---

## Metronome & Indicators
- LED Metronome: Play & Rec
- Piezo Metronome: Rec only
- First beat accented by piezo
- Count-in only in Rec mode

---

## Notes
- Maximum 16 tracks (16 MIDI channels)
- Projects stored in flash (persistent)
- Designed for real-time performance recording

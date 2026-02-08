
ALPHA1 — ASCII STATE DIAGRAM (v1.0, EN)

GLOBAL STATES

POWER OFF -> BOOTING -> STOP (Idle / Edit)

STOP
  | Play
  v
PLAYING
  | Stop
  v
STOP

STOP
  | Rec
  v
RECORD ARM (Count-in, 4 beats)
  |
  v
RECORDING
  | Stop
  v
STOP

RECORDING MODES

Linear:
- Destructive recording
- Count-in before recording
- Piezo + LED metronome active

Loop:
- Non-destructive overdub
- Loop wraps at loop length
- REC during recording clears current track
- FF/REW switches tracks in real time

MENU LOCKS

STOP:
 Save, Load, Clean, Quantize, BPM, Seq Mode, Loop Length = ENABLED

PLAYING / RECORDING:
 Menu actions = DISABLED

EDIT MODE

STOP -> Encoder Click -> EDIT MODE (*)
Rotate = change value
Click = apply and exit

PANIC

ANY STATE:
 FF + REW -> All Notes Off (current channel)

METRONOME

LED:
 Active in PLAY and RECORD

Piezo:
 Active in RECORD only
 Accented first beat

QUANTIZE

STOP ONLY
 Global (per project)
 1/4, 1/8, 1/16
 Applies to recorded events
 No grid or visual editing

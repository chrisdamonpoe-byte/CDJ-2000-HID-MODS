# CDJ-2000 features: HID and USB modes

Working Version 1.0, November 23, 2026.

- **HID** = PC LINK with VirtualDJ. **USB** = playing from a stick.
- "Native" = the player's or original mod's own behaviour, not added here.

## Current choice

The user chose to stay with the **blue clone scrolling waveform** with all four
zoom sizes. Detailed waveform streaming is parked.

| Component | SHA-256 | Package |
| --- | --- | --- |
| GUI (blue/colored clone) | `030b8c42b8022e13435581553264286a8369fe06724ba4c1096d8d5e8222ebac` | CDJ2000-Lower-Wave-Cloned-to-Scroll-Test-2026-11-14.zip |
| MAIN (four zoom) | `41fabccb7ad781f35362ffc0b76622e28290cc0c4451cd9f071b36c9ce16e7ab` | CDJ2000-Four-Scroll-Zoom-Levels-Test-2026-11-13.zip |
| Mapper (Enhanced Waveform) | `331f237f6b842e835efa4e8dfeef15e4eda2411c1743ec9a689e7b5ee9001a1b` | same as MAIN |
| GUI rollback | `38c43d1668639a2380e5625036c58701dfbe6bb9bc78df9950cc918a6d2f9f18` | in the clone package |

The clone is a GUI-only change if that MAIN and mapper are already installed.
These hashes identify the chosen set; they don't prove what is on each player.

## Waveform

| Feature | HID | USB |
| --- | --- | --- |
| Main waveform | Added: clone of the lower wave, mirrored, always visible in LINK | Native |
| SCROLLING / STATIC (UTILITY: LINK WAVEFORM) | Added | Native |
| Main wave color (UTILITY: SCROLL COLOR, COLORED or BLUE/GREEN) | Added | Native |
| Lower wave color (UTILITY: LINK OVERVIEW COLOR, BLUE or COLORED) | Added, independent | Native |
| Zoom 20 / 40 / 80 / 160 s (hold TAG TRACK + wheel) | Added, starts at 80 s | Not added |
| Fixed centre playhead, shorter line, no dotted cue stems | Added | Native |
| Beat-grid ticks above and below, held while paused | Added | Native grid |
| Beat and bar counter | Added, follows VirtualDJ | Original mod's counter |
| Lettered, colored cue flags | Added | Native markers; cue letters on the overview were added |
| Frosted loop region | Added | Native |

## Display

| Feature | HID | USB |
| --- | --- | --- |
| Title and artist | Added: from VirtualDJ, in a blue bar | Native rekordbox info |
| BPM | Added: two decimals | Native precision |
| Orange BPM box, digits and caption | Shared | Shared |
| Gold PLAYER border, label and number | Shared | Shared |
| Inter font (text, menus, numbers, labels, badges) | Shared | Shared |
| DISPLAY THEME: NIGHT / DAY (white) | Added | Shared display path; not checked on browse screens |
| QUANTIZE label | Added: always lit, display only | Native |
| MENU / UTILITY while LINK is active | Restored | Native |
| Switch LINK to USB with the laptop connected | Fixed | Receives the switch |

## Hot cues and banks

| Feature | HID | USB |
| --- | --- | --- |
| Six hot cues, banks A/B/C and D/E/F | Added (mapper) | Added (MAIN); needs exported rekordbox Hot Cues, not only Memory Cues |
| REC/CALL hold, about 3 s, to switch bank | Added (mapper) | Added (MAIN) |
| Lights flash twice for D/E/F, once for A/B/C | Added | Added |
| Cue lights follow the bank | Added | Not recorded |
| REC/CALL + hot cue deletes that cue | Added (mapper) | Not added |
| Preload A/B/C when a track loads | Not applicable | Added; keep Auto Cue on |
| Quick repeat press on D/E/F | Not applicable | Added; pairs A/D, B/E, C/F share a slot, so switching within a pair reloads it |

## Buttons and controls

The mapper is used only in HID. In USB these keep their native behaviour.

| Control | HID (mapper) |
| --- | --- |
| TIME MODE tap / hold and release / hold 3 s | Elapsed or remain / Auto Cue / unload deck |
| TAG TRACK held + wheel | Zoom; wheel alone browses |
| MEMORY | Smart loop |
| CALL left / right | Halve / double the loop |
| 4-BEAT LOOP | Loop on or off |
| DELETE held | Shift |
| EJECT held 1.5 s | Swap controllers |
| Vinyl speed touch / release knobs | Effect sliders 1 / 2 |
| Play, cue, search, track skip, needle search, reverse | Mapped |
| Pitch, range, tempo reset, master tempo, vinyl mode, jog | Mapped |
| Loop in / out / reloop, browse, back, enter | Mapped |

## Resets at power-off

SCROLL COLOR returns to COLORED, LINK OVERVIEW COLOR to BLUE, LINK WAVEFORM to
SCROLLING and DISPLAY THEME to NIGHT. So the blue main wave must be chosen again
after each restart: hold MENU, then SCROLL COLOR, BLUE/GREEN.

## Not in this set

- **Smoother USB colour waveform:** a separate test MAIN. Its code is not in
  `41fabccb` (compared byte by byte). The Bank 2 repeat fix is.
- **Detailed three-band streaming:** the MAIN keeps its receiver, but the clone
  GUI does not draw the detail.
- **Fin waveform, honest wave and diagnostic boxes:** replaced. Never reinstall
  the diagnostic GUI `a55f5b93`; it blocked reflashing.
- **Visual EQ or drum detection:** not implemented. Wave heights can't be split
  by frequency.
- **Live QUANTIZE state:** parked.

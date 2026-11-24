# Working Version 1.0 — blue clone waveforms and four zoom levels

Matched firmware and VirtualDJ Enhanced Waveform mapper for the original
Pioneer CDJ-2000.

## Included

- Blue/colored clone main waveform with SCROLLING/STATIC selection.
- 20/40/80/160-second scrolling zoom with TAG TRACK + browse wheel.
- Independent main and lower waveform color selections.
- Six Hot Cues in two banks, REC/CALL bank switching, and bank-flash feedback.
- HID cue flags, beat grids, beat/bar counter, and frosted active-loop region.
- VirtualDJ title/artist and precise BPM display.
- Orange BPM, gold PLAYER, updated fonts, and existing NIGHT/DAY display themes.
- Three-action TIME_MODE mapper and restored MENU/USB source access during LINK.

The downloadable firmware ZIP is the original verified Version 1.0 archive,
unchanged by this documentation and diagram publication. It includes matching
MAIN, GUI, mapper, checksums, and rollback options.

Use `Install/Firmware` and `Install/Mapper`. Read `README-FIRST.txt` inside the
archive before installation. Select **UTILITY → SCROLL COLOR → BLUE/GREEN**
for blue, or **DISPLAY THEME → DAY** for the white daytime display.

Full mode support, controls, limits, and screenshots are in the repository
[README](https://github.com/chrisdamonpoe-byte/CDJ-2000-HID-MODS#readme) and
[feature guide](https://github.com/chrisdamonpoe-byte/CDJ-2000-HID-MODS/blob/main/features.md).

## Validation and limits

Packaged checks record 58 emulator checks, 2010/2010 packets, MAIN replay tests,
and GUI update-receive simulation. Complete physical validation of every feature
in both modes is not recorded. The current waveform remains overview-derived;
detailed streaming and live Quantize-state feedback are not enabled. The lit
QUANTIZE indicator is display-only. USB cue-cache and timing limitations are
documented in the feature guide.

## Feature illustrations

The repository gallery and release assets include matching Night, Day, and
Static full-track player diagrams. STATIC shows the complete track with a moving
playhead. These image additions do not change the firmware ZIP or mapper.

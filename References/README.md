# References

This folder contains reference material for the **PS2 BlueZZZ** project.

References are used to keep datasheets, source links, module notes, pinout information, and related research in one place.

## Purpose

The purpose of this folder is to collect supporting information used during the design, testing, assembly, and documentation of PS2 BlueZZZ.

This helps keep the project easier to understand and easier to revise later.

## Folder Contents

This folder may include:

| Folder/File | Purpose |
|---|---|
| `Datasheets/` | Datasheets for ICs, modules, connectors, and related parts |
| `Source-Links.md` | Links to useful source material and related projects |
| `README.md` | Reference folder overview |

## Reference Types

Useful references may include:

- Bluetooth audio emitter documentation
- MAX16054 datasheet
- PS2 Slim board notes
- Audio signal notes
- Power control notes
- Pushbutton controller notes
- Connector datasheets
- PCB fabrication rules
- JLCPCB notes
- Related GitHub repositories
- Related forum posts
- Related testing notes

## Important Project References

The main reference topics for this project include:

| Topic | Why It Matters |
|---|---|
| KCX_BT_EMITTER | Main Bluetooth audio emitter module used by the project |
| MAX16054 | Pushbutton on/off controller used for power toggle |
| PS2 Slim audio points | Needed for audio input wiring |
| Audio attenuation | Needed to reduce distortion |
| JLCPCB design rules | Needed for PCB manufacturing |
| Bracket fitment | Needed for internal PS2 Slim installation |

## Datasheets

Datasheets should be stored in the `Datasheets/` folder when allowed.

Suggested datasheets to include:

| Datasheet | Purpose |
|---|---|
| `MAX16054.pdf` | Pushbutton on/off controller datasheet |
| Bluetooth emitter documentation | Bluetooth audio module reference |
| MOSFET datasheets | Power switching reference |
| LED datasheets | Indicator LED reference |
| Connector datasheets | Connector and pad layout reference |

## Source Links

External links should be documented in:

- `References/Source-Links.md`

This keeps the main README cleaner and gives the project one place to track source material.

## PS2 Board Notes

PS2 Slim board notes may include:

- Audio pickup locations
- 5V source locations
- Ground points
- Shell clearance notes
- RF shield notes
- Model-specific fitment notes
- Motherboard revision differences

If these notes become large, they can be split into separate files later.

## Bluetooth Module Notes

Bluetooth module notes may include:

- Module revision
- Pair/connect button behavior
- LED behavior
- AT command behavior
- Power requirements
- Audio input notes
- Pairing and reconnect behavior
- Headphone compatibility notes

Because Bluetooth module revisions may behave differently, record the exact module version whenever testing.

## MAX16054 Notes

MAX16054 reference notes may include:

- Pinout
- Pushbutton input behavior
- OUT and active-low OUT behavior
- CLEAR input behavior
- Power-up default state
- Required supply voltage
- Debounce behavior
- Typical application circuits

These notes are useful for troubleshooting the pushbutton power control circuit.

## Manufacturing References

Manufacturing references may include:

- JLCPCB design rules
- KiCad export notes
- Castellated edge notes
- Edge solder pad notes
- Surface finish notes
- Board thickness notes
- Assembly service notes

Detailed JLCPCB project notes are located in:

- `Manufacturing/JLCPCB-Notes.md`

## Test References

Testing references may include:

- Audio testing notes
- Power testing notes
- Bluetooth pairing notes
- Fitment photos
- Revision test logs
- Known issue reports

Project test data should be stored in:

- `Test-Data/`

## File Naming

Use clear names for reference files.

Recommended examples:

| File Name | Purpose |
|---|---|
| `MAX16054-Datasheet.pdf` | MAX16054 datasheet |
| `KCX-BT-EMITTER-Notes.md` | Bluetooth module notes |
| `PS2-Slim-Audio-Points.md` | Audio pickup reference |
| `JLCPCB-Design-Rules.pdf` | PCB manufacturing reference |
| `Bluetooth-Emitter-AT-Commands.md` | AT command notes |

## Reference Quality Notes

When adding references, try to record:

- Source name
- Source link
- Date accessed
- What the reference is used for
- Any uncertainty or version-specific notes

This makes it easier to understand later why a reference was included.

## Version-Specific Notes

Some information may depend on the hardware version.

Track version-specific details for:

- Bluetooth emitter revision
- PS2 Slim motherboard revision
- Interface board revision
- Controller board revision
- Bracket revision
- Firmware version, if applicable

## Known Concerns

Items to watch:

- Some Bluetooth emitter information may be incomplete or translated
- Module behavior may change between revisions
- Forum information may need verification
- Marketplace listings may disappear over time
- Datasheets may be updated by manufacturers
- PCB manufacturing rules may change
- PS2 Slim revisions may have different internal clearance

## Related Documents

- `References/Source-Links.md`
- `Documents/01-Project-Overview.md`
- `Documents/03-Interface-Board.md`
- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Manufacturing/JLCPCB-Notes.md`
- `Test-Data/README.md`

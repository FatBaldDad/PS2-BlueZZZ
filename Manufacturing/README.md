# Manufacturing

This folder contains manufacturing notes for the **PS2 BlueZZZ** project.

The goal of this section is to keep PCB fabrication, assembly, inspection, and quality-control notes organized in one place.

## Purpose

The PS2 BlueZZZ project includes custom circuit boards and mounting hardware. These parts need to be manufactured, assembled, inspected, and tested before they are installed inside a PlayStation 2 Slim console.

This folder is used to document:

- PCB fabrication notes
- Assembly notes
- Board revision notes
- Manufacturer-specific notes
- Quality-control steps
- Common assembly issues
- Pre-install inspection steps
- Final test checklist

## Folder Contents

This folder may include:

| File | Purpose |
|---|---|
| `README.md` | Manufacturing section overview |
| `Assembly-Notes.md` | Notes for assembling the boards |
| `JLCPCB-Notes.md` | Notes specific to JLCPCB ordering and fabrication |
| `QA-Checklist.md` | Quality-control checklist before installation |

## Manufacturing Goals

The manufacturing process should make the PS2 BlueZZZ boards:

- Easy to fabricate
- Easy to assemble
- Easy to inspect
- Easy to test
- Easy to revise
- Consistent between builds
- Safe to install inside the console

## Supported Boards

The PS2 BlueZZZ hardware may include:

- Interface board
- Controller board
- Bracket or mounting hardware
- Future expansion or revision boards

Each board should have its own revision tracking and manufacturing files.

## PCB Fabrication

PCB fabrication files should be exported and stored by revision.

Suggested folder format:

| Folder | Purpose |
|---|---|
| `Hardware/Interface-Board/Gerbers/Rev-1.0/` | Interface board Rev 1.0 manufacturing files |
| `Hardware/Controller-Board/Gerbers/Rev-1.0/` | Controller board Rev 1.0 manufacturing files |

Each fabrication release should include:

- Gerber files
- Drill files
- Board outline
- Solder mask layers
- Silkscreen layers
- Copper layers
- Fabrication notes
- Board thickness notes
- Board color notes, if important

## Board Thickness

The board thickness should be selected based on fitment and soldering needs.

Possible board thicknesses:

| Thickness | Notes |
|---|---|
| 1.6 mm | Standard PCB thickness, but may be too thick for tight installs |
| 1.0 mm | Thinner option for tight internal mounting |
| 0.8 mm | Useful where low profile fitment is important |

Final board thickness should be documented for each revision.

## Board Color

Board color is mostly cosmetic, but it should still be documented for repeatability.

Possible board colors:

- Purple
- Black
- Blue
- Green
- White

If the board color matters for the project look, note it in the fabrication release.

## Surface Finish

Surface finish should be selected based on availability, solderability, and cost.

Common options:

- HASL
- Lead-free HASL
- ENIG

For small pads and cleaner assembly, ENIG may be preferred when cost allows.

## Assembly Notes

Assembly notes should include:

- Component values
- Component orientation
- Soldering order
- Inspection steps
- Common mistakes
- Test points
- Rework notes
- Bluetooth emitter attachment notes
- Edge solder pad notes

Detailed assembly notes should be kept in:

- `Manufacturing/Assembly-Notes.md`

## Quality Control

Each assembled board should be inspected and tested before installation.

Basic QC should include:

- Visual inspection
- Continuity test
- Power test
- Pushbutton toggle test
- Switched 5V test
- LED test
- Audio continuity test
- Bluetooth emitter power test
- Fitment test

Detailed QC steps should be kept in:

- `Manufacturing/QA-Checklist.md`

## Revision Tracking

Manufacturing files should be organized by revision.

Do not overwrite old manufacturing files after a board has been ordered.

Suggested revision style:

| Revision | Meaning |
|---|---|
| Rev 0.1 | Early prototype |
| Rev 0.2 | Updated prototype |
| Rev 1.0 | First public/test release |
| Rev 1.1 | Minor improvement |
| Rev 2.0 | Major redesign |

## Release Checklist

Before releasing manufacturing files, verify:

- Schematic is updated
- PCB layout matches schematic
- DRC passes or known exceptions are documented
- Board outline is correct
- Edge solder pads are correct
- Silkscreen is readable
- Component references are correct
- Mounting holes are correct
- Gerbers are exported
- Drill files are included
- BOM is updated
- Assembly notes are updated
- Revision number is correct

## Pre-Order Checklist

Before ordering boards:

- Confirm board revision
- Confirm board thickness
- Confirm board color
- Confirm copper weight
- Confirm surface finish
- Confirm quantity
- Confirm castellated or edge pad requirements, if used
- Confirm minimum trace/space rules
- Confirm minimum drill size
- Confirm silkscreen placement
- Confirm no important markings are clipped
- Confirm the board outline is correct

## Post-Order Inspection

When boards arrive, inspect:

- Board outline
- Board thickness
- Board color
- Solder mask alignment
- Silkscreen readability
- Edge solder pads
- Drill alignment
- Pad quality
- Missing copper
- Scratches or damage
- Shorts or manufacturing defects

## Assembly Inspection

After assembly, inspect:

- Component orientation
- Solder joints
- Solder bridges
- Flux residue
- Edge solder joints
- Bluetooth emitter alignment
- LED polarity
- MAX16054 orientation
- MOSFET orientation
- Resistor and capacitor values
- Connector or pad labeling

## Test Before Install

Before installing into a PS2 Slim, test:

- No short between 5V and ground
- MAX16054 toggles correctly
- Switched 5V turns on and off
- Power/status LED works
- Pair/connect controls work, if installed
- Audio continuity is correct
- Left and right channels are not swapped
- Bluetooth emitter powers on and off
- Audio passes through the Bluetooth emitter

## Known Manufacturing Concerns

Items to watch:

- Edge solder pads may need careful fabrication review
- Board thickness may affect fitment
- Silkscreen may be too small to read
- Small components may be difficult to hand solder
- Bluetooth emitter alignment matters
- Rework may damage small pads
- Solder bridges may occur around close pads
- Bracket fitment may need revision after real-world testing

## Related Documents

- `Manufacturing/Assembly-Notes.md`
- `Manufacturing/JLCPCB-Notes.md`
- `Manufacturing/QA-Checklist.md`
- `Documents/03-Interface-Board.md`
- `Documents/04-Controller-Board.md`
- `Documents/07-Installation-Planning.md`
- `Documents/08-Testing.md`
- `Hardware/Interface-Board/README.md`
- `Hardware/Controller-Board/README.md`
- `Hardware/Brackets/README.md`

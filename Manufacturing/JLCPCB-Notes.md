# JLCPCB Notes

This document contains JLCPCB ordering and fabrication notes for the **PS2 BlueZZZ** project.

These notes are used to help keep board orders consistent between revisions.

## Purpose

The purpose of this document is to record the settings, options, and checks used when ordering PS2 BlueZZZ boards from JLCPCB.

This helps make future orders more repeatable and reduces the chance of ordering the wrong board thickness, color, finish, or revision.

## Important Note

Always verify the current JLCPCB order page before placing an order.

JLCPCB options, prices, design limits, colors, surface finishes, and assembly services can change over time.

These notes are project-specific guidance, not a replacement for checking the current manufacturing rules.

## Boards Covered

These notes may apply to:

- PS2 BlueZZZ interface board
- PS2 BlueZZZ controller board
- Future PS2 BlueZZZ revision boards

Bracket files are handled separately and are not part of the PCB order unless a PCB-based bracket or support board is created.

## Suggested Order Settings

Use this section to record the preferred settings for each board revision.

| Setting | Preferred Value | Notes |
|---|---|---|
| Manufacturer | JLCPCB | Verify current capabilities before ordering |
| Board type | PCB | Standard PCB order |
| Layers | 2-layer | Update if future revision changes |
| Board thickness | TBD | 0.8 mm may be useful for tight fitment |
| Board color | TBD | Purple, blue, or black may fit the project look |
| Surface finish | TBD | ENIG may be preferred for small pads |
| Copper weight | 1 oz | Update if needed |
| Castellated holes | TBD | Only select if the board uses true castellated features |
| Edge plating | TBD | Only select if required by final design |
| Via covering | Tented or default | Verify per revision |
| Remove order number | Yes, if desired | Helps keep the board cleaner looking |

## Board Thickness Notes

Board thickness matters because PS2 BlueZZZ is installed inside a PS2 Slim shell.

Possible options:

| Thickness | Notes |
|---|---|
| 1.6 mm | Standard PCB thickness, but may be too tall for tight internal installs |
| 1.0 mm | Thinner option with better fitment |
| 0.8 mm | Good candidate for low-profile internal console hardware |

The final board thickness should be documented for each revision.

Record final thickness here:

| Board | Revision | Thickness | Notes |
|---|---|---:|---|
| Interface board | Rev 1.0 | TBD | TBD |
| Controller board | Rev 1.0 | TBD | TBD |

## Board Color Notes

Board color is mostly cosmetic, but it should be documented for repeatability.

Possible colors:

- Purple
- Blue
- Black
- Green
- White

Record chosen colors here:

| Board | Revision | Color | Notes |
|---|---|---|---|
| Interface board | Rev 1.0 | TBD | TBD |
| Controller board | Rev 1.0 | TBD | TBD |

## Surface Finish Notes

Surface finish affects solderability and appearance.

Common choices:

| Finish | Notes |
|---|---|
| HASL | Lower cost, common option |
| Lead-free HASL | Common lead-free option |
| ENIG | Flatter finish, often better for small pads and cleaner soldering |

For small pads, edge solder pads, and cleaner assembly, ENIG may be preferred if cost allows.

Record final surface finish here:

| Board | Revision | Surface Finish | Notes |
|---|---|---|---|
| Interface board | Rev 1.0 | TBD | TBD |
| Controller board | Rev 1.0 | TBD | TBD |

## Edge Solder Pad Notes

The interface board uses edge solder pads to help attach to the Bluetooth audio emitter.

Before ordering, verify:

- Edge pads are included in the correct copper layer
- Solder mask clearance is correct
- Pads extend to the board edge if required
- Board outline cuts through the intended edge pads if designed that way
- DRC exceptions are understood and documented
- The fabrication preview shows the pads correctly
- No important copper is accidentally clipped
- No unintended copper is exposed at the edge

If the design uses true castellated edges, make sure the JLCPCB order options and board design both support that.

## Castellated Edge Notes

Only select castellated holes if the board actually uses castellated plated half-holes.

For PS2 BlueZZZ, some edge pads may simply be exposed solder pads at the board edge, not true castellated holes.

Record which style is used:

| Board | Revision | Edge Style | Notes |
|---|---|---|---|
| Interface board | Rev 1.0 | TBD | Edge pads or castellated pads |
| Controller board | Rev 1.0 | TBD | TBD |

## Gerber Export Checklist

Before uploading Gerbers to JLCPCB, verify the export includes:

- Front copper
- Back copper
- Front solder mask
- Back solder mask
- Front silkscreen
- Back silkscreen, if used
- Board outline
- Drill file
- NPTH drill file, if used
- Solder paste layers, if assembly or stencil is needed

## KiCad Pre-Export Checklist

Before exporting from KiCad:

- Update schematic from PCB
- Run ERC
- Run DRC
- Review known DRC warnings
- Confirm board outline
- Confirm mounting holes
- Confirm edge solder pads
- Confirm silkscreen is not on pads
- Confirm reference designators are readable
- Confirm logo graphics do not violate spacing rules
- Confirm copper pours are updated
- Confirm no unrouted nets remain
- Confirm revision text is correct
- Confirm board name is correct

## JLCPCB Upload Review

After uploading the Gerber file, review the JLCPCB preview carefully.

Check:

- Board outline looks correct
- Board size is correct
- Holes appear in the correct locations
- Edge solder pads appear correctly
- Silkscreen is readable
- Logos appear correctly
- No important silkscreen is missing
- No text is clipped
- No copper is missing
- No layer appears mirrored incorrectly
- Solder mask openings look correct

Do not place the order until the preview looks correct.

## Order Number Placement

JLCPCB may place an order number on the board unless the option is removed or a location is specified.

Preferred approach:

- Remove order number if available and affordable
- Or specify an order number location away from functional areas
- Avoid placing order numbers on logos, labels, pads, or visible design areas

Record order number handling here:

| Board | Revision | Order Number Option | Notes |
|---|---|---|---|
| Interface board | Rev 1.0 | TBD | TBD |
| Controller board | Rev 1.0 | TBD | TBD |

## Silkscreen Notes

Silkscreen should help assembly and troubleshooting.

Before ordering, verify:

- Pin 1 markings are clear
- Component labels are readable
- Polarity markings are clear
- Power labels are clear
- Audio left/right labels are clear
- Button and LED labels are clear
- Revision number is printed on the board
- Board name is printed on the board
- No silkscreen overlaps exposed pads

## Revision Marking

Every PCB order should include a clear board revision marking.

Suggested format:

| Marking | Meaning |
|---|---|
| PS2 BlueZZZ Interface Rev 1.0 | Interface board revision 1.0 |
| PS2 BlueZZZ Controller Rev 1.0 | Controller board revision 1.0 |

Do not order boards without a revision number.

## File Naming

Use clear filenames for manufacturing exports.

Suggested format:

| File/Folder | Example |
|---|---|
| Interface Gerbers | `PS2-BlueZZZ-Interface-Rev-1.0-Gerbers.zip` |
| Controller Gerbers | `PS2-BlueZZZ-Controller-Rev-1.0-Gerbers.zip` |
| Interface BOM | `PS2-BlueZZZ-Interface-Rev-1.0-BOM.csv` |
| Controller BOM | `PS2-BlueZZZ-Controller-Rev-1.0-BOM.csv` |
| Pick and Place | `PS2-BlueZZZ-Interface-Rev-1.0-CPL.csv` |

## Assembly Service Notes

If using JLCPCB assembly, confirm:

- Parts are available
- Footprints match the selected parts
- LCSC part numbers are correct
- Polarity is correct
- Rotation is correct
- BOM file is correct
- CPL file is correct
- Parts not assembled by JLCPCB are clearly marked as DNP
- Hand-soldered parts are documented

If hand assembling, assembly service files may not be needed.

## DNP Notes

DNP means Do Not Populate.

Use DNP for:

- Optional resistor values
- Test pads
- Alternate attenuation parts
- Unused LED options
- Optional connector positions
- Prototype-only parts

Record DNP parts clearly in the BOM and assembly notes.

## Stencil Notes

A stencil may be useful if assembling several boards.

Stencil may help with:

- Small ICs
- Small passives
- Consistent solder paste
- Cleaner batch assembly

Stencil may not be needed for:

- One-off prototypes
- Simple hand-soldered builds
- Boards with mostly large pads

Record stencil choice here:

| Board | Revision | Stencil Ordered | Notes |
|---|---|---|---|
| Interface board | Rev 1.0 | TBD | TBD |
| Controller board | Rev 1.0 | TBD | TBD |

## Panelization Notes

Panelization is probably not needed for early prototypes.

If ordering many boards, panelization may help with assembly and handling.

Before panelizing, verify:

- Board outline
- Breakaway tabs
- Mouse bites
- Tooling holes
- Edge solder pad clearance
- No tabs interfere with functional edge pads
- Final separated board dimensions

## Post-Delivery Inspection

When boards arrive from JLCPCB, inspect:

- Board quantity
- Board thickness
- Board color
- Surface finish
- Board outline
- Edge solder pads
- Solder mask alignment
- Silkscreen quality
- Drill alignment
- Pad quality
- Scratches or damage
- Warping
- Shorts or exposed copper problems

## First Article Inspection

Before assembling all boards, fully inspect and assemble one board first.

First article steps:

1. Inspect bare PCB.
2. Assemble one board.
3. Test for shorts.
4. Power the board.
5. Test pushbutton power control.
6. Test switched 5V.
7. Test Bluetooth emitter power.
8. Test audio.
9. Test fit inside PS2 Slim.
10. Record all issues before assembling more boards.

## Order Tracking

Use this section to track board orders.

| Date Ordered | Board | Revision | Quantity | Thickness | Color | Finish | Result |
|---|---|---|---:|---:|---|---|---|
| TBD | Interface board | Rev 1.0 | TBD | TBD | TBD | TBD | TBD |
| TBD | Controller board | Rev 1.0 | TBD | TBD | TBD | TBD | TBD |

## Manufacturing Issue Log

Use this section to track manufacturing issues.

| Issue | Board | Revision | Cause | Fix |
|---|---|---|---|---|
| TBD | TBD | TBD | TBD | TBD |

## Known Concerns

Items to watch when ordering:

- Edge pads may be interpreted differently than expected
- Castellated features may require specific settings
- Board thickness may affect fitment
- Silkscreen may be too small
- Logos or graphics may not render as expected
- Solder mask openings may expose more copper than intended
- Order number may be placed in an unwanted location
- Surface finish choice may affect soldering
- Assembly service part rotation may need careful review

## Related Documents

- `Manufacturing/README.md`
- `Manufacturing/Assembly-Notes.md`
- `Manufacturing/QA-Checklist.md`
- `Documents/03-Interface-Board.md`
- `Documents/07-Installation-Planning.md`
- `Documents/08-Testing.md`
- `Hardware/Interface-Board/README.md`
- `Hardware/Controller-Board/README.md`

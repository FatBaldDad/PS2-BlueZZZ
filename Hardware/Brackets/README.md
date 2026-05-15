# Brackets

This folder contains bracket and mounting hardware files for the **PS2 BlueZZZ** project.

The bracket is used to help mount the Bluetooth audio interface board, Bluetooth audio emitter, and related hardware inside a PlayStation 2 Slim console.

## Purpose

The PS2 BlueZZZ bracket is part of the project because the board needs to be mounted cleanly and safely inside the console.

A working circuit is not enough if the board is loose, presses against the shell, shorts against shielding, or makes the console difficult to close.

The bracket helps make the installation:

- Cleaner
- Safer
- More repeatable
- Easier to service
- Easier to document

## Main Goals

The bracket should:

- Hold the Bluetooth audio interface board securely
- Support the Bluetooth audio emitter module
- Fit inside the PS2 Slim shell
- Avoid RF shield contact
- Avoid screw post interference
- Avoid shell clip interference
- Avoid putting stress on solder joints
- Keep wiring paths manageable
- Allow the console shell to close normally

## Folder Contents

This folder may include:

| Folder/File | Purpose |
|---|---|
| `STL/` | 3D printable bracket files |
| `STEP/` | Editable CAD/export files |
| `Images/` | Bracket renders, fitment photos, and install photos |
| `README.md` | Bracket overview and fitment notes |

## Suggested Files To Add

Add the following files as the bracket design progresses:

| File | Purpose |
|---|---|
| `STL/PS2-BlueZZZ-Bracket-Rev-1.0.stl` | Printable bracket file |
| `STEP/PS2-BlueZZZ-Bracket-Rev-1.0.step` | Editable CAD model |
| `Images/Bracket-Render.png` | Render of the bracket |
| `Images/Test-Fit-Top.png` | Photo of bracket test fit from above |
| `Images/Test-Fit-Side.png` | Photo of bracket side clearance |
| `Images/Installed-Bracket.png` | Photo of bracket installed in console |

## Bracket Function

The bracket should hold the PS2 BlueZZZ hardware in a fixed location inside the PS2 Slim.

It should prevent the board assembly from moving during handling, shipping, or normal console use.

The bracket may support:

- Interface board
- Bluetooth audio emitter
- Controller board, if located nearby
- Wire strain relief
- Insulation spacing
- Board height control

## Fitment Goals

The bracket should fit without forcing the PS2 Slim shell closed.

Fitment goals include:

- No top shell interference
- No bottom shell interference
- No RF shield interference
- No blocked screw posts
- No blocked shell clips
- No pressure on the motherboard
- No pressure on the Bluetooth emitter
- No pinched wires
- No exposed pads touching metal

## Board Clearance

The bracket should keep the board high enough to avoid shorts, but low enough to fit inside the console.

Clearance should be checked around:

- Interface board edges
- Bluetooth audio emitter
- Edge solder pads
- Solder joints
- Wire exits
- RF shielding
- Shell ribs
- Screw posts
- Nearby motherboard components

## RF Shield Clearance

The PS2 Slim uses metal shielding that can create shorting risks.

The bracket should prevent the board from touching the RF shield.

If clearance is tight, use insulation where needed.

Possible insulation options:

- Kapton tape
- Thin plastic sheet
- Fish paper
- Printed bracket standoffs
- Non-conductive spacer

## Wire Routing

The bracket should not trap or pinch wires.

Good wire routing should:

- Keep wires away from screw posts
- Keep wires away from shell clips
- Keep wires away from sharp metal
- Keep audio wires away from noisy power wiring
- Allow the shell to close naturally
- Avoid putting tension on solder pads
- Leave enough service loop for inspection or rework

## Mounting Method

The final mounting method may vary depending on console revision and bracket design.

Possible mounting methods:

- Existing screw location
- Adhesive mounting
- Double-sided mounting tape
- Mechanical clip
- Printed locating features
- RF shield attachment point
- Custom console shell feature

Avoid mounting methods that create stress on the PS2 motherboard or require unnecessary shell damage.

## Material Notes

Bracket material should be non-conductive and stable enough for the console environment.

Possible materials:

- PLA for early test prints
- PETG for improved heat resistance
- ABS or ASA for stronger finished parts
- Resin print for small detailed parts, if tested carefully

For early prototypes, PLA is acceptable for quick fitment testing. For final installs, a more heat-tolerant material may be preferred.

## Test Fit Process

Before final installation:

1. Print or fabricate the bracket.
2. Test fit the bracket without the board installed.
3. Check for shell and RF shield clearance.
4. Install the board on the bracket.
5. Check board height and solder joint clearance.
6. Route wires temporarily.
7. Close the shell gently without screws.
8. Check for pressure points.
9. Install screws and check again.
10. Remove the shell and inspect for rubbing or contact marks.

## Fitment Checklist

Before final assembly, verify:

- Bracket sits flat
- Board is held securely
- Bluetooth emitter clears the shell
- Solder pads do not touch shielding
- Wires are not pinched
- Shell closes without force
- Screw posts are not blocked
- Shell clips are not blocked
- Button and LED wiring still reaches the controller board
- Board can be inspected or serviced if needed

## Revision Tracking

Bracket revisions should be tracked carefully because small fitment changes can matter inside the PS2 Slim.

Record:

- Console model tested
- Motherboard revision, if known
- Bracket revision
- Print material
- Fitment result
- Clearance issues
- Shell closure result
- Changes needed

## Fitment Test Table

| Bracket Revision | Console Model | Board Revision | Result | Notes |
|---|---|---|---|---|
| Rev 0.1 | TBD | TBD | TBD | Initial test |
| Rev 1.0 | TBD | TBD | TBD | First public/test revision |
| Rev 1.1 | TBD | TBD | TBD | Future update |

## Known Concerns

Items to watch:

- Bracket may need changes between PS2 Slim revisions
- Board height may be too tall after soldering
- Edge solder pads may reduce available clearance
- RF shield may require insulation
- Wires may be pinched when the shell is closed
- Controller board placement may affect bracket location
- Adhesive mounting may loosen over time
- Printed material may soften if exposed to heat

## Revision Notes

Use this section to track bracket changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial bracket concept |
| Rev 1.0 | First public/test bracket |
| Rev 1.1 | Future bracket changes |

## Related Documents

- `Documents/07-Installation-Planning.md`
- `Documents/08-Testing.md`
- `Documents/09-Known-Issues.md`
- `Hardware/Interface-Board/README.md`
- `Hardware/Controller-Board/README.md`
- `Manufacturing/Assembly-Notes.md`
- `Manufacturing/QA-Checklist.md`

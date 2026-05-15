# Controller Board Hardware

This folder contains the hardware files for the **PS2 BlueZZZ Controller Board**.

The controller board is the user-facing control board for the Bluetooth audio system. It provides a cleaner way to mount buttons, LEDs, and other user controls inside or near the PS2 Slim shell.

## Purpose

The purpose of the controller board is to move the user controls away from the Bluetooth audio emitter and interface board.

Instead of reaching inside the console or wiring buttons directly to the Bluetooth emitter, the controller board provides a cleaner and more repeatable way to control the PS2 BlueZZZ system.

## Main Features

- Remote enable button support
- Power/status LED support
- Pair/connect button support
- Pair/connect LED support
- Cleaner wiring between shell controls and interface board
- Small board intended for internal PS2 Slim mounting
- Designed to make the install look more finished
- Revision tracking for future improvements

## Folder Contents

This folder may include:

| Folder/File | Purpose |
|---|---|
| `KiCad/` | KiCad schematic and PCB layout files |
| `Gerbers/` | Exported manufacturing files |
| `BOM/` | Bill of materials and part sourcing notes |
| `Images/` | Board renders, screenshots, and assembly photos |
| `README.md` | Controller board hardware overview |

## Board Function

The controller board may handle:

- Bluetooth audio enable pushbutton
- Power/status LED
- Pair/connect pushbutton
- Pair/connect indicator LED
- Ground connections for button wiring
- Signal connections back to the interface board

The exact features may vary depending on board revision.

## Enable Button

The enable button is used to turn the Bluetooth audio system on and off.

The button connects back to the MAX16054 pushbutton control circuit on the interface board.

Expected behavior:

| Button Action | Bluetooth Audio State |
|---|---|
| Press once | On |
| Press again | Off |

The enable button is intended to be a momentary pushbutton, not a latching mechanical switch.

## Power/Status LED

The power/status LED shows when the Bluetooth audio system is enabled.

Expected behavior:

| Bluetooth Audio State | LED State |
|---|---|
| Off | LED off |
| On | LED on |

LED brightness should be kept reasonable because PS2 BlueZZZ is intended for late-night gaming.

## Pair/Connect Button

The controller board may support an external pair/connect button.

This can be useful if the onboard button on the Bluetooth audio emitter is removed, hidden, or difficult to access after installation.

Possible uses:

- Start pairing mode
- Reconnect to a known Bluetooth device
- Trigger the module connect function
- Replace the small onboard Bluetooth emitter button

The exact behavior should be tested with the Bluetooth emitter revision being used.

## Pair/Connect LED

The controller board may support a Bluetooth status LED.

Possible status uses:

- Searching
- Pairing
- Connected
- Disconnected
- Bluetooth activity

The final LED behavior depends on the Bluetooth audio emitter module and board wiring.

## Active-Low Button Wiring

Where practical, the controller board uses active-low button wiring.

This means pressing the button pulls the signal to ground.

Benefits:

- Simple wiring
- Safer signal routing
- Easier troubleshooting
- Less chance of sending voltage into the wrong circuit
- Works well with pull-up based inputs

Always follow the schematic for the exact board revision being assembled.

## LED Wiring

LED wiring may vary depending on board revision.

Possible LED wiring methods include:

- LED tied to local voltage through a resistor and switched to ground
- LED tied to ground and driven by a positive signal
- LED controlled through a transistor inverter
- LED powered from switched 5V
- LED controlled by a signal from the Bluetooth emitter

The preferred method should be documented in the schematic and assembly notes.

## Suggested Files To Add

Add the following files as the design progresses:

| File | Purpose |
|---|---|
| `KiCad/PS2-BlueZZZ-Controller.kicad_pro` | KiCad project file |
| `KiCad/PS2-BlueZZZ-Controller.kicad_sch` | Schematic file |
| `KiCad/PS2-BlueZZZ-Controller.kicad_pcb` | PCB layout file |
| `Gerbers/Rev-1.0/` | Manufacturing files for Rev 1.0 |
| `BOM/PS2-BlueZZZ-Controller-BOM.csv` | Bill of materials |
| `Images/Board-Render-Front.png` | Front board render |
| `Images/Board-Render-Back.png` | Back board render |
| `Images/Assembled-Board.png` | Photo of assembled board |
| `Images/Installed-Location.png` | Photo showing board location inside the shell |

## Placement Goals

The controller board should be placed where the user can access the button and see the LED indicators.

Placement goals:

- Easy access to enable button
- Visible status LED
- Clean wire routing
- No shell interference
- No pressure on the board
- No contact with RF shielding
- No blocked screw posts
- No unnecessary shell cutting

## Installation Notes

When installing the controller board:

- Confirm button location before drilling or cutting
- Confirm LED visibility before final mounting
- Keep wires short where possible
- Avoid routing wires near noisy power circuits
- Avoid wire pinch points
- Use insulation where needed
- Make sure the shell closes without force
- Confirm the button can be pressed after assembly

## Pre-Power Checklist

Before applying power:

- Check button wiring
- Check LED polarity
- Check resistor values
- Check ground continuity
- Check for solder bridges
- Check connector or pad orientation
- Check wiring between controller board and interface board
- Confirm no exposed pads are touching metal

## Functional Testing

After wiring the controller board, verify:

- Enable button toggles Bluetooth audio power
- Power/status LED follows the power state
- Pair/connect button works as expected
- Pair/connect LED behaves as expected
- LED brightness is acceptable
- Button press does not reset or disturb the PS2
- Wires do not move or disconnect when the shell is handled

## Known Concerns

Items to watch:

- Button placement may be awkward after assembly
- LED may be too bright for late-night use
- LED polarity may be easy to install incorrectly
- Pair/connect behavior may vary by Bluetooth emitter revision
- Long button wires may pick up noise
- Controller board may interfere with shell fitment
- Wires may be pinched near screw posts or shell clips

## Revision Notes

Use this section to track controller board hardware revisions.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial layout concept |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future hardware changes |

## Related Documents

- `Documents/04-Controller-Board.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/07-Installation-Planning.md`
- `Documents/08-Testing.md`
- `Hardware/Interface-Board/README.md`
- `Manufacturing/Assembly-Notes.md`
- `Manufacturing/QA-Checklist.md`

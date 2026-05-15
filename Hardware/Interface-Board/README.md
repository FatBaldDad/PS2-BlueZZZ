# Interface Board Hardware

This folder contains the hardware files for the **PS2 BlueZZZ Interface Board**.

The interface board is the main adapter board that connects the Bluetooth audio emitter module to the PlayStation 2 Slim.

## Purpose

The purpose of the interface board is to make the Bluetooth audio emitter easier to install cleanly inside a PS2 Slim console.

Instead of wiring directly to the small Bluetooth emitter pads, this board provides a cleaner connection system, larger soldering areas, audio attenuation, and pushbutton-controlled power.

## Main Features

- Designed for internal PS2 Slim Bluetooth audio installs
- Sits flush with the Bluetooth audio emitter module
- Edge solder pads for cleaner soldering
- Audio attenuation for left and right audio channels
- MAX16054 pushbutton on/off control
- Switched 5V output for Bluetooth emitter power
- Controller board connection support
- Cleaner wiring and easier serviceability
- Revision tracking for future board improvements

## Folder Contents

This folder may include:

| Folder/File | Purpose |
|---|---|
| `KiCad/` | KiCad schematic and PCB layout files |
| `Gerbers/` | Exported manufacturing files |
| `BOM/` | Bill of materials and part sourcing notes |
| `Images/` | Board renders, screenshots, and assembly photos |
| `README.md` | Interface board hardware overview |

## Board Function

The interface board handles several important parts of the PS2 BlueZZZ system:

- Audio input from the PS2
- Audio attenuation before the Bluetooth emitter
- 5V power input
- Switched 5V output
- Pushbutton toggle control
- Status/control connections to the controller board
- Physical attachment to the Bluetooth audio emitter

## Audio Section

The PS2 left and right audio signals pass through the interface board before reaching the Bluetooth audio emitter.

The board includes an attenuation circuit to reduce the audio level and help prevent distortion.

Signals:

- Left audio input
- Right audio input
- Audio ground
- Attenuated left audio output
- Attenuated right audio output

Both left and right channels should use matching resistor values so the stereo balance stays even.

## Power Section

The interface board receives 5V power and switches that power to the Bluetooth audio emitter.

The switched 5V output allows the Bluetooth audio emitter to be turned on and off without disconnecting the whole PS2 console.

Signals:

- 5V input
- Ground
- Switched 5V output

Always verify polarity before powering the board.

## Pushbutton Toggle Section

The board uses a MAX16054 pushbutton on/off controller.

This allows a momentary pushbutton to control the Bluetooth audio power state.

Expected behavior:

| Button Action | Bluetooth Audio State |
|---|---|
| Press once | On |
| Press again | Off |

The preferred default behavior is for Bluetooth audio to remain off when the PS2 powers up.

## Controller Board Connection

The interface board connects to the PS2 BlueZZZ controller board.

The controller board may provide:

- Enable pushbutton
- Power/status LED
- Pair/connect button support
- Pair/connect LED support

The exact signal list may change between board revisions.

## Edge Solder Pads

The interface board includes edge solder pads to make the Bluetooth emitter easier to attach.

These pads are intended to:

- Improve soldering access
- Create a cleaner physical connection
- Reduce loose wiring
- Improve mechanical strength
- Make inspection easier after assembly

Inspect all edge solder joints carefully before powering the board.

## Suggested Files To Add

Add the following files as the design progresses:

| File | Purpose |
|---|---|
| `KiCad/PS2-BlueZZZ-Interface.kicad_pro` | KiCad project file |
| `KiCad/PS2-BlueZZZ-Interface.kicad_sch` | Schematic file |
| `KiCad/PS2-BlueZZZ-Interface.kicad_pcb` | PCB layout file |
| `Gerbers/Rev-1.0/` | Manufacturing files for Rev 1.0 |
| `BOM/PS2-BlueZZZ-Interface-BOM.csv` | Bill of materials |
| `Images/Board-Render-Front.png` | Front board render |
| `Images/Board-Render-Back.png` | Back board render |
| `Images/Assembled-Board.png` | Photo of assembled board |

## Assembly Notes

Before assembly:

- Verify the board revision
- Verify component values
- Verify component orientation
- Inspect the PCB for manufacturing issues
- Check edge solder pads for cleanliness
- Confirm the Bluetooth emitter orientation
- Confirm the MAX16054 orientation
- Confirm MOSFET or power switch orientation
- Confirm LED polarity if LEDs are installed on this board

## Pre-Power Checklist

Before applying power:

- Check for shorts between 5V and ground
- Check for shorts between switched 5V and ground
- Check for shorts on left and right audio
- Check MAX16054 pin orientation
- Check all solder joints
- Check for solder bridges
- Confirm button input is not stuck low
- Confirm CLEAR pin wiring if used
- Confirm the Bluetooth emitter is not installed backwards

## Initial Power Test

For first power-up, use a current-limited power supply when possible.

Verify:

- Board receives 5V
- MAX16054 receives correct supply voltage
- Switched 5V is off by default
- Enable button toggles switched 5V
- No parts heat up
- No abnormal current draw
- Power/status signal behaves as expected

## Bluetooth Emitter Test

After the power section is verified, test with the Bluetooth audio emitter connected.

Verify:

- Bluetooth emitter powers on when enabled
- Bluetooth emitter powers off when disabled
- Bluetooth module can pair or reconnect
- Audio passes through left and right channels
- Audio is not distorted
- Status LEDs behave as expected

## Installation Notes

When installing inside a PS2 Slim:

- Keep audio wiring short
- Keep power wiring secure
- Avoid routing audio wires near noisy power wiring
- Avoid pinching wires under the shell
- Avoid contact with RF shielding
- Use insulation where needed
- Confirm the shell closes without force
- Confirm the board does not move inside the console

## Known Concerns

Items to watch:

- Audio attenuation value may need tuning
- Bluetooth emitter revision behavior may vary
- Pair/connect behavior may need testing
- Edge solder pads need careful inspection
- Switched 5V must fully turn off
- Board height may affect shell clearance
- RF shielding may require insulation

## Revision Notes

Use this section to track interface board hardware revisions.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial layout concept |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future hardware changes |

## Related Documents

- `Documents/03-Interface-Board.md`
- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/07-Installation-Planning.md`
- `Documents/08-Testing.md`
- `Manufacturing/Assembly-Notes.md`
- `Manufacturing/QA-Checklist.md`

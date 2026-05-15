# Controller Board

The **PS2 BlueZZZ Controller Board** is the user-facing control board for the Bluetooth audio system.

The goal of this board is to give the PS2 BlueZZZ install a clean way to control Bluetooth audio from the outside or edge of the console, without running messy wiring directly to the Bluetooth emitter module.

## Purpose

The controller board is intended to handle the buttons and indicator LEDs for the Bluetooth audio system.

Instead of placing all controls directly on the Bluetooth audio emitter or interface board, the controller board allows those controls to be moved to a more practical location inside the PS2 Slim shell.

This makes the installation cleaner, easier to use, and easier to service.

## Main Functions

The controller board may provide:

- Bluetooth audio enable pushbutton
- Power/status LED
- Pair/connect pushbutton support
- Pair/connect indicator LED support
- Cleaner wiring between the shell controls and interface board
- A more finished user-facing install

## Enable Pushbutton

The enable pushbutton is used to turn the Bluetooth audio system on and off.

The controller board connects this pushbutton back to the interface board, where the MAX16054 pushbutton on/off controller handles the actual toggle behavior.

Basic operation:

- Press once to turn Bluetooth audio on
- Press again to turn Bluetooth audio off

This allows the Bluetooth audio system to be controlled by a simple momentary button.

## Power/Status LED

The controller board may include an LED to show when the Bluetooth audio system is powered on.

This gives the user quick visual feedback without needing to open the console or check the internal board.

Possible LED behavior:

- LED off: Bluetooth audio power is off
- LED on: Bluetooth audio power is on

Final LED behavior may depend on the interface board revision and wiring method used.

## Pair/Connect Button Support

The controller board may also provide support for a pair or connect button.

This would allow the user to trigger pairing or connection behavior from a cleaner location, instead of pressing the small button directly on the Bluetooth audio emitter board.

Possible uses:

- Start pairing mode
- Reconnect to a previously paired device
- Trigger the Bluetooth module connect function, if supported by the module revision
- Provide an external button after the onboard button is removed or bypassed

The exact behavior depends on the Bluetooth audio emitter module version and how the board is wired.

## Pair/Connect Indicator Support

The controller board may support a Bluetooth status LED.

This LED may be used to show connection, pairing, or activity status from the Bluetooth audio emitter.

Possible indicator uses:

- Pairing status
- Connected status
- Searching status
- Bluetooth activity indication

Final LED behavior should be verified during testing because Bluetooth module revisions may behave differently.

## Wiring Philosophy

The controller board is intended to keep wiring cleaner and more organized.

Instead of running several loose wires to multiple random points, the controller board should provide a clear connection point for the user-facing controls.

Wiring goals include:

- Keep button wiring short where possible
- Keep LED wiring clean
- Avoid crossing noisy power wiring with audio wiring
- Use labeled pads or connectors
- Make troubleshooting easier
- Make installation more repeatable

## Active-Low Control Preference

Where practical, PS2 BlueZZZ favors active-low button wiring.

This means a button press usually pulls a signal to ground instead of sending a positive voltage across the console.

Reasons for this preference:

- Simple wiring
- Reduced risk of injecting voltage into the wrong place
- Easier button handling
- Cleaner control signal routing
- Less chance of interference with nearby circuits

The final wiring should always match the schematic for the board revision being assembled.

## LED Wiring Notes

LEDs may be wired so that the controller board provides the visible indicator while the interface board provides the control signal.

Possible LED wiring styles:

- LED anode tied to local voltage through a resistor, with the control signal sinking current to ground
- LED cathode tied to ground, with the control signal sourcing current
- LED driven through a transistor inverter if the source signal polarity needs to be changed

The preferred method may vary depending on the Bluetooth emitter signal behavior and the controller board revision.

## Installation Placement

The controller board should be placed where the user can access the button and see the LED indicators.

Possible mounting locations may include:

- Near an existing shell opening
- Behind a small custom light pipe
- Near a custom button location
- On a bracket inside the shell
- Near the Bluetooth audio interface board if direct access is not required

Final placement depends on the PS2 Slim model, shell clearance, and the desired look of the build.

## Mechanical Goals

The controller board should be easy to mount and should not interfere with the console shell or internal hardware.

Mechanical goals include:

- Small footprint
- Easy button access
- Visible LED location
- Secure mounting
- Minimal shell cutting
- No pressure on the motherboard
- No interference with RF shielding
- No interference with screw posts

## Testing Checklist

Before final installation, verify:

- Enable button toggles Bluetooth audio power correctly
- Power/status LED turns on and off correctly
- Pair/connect button works as expected
- Pair/connect LED behaves as expected
- Button presses do not reset or disturb the console
- Wires are not pinched by the shell
- LEDs are visible from the intended location
- Board does not short against shielding or metal parts
- Controller board does not interfere with shell fitment

## Known Design Concerns

Items to watch during testing:

- Button bounce or inconsistent triggering
- LED polarity mistakes
- LED brightness being too high or too low
- Pair/connect behavior changing between Bluetooth module revisions
- Wires being too long or routed near noisy power circuits
- Button location being hard to reach after assembly
- Shell clearance around the button and LEDs

## Revision Notes

Use this section to track controller board changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial rough-in design |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future revision notes |

## Related Documents

- `Documents/03-Interface-Board.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/07-Installation-Planning.md`
- `Hardware/Controller-Board/README.md`
- `Manufacturing/Assembly-Notes.md`

# Interface Board

The **PS2 BlueZZZ Interface Board** is the main board that connects the Bluetooth audio emitter module to the PlayStation 2 Slim.

This board is designed to make the Bluetooth audio install cleaner, easier to solder, and easier to repeat across future builds.

## Purpose

The interface board solves several problems that come up when trying to install a Bluetooth audio emitter directly inside a PS2 Slim.

Direct wiring can work, but it can be messy and difficult to service. The Bluetooth emitter board is small, and soldering directly to it can be awkward.

The interface board gives the Bluetooth emitter a cleaner connection system and adds supporting circuitry for audio attenuation and power control.

## Main Functions

The interface board provides:

- Cleaner soldering points for the Bluetooth audio emitter
- Edge solder pads for easier assembly
- Audio input connections from the PS2
- Audio attenuation before the Bluetooth module
- 5V power switching for the Bluetooth audio emitter
- Ground connections
- Pushbutton power toggle support
- Controller board connection points
- A cleaner layout for installation inside the PS2 Slim

## Bluetooth Emitter Mounting

The interface board is designed to sit flush with the Bluetooth audio emitter board.

This helps create a compact assembly that can be mounted inside the console more cleanly than a loose board-and-wire setup.

The edge solder pads are added around the board to help join the interface board and emitter board together in a controlled way.

## Edge Solder Pads

The board includes solder pads around the edge to make the emitter easier to attach.

These pads are intended to:

- Make soldering easier
- Improve mechanical strength
- Keep the install cleaner
- Reduce loose wire clutter
- Make the board easier to inspect after assembly

The goal is to make the interface board feel like a proper adapter instead of a collection of hand-wired connections.

## Audio Input

The PS2 left and right audio signals are routed into the interface board before going to the Bluetooth audio emitter.

The audio section should be treated carefully because poor routing or incorrect levels may cause noise, imbalance, or distortion.

Audio signals include:

- Left audio
- Right audio
- Audio ground

## Audio Attenuation

The interface board includes attenuation for the PS2 audio signals.

This is needed because directly connecting the PS2 audio output to the Bluetooth audio emitter can cause distortion when the console audio gets loud.

The attenuation circuit reduces the audio signal before it reaches the Bluetooth audio emitter.

More details are documented in:

- `Documents/05-Audio-Attenuation.md`

## Power Input

The interface board receives power from the PS2 Slim.

The Bluetooth audio emitter uses a 5V supply, so the board is designed around switching and controlling the 5V feed to the emitter.

Power signals may include:

- 5V input
- Switched 5V output
- Ground

Always verify polarity before powering the board.

## Pushbutton Power Control

The interface board uses a MAX16054 pushbutton on/off controller for power control.

This allows the Bluetooth audio system to be controlled with a momentary pushbutton:

- Press once to turn Bluetooth audio on
- Press again to turn Bluetooth audio off

The MAX16054 output controls the power switching circuit for the Bluetooth audio emitter.

More details are documented in:

- `Documents/06-Pushbutton-Power-Control.md`

## Controller Board Connection

The interface board is intended to connect to a separate Bluetooth audio controller board.

The controller board may provide:

- Enable pushbutton
- Power/status LED
- Pair/connect button support
- Pair/connect indicator support

The goal is to keep the user-facing controls in a clean location while keeping the Bluetooth audio hardware mounted internally.

## Installation Notes

The interface board should be installed in a location where it:

- Does not interfere with the PS2 shell
- Does not press against the motherboard
- Does not short against RF shielding
- Does not block screw posts or mounting points
- Keeps wiring short and clean
- Allows access for inspection during testing

Final mounting may depend on the PS2 Slim motherboard revision and the internal bracket design.

## Testing Checklist

Before installing the board permanently, verify:

- No shorts between 5V and ground
- No shorts between audio left and ground
- No shorts between audio right and ground
- MAX16054 output toggles correctly
- Switched 5V turns on and off correctly
- Audio passes through both channels
- Bluetooth emitter powers on correctly
- Controller board button works
- LEDs behave as expected
- Board does not interfere with shell fitment

## Known Design Concerns

Items to watch during testing:

- Audio distortion at high game volume
- Audio imbalance between left and right channels
- Noise pickup from long wires
- Grounding issues between PS2 audio ground and digital ground
- Bluetooth pairing behavior
- Heat or current draw from the 5V rail
- Mechanical clearance inside the PS2 Slim

## Revision Notes

Use this section to track interface board changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial rough-in design |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future revision notes |

## Related Documents

- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/07-Installation-Planning.md`
- `Manufacturing/Assembly-Notes.md`
- `Hardware/Interface-Board/README.md`

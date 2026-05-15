# Pushbutton Power Control

The **PS2 BlueZZZ** interface board uses a MAX16054 pushbutton on/off controller to control power to the Bluetooth audio emitter.

The goal is to make the Bluetooth audio system easy to turn on and off with a simple momentary pushbutton.

## Purpose

The Bluetooth audio emitter does not need to be powered all the time.

The pushbutton power control circuit allows the user to enable or disable Bluetooth audio without needing a large mechanical switch.

Basic operation:

- Press once to turn Bluetooth audio on
- Press again to turn Bluetooth audio off

This keeps the install cleaner and gives the PS2 BlueZZZ system a more finished feel.

## Why Use a Pushbutton Toggle

A normal momentary pushbutton only makes contact while it is being pressed.

For this project, the button needs to act more like a power toggle.

The MAX16054 handles that behavior by latching the output state after the button is pressed.

This allows a small momentary button to control the Bluetooth audio power state.

## Main Functions

The pushbutton power control section provides:

- Momentary pushbutton input
- Debounced button handling
- Push-on / push-off toggle behavior
- Latched output state
- Default off behavior on power-up
- Control signal for the Bluetooth audio power switch
- Support for a remote enable button on the controller board

## Basic Operation

When the Bluetooth audio system is off:

- The Bluetooth audio emitter is not powered
- The power/status LED should be off
- Pressing the enable button toggles the circuit on

When the Bluetooth audio system is on:

- The Bluetooth audio emitter receives power
- The power/status LED should turn on
- Pressing the enable button again toggles the circuit off

## MAX16054 Role

The MAX16054 is used as the logic control device for the pushbutton toggle circuit.

It receives the momentary button press and produces a latched output signal.

That output is then used to control the power switching section for the Bluetooth audio emitter.

## Button Input

The button input is intended to be active-low.

This means the button pulls the input signal to ground when pressed.

This is useful because it keeps the external button wiring simple and avoids sending a positive voltage across the console shell.

Button wiring concept:

- One side of the button goes to the MAX16054 input
- The other side of the button goes to ground
- Pressing the button pulls the input low
- The MAX16054 toggles the output state

## Default Power State

The preferred default state is Bluetooth audio off when the console powers up.

This prevents the Bluetooth audio emitter from automatically powering on every time the PS2 is started.

Preferred behavior:

- Console powers on
- Bluetooth audio remains off
- User presses the enable button if Bluetooth audio is wanted

This keeps the Bluetooth audio system optional and user-controlled.

## Power Switching

The MAX16054 does not directly power the Bluetooth audio emitter by itself.

Instead, the MAX16054 output controls a power switching circuit.

The power switching circuit controls the 5V feed going to the Bluetooth audio emitter.

The purpose of switching the 5V feed is to:

- Disable the Bluetooth audio emitter when not needed
- Reduce unnecessary power draw
- Avoid unwanted Bluetooth pairing or reconnect behavior
- Keep the mod optional during normal console use

## LED Status

The controller board may include a power/status LED.

This LED should show whether the Bluetooth audio system is enabled.

Basic LED behavior:

| Bluetooth Audio State | LED State |
|---|---|
| Off | LED off |
| On | LED on |

The exact LED wiring may depend on the board revision.

Possible LED wiring methods include:

- MAX16054 output directly controlling an LED
- MAX16054 output controlling a transistor
- Switched 5V powering the LED circuit
- Active-low LED control through a sinking transistor

## Controller Board Connection

The pushbutton input may be routed to the Bluetooth audio controller board.

This allows the enable button to be mounted in a more convenient location instead of directly on the interface board.

Controller board signals may include:

- Enable button signal
- Ground
- Power/status LED control
- Optional switched 5V status
- Optional pair/connect support

## Active-Low Wiring Preference

Where practical, the enable button should use active-low wiring.

Reasons for active-low control:

- Simple button wiring
- Easier to route safely
- Less chance of injecting voltage into the wrong circuit
- Works well with pull-up style inputs
- Allows the button to simply short the signal to ground

The final wiring should always match the schematic for the board revision being assembled.

## CLEAR Input Notes

The MAX16054 includes a CLEAR input that can force the output state off.

For PS2 BlueZZZ, this may be useful for future revisions if the board needs a way to force Bluetooth audio off under certain conditions.

Possible future uses:

- Force Bluetooth audio off when the console powers down
- Force Bluetooth audio off during reset
- Add a service/test disable input
- Allow another board to control the Bluetooth audio state

If CLEAR is not used, it should be wired according to the schematic and datasheet requirements for the board revision.

## Power-Up Behavior

The power-up behavior should be tested carefully.

Expected behavior:

- Bluetooth audio should start off
- The power/status LED should remain off
- The enable button should turn the Bluetooth audio on
- Pressing the enable button again should turn it off

If the Bluetooth audio starts on by default, the circuit should be reviewed.

Possible causes:

- CLEAR wiring issue
- Output polarity issue
- MOSFET control issue
- Incorrect pull-up or pull-down value
- Wrong output pin used
- Incorrect LED or transistor wiring

## Testing Checklist

Before connecting the Bluetooth audio emitter, test the power control circuit by itself.

Verify:

- No shorts between 5V and ground
- MAX16054 receives the correct supply voltage
- Enable button pulls the input low
- Output toggles with each button press
- Output does not chatter or bounce
- Default state is off at power-up
- Switched 5V turns on and off correctly
- LED status matches the power state
- CLEAR input behaves correctly if used
- The circuit does not affect the PS2 power/reset behavior

## Testing With the Bluetooth Emitter

After the power control circuit works by itself, test it with the Bluetooth audio emitter connected.

Verify:

- Bluetooth emitter powers on when enabled
- Bluetooth emitter turns off when disabled
- Pairing or reconnect behavior works as expected
- No unexpected resets occur
- No voltage drop causes unstable Bluetooth behavior
- Power/status LED still behaves correctly
- Audio output works when Bluetooth audio is enabled
- Audio output stops when Bluetooth audio is disabled

## Known Concerns

Items to watch during testing:

- Bluetooth audio powering on by default
- Button input triggering randomly
- Long button wires picking up noise
- LED polarity mistakes
- Output polarity being reversed
- MOSFET gate not being driven correctly
- Switched 5V not fully turning off
- Bluetooth emitter reconnect behavior after power cycling
- Power draw from the 5V rail

## Troubleshooting Notes

If the button does not toggle the circuit:

- Check button wiring
- Check ground connection
- Check MAX16054 supply voltage
- Check the input pin
- Check the output pin
- Check CLEAR pin wiring
- Check for solder bridges
- Check the orientation of the MAX16054

If the Bluetooth emitter does not power on:

- Check 5V input
- Check switched 5V output
- Check MOSFET orientation
- Check gate control signal
- Check ground connection
- Check for shorts or open solder joints

If the Bluetooth emitter never turns off:

- Check whether the MOSFET is wired correctly
- Check whether the wrong MAX16054 output polarity is being used
- Check for leakage paths
- Check for solder bridges around the power switch
- Check if 5V is bypassing the switched power path

## Revision Notes

Use this section to track pushbutton power control changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial MAX16054 pushbutton toggle concept |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future power control changes |

## Related Documents

- `Documents/03-Interface-Board.md`
- `Documents/04-Controller-Board.md`
- `Documents/07-Installation-Planning.md`
- `Documents/08-Testing.md`
- `Hardware/Interface-Board/README.md`
- `Hardware/Controller-Board/README.md`
- `Manufacturing/Assembly-Notes.md`

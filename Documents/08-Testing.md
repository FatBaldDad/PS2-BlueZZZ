# Testing

This document is used to track testing for the **PS2 BlueZZZ** Bluetooth audio interface system.

Testing should verify the interface board, controller board, audio attenuation, pushbutton power control, Bluetooth behavior, and PS2 Slim fitment before the design is considered ready.

## Purpose

The purpose of testing is to make sure PS2 BlueZZZ works reliably before it is installed permanently inside a console.

Testing should confirm:

- The board powers correctly
- The pushbutton toggle works
- The Bluetooth audio emitter turns on and off correctly
- Audio passes through both channels
- Audio is not distorted
- LEDs behave as expected
- Pair/connect controls work
- The install fits inside the PS2 Slim
- The console still operates normally

## Testing Stages

Testing should be done in stages.

Recommended order:

1. Visual inspection
2. Continuity testing
3. Power testing without Bluetooth emitter installed
4. Pushbutton toggle testing
5. Switched 5V testing
6. Controller board testing
7. Bluetooth emitter testing
8. Audio attenuation testing
9. Console fitment testing
10. Full system test inside the PS2 Slim

## Visual Inspection

Before applying power, inspect the board carefully.

Check for:

- Solder bridges
- Missing components
- Incorrect component values
- Incorrect component orientation
- Damaged pads
- Lifted traces
- Poor solder joints
- Flux residue
- Shorts near fine-pitch parts
- Correct MAX16054 orientation
- Correct MOSFET orientation
- Correct connector or pad labels

Do not apply power until the board passes visual inspection.

## Continuity Testing

Use a multimeter to check for shorts and open circuits.

Before powering the board, verify:

- No short between 5V and ground
- No short between switched 5V and ground
- No short between left audio and ground
- No short between right audio and ground
- No short between left and right audio
- Button input is not stuck low
- LED connections are not shorted
- Audio attenuation resistors are connected correctly
- Ground points are connected where intended

## Power Input Testing

Test the board power input before connecting the Bluetooth audio emitter.

Verify:

- Correct 5V input
- Correct ground connection
- No excessive current draw
- No parts heating up
- MAX16054 receives correct supply voltage
- Switched 5V output is off by default, if designed that way

Record the measured voltage:

| Test Point | Expected | Measured | Pass/Fail | Notes |
|---|---:|---:|---|---|
| 5V input | 5V | TBD | TBD | TBD |
| MAX16054 VCC | 5V or design value | TBD | TBD | TBD |
| Switched 5V off state | 0V | TBD | TBD | TBD |
| Ground continuity | 0 ohms | TBD | TBD | TBD |

## Pushbutton Toggle Testing

Test the MAX16054 pushbutton toggle behavior.

Expected behavior:

- Press once: output changes state
- Press again: output changes back
- Button does not chatter
- Output stays latched after button release
- Power state does not randomly change

Test table:

| Button Press | Expected State | Measured State | Pass/Fail | Notes |
|---|---|---|---|---|
| Power-up | Off | TBD | TBD | TBD |
| Press 1 | On | TBD | TBD | TBD |
| Press 2 | Off | TBD | TBD | TBD |
| Press 3 | On | TBD | TBD | TBD |
| Press 4 | Off | TBD | TBD | TBD |

## Switched 5V Testing

The switched 5V output powers the Bluetooth audio emitter.

Before connecting the emitter, test switched 5V by itself.

Verify:

- Switched 5V is off when disabled
- Switched 5V is on when enabled
- Voltage is stable
- MOSFET or switching device does not get hot
- No unexpected voltage remains when off
- LED status matches the switched power state

Test table:

| State | Expected Switched 5V | Measured | Pass/Fail | Notes |
|---|---:|---:|---|---|
| Off | 0V | TBD | TBD | TBD |
| On | 5V | TBD | TBD | TBD |
| Off again | 0V | TBD | TBD | TBD |

## Controller Board Testing

Test the controller board before final installation.

Verify:

- Enable button works
- Power/status LED works
- Pair/connect button works, if installed
- Pair/connect LED works, if installed
- Wiring between controller board and interface board is correct
- Button presses do not cause unstable behavior
- LED brightness is acceptable for late-night use

Test table:

| Function | Expected Result | Actual Result | Pass/Fail | Notes |
|---|---|---|---|---|
| Enable button | Toggles power | TBD | TBD | TBD |
| Power LED | On when enabled | TBD | TBD | TBD |
| Pair/connect button | Triggers pair/connect | TBD | TBD | TBD |
| Pair/connect LED | Shows status | TBD | TBD | TBD |

## Bluetooth Emitter Power Testing

After switched 5V is verified, connect the Bluetooth audio emitter.

Verify:

- Bluetooth emitter powers on
- Bluetooth emitter turns off
- Power cycling works repeatedly
- Module does not lock up
- Module reconnects as expected
- No parts overheat
- No voltage drop causes unstable behavior

Test table:

| Test | Expected Result | Actual Result | Pass/Fail | Notes |
|---|---|---|---|---|
| Enable Bluetooth power | Emitter turns on | TBD | TBD | TBD |
| Disable Bluetooth power | Emitter turns off | TBD | TBD | TBD |
| Re-enable Bluetooth power | Emitter powers back on | TBD | TBD | TBD |
| Reconnect test | Reconnects to headset | TBD | TBD | TBD |

## Audio Attenuation Testing

The attenuation circuit should reduce the PS2 audio level enough to prevent distortion.

Test with multiple audio sources and game scenes.

Verify:

- Left audio works
- Right audio works
- Stereo channels are not swapped
- Audio is not distorted
- Audio is not too quiet
- Headphone volume range feels usable
- No hum, buzz, or hiss is present
- Loud scenes remain clean

Test table:

| Test | Game/Source | Attenuation Values | Result | Notes |
|---|---|---|---|---|
| Test 1 | TBD | TBD | TBD | TBD |
| Test 2 | TBD | TBD | TBD | TBD |
| Test 3 | TBD | TBD | TBD | TBD |

## Audio Quality Checklist

During audio testing, listen for:

- Distortion
- Clipping
- Crackling
- Hiss
- Hum
- Buzzing
- Low volume
- Left/right imbalance
- Missing channel
- Harsh sound during loud effects
- Audio delay or latency
- Bluetooth dropouts

## Bluetooth Pairing Testing

Pairing and reconnect behavior should be tested with more than one Bluetooth device if possible.

Test with:

- Bluetooth headphones
- Bluetooth earbuds
- Bluetooth speaker
- Previously paired device
- New device pairing
- Power-cycle reconnect behavior

Test table:

| Device | Pairing Result | Reconnect Result | Audio Quality | Notes |
|---|---|---|---|---|
| Device 1 | TBD | TBD | TBD | TBD |
| Device 2 | TBD | TBD | TBD | TBD |
| Device 3 | TBD | TBD | TBD | TBD |

## Fitment Testing

Before final installation, test fit the hardware inside the PS2 Slim shell.

Verify:

- Interface board fits
- Controller board fits
- Bracket fits
- Bluetooth emitter clears the shell
- Wires are not pinched
- RF shield does not short anything
- Screw posts are not blocked
- Shell closes without force
- Buttons are accessible
- LEDs are visible

Fitment table:

| Area | Result | Notes |
|---|---|---|
| Interface board clearance | TBD | TBD |
| Controller board clearance | TBD | TBD |
| Bracket fitment | TBD | TBD |
| RF shield clearance | TBD | TBD |
| Shell closure | TBD | TBD |
| Button access | TBD | TBD |
| LED visibility | TBD | TBD |

## Full Console Testing

After the board is installed, test the full console.

Verify:

- PS2 powers on normally
- PS2 resets normally
- Video output still works
- Wired audio still works if applicable
- Bluetooth audio can be enabled
- Bluetooth audio can be disabled
- Game audio plays correctly
- No unexpected interference occurs
- Console shell fits correctly
- Console can run for an extended period without issues

## Extended Runtime Testing

Run the console for an extended test session.

Suggested tests:

- 30-minute basic test
- 1-hour game test
- Multiple power cycles
- Multiple Bluetooth enable/disable cycles
- Multiple pairing/reconnect tests
- Loud game audio test
- Quiet game audio test

Record results:

| Test Duration | Game/Source | Result | Notes |
|---|---|---|---|
| 30 minutes | TBD | TBD | TBD |
| 1 hour | TBD | TBD | TBD |
| Multiple power cycles | TBD | TBD | TBD |

## Pass Criteria

A test revision should only be considered successful if:

- The board powers correctly
- The pushbutton toggle works reliably
- Bluetooth audio can be turned on and off
- Audio is clean and usable
- No major distortion is present
- Left and right channels work correctly
- LEDs behave correctly
- Pair/connect behavior works as expected
- The system fits inside the PS2 Slim
- The console works normally after installation

## Failure Notes

Use this section to document failures.

| Issue | Possible Cause | Fix Tried | Result |
|---|---|---|---|
| TBD | TBD | TBD | TBD |

## Known Concerns

Items to watch during testing:

- Distortion during loud audio
- Audio being too quiet after attenuation
- Bluetooth reconnect issues
- Button triggering randomly
- LED brightness being too high
- Long wires picking up noise
- Switched 5V not fully turning off
- Fitment differences between PS2 Slim revisions
- RF shield clearance
- Grounding issues

## Revision Notes

Use this section to track testing document changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial testing document |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future test updates |

## Related Documents

- `Documents/03-Interface-Board.md`
- `Documents/04-Controller-Board.md`
- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/07-Installation-Planning.md`
- `Documents/09-Known-Issues.md`
- `Test-Data/README.md`

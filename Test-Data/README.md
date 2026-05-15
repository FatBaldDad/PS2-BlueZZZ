# Test Data

This folder contains test data, notes, measurements, and validation records for the **PS2 BlueZZZ** project.

The goal of this folder is to keep real-world test information organized so hardware revisions can be improved based on actual results.

## Purpose

PS2 BlueZZZ includes audio circuitry, power switching, Bluetooth behavior, controller board wiring, and internal PS2 Slim fitment.

Testing helps confirm that the project works correctly before a board revision is considered ready.

This folder is used to document:

- Audio test results
- Power test results
- Pushbutton toggle behavior
- Bluetooth pairing and reconnect behavior
- LED behavior
- Fitment test results
- Bracket test results
- Known problems found during testing
- Changes needed for future revisions

## Folder Contents

This folder may include:

| Folder/File | Purpose |
|---|---|
| `Audio-Tests/` | Audio attenuation, distortion, volume, and channel-balance tests |
| `Power-Tests/` | 5V input, switched 5V, current draw, and MAX16054 toggle tests |
| `Fitment-Tests/` | PS2 Slim shell, bracket, board clearance, and wire-routing tests |
| `README.md` | Test data overview |

## Suggested Folder Layout

Suggested structure:

| Folder | Example Contents |
|---|---|
| `Audio-Tests/` | Audio notes, attenuation resistor tests, listening test results |
| `Power-Tests/` | Voltage readings, current draw, switched 5V tests |
| `Fitment-Tests/` | Bracket photos, shell clearance notes, console model notes |
| `Bluetooth-Tests/` | Pairing, reconnect, headset compatibility, latency notes |
| `LED-Tests/` | LED brightness, polarity, visibility, light bleed notes |
| `Photos/` | General test photos, bench setup photos, installed test photos |

## Test Goals

Testing should confirm that:

- The board powers safely
- The pushbutton toggle works reliably
- Switched 5V turns on and off correctly
- The Bluetooth audio emitter powers on and off correctly
- Audio passes through both left and right channels
- Audio is not distorted
- Audio is not too quiet
- Bluetooth pairing and reconnect behavior is acceptable
- LEDs behave correctly
- LED brightness is acceptable for late-night use
- The board fits inside the PS2 Slim
- The bracket holds the board securely
- The console shell closes without force
- The PS2 still operates normally after installation

## Test Naming

Use clear names for test files.

Recommended examples:

| Test Type | Example File Name |
|---|---|
| Audio test | `Audio-Test-Rev-1.0-Initial.md` |
| Attenuation test | `Attenuation-Values-Rev-1.0.md` |
| Power test | `Power-Test-Rev-1.0.md` |
| Fitment test | `Fitment-Test-SCPH-79001-Rev-1.0.md` |
| Bluetooth test | `Bluetooth-Reconnect-Test-Rev-1.0.md` |
| LED test | `LED-Brightness-Test-Rev-1.0.md` |

## Board Revision Tracking

Every test should record the board revision being tested.

Important revision details:

| Item | Value |
|---|---|
| Interface Board Revision | TBD |
| Controller Board Revision | TBD |
| Bracket Revision | TBD |
| Bluetooth Emitter Version | TBD |
| Console Model | TBD |
| PS2 Motherboard Revision | TBD |
| Test Date | TBD |
| Tester | TBD |

## Audio Test Notes

Audio testing should focus on distortion, volume, stereo balance, and unwanted noise.

Record:

- Game or audio source tested
- Bluetooth headphones or speaker used
- Audio attenuation resistor values
- Left channel result
- Right channel result
- Distortion result
- Volume result
- Noise, hum, or hiss
- Bluetooth latency notes
- Final opinion of the result

## Audio Test Table

| Test | Game/Source | Attenuation Values | Headphones/Receiver | Result | Notes |
|---|---|---|---|---|---|
| Test 1 | TBD | TBD | TBD | TBD | TBD |
| Test 2 | TBD | TBD | TBD | TBD | TBD |
| Test 3 | TBD | TBD | TBD | TBD | TBD |

## Power Test Notes

Power testing should confirm that the board safely controls 5V power to the Bluetooth audio emitter.

Record:

- 5V input voltage
- MAX16054 supply voltage
- Switched 5V off-state voltage
- Switched 5V on-state voltage
- Current draw when off
- Current draw when on
- Whether any part gets hot
- Whether the circuit toggles reliably

## Power Test Table

| Test Point | Expected | Measured | Pass/Fail | Notes |
|---|---:|---:|---|---|
| 5V input | 5V | TBD | TBD | TBD |
| MAX16054 VCC | Design value | TBD | TBD | TBD |
| Switched 5V off | 0V | TBD | TBD | TBD |
| Switched 5V on | 5V | TBD | TBD | TBD |
| Current draw off | TBD | TBD | TBD | TBD |
| Current draw on | TBD | TBD | TBD | TBD |

## Pushbutton Toggle Test Notes

The enable button should toggle the Bluetooth audio power state.

Expected behavior:

| Button Action | Expected Result |
|---|---|
| Power applied | Bluetooth audio off |
| Press once | Bluetooth audio on |
| Press again | Bluetooth audio off |
| Press again | Bluetooth audio on |

Record any missed presses, double-triggering, random triggering, or failure to latch.

## Bluetooth Test Notes

Bluetooth testing should confirm that the module works with real Bluetooth audio devices.

Record:

- Bluetooth emitter version
- Headphones or speaker used
- Pairing result
- Reconnect result
- Audio quality
- Delay or latency
- Dropouts
- Behavior after power cycling
- Behavior after disabling and re-enabling Bluetooth audio

## Bluetooth Test Table

| Device | Pairing Result | Reconnect Result | Audio Quality | Notes |
|---|---|---|---|---|
| Device 1 | TBD | TBD | TBD | TBD |
| Device 2 | TBD | TBD | TBD | TBD |
| Device 3 | TBD | TBD | TBD | TBD |

## LED Test Notes

LED testing should confirm that the indicators work and are not too bright.

Since PS2 BlueZZZ is intended for late-night gaming, LED brightness should be useful but not distracting.

Record:

- LED color
- Resistor value
- LED current, if measured
- Visibility through shell
- Brightness in a dark room
- Light bleed
- Whether brightness should be reduced

## LED Test Table

| LED | Resistor Value | Brightness Result | Pass/Fail | Notes |
|---|---:|---|---|---|
| Power/status LED | TBD | TBD | TBD | TBD |
| Pair/connect LED | TBD | TBD | TBD | TBD |

## Fitment Test Notes

Fitment testing should confirm that the board, bracket, and wiring fit inside the PS2 Slim.

Record:

- Console model
- Motherboard revision, if known
- Interface board revision
- Controller board revision
- Bracket revision
- Board location
- Button location
- LED location
- RF shield clearance
- Shell closure result
- Wire pinch points
- Any needed bracket changes

## Fitment Test Table

| Console Model | Board Revision | Bracket Revision | Result | Notes |
|---|---|---|---|---|
| SCPH-700xx | TBD | TBD | TBD | TBD |
| SCPH-750xx | TBD | TBD | TBD | TBD |
| SCPH-770xx | TBD | TBD | TBD | TBD |
| SCPH-790xx | TBD | TBD | TBD | TBD |

## Bracket Test Notes

Bracket testing should confirm that the board is secure and does not interfere with the console.

Record:

- Bracket revision
- Print material
- Print orientation
- Board fit
- Shell clearance
- RF shield clearance
- Wire routing
- Whether the board moves
- Whether the bracket needs changes

## Full Console Test Notes

After installation, test the full console.

Record:

- Console powers on normally
- Console resets normally
- Video works
- Bluetooth audio turns on
- Bluetooth audio turns off
- Audio works in both channels
- Audio is clean
- LEDs work
- Pair/connect function works
- Shell closes correctly
- No rattles or loose parts
- No unexpected interference

## Extended Runtime Tests

Run the console for longer sessions to check stability.

Suggested tests:

| Test | Duration | Result | Notes |
|---|---:|---|---|
| Basic power-on test | 30 minutes | TBD | TBD |
| Game audio test | 1 hour | TBD | TBD |
| Bluetooth reconnect test | TBD | TBD | TBD |
| Pushbutton cycle test | TBD | TBD | TBD |
| Heat check | TBD | TBD | TBD |

## Test Result Categories

Use simple result categories.

| Result | Meaning |
|---|---|
| Pass | Works as expected |
| Fail | Does not work as expected |
| Needs More Testing | Not enough data yet |
| Partial Pass | Works, but with a concern |
| Not Tested | Not tested yet |

## Issue Tracking

Use this table to record issues found during testing.

| Issue | Test Area | Board Revision | Severity | Notes |
|---|---|---|---|---|
| TBD | TBD | TBD | TBD | TBD |

## Severity Levels

Suggested severity levels:

| Severity | Meaning |
|---|---|
| Low | Minor issue or cosmetic concern |
| Medium | Needs improvement but does not stop testing |
| High | Must be fixed before final install or public release |
| Critical | Could damage hardware or cause unsafe behavior |

## Data To Keep

Useful data to keep:

- Multimeter readings
- Current draw readings
- Audio attenuation values
- Photos of test setup
- Photos of installed board
- Scope captures, if available
- Notes from listening tests
- Fitment photos
- Bracket revision notes
- Bluetooth device compatibility notes

## What To Avoid

Avoid storing unclear test data.

Try not to use:

- Random filenames
- Photos with no explanation
- Test notes without board revision
- Test notes without console model
- Test notes without resistor values
- Test results without pass/fail status

## Related Documents

- `Documents/08-Testing.md`
- `Documents/09-Known-Issues.md`
- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/07-Installation-Planning.md`
- `Manufacturing/QA-Checklist.md`
- `Hardware/Interface-Board/README.md`
- `Hardware/Controller-Board/README.md`
- `Hardware/Brackets/README.md`

# QA Checklist

This checklist is used for quality control on the **PS2 BlueZZZ** boards before they are installed inside a PlayStation 2 Slim console.

The goal is to catch problems before the board is powered, installed, or shipped.

## Purpose

The PS2 BlueZZZ system is installed inside a console, so each board should be inspected and tested carefully.

This checklist helps verify:

- PCB quality
- Assembly quality
- Electrical safety
- Pushbutton power control
- Bluetooth audio power switching
- Audio signal continuity
- LED behavior
- Controller board function
- Bracket fitment
- Final console operation

## Board Information

Fill this out before testing.

| Item | Value |
|---|---|
| Project | PS2 BlueZZZ |
| Board | TBD |
| Board Revision | TBD |
| Assembly Date | TBD |
| Assembled By | TBD |
| Tested By | TBD |
| Test Result | TBD |
| Notes | TBD |

## Bare PCB Inspection

Inspect the bare PCB before assembly.

| Check | Pass/Fail | Notes |
|---|---|---|
| Correct board revision | TBD | TBD |
| Board outline is correct | TBD | TBD |
| Board thickness is correct | TBD | TBD |
| Board color is correct | TBD | TBD |
| Surface finish looks good | TBD | TBD |
| No visible PCB damage | TBD | TBD |
| No scratches through copper | TBD | TBD |
| Solder mask alignment is acceptable | TBD | TBD |
| Silkscreen is readable | TBD | TBD |
| Revision marking is visible | TBD | TBD |
| Edge solder pads look correct | TBD | TBD |
| Drill holes are aligned | TBD | TBD |
| No obvious manufacturing defects | TBD | TBD |

## Assembly Inspection

Inspect the assembled board before applying power.

| Check | Pass/Fail | Notes |
|---|---|---|
| Correct components installed | TBD | TBD |
| Correct resistor values installed | TBD | TBD |
| Correct capacitor values installed | TBD | TBD |
| MAX16054 orientation correct | TBD | TBD |
| MOSFET or power switch orientation correct | TBD | TBD |
| LED polarity correct | TBD | TBD |
| Diode polarity correct, if used | TBD | TBD |
| Bluetooth emitter orientation correct | TBD | TBD |
| Connectors installed correctly, if used | TBD | TBD |
| No missing components | TBD | TBD |
| No solder bridges | TBD | TBD |
| No cold solder joints | TBD | TBD |
| No lifted pads | TBD | TBD |
| Flux residue cleaned, if needed | TBD | TBD |
| Edge solder joints inspected | TBD | TBD |

## Continuity Checks

Use a multimeter before applying power.

| Check | Expected Result | Measured/Result | Pass/Fail |
|---|---|---|---|
| 5V to GND | No short | TBD | TBD |
| Switched 5V to GND | No short | TBD | TBD |
| Left audio to GND | No short | TBD | TBD |
| Right audio to GND | No short | TBD | TBD |
| Left audio to right audio | No short | TBD | TBD |
| Ground continuity | Connected where intended | TBD | TBD |
| Enable button input | Not stuck low | TBD | TBD |
| Power LED path | No short | TBD | TBD |
| Pair/connect button path | Correct continuity | TBD | TBD |
| Pair/connect LED path | No short | TBD | TBD |

## Power Input Test

Use a current-limited power supply when possible.

| Test | Expected Result | Measured/Result | Pass/Fail |
|---|---|---|---|
| Apply 5V input | No excessive current draw | TBD | TBD |
| MAX16054 VCC | Correct supply voltage | TBD | TBD |
| Board current draw, off state | TBD | TBD | TBD |
| Board current draw, on state | TBD | TBD | TBD |
| No parts heating | No heat issue | TBD | TBD |
| Switched 5V default state | Off, unless design says otherwise | TBD | TBD |

## Pushbutton Toggle Test

Test the MAX16054 pushbutton power control.

| Test | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| Power-up state | Bluetooth power off | TBD | TBD |
| Press enable button once | Switched 5V turns on | TBD | TBD |
| Press enable button again | Switched 5V turns off | TBD | TBD |
| Press enable button multiple times | Toggles reliably | TBD | TBD |
| Button release | State remains latched | TBD | TBD |
| Random triggering | No random toggles | TBD | TBD |

## Switched 5V Test

Verify the Bluetooth audio emitter power output.

| State | Expected Switched 5V | Measured Voltage | Pass/Fail |
|---|---:|---:|---|
| Off | 0V | TBD | TBD |
| On | 5V | TBD | TBD |
| Off again | 0V | TBD | TBD |

Additional checks:

| Check | Pass/Fail | Notes |
|---|---|---|
| Switched 5V does not sag under load | TBD | TBD |
| Switched 5V fully turns off | TBD | TBD |
| No backfeeding when off | TBD | TBD |
| MOSFET or switch does not heat up | TBD | TBD |

## Controller Board Test

Test the controller board by itself and when connected to the interface board.

| Function | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| Enable button | Toggles Bluetooth power | TBD | TBD |
| Power/status LED | On when Bluetooth power is enabled | TBD | TBD |
| Power/status LED off state | Off when Bluetooth power is disabled | TBD | TBD |
| Pair/connect button | Triggers expected behavior | TBD | TBD |
| Pair/connect LED | Shows expected status | TBD | TBD |
| LED brightness | Acceptable for late-night use | TBD | TBD |
| Wiring strain relief | Wires are secure | TBD | TBD |

## Bluetooth Emitter Power Test

Connect the Bluetooth audio emitter only after power switching is verified.

| Test | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| Enable Bluetooth power | Emitter powers on | TBD | TBD |
| Disable Bluetooth power | Emitter powers off | TBD | TBD |
| Re-enable Bluetooth power | Emitter powers back on | TBD | TBD |
| Power cycle repeat test | Works repeatedly | TBD | TBD |
| Module does not overheat | No heat issue | TBD | TBD |
| Module reconnects | Reconnects as expected | TBD | TBD |

## Pairing and Connect Test

Test Bluetooth pairing behavior.

| Test | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| Pair with headset | Pairs successfully | TBD | TBD |
| Reconnect to known headset | Reconnects successfully | TBD | TBD |
| Pair/connect button | Works as expected | TBD | TBD |
| Pair/connect LED | Shows expected behavior | TBD | TBD |
| Power-cycle reconnect | Reconnects after power toggle | TBD | TBD |

## Audio Continuity Test

Check audio signal paths before doing a listening test.

| Check | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| Left audio input to attenuator | Continuity present | TBD | TBD |
| Right audio input to attenuator | Continuity present | TBD | TBD |
| Left audio output to emitter | Continuity present | TBD | TBD |
| Right audio output to emitter | Continuity present | TBD | TBD |
| Audio ground continuity | Correct connection | TBD | TBD |
| Left/right not shorted together | No short | TBD | TBD |
| Audio channels not swapped | Correct routing | TBD | TBD |

## Audio Listening Test

Test audio through Bluetooth headphones or a Bluetooth speaker.

| Test | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| Left channel | Audio present | TBD | TBD |
| Right channel | Audio present | TBD | TBD |
| Stereo balance | Balanced | TBD | TBD |
| Loud audio scene | No distortion | TBD | TBD |
| Quiet audio scene | Still audible | TBD | TBD |
| No-audio scene | No major hiss or hum | TBD | TBD |
| Headphone volume range | Usable | TBD | TBD |
| Bluetooth latency | Acceptable for intended use | TBD | TBD |

## Fitment Test

Test fit the board, bracket, and wiring inside the PS2 Slim shell.

| Check | Pass/Fail | Notes |
|---|---|---|
| Interface board fits | TBD | TBD |
| Controller board fits | TBD | TBD |
| Bracket fits | TBD | TBD |
| Bluetooth emitter clears shell | TBD | TBD |
| RF shield clearance is acceptable | TBD | TBD |
| Screw posts are not blocked | TBD | TBD |
| Shell clips are not blocked | TBD | TBD |
| Wires are not pinched | TBD | TBD |
| Shell closes without force | TBD | TBD |
| Button is accessible | TBD | TBD |
| LEDs are visible | TBD | TBD |
| No exposed pads touch metal | TBD | TBD |
| Insulation added where needed | TBD | TBD |

## Final Console Test

After installation, test the console fully assembled.

| Test | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| Console powers on normally | Pass | TBD | TBD |
| Console resets normally | Pass | TBD | TBD |
| Video output works | Pass | TBD | TBD |
| Wired audio still works, if applicable | Pass | TBD | TBD |
| Bluetooth audio can be enabled | Pass | TBD | TBD |
| Bluetooth audio can be disabled | Pass | TBD | TBD |
| Audio plays through Bluetooth device | Pass | TBD | TBD |
| No unexpected interference | Pass | TBD | TBD |
| Shell remains fully closed | Pass | TBD | TBD |
| No rattles or loose parts | Pass | TBD | TBD |

## Extended Runtime Test

Run the console long enough to check for stability.

| Test | Duration | Result | Notes |
|---|---:|---|---|
| Basic runtime test | 30 minutes | TBD | TBD |
| Game audio test | 1 hour | TBD | TBD |
| Power toggle cycle test | TBD | TBD | TBD |
| Bluetooth reconnect test | TBD | TBD | TBD |
| Heat check | TBD | TBD | TBD |

## Failure Log

Use this section to record any issues found during QA.

| Issue | Board/Revision | Possible Cause | Fix Tried | Result |
|---|---|---|---|---|
| TBD | TBD | TBD | TBD | TBD |

## Pass Criteria

A board passes QA when:

- Visual inspection passes
- Continuity checks pass
- Power input test passes
- Pushbutton toggle works reliably
- Switched 5V turns on and off correctly
- Controller board works
- Bluetooth emitter powers on and off
- Pair/connect behavior works as expected
- Audio works in both channels
- Audio is not distorted
- Board fits inside the PS2 Slim
- Console works normally after installation

## Final QA Sign-Off

| Item | Value |
|---|---|
| Board Revision | TBD |
| Passed QA | Yes / No |
| Approved For Install | Yes / No |
| Approved For Public Release | Yes / No |
| Tester | TBD |
| Date | TBD |
| Notes | TBD |

## Related Documents

- `Manufacturing/README.md`
- `Manufacturing/Assembly-Notes.md`
- `Manufacturing/JLCPCB-Notes.md`
- `Documents/08-Testing.md`
- `Documents/09-Known-Issues.md`
- `Hardware/Interface-Board/README.md`
- `Hardware/Controller-Board/README.md`
- `Hardware/Brackets/README.md`

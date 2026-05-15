# Assembly Notes

This document contains assembly notes for the **PS2 BlueZZZ** hardware.

These notes are intended to help with hand assembly, inspection, rework, and pre-install testing of the PS2 BlueZZZ interface board, controller board, and related hardware.

## Purpose

The goal of these assembly notes is to make the build process cleaner and more repeatable.

PS2 BlueZZZ is intended to be installed inside a PlayStation 2 Slim, so the assembled boards need to be:

- Clean
- Low profile
- Electrically safe
- Mechanically stable
- Easy to inspect
- Ready for internal installation

## Boards Covered

These notes may apply to:

- PS2 BlueZZZ interface board
- PS2 BlueZZZ controller board
- Bluetooth audio emitter attachment
- Internal bracket installation
- Wiring between boards
- Final console installation

## Before Assembly

Before soldering, verify:

- Correct PCB revision
- Correct schematic revision
- Correct BOM revision
- Correct component values
- Correct component packages
- Correct board thickness
- Correct Bluetooth emitter version
- Correct orientation markings
- No visible PCB damage
- No missing pads or traces

Do not begin assembly if the board revision and BOM do not match.

## Recommended Tools

Suggested tools:

- Fine-tip soldering iron
- Good flux
- Leaded or lead-free solder based on preference
- Tweezers
- Magnification
- Multimeter
- Flush cutters
- Isopropyl alcohol
- ESD-safe brush
- Kapton tape
- Current-limited bench power supply
- USB microscope, if available

## General Assembly Order

A good assembly order is:

1. Inspect bare PCB.
2. Install lowest-profile passive parts.
3. Install small ICs.
4. Install MOSFETs or switching parts.
5. Install LEDs.
6. Install connectors or wire pads, if used.
7. Clean and inspect the board.
8. Test for shorts.
9. Power the logic section.
10. Test pushbutton toggle behavior.
11. Attach the Bluetooth audio emitter.
12. Test switched 5V.
13. Test audio continuity.
14. Test Bluetooth power and pairing.
15. Install into bracket.
16. Test fit inside console.

## Bare PCB Inspection

Before installing parts, inspect the bare PCB.

Check:

- Board outline
- Edge solder pads
- Castellated or exposed edge pads, if used
- Solder mask alignment
- Silkscreen readability
- Drill alignment
- Scratches or damaged copper
- Missing pads
- Shorts between close pads
- Board thickness

Pay extra attention to the edge solder pads because they are important for attaching the Bluetooth audio emitter cleanly.

## Component Orientation

Before soldering any polarized or directional part, verify orientation.

Parts that may require orientation checks:

- MAX16054
- MOSFET or power-switching device
- LEDs
- Diodes, if used
- Polarized capacitors, if used
- Bluetooth audio emitter
- Connectors, if used

Incorrect orientation can damage parts or prevent the board from working.

## Passive Components

Install resistors and capacitors carefully.

Recommended checks:

- Confirm resistor values before soldering
- Confirm capacitor values before soldering
- Keep paired audio attenuation resistors matched between left and right channels
- Avoid tombstoning small parts
- Inspect for solder bridges
- Clean flux if needed

## Audio Attenuation Resistors

The audio attenuation section should be assembled with matching values for the left and right channels.

Check:

- Left channel resistor values
- Right channel resistor values
- Matching resistor placement
- No solder bridges
- No shorts to ground
- No left/right channel swap
- No open circuit in the audio path

Record final tested values in:

- `Documents/05-Audio-Attenuation.md`
- `Test-Data/Audio-Tests/`

## MAX16054 Assembly

The MAX16054 controls the pushbutton power toggle.

Before soldering:

- Verify package type
- Verify pin 1 location
- Verify board silkscreen orientation
- Verify no pads are bridged
- Verify CLEAR pin wiring matches the schematic
- Verify OUT or active-low OUT usage matches the design

After soldering:

- Inspect under magnification
- Check for solder bridges
- Check continuity to nearby parts
- Confirm supply and ground are not shorted

## Power Switching Section

The power switching section controls 5V to the Bluetooth audio emitter.

Before applying power:

- Verify MOSFET or switch orientation
- Verify gate/control resistor values, if used
- Verify pull-up or pull-down resistors, if used
- Verify 5V input path
- Verify switched 5V output path
- Verify there is no short to ground

The Bluetooth audio emitter should not be connected until the switched 5V output has been tested.

## LED Assembly

LEDs should be installed with correct polarity.

Before soldering LEDs:

- Confirm anode and cathode orientation
- Confirm resistor value
- Confirm whether the LED is active-high or active-low
- Confirm whether the LED is powered from switched or unswitched 5V
- Confirm LED brightness target

Since PS2 BlueZZZ is intended for late-night gaming, avoid making status LEDs overly bright.

## Controller Board Assembly

The controller board may include:

- Enable pushbutton
- Power/status LED
- Pair/connect button
- Pair/connect LED
- Connector or solder pads to interface board

Before assembly:

- Verify button footprint
- Verify LED polarity
- Verify resistor values
- Verify connector orientation, if used
- Verify wiring labels

After assembly:

- Test button continuity
- Test LED polarity
- Test ground continuity
- Test connection to the interface board

## Bluetooth Audio Emitter Attachment

The Bluetooth audio emitter should be attached carefully to the PS2 BlueZZZ interface board.

Before attaching:

- Confirm emitter orientation
- Confirm pads are clean
- Confirm edge solder pads align
- Confirm no mechanical interference
- Confirm audio, power, ground, and control pads are correct

During soldering:

- Use flux
- Use enough heat for a clean joint
- Avoid excessive solder
- Avoid bridging adjacent pads
- Avoid overheating the Bluetooth emitter
- Keep the emitter seated flush if the design requires it

After soldering:

- Inspect every edge solder joint
- Check for bridges
- Check continuity
- Check mechanical strength
- Clean flux if needed

## Edge Solder Pad Notes

The edge solder pads are intended to make the emitter easier to attach and inspect.

Good edge solder joints should:

- Wet both pads
- Have a smooth fillet
- Not bridge nearby pads
- Not create tall solder blobs
- Not interfere with bracket or shell clearance

If a joint looks dull, cracked, or incomplete, reflow it with flux.

## Wire Assembly

If wires are used, keep them clean and intentional.

General wiring notes:

- Use appropriate wire gauge
- Keep wires as short as practical
- Avoid unnecessary loops
- Avoid routing audio wires near noisy power wiring
- Use strain relief where needed
- Avoid wires crossing sharp metal edges
- Avoid wire paths that can be pinched by the shell

## Suggested Wire Groups

Keep wire groups organized.

| Wire Group | Notes |
|---|---|
| Audio left/right | Keep short and away from noisy power wiring |
| Audio ground | Route carefully to avoid hum or noise |
| 5V power | Verify polarity and secure routing |
| Ground | Verify continuity |
| Enable button | Active-low preferred where practical |
| LED wiring | Verify polarity and brightness |
| Pair/connect wiring | Verify behavior before final install |

## Cleaning

After soldering, clean the board if needed.

Cleaning goals:

- Remove sticky flux residue
- Improve inspection visibility
- Reduce possible leakage paths
- Make the board look cleaner
- Make photos easier to document

Use care around buttons, connectors, and the Bluetooth emitter.

## Visual Inspection After Assembly

After assembly, inspect:

- All solder joints
- Edge solder pads
- IC orientation
- MOSFET orientation
- LED polarity
- Resistor values
- Capacitor values
- Connector orientation
- Wire routing
- Solder bridges
- Loose parts
- Damaged pads
- Flux residue

Do not power the board until inspection is complete.

## Continuity Checks

Before applying power, use a multimeter to verify:

- No short between 5V and ground
- No short between switched 5V and ground
- No short between left audio and ground
- No short between right audio and ground
- No short between left and right audio
- Ground continuity is correct
- Button input is not stuck low
- LED wiring is not shorted
- Audio attenuation path is complete

## First Power-Up

Use a current-limited bench supply for first power-up when possible.

Initial checks:

- Apply 5V to the board
- Confirm current draw is normal
- Confirm no parts heat up
- Confirm MAX16054 receives proper supply voltage
- Confirm switched 5V is off by default
- Press enable button
- Confirm switched 5V turns on
- Press enable button again
- Confirm switched 5V turns off

Do not connect the board to the PS2 until basic power testing passes.

## Pushbutton Test

Verify the enable button works repeatedly.

| Test | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| Power applied | Bluetooth power off | TBD | TBD |
| Press 1 | Bluetooth power on | TBD | TBD |
| Press 2 | Bluetooth power off | TBD | TBD |
| Press 3 | Bluetooth power on | TBD | TBD |
| Press 4 | Bluetooth power off | TBD | TBD |

## Bluetooth Emitter Test

After the switched 5V output is verified, test the Bluetooth emitter.

Check:

- Emitter powers on
- Emitter turns off
- Status LED behaves as expected
- Pair/connect function works
- Module pairs or reconnects
- No overheating
- No unstable power behavior

## Audio Test

After power testing passes, test audio.

Check:

- Left channel works
- Right channel works
- Channels are not swapped
- Audio is not distorted
- Audio is not too quiet
- No hum or buzzing
- No clipping during loud game audio
- Bluetooth headphone volume range feels usable

Record results in:

- `Documents/08-Testing.md`
- `Test-Data/Audio-Tests/`

## Bracket Assembly

If a bracket is used, test fit the board before final installation.

Check:

- Board sits flat
- Bluetooth emitter clears bracket
- Solder joints do not interfere
- Wires have room to exit
- Board is held securely
- No exposed pads touch mounting hardware
- Bracket does not stress the PCB

## Console Fitment

Before final installation, test fit the assembled board inside the PS2 Slim.

Check:

- Interface board clearance
- Controller board clearance
- Bracket clearance
- RF shield clearance
- Shell closure
- Screw post clearance
- Wire routing
- Button access
- LED visibility

Do not force the shell closed.

## Final Pre-Install Checklist

Before installing permanently:

- Board passes visual inspection
- Board passes continuity checks
- Pushbutton toggle works
- Switched 5V works
- Bluetooth emitter powers on and off
- Audio works
- LEDs work
- Pair/connect works if installed
- Bracket fits
- Console shell closes without force
- No exposed pads can short against metal

## Common Assembly Mistakes

Common issues to watch for:

- MAX16054 installed backwards
- MOSFET installed backwards
- LED polarity reversed
- Wrong resistor values in audio attenuator
- Left and right audio swapped
- Solder bridge on edge pads
- Switched 5V bypassed accidentally
- CLEAR pin wired incorrectly
- Button input stuck low
- Audio ground connected incorrectly
- Bluetooth emitter not seated flush
- Wires routed where the shell pinches them

## Rework Notes

If rework is needed:

- Use flux
- Use controlled heat
- Avoid lifting small pads
- Avoid overheating the Bluetooth emitter
- Inspect after every change
- Clean the area after rework
- Retest continuity before applying power

## Revision Notes

Use this section to track assembly note changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial assembly notes |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future assembly updates |

## Related Documents

- `Manufacturing/README.md`
- `Manufacturing/JLCPCB-Notes.md`
- `Manufacturing/QA-Checklist.md`
- `Documents/03-Interface-Board.md`
- `Documents/04-Controller-Board.md`
- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/07-Installation-Planning.md`
- `Documents/08-Testing.md`
- `Hardware/Interface-Board/README.md`
- `Hardware/Controller-Board/README.md`
- `Hardware/Brackets/README.md`

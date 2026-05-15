# Installation Planning

The **PS2 BlueZZZ** system is designed for clean internal installation inside a PlayStation 2 Slim console.

This document is used to plan fitment, mounting, wiring, button placement, LED placement, and general installation layout before final assembly.

## Purpose

The goal of installation planning is to make sure the Bluetooth audio system fits cleanly inside the PS2 Slim before anything is permanently mounted.

A working circuit is only part of the project. The install also needs to be:

- Clean
- Secure
- Serviceable
- Safe
- Repeatable
- Practical inside the console shell

## Install Components

A full PS2 BlueZZZ install may include:

- Bluetooth audio emitter module
- PS2 BlueZZZ interface board
- PS2 BlueZZZ controller board
- Internal mounting bracket
- Enable pushbutton
- Power/status LED
- Pair/connect button wiring
- Pair/connect LED wiring
- Audio input wiring
- 5V power wiring
- Ground wiring

## Main Installation Goals

The installation should:

- Fit fully inside the PS2 Slim shell
- Avoid interfering with the motherboard
- Avoid interfering with the RF shield
- Avoid interfering with screw posts
- Avoid blocking shell clips
- Avoid creating pressure points
- Keep wiring short and clean
- Keep audio wiring away from noisy power wiring
- Make the button and LEDs usable from the outside
- Allow the console to close normally

## Board Placement

The interface board should be placed where it has enough room around it and does not press into the shell or metal shielding.

Placement considerations:

- Board height
- Bluetooth emitter height
- Solder joint clearance
- Wire exit direction
- Nearby screw posts
- Nearby shell clips
- Nearby metal shielding
- Distance to audio source points
- Distance to 5V power source
- Distance to controller board location

## Controller Board Placement

The controller board should be placed where the user can access the enable button and see the status LEDs.

Possible locations may include:

- Near an existing shell opening
- Near a custom button location
- Near the front or side of the shell
- Behind a small light pipe
- On an internal bracket
- Near the Bluetooth interface board if external access is not required

The final location should be easy to use but should not require unnecessary shell cutting.

## Bracket Planning

The bracket should hold the Bluetooth audio hardware securely inside the console.

Bracket goals include:

- Hold the interface board in place
- Support the Bluetooth audio emitter
- Avoid shorting against metal parts
- Avoid stress on solder joints
- Keep the board from moving during transport
- Keep the board serviceable
- Fit without forcing the shell closed

## Shell Clearance

Before final mounting, test shell clearance carefully.

Check for:

- Top shell interference
- Bottom shell interference
- RF shield interference
- Screw post interference
- Button clearance
- LED clearance
- Wire pinch points
- Board flexing
- Pressure on the Bluetooth emitter
- Pressure on solder pads

Do not force the console shell closed. If the shell does not close naturally, something needs to be adjusted.

## Wiring Plan

Wiring should be planned before soldering.

The main wiring groups are:

- Audio wiring
- Power wiring
- Ground wiring
- Button wiring
- LED wiring
- Pair/connect wiring

Each wire group should be routed in a way that keeps the install clean and avoids unnecessary interference.

## Audio Wiring

Audio wiring should be treated carefully because it can pick up noise.

Audio wiring goals:

- Keep audio wires short
- Keep left and right channels routed together
- Keep audio wiring away from switching power wiring
- Avoid routing audio near high-current paths
- Avoid unnecessary loops
- Use a clean audio ground reference
- Verify left and right channels before final assembly

Audio signals:

- Left audio
- Right audio
- Audio ground

## Power Wiring

The Bluetooth audio emitter uses 5V power.

Power wiring goals:

- Use a clean 5V source
- Verify polarity before connecting the board
- Keep power wiring secure
- Avoid thin or fragile wires for power
- Avoid routing power wires where they can be pinched
- Confirm switched 5V turns on and off correctly

Power signals:

- 5V input
- Switched 5V output
- Ground

## Ground Wiring

Ground wiring should be clean and intentional.

Ground planning should consider:

- Main board ground
- Audio ground
- Controller board ground
- Button ground
- LED ground
- Bluetooth emitter ground

Poor grounding can cause noise, unstable operation, or incorrect LED behavior.

## Button Wiring

The enable button is intended to be a momentary pushbutton.

Button wiring goals:

- Keep wiring simple
- Use active-low wiring where practical
- Avoid running button wiring near noisy power traces
- Make the button easy to press
- Avoid mounting the button where it can be pressed accidentally
- Verify the button toggles the MAX16054 correctly

## LED Placement

LEDs should be visible but not distracting.

LED planning should consider:

- Power/status LED visibility
- Pair/connect LED visibility
- LED brightness
- Light bleed through the shell
- Light pipe options
- Resistor values
- LED polarity
- Whether the LED is too bright in a dark room

Since this project is intended for late-night gaming, LED brightness should be kept reasonable.

## Pair/Connect Control

Pair/connect behavior may depend on the Bluetooth audio emitter revision.

Before finalizing the install, verify:

- Which pad or button controls pairing
- Whether the onboard button is being removed
- Whether an external button is wired in parallel
- Whether a separate connect pad is being used
- Whether firmware settings affect connect behavior
- Whether the button works after final assembly

## Mechanical Safety

The installed board should not create any mechanical risk inside the console.

Check for:

- Exposed pads touching shielding
- Wires rubbing on sharp metal
- Boards moving inside the shell
- Solder joints under stress
- Bracket flex
- Loose hardware
- Wires near moving parts
- Wires near hot parts
- Pressure on the motherboard

Use insulation where needed.

## Electrical Safety

Before powering the console, verify:

- No shorts between 5V and ground
- No shorts between audio lines and ground
- No shorts between switched 5V and ground
- No reversed polarity
- No solder bridges
- No loose strands of wire
- No exposed pads touching metal
- MAX16054 orientation is correct
- MOSFET orientation is correct
- Bluetooth emitter orientation is correct

## Pre-Install Bench Test

Before mounting the system inside the PS2 Slim, test the board outside the console when possible.

Bench test items:

- 5V input
- MAX16054 toggle behavior
- Switched 5V output
- Power/status LED
- Pair/connect button
- Pair/connect LED
- Left audio continuity
- Right audio continuity
- Ground continuity
- Bluetooth emitter power-on behavior

## Console Test Fit

Before soldering final wires, test fit the parts inside the console.

Check:

- Interface board location
- Controller board location
- Bracket location
- Wire routing
- Shell clearance
- Button access
- LED visibility
- RF shield clearance
- Screw installation
- Final shell closure

## Final Install Checklist

Before closing the console:

- Board is mounted securely
- Bracket is installed correctly
- Wires are routed cleanly
- Wires are not pinched
- Wires are not under tension
- Audio wiring is separated from noisy power wiring
- 5V and ground are verified
- Enable button works
- LEDs work
- Bluetooth emitter powers on and off
- Audio works in both channels
- Pair/connect behavior works
- Shell closes without force

## Post-Install Testing

After the console is fully assembled, test:

- Console powers on normally
- Bluetooth audio stays off by default, if designed that way
- Enable button turns Bluetooth audio on
- Enable button turns Bluetooth audio off
- Bluetooth device pairs or reconnects
- Audio plays through Bluetooth headphones
- Left and right channels are correct
- Audio is not distorted
- No buzzing, hum, or hiss is present
- LEDs are visible but not too bright
- Shell does not flex or press on the board
- Console still operates normally without Bluetooth audio enabled

## Known Fitment Concerns

Items to watch during install:

- Different PS2 Slim board revisions may have different clearances
- RF shield shape may affect bracket placement
- Shell clips may interfere with board placement
- Button placement may require small shell modifications
- LED placement may need light pipes or small openings
- Wires may be pinched near screw posts
- Board height may be greater than expected after soldering

## Revision Notes

Use this section to track installation planning changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial installation planning document |
| Rev 1.0 | First public/test install notes |
| Rev 1.1 | Future fitment updates |

## Related Documents

- `Documents/03-Interface-Board.md`
- `Documents/04-Controller-Board.md`
- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/08-Testing.md`
- `Hardware/Brackets/README.md`
- `Manufacturing/Assembly-Notes.md`

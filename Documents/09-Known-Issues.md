# Known Issues

This document tracks known issues, concerns, limitations, and items that need more testing for the **PS2 BlueZZZ** project.

The goal is to keep problems visible so they can be tested, fixed, or improved in future revisions.

## Purpose

PS2 BlueZZZ is an active hardware project, so some items may still need testing or revision.

This document is used to track:

- Known hardware issues
- Possible fitment problems
- Audio problems
- Bluetooth behavior problems
- Power control problems
- Assembly concerns
- Installation concerns
- Items that need more testing

## Current Status

The project is currently in development and testing.

Some issues listed here may be temporary and may be resolved in later board revisions.

## Known Issue Summary

| Issue | Status | Priority | Notes |
|---|---|---|---|
| Audio attenuation value still needs final testing | Open | High | Final resistor values need to be verified with real PS2 audio |
| Bluetooth module revision behavior may vary | Open | Medium | Different KCX_BT_EMITTER versions may behave differently |
| Pair/connect pad behavior needs confirmation | Open | Medium | Button and pad behavior should be tested before final documentation |
| Controller board LED polarity needs verification | Open | Medium | LED behavior depends on final wiring method |
| Internal bracket fitment needs console testing | Open | High | Fitment may vary by PS2 Slim model and motherboard revision |
| LED brightness may be too high for late-night use | Open | Low | Final resistor values may need adjustment |

## Audio Issues

### Possible Distortion

The PS2 audio signal may be too strong for the Bluetooth audio emitter if connected directly.

The interface board includes attenuation to reduce the signal level, but the final resistor values need to be tested.

Possible symptoms:

- Harsh audio
- Crackling
- Clipping
- Distortion during loud game scenes
- Audio sounds fine at low volume but bad during loud effects

Possible fixes:

- Increase attenuation
- Test different resistor values
- Verify audio ground
- Check left and right audio routing
- Confirm the Bluetooth module input is not being overdriven

### Audio Too Quiet

If the attenuation is too strong, the Bluetooth output may become too quiet.

Possible symptoms:

- Headphones need to be turned up too high
- Quiet game audio is hard to hear
- Background hiss becomes more noticeable
- Audio feels weak compared to normal output

Possible fixes:

- Reduce attenuation
- Test alternate resistor values
- Verify the audio source point on the PS2 motherboard
- Test with more than one Bluetooth headset or speaker

### Left/Right Channel Imbalance

The left and right channels should have matching attenuation.

Possible symptoms:

- One side sounds louder than the other
- Stereo image sounds shifted
- One channel is missing or weak

Possible fixes:

- Verify matching resistor values on both channels
- Check solder joints
- Check continuity from PS2 audio source to Bluetooth module
- Confirm left and right channels are not swapped
- Confirm neither channel is shorted to ground

## Bluetooth Issues

### Pairing Behavior May Vary

The Bluetooth emitter module may behave differently depending on revision or firmware.

Possible symptoms:

- Pairing button does not behave as expected
- Connect pad does not trigger the expected function
- Module reconnects differently after power cycling
- Module pairs with some devices but not others

Possible fixes:

- Confirm the exact Bluetooth emitter revision
- Test onboard button behavior before removing or bypassing it
- Test external pair/connect button wiring
- Document behavior for each tested module version
- Test with multiple headphones or speakers

### Bluetooth Reconnect Delay

After power cycling the Bluetooth emitter, it may take time to reconnect.

Possible symptoms:

- Audio does not start immediately
- Headphones connect after a delay
- Module requires another button press
- Module connects inconsistently

Possible fixes:

- Allow enough time for reconnect testing
- Test with the same headset over multiple cycles
- Record reconnect timing
- Test whether power cycling or pair/connect input changes behavior

### Bluetooth Latency

Bluetooth audio may have noticeable delay.

Possible symptoms:

- Audio is slightly behind video
- Timing-sensitive games feel different
- Button press sounds are delayed

Possible notes:

- Some Bluetooth latency is expected
- Latency may depend on the Bluetooth headset or speaker
- This project is mainly intended for quiet late-night play, not latency-critical competitive use

## Power Control Issues

### Bluetooth Audio Starts On By Default

The preferred behavior is for Bluetooth audio to start off when the console powers up.

Possible symptoms:

- Bluetooth module powers on immediately
- Power/status LED is on at console startup
- Enable button turns the system off instead of on

Possible fixes:

- Check MAX16054 output polarity
- Check CLEAR pin wiring
- Check MOSFET orientation
- Check pull-up or pull-down resistors
- Confirm whether active-high or active-low output is being used

### Pushbutton Does Not Toggle

The enable button should toggle Bluetooth audio power on and off.

Possible symptoms:

- Button does nothing
- Button only works once
- Button works randomly
- Button must be held down
- Output chatters or toggles more than once

Possible fixes:

- Check button wiring
- Check ground connection
- Check MAX16054 orientation
- Check input pin soldering
- Check CLEAR pin state
- Check for solder bridges
- Check if the button wire is too long or routed near noisy signals

### Switched 5V Does Not Fully Turn Off

The Bluetooth emitter should lose power when disabled.

Possible symptoms:

- Bluetooth module stays partially powered
- LED glows dimly when off
- Bluetooth reconnects even when disabled
- Switched 5V measures above 0V when off

Possible fixes:

- Check MOSFET orientation
- Check for alternate power paths
- Check LED wiring
- Check pull-up or pull-down values
- Check whether signal lines are backfeeding the module
- Check for solder bridges around the power switch

## LED Issues

### LED Too Bright

Since PS2 BlueZZZ is intended for late-night gaming, LEDs should not be distracting.

Possible symptoms:

- LED is too bright in a dark room
- LED shines through the shell too strongly
- LED creates unwanted light bleed

Possible fixes:

- Increase LED resistor value
- Use a dimmer LED
- Use a smaller indicator window
- Use a light pipe with diffusion
- Reduce LED current

### LED Does Not Turn On

Possible symptoms:

- Power/status LED stays off
- Pair/connect LED stays off
- LED only flashes briefly
- LED works only when touched or moved

Possible fixes:

- Check LED polarity
- Check resistor value
- Check solder joints
- Check control signal polarity
- Check whether the LED needs an inverter or transistor driver
- Check whether the board expects active-high or active-low LED control

### LED Is On When It Should Be Off

Possible symptoms:

- LED glows when Bluetooth power is disabled
- LED is inverted
- LED faintly glows due to leakage
- Pair/connect LED does not match module status

Possible fixes:

- Check LED wiring style
- Check signal polarity
- Check transistor orientation
- Check pull-up or pull-down resistors
- Check if the LED is connected to switched 5V or unswitched 5V

## Fitment Issues

### Board Clearance

The interface board and Bluetooth emitter assembly must fit inside the PS2 Slim without forcing the shell closed.

Possible symptoms:

- Shell does not close fully
- Shell flexes near the board
- Board presses against shielding
- Board presses against the top shell
- Solder joints touch metal parts

Possible fixes:

- Move the board location
- Revise bracket height
- Add insulation
- Shorten solder joints where possible
- Check shell clearance before final wiring

### Bracket Fitment

The bracket may need changes after real console testing.

Possible symptoms:

- Bracket does not sit flat
- Bracket interferes with screw posts
- Bracket blocks shell clips
- Bracket holds the board too high
- Bracket allows the board to move

Possible fixes:

- Revise bracket model
- Add clearance cuts
- Adjust mounting points
- Lower board height
- Add support features
- Test fit in multiple Slim revisions

### Wire Pinch Points

Wires must not be pinched when the shell is closed.

Possible symptoms:

- Console shell does not close smoothly
- Wire insulation is damaged
- Button or LED stops working after closing shell
- Audio cuts in and out when shell is moved

Possible fixes:

- Reroute wires
- Use thinner wire where appropriate
- Secure wires with tape or adhesive
- Avoid screw posts and shell clips
- Check all wire paths before final assembly

## Assembly Issues

### Edge Solder Pads Need Careful Inspection

The interface board uses edge solder pads to help connect cleanly to the Bluetooth emitter.

Possible symptoms:

- Weak solder joint
- Cold solder joint
- Solder bridge between pads
- Poor mechanical connection
- Pad lifts during rework

Possible fixes:

- Use flux
- Use proper heat
- Inspect under magnification
- Avoid excessive solder
- Avoid excessive mechanical force
- Rework carefully

### Component Orientation Mistakes

Some parts must be installed in the correct orientation.

Parts to verify:

- MAX16054
- MOSFET or power switch device
- LEDs
- Diodes, if used
- Polarized capacitors, if used
- Bluetooth emitter orientation

Possible fixes:

- Check schematic
- Check board silkscreen
- Check datasheets
- Check continuity before power
- Use current-limited bench power for first power-up

## Grounding Issues

Grounding problems may cause noise or unstable behavior.

Possible symptoms:

- Hum or buzz in audio
- Bluetooth module behaves unpredictably
- LED behavior is inconsistent
- Button triggers randomly
- Audio quality changes when touching the board

Possible fixes:

- Verify ground continuity
- Confirm audio ground routing
- Keep audio wiring away from power wiring
- Avoid unnecessary ground loops
- Check all solder joints
- Review grounding plan in the schematic

## Items Needing More Testing

The following items should be tested and documented:

- Final audio attenuation resistor values
- Best PS2 audio pickup points
- Bluetooth emitter V1.7 behavior
- Pair/connect pad behavior
- External button behavior
- Power/status LED brightness
- Pair/connect LED behavior
- MAX16054 default off behavior
- Switched 5V off-state leakage
- Fitment in different PS2 Slim revisions
- Bracket fitment
- Long-term runtime behavior
- Bluetooth reconnect behavior after power cycling

## Resolved Issues

Use this section to move issues once they are fixed.

| Issue | Resolution | Revision Fixed | Notes |
|---|---|---|---|
| TBD | TBD | TBD | TBD |

## Revision Notes

Use this section to track known-issues document changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial known issues document |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future issue updates |

## Related Documents

- `Documents/03-Interface-Board.md`
- `Documents/04-Controller-Board.md`
- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/07-Installation-Planning.md`
- `Documents/08-Testing.md`
- `Test-Data/README.md`

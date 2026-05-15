# Design Goals

The goal of **PS2 BlueZZZ** is to make internal Bluetooth audio installation in a PlayStation 2 Slim cleaner, easier, and more repeatable.

This project is not just about making Bluetooth audio work. It is about building a small system that can be installed neatly, documented properly, revised over time, and shared publicly.

## Primary Goal

The primary goal is to allow late-night PS2 gaming with Bluetooth headphones.

The system should let the user play without disturbing people nearby, while keeping the console clean and practical to use.

## Hardware Goals

The hardware should be designed around clean integration inside a PS2 Slim.

Main hardware goals include:

- Keep the Bluetooth audio install compact
- Reduce messy point-to-point wiring
- Provide cleaner soldering points
- Mount the Bluetooth audio emitter securely
- Support a separate controller board for buttons and LEDs
- Include audio attenuation to reduce distortion
- Include pushbutton-controlled power
- Keep the design serviceable after installation
- Keep the install repeatable for future builds

## Interface Board Goals

The interface board should make the Bluetooth audio emitter easier to use inside the console.

The board should:

- Sit flush with the Bluetooth audio emitter
- Provide larger solder pads around the board edge
- Make the emitter easier to solder cleanly
- Provide connection points for audio, power, ground, and control signals
- Support the audio attenuation circuit
- Support the MAX16054 pushbutton power control circuit
- Help keep the wiring organized inside the console

## Audio Goals

The audio section should reduce the chance of distortion.

The PS2 audio signal may be too strong when connected directly to the Bluetooth audio emitter. The interface board includes attenuation to dial back the signal before it reaches the Bluetooth module.

Audio goals include:

- Reduce input level going into the Bluetooth audio emitter
- Prevent distortion during loud game audio
- Keep left and right audio channels balanced
- Keep the analog audio wiring clean
- Avoid unnecessary noise pickup
- Document tested resistor values and results

## Power Control Goals

The Bluetooth audio system should be easy to turn on and off.

The board uses a pushbutton toggle design so the user does not need a bulky mechanical switch.

Power control goals include:

- Press once to turn Bluetooth audio on
- Press again to turn Bluetooth audio off
- Use a remote momentary pushbutton
- Keep power control simple and reliable
- Allow the Bluetooth audio board to be disabled when not needed
- Provide a way to show power status with an LED

## Controller Board Goals

The controller board should provide the user-facing side of the system.

This board may include:

- Enable button
- Power/status LED
- Pair/connect button support
- Pair/connect indicator support
- Clean wiring back to the interface board

The controller board should make the install feel more finished and less like a loose internal mod.

## Bracket Goals

The bracket should help mount the Bluetooth audio hardware inside the PS2 Slim.

Bracket goals include:

- Hold the board securely
- Fit inside the PS2 Slim shell
- Avoid interfering with other parts of the console
- Keep the install clean and repeatable
- Make the board easier to position during assembly
- Allow future revisions if fitment needs to change

## Documentation Goals

This repository should keep all project information in one place.

Documentation goals include:

- Explain what the project does
- Track hardware revisions
- Store KiCad files
- Store manufacturing files
- Store bracket files
- Document assembly steps
- Document install notes
- Document test results
- Record known issues
- Make the project easier for others to understand

## Manufacturing Goals

The board should be practical to fabricate and assemble.

Manufacturing goals include:

- Use common PCB fabrication services
- Keep board thickness and layout practical
- Use readable silkscreen labels
- Keep solder pads easy to access
- Make assembly inspection easier
- Track BOM changes between revisions
- Keep manufacturing notes organized

## Serviceability Goals

The install should not be impossible to troubleshoot after it is built.

Serviceability goals include:

- Keep important signals labeled
- Keep wiring paths understandable
- Make the board easier to inspect
- Allow power and audio issues to be tested
- Document common failure points
- Document known problems and fixes

## Revision Goals

This project is expected to improve over time.

Revision goals include:

- Track what changed between board versions
- Record why each change was made
- Keep notes from real-world testing
- Use test results to guide the next revision
- Keep older revisions documented for reference

## Overall Design Philosophy

PS2 BlueZZZ should be simple, clean, and useful.

The design should avoid unnecessary complexity when a simpler solution works. The goal is a practical Bluetooth audio install that looks intentional, installs cleanly, and can be improved over time.

# PS2 BlueZZZ Project Overview

**PS2 BlueZZZ** is a Bluetooth audio integration project for PlayStation 2 Slim consoles.

The goal of this project is to make internal Bluetooth audio installs cleaner, easier to build, easier to document, and easier to repeat across future PS2 Slim builds.

## Project Purpose

PS2 BlueZZZ was created for late-night gaming.

The idea is simple: allow someone to play a PlayStation 2 with Bluetooth headphones so they can enjoy the console without disturbing people nearby.

This project is not just about adding Bluetooth audio. It is about making the installation cleaner, more reliable, and easier to reproduce.

## What This Project Includes

PS2 BlueZZZ includes several related parts:

- Bluetooth audio interface board
- Bluetooth audio controller board
- Internal installation bracket
- Audio attenuation circuit
- Pushbutton power toggle circuit
- Board revision tracking
- Installation notes
- Manufacturing notes
- Test results and validation notes

## Main Hardware Concept

The interface board is designed to sit flush with the Bluetooth audio emitter module.

Instead of soldering loose wires directly to the small Bluetooth emitter pads, the interface board provides larger and cleaner solder points around the edge of the board. This makes the install easier to assemble and easier to inspect.

The board also includes an attenuation circuit to lower the PS2 audio signal before it enters the Bluetooth audio module. This helps reduce distortion when the game audio level is high.

## Power Control

The board uses a MAX16054 pushbutton on/off controller.

This allows the Bluetooth audio system to be controlled with a simple momentary pushbutton:

- Press once to turn Bluetooth audio on
- Press again to turn Bluetooth audio off

This makes the Bluetooth audio system easier to control from outside the console without needing a bulky mechanical switch.

## Controller Board

The Bluetooth audio controller board is intended to provide the user-facing controls and indicators for the system.

This may include:

- Bluetooth audio enable button
- Power/status LED
- Pair/connect button support
- Pair/connect indicator support
- Cleaner wiring between the PS2 shell and the internal Bluetooth audio hardware

## Installation Bracket

The project also includes bracket support for mounting the Bluetooth audio hardware inside the PS2 Slim.

The bracket is part of the project because fitment matters. A working circuit is only useful if it can be installed cleanly, safely, and consistently inside the console.

## Why This Matters

A one-off Bluetooth audio install can be done with wires, glue, and patience.

PS2 BlueZZZ is meant to turn that idea into a more organized hardware project.

The goals are:

- Cleaner soldering
- Cleaner mounting
- Less messy wiring
- Better documentation
- Repeatable installation
- Easier troubleshooting
- Public revision tracking

## Current Development Focus

The current focus is to prove the first working version of the system.

This includes:

- Verifying the interface board fitment
- Testing the audio attenuation values
- Testing Bluetooth audio quality
- Testing pushbutton power control
- Testing controller board wiring
- Testing bracket fitment inside the PS2 Slim
- Documenting any issues found during assembly and installation

## Long-Term Goal

The long-term goal is to make PS2 BlueZZZ a clean, documented, open hardware reference for adding Bluetooth audio to PS2 Slim consoles.

The project should be useful for:

- Personal PS2 builds
- Future Fat Bald Dad builds
- Other modders who want a cleaner Bluetooth audio install
- Revision tracking and public feedback
- Documenting what works and what needs improvement

## Project Status

This project is currently in active development.

More information will be added as the boards are assembled, tested, revised, and installed into real PS2 Slim consoles.

# Source Links

This document collects source links, reference links, datasheets, and related project material for the **PS2 BlueZZZ** project.

The goal is to keep important references in one place so the project can be documented, revised, and verified more easily.

## Purpose

PS2 BlueZZZ uses a combination of custom hardware and existing modules.

This file is used to track references for:

- Bluetooth audio emitter module information
- KCX_BT_EMITTER programming notes
- KCX_BT_EMITTER V1.7 notes
- MAX16054 pushbutton on/off controller
- PCB manufacturing notes
- PS2 Slim installation research
- Audio attenuation notes
- Related projects and forum discussions

## Important Note

Some links may change or disappear over time.

When using any source, record:

- What information was used
- Date accessed
- Hardware revision involved
- Any uncertainty
- Any testing needed to confirm the information

Do not assume all module versions behave the same.

## Main Project References

| Topic | Link | Notes |
|---|---|---|
| KCX_BT_EMITTER GitHub reference | https://github.com/Mark-MDO47/BluetoothAudioTransmitter_KCX_BT_EMITTER | Useful reference for KCX_BT_EMITTER programming and notes |
| KCX_BT_EMITTER V1.7 branch | https://github.com/Mark-MDO47/BluetoothAudioTransmitter_KCX_BT_EMITTER/tree/KCX_BT_EMITTER_V1.7 | Branch for V1.7 module behavior and updated commands |
| Pandel V1.7 fork/reference | https://github.com/pandel/BluetoothAudioTransmitter_KCX_BT_EMITTER/tree/v1.7 | V1.7-related updates and command handling |
| KCX_BT_EMITTER Electro-Tech thread | https://www.electro-tech-online.com/threads/kcx_bt_emitter-low-cost-bluetooth-bt-audio-module.158156/ | Forum discussion with useful module notes |
| KCX_BT_EMITTER AliExpress listing | https://www.aliexpress.com/item/33058710334.html | Marketplace listing and module source reference |
| KCX_BT_EMITTER Taobao listing | https://item.taobao.com/item.htm?id=570274835710 | Original/alternate listing reference; may require translation |
| MAX16054 product page | https://www.analog.com/en/products/max16054.html | Pushbutton on/off controller reference |
| MAX16054 datasheet | https://www.analog.com/media/en/technical-documentation/data-sheets/MAX16054.pdf | Datasheet for pushbutton latch controller |

## KCX_BT_EMITTER Notes

The KCX_BT_EMITTER is the Bluetooth audio module used by this project.

Important project-related notes:

- Used as the Bluetooth audio emitter/transmitter
- Accepts stereo audio input
- Can be used for Bluetooth headphone or speaker output
- May support AT-command configuration depending on module version
- Module revision matters
- Pair/connect behavior may vary between versions
- LED behavior may vary between versions
- Some documentation may be translated or incomplete

## KCX_BT_EMITTER Version Notes

Different versions of the KCX_BT_EMITTER may behave differently.

Known versions or references may include:

| Version | Notes |
|---|---|
| V1.1 | Older module/version referenced in early documentation |
| V1.4 | Replacement/update mentioned in module listing notes |
| V1.7 | Newer version with updated AT command behavior |
| V1.7 Bluetooth 5.3 listing | Newer listing describes Bluetooth 5.3 audio transceiver behavior |

When documenting tests, always record the exact version of the module being used.

## Bluetooth Audio Input Notes

The Bluetooth audio emitter should be treated as a line-level audio device.

For PS2 BlueZZZ, this matters because the PS2 audio signal may need attenuation before going into the module.

Related project document:

- `Documents/05-Audio-Attenuation.md`

## Bluetooth Pair/Connect Notes

The pair/connect behavior needs testing on the exact module version used.

Items to verify:

- Onboard button behavior
- External button behavior
- CONNECT pad behavior
- LINK pad behavior
- Pairing mode behavior
- Reconnect behavior after power cycle
- LED status behavior
- AT-command behavior, if used

Related project documents:

- `Documents/04-Controller-Board.md`
- `Documents/08-Testing.md`
- `Documents/09-Known-Issues.md`

## MAX16054 Notes

The MAX16054 is used for pushbutton-controlled power switching.

Important project-related notes:

- Pushbutton on/off controller
- Built-in debounce
- Latched output
- Momentary pushbutton input
- Useful for push-on / push-off behavior
- Operates from a low-voltage supply range suitable for logic control
- Provides complementary outputs
- Includes CLEAR input for forcing the output off

Related project document:

- `Documents/06-Pushbutton-Power-Control.md`

## MAX16054 Project Use

PS2 BlueZZZ uses the MAX16054 so the Bluetooth audio system can be controlled with a simple momentary pushbutton.

Expected behavior:

| Button Action | Result |
|---|---|
| Press once | Bluetooth audio turns on |
| Press again | Bluetooth audio turns off |

The final board revision should document which MAX16054 output is used and how it controls the power-switching circuit.

## PCB Manufacturing References

PCB manufacturing notes should be kept in:

- `Manufacturing/JLCPCB-Notes.md`

Useful manufacturing references may include:

| Topic | Link | Notes |
|---|---|---|
| JLCPCB | https://jlcpcb.com/ | PCB manufacturing service |
| JLCPCB capabilities | https://jlcpcb.com/capabilities/Capabilities | Verify current PCB fabrication limits before ordering |
| JLCPCB assembly | https://jlcpcb.com/smt-assembly | Assembly service reference, if used |
| KiCad | https://www.kicad.org/ | PCB design software used for the project |

Always verify the current JLCPCB order page before placing an order.

## KiCad References

PS2 BlueZZZ hardware is designed in KiCad.

Useful KiCad references:

| Topic | Link | Notes |
|---|---|---|
| KiCad website | https://www.kicad.org/ | Main KiCad project page |
| KiCad documentation | https://docs.kicad.org/ | Official KiCad documentation |
| KiCad forum | https://forum.kicad.info/ | Community support and troubleshooting |

## PS2 Slim Reference Notes

PS2 Slim installation details may vary by console model and motherboard revision.

Important PS2-related information to document:

- Console model
- Motherboard revision
- Audio pickup points
- 5V source point
- Ground point
- RF shield clearance
- Shell clearance
- Bracket fitment
- Button location
- LED location

Possible console models to test:

| Model Family | Notes |
|---|---|
| SCPH-700xx | Early PS2 Slim family |
| SCPH-750xx | Slim revision family |
| SCPH-770xx | Slim revision family |
| SCPH-790xx | Later Slim revision with smaller/lower-power board |
| SCPH-900xx | Final Slim family with internal PSU |

Fitment and wiring notes should be verified on real hardware before being treated as final.

## Audio Attenuation References

The audio attenuation circuit is used to reduce the PS2 audio level before feeding the Bluetooth audio emitter.

Project documents:

- `Documents/05-Audio-Attenuation.md`
- `Documents/08-Testing.md`
- `Test-Data/Audio-Tests/`

Important values to document:

- Series resistor value
- Shunt resistor value
- Final attenuation ratio
- Test game/source
- Headphones or Bluetooth receiver used
- Audio quality result
- Distortion result
- Volume result

## Related Project Links

Use this section to track related projects or resources.

| Project/Resource | Link | Notes |
|---|---|---|
| Fat Bald Dad website | https://retrogame.fatbalddad.com/ | Main FBD project/site reference |
| GitHub | https://github.com/ | Repository hosting |
| PSX-Place | https://www.psx-place.com/ | PS2 modding/community reference |
| BitBuilt | https://bitbuilt.net/ | Console modding/community reference |

## Marketplace and Parts Links

Use this section to track part sourcing.

| Part | Link | Notes |
|---|---|---|
| KCX_BT_EMITTER | https://www.aliexpress.com/item/33058710334.html | Bluetooth audio emitter module reference |
| MAX16054 | https://www.analog.com/en/products/max16054.html | Pushbutton on/off controller |
| PCB fabrication | https://jlcpcb.com/ | PCB ordering reference |

Part links may change. When ordering parts, verify the exact part number and package before purchasing.

## Datasheets To Store Locally

When allowed, store important datasheets in:

- `References/Datasheets/`

Suggested datasheets:

| File | Purpose |
|---|---|
| `MAX16054-Datasheet.pdf` | Pushbutton on/off controller |
| `KCX-BT-EMITTER-Notes.pdf` | Bluetooth module notes, if available |
| `MOSFET-Datasheet.pdf` | Power switching part |
| `LED-Datasheet.pdf` | Indicator LED |
| `Connector-Datasheet.pdf` | Connector reference, if used |

## Source Verification Table

Use this table to track source verification.

| Source | Date Accessed | Used For | Verified By Testing | Notes |
|---|---|---|---|---|
| Mark-MDO47 KCX_BT_EMITTER GitHub | TBD | Module programming/reference notes | TBD | TBD |
| Pandel V1.7 branch | TBD | V1.7 command behavior | TBD | TBD |
| MAX16054 datasheet | TBD | Pushbutton power control | TBD | TBD |
| JLCPCB capabilities | TBD | PCB manufacturing limits | TBD | TBD |
| KCX_BT_EMITTER marketplace listing | TBD | Module revision and feature notes | TBD | TBD |

## Testing References

Testing should be documented in:

- `Documents/08-Testing.md`
- `Test-Data/README.md`
- `Test-Data/Audio-Tests/`
- `Test-Data/Power-Tests/`
- `Test-Data/Fitment-Tests/`

Important test records:

- Audio distortion tests
- Attenuation value tests
- Bluetooth pairing tests
- Bluetooth reconnect tests
- Pushbutton toggle tests
- Switched 5V tests
- LED brightness tests
- Bracket fitment tests

## Notes About Uncertainty

Some references may not be complete or may not apply to every module version.

When in doubt:

- Test on real hardware
- Record the exact board/module revision
- Record the test setup
- Record the result
- Update the documentation after testing

## Related Documents

- `References/README.md`
- `Documents/01-Project-Overview.md`
- `Documents/03-Interface-Board.md`
- `Documents/04-Controller-Board.md`
- `Documents/05-Audio-Attenuation.md`
- `Documents/06-Pushbutton-Power-Control.md`
- `Documents/08-Testing.md`
- `Documents/09-Known-Issues.md`
- `Manufacturing/JLCPCB-Notes.md`
- `Test-Data/README.md`

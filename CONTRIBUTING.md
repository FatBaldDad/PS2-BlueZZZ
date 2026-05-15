# Contributing

Thank you for your interest in contributing to **PS2 BlueZZZ**.

PS2 BlueZZZ is a hobby open hardware project for adding clean internal Bluetooth audio support to PlayStation 2 Slim consoles.

The goal of this repository is to document the design, track revisions, collect testing results, and make the project easier for others to understand, build, and improve.

## Project Goal

The main goal of PS2 BlueZZZ is simple:

Help people play PlayStation 2 games with Bluetooth headphones during late-night gaming without disturbing others nearby.

The hardware is designed to make internal Bluetooth audio installation cleaner, easier to solder, easier to mount, and easier to repeat.

## Ways To Contribute

You can contribute by helping with:

- Documentation improvements
- Spelling and grammar fixes
- Installation notes
- Test results
- Audio attenuation testing
- Bluetooth headset compatibility testing
- PS2 Slim fitment testing
- Bracket improvements
- KiCad review
- BOM review
- Manufacturing notes
- Known issue reports
- Photos of builds or test setups

## Helpful Test Information

If you test the project, please include as much useful information as possible.

Helpful details include:

| Item | Example |
|---|---|
| Console model | SCPH-79001 |
| Motherboard revision | GH-061-xx, if known |
| Interface board revision | Rev 1.0 |
| Controller board revision | Rev 1.0 |
| Bracket revision | Rev 1.0 |
| Bluetooth emitter version | KCX_BT_EMITTER V1.7 |
| Headphones used | Brand/model |
| Power source | PS2 internal 5V |
| Audio pickup point | Location or photo |
| Test result | Pass, fail, or needs more testing |

## Reporting Issues

If you find a problem, please open an issue and include:

- What happened
- What you expected to happen
- Board revision used
- Console model used
- Bluetooth emitter version used
- Photos, if helpful
- Measurements, if available
- Steps to reproduce the issue
- Any fixes already tried

Good issue reports make the project easier to improve.

## Good Issue Examples

Useful issue examples:

- Audio distorts during loud scenes with specific resistor values
- Bluetooth emitter does not fully power off
- Pair/connect button does not work on a specific module revision
- Bracket interferes with a screw post on a specific PS2 Slim model
- LED is too bright for dark-room use
- Shell does not close with a specific bracket revision
- Left and right audio channels are swapped

## Pull Requests

Pull requests are welcome.

Good pull requests may include:

- Documentation fixes
- Better markdown formatting
- Updated test results
- Improved installation notes
- Corrected BOM information
- Updated KiCad files
- Bracket file improvements
- Photos or diagrams
- Known issue updates

## Pull Request Guidelines

Before submitting a pull request:

- Keep changes focused
- Use clear commit messages
- Explain what changed
- Explain why the change was made
- Include photos or test data when useful
- Do not remove revision history without a reason
- Do not overwrite tested files without noting the revision

## Hardware File Contributions

If contributing hardware files, please include:

- KiCad project files
- Schematic files
- PCB layout files
- Gerber files, if ready for fabrication
- BOM files
- Revision number
- Notes about what changed
- Any known issues
- Any testing already completed

Do not replace a known working revision without keeping the older files available for reference.

## Bracket File Contributions

If contributing bracket files, please include:

- STL file
- STEP file, if available
- Bracket revision
- Console model tested
- Board revision tested
- Print material used
- Fitment result
- Photos of test fit, if possible

Bracket fitment may vary between PS2 Slim revisions, so please document the console model used.

## Test Data Contributions

Test data is very helpful.

Good test data may include:

- Audio listening notes
- Resistor values tested
- Voltage readings
- Current draw readings
- Bluetooth pairing results
- Reconnect behavior
- Headset compatibility
- LED brightness notes
- Fitment photos
- Long-term runtime results

Test data should be placed in:

- `Test-Data/Audio-Tests/`
- `Test-Data/Power-Tests/`
- `Test-Data/Fitment-Tests/`
- `Test-Data/Bluetooth-Tests/`
- `Test-Data/LED-Tests/`

If those folders do not exist yet, they can be added later.

## Documentation Style

Please keep documentation:

- Clear
- Practical
- Beginner-friendly
- Honest about uncertainty
- Based on tested results when possible
- Organized by board revision when needed

Avoid making unsupported claims.

If something is only a theory or still needs testing, mark it clearly.

## Photos and Images

Photos are welcome if they help explain the project.

Useful photos include:

- Board renders
- Assembled boards
- Edge solder pad closeups
- Bracket fitment
- Installed board location
- Wire routing
- Button and LED placement
- Test setups
- Known issue examples

Before adding photos, make sure they do not show personal information or unrelated private details.

## Safety Notes

This project involves modifying original PlayStation 2 hardware.

Contributors should be careful when sharing instructions or recommendations.

Please avoid unsafe shortcuts.

Important reminders:

- Verify polarity before powering anything
- Check for shorts before applying power
- Use insulation where boards may contact shielding
- Do not force the shell closed
- Do not leave loose boards or wires inside the console
- Test with current-limited power when possible
- Document uncertainty clearly

## Respecting Other Projects

PS2 BlueZZZ may reference other open projects, datasheets, forum posts, or module documentation.

When adding references:

- Credit the source
- Link to the original material when possible
- Do not copy large sections of someone else’s work
- Note when information still needs verification
- Respect the license of any external project

## Project Tone

This project is meant to be useful, practical, and welcoming.

Good contributions should help make the project easier to understand and easier to build.

Please keep discussions respectful and focused on improving the project.

## Not Ready For Production

PS2 BlueZZZ is still in development.

Until a revision is fully tested, treat the design as experimental.

Contributions that help test, document, and improve the project are appreciated.

## Contributor Checklist

Before submitting a contribution, check:

- The change is useful to the project
- The file path is correct
- Markdown formatting works in GitHub
- Images load correctly
- Links work
- Board revisions are documented
- Test results include enough detail
- Any uncertainty is clearly marked
- No personal/private information is included

## Questions and Discussion

Use GitHub issues or discussions, if enabled, for questions, build notes, test reports, and project feedback.

Helpful questions and test reports are welcome.

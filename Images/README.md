# Images

This folder contains images for the **PS2 BlueZZZ** project.

Images are used for the main README, documentation pages, board renders, installation examples, bracket fitment, testing photos, and project branding.

## Purpose

The purpose of this folder is to keep all project images organized in one place.

Images help document:

- Project branding
- Board layout
- PCB renders
- Assembly steps
- Bracket fitment
- Installation examples
- Test results
- Known issues
- Revision changes

## Folder Contents

This folder may include:

| Folder | Purpose |
|---|---|
| `Logos/` | Project logos and repo branding images |
| `Board-Renders/` | PCB front/back renders and layout images |
| `Install-Photos/` | Photos showing installation inside the PS2 Slim |
| `README.md` | Image folder overview |

## Logo Files

The main PS2 BlueZZZ logo files are stored in:

| File | Purpose |
|---|---|
| `Images/Logos/PS2-BlueZZZ-Logo-Dark.png` | Logo for dark theme |
| `Images/Logos/PS2-BlueZZZ-Logo-Light.png` | Logo for light theme |

The main README uses GitHub theme detection to load the correct logo based on the user’s browser or GitHub theme setting.

## README Logo Example

The main README should use this image block at the top:

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="Images/Logos/PS2-BlueZZZ-Logo-Dark.png">
    <source media="(prefers-color-scheme: light)" srcset="Images/Logos/PS2-BlueZZZ-Logo-Light.png">
    <img
      src="Images/Logos/PS2-BlueZZZ-Logo-Light.png"
      alt="PS2 BlueZZZ Logo"
      width="70%"
    >
  </picture>
</p>

## Image Organization

Keep images organized by purpose.

Suggested layout:

| Folder | Example Images |
|---|---|
| `Logos/` | Project logos, light theme logo, dark theme logo |
| `Board-Renders/` | Front render, back render, 3D board view |
| `Install-Photos/` | Board installed, bracket installed, wiring route |
| `Assembly-Photos/` | Soldering steps, component placement, edge pad soldering |
| `Testing-Photos/` | Bench testing, voltage checks, Bluetooth pairing tests |
| `Fitment-Photos/` | Shell clearance, RF shield clearance, bracket test fit |

## Suggested Files To Add

Add images as the project develops.

| File | Purpose |
|---|---|
| `Logos/PS2-BlueZZZ-Logo-Light.png` | Logo for normal/light GitHub theme |
| `Logos/PS2-BlueZZZ-Logo-Dark.png` | Logo for dark GitHub theme |
| `Board-Renders/Interface-Board-Front.png` | Front render of the interface board |
| `Board-Renders/Interface-Board-Back.png` | Back render of the interface board |
| `Board-Renders/Controller-Board-Front.png` | Front render of the controller board |
| `Board-Renders/Controller-Board-Back.png` | Back render of the controller board |
| `Install-Photos/Interface-Board-Installed.png` | Interface board installed in PS2 Slim |
| `Install-Photos/Controller-Board-Installed.png` | Controller board installed in PS2 Slim |
| `Install-Photos/Bracket-Installed.png` | Bracket installed in PS2 Slim |
| `Testing-Photos/Bench-Test.png` | Bench test setup |
| `Fitment-Photos/Shell-Clearance.png` | Shell clearance photo |

## Image Naming

Use clear filenames so images are easy to understand without opening them.

Recommended naming style:

| Type | Example |
|---|---|
| Logo | `PS2-BlueZZZ-Logo-Light.png` |
| Board render | `Interface-Board-Rev-1.0-Front.png` |
| Install photo | `Interface-Board-Installed-SCPH-79001.png` |
| Bracket photo | `Bracket-Rev-1.0-Test-Fit.png` |
| Test photo | `Audio-Test-Setup-Rev-1.0.png` |

## Image Format

Recommended formats:

| Format | Use |
|---|---|
| PNG | Logos, screenshots, board renders, documentation images |
| JPG | Photos where file size matters |
| SVG | Vector artwork, icons, and logos when supported |
| WEBP | Optional compressed images |

For GitHub README images, PNG is usually a good choice.

## Image Size Notes

Large images can make the repository harder to browse.

Suggested approach:

- Use reasonable image sizes for README display
- Keep original high-resolution images only when useful
- Use compressed copies for documentation
- Avoid uploading unnecessary duplicate images
- Use clear image names instead of random camera filenames

## Board Render Notes

Board renders should show the PCB clearly.

Useful board render images include:

- Front view
- Back view
- Angled 3D view
- Interface board with Bluetooth emitter attached
- Controller board render
- Important pad labels
- Edge solder pad details
- Revision marking

## Installation Photo Notes

Installation photos should show how the system fits inside the PS2 Slim.

Useful installation photos include:

- Board location
- Bracket location
- Wire routing
- Audio pickup points
- 5V pickup point
- Ground point
- Controller board location
- Button location
- LED location
- Shell clearance
- RF shield clearance

## Testing Photo Notes

Testing photos should help explain how the board was validated.

Useful testing photos include:

- Bench power setup
- Multimeter voltage readings
- Current draw testing
- Pushbutton toggle test
- Switched 5V test
- Bluetooth pairing test
- Audio test setup
- Fitment test before final assembly

## Image Captions

When using images in documentation, add a short caption or description when possible.

Good image captions explain:

- What the image shows
- Which board revision is shown
- Which console model is shown
- What test or install step is being shown
- Any important warning or note

## Accessibility Notes

Use descriptive alt text when adding images to markdown.

Good alt text examples:

| Image | Good Alt Text |
|---|---|
| Logo | `PS2 BlueZZZ Logo` |
| Board render | `Front render of the PS2 BlueZZZ interface board` |
| Install photo | `PS2 BlueZZZ interface board installed inside a PS2 Slim` |
| Bracket photo | `PS2 BlueZZZ bracket test fit inside the console shell` |

## Example Markdown Image

Use normal markdown for simple images:

![PS2 BlueZZZ interface board render](Board-Renders/Interface-Board-Rev-1.0-Front.png)

## Example Centered Image

Use HTML when an image needs to be centered and scaled:

<p align="center">
  <img
    src="Board-Renders/Interface-Board-Rev-1.0-Front.png"
    alt="PS2 BlueZZZ interface board front render"
    width="70%"
  >
</p>

## Known Concerns

Items to watch:

- Image filenames must match exactly, including capitalization
- GitHub paths are case-sensitive
- Large images can make pages load slowly
- Transparent images may be hard to see on dark themes
- Dark logos and light logos should both be tested
- Photos should not show accidental personal information
- Photos should not show unrelated project clutter if used for public documentation

## Related Documents

- `README.md`
- `Documents/01-Project-Overview.md`
- `Documents/03-Interface-Board.md`
- `Documents/04-Controller-Board.md`
- `Documents/07-Installation-Planning.md`
- `Hardware/Interface-Board/README.md`
- `Hardware/Controller-Board/README.md`
- `Hardware/Brackets/README.md`

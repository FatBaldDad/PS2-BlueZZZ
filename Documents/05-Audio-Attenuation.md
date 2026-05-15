# Audio Attenuation

The **PS2 BlueZZZ** interface board includes an audio attenuation circuit for the left and right PS2 audio signals.

The goal is to reduce the audio level going into the Bluetooth audio emitter so the sound does not distort when the game audio gets loud.

## Purpose

During early testing, connecting the PS2 audio directly to the Bluetooth audio emitter could cause distortion when the console audio level was high.

The attenuation circuit was added to dial back the audio signal before it reaches the Bluetooth audio module.

This helps make the Bluetooth audio output cleaner and more usable.

## Why Attenuation Is Needed

The Bluetooth audio emitter expects a line-level audio signal.

If the signal going into the module is too strong, the input can be overdriven. When that happens, the Bluetooth audio may sound distorted, harsh, clipped, or muddy.

The attenuation circuit reduces the signal level before it reaches the Bluetooth audio emitter.

## Audio Signals

The PS2 BlueZZZ board handles the following audio signals:

- Left audio
- Right audio
- Audio ground

Both the left and right channels should use the same attenuation values so the stereo balance stays even.

## Basic Circuit Concept

The attenuation circuit works like a simple voltage divider.

Each audio channel has a resistor network that reduces the audio signal before it enters the Bluetooth audio emitter.

Basic signal path:

- PS2 left audio enters the interface board
- Left audio is attenuated
- Reduced left audio goes to the Bluetooth emitter

- PS2 right audio enters the interface board
- Right audio is attenuated
- Reduced right audio goes to the Bluetooth emitter

## Design Goals

The audio attenuation section should:

- Reduce the PS2 audio level
- Help prevent distortion
- Keep left and right audio levels balanced
- Avoid unnecessary noise pickup
- Use simple common resistor values
- Be easy to revise during testing
- Be small enough for the interface board layout

## Adjustable or Testable Values

The first revision may use resistor values that are easy to change during testing.

The board may include extra pads or resistor options so different attenuation levels can be tested without redesigning the entire board.

This is useful because the best resistor values may depend on:

- PS2 model
- Audio source point on the motherboard
- Bluetooth emitter revision
- Headphones or receiver being used
- Final audio quality preference

## Initial Testing Goals

The first tests should check whether the attenuation level is enough to prevent distortion without making the audio too quiet.

Testing should include:

- Quiet game audio
- Loud game audio
- Music-heavy scenes
- Sound effects
- Menu audio
- Left and right channel balance
- Bluetooth headphone volume range
- Noise or hum when no audio is playing

## Test Notes To Record

When testing resistor values, record:

- Resistor values used
- Game or audio source tested
- Bluetooth headphones or receiver used
- Whether distortion was present
- Whether audio was too quiet
- Whether left and right channels were balanced
- Any noise, hum, or hiss noticed
- Whether the result should be kept or changed

## Example Test Table

| Test | Left Channel Values | Right Channel Values | Result | Notes |
|---|---|---|---|---|
| Test 1 | TBD | TBD | TBD | Initial test |
| Test 2 | TBD | TBD | TBD | Alternate attenuation |
| Test 3 | TBD | TBD | TBD | Final candidate |

## Audio Ground Notes

Audio ground should be handled carefully.

Poor grounding can cause noise, hum, or other unwanted audio problems.

General notes:

- Keep audio wiring short where possible
- Keep audio wiring away from noisy power wiring
- Avoid unnecessary ground loops
- Verify the correct ground reference before powering the board
- Keep left and right channel routing similar where practical

## Routing Notes

The audio traces should be treated as low-level analog signals.

Layout goals include:

- Keep left and right audio traces clean
- Avoid routing audio near switching power traces
- Avoid routing audio near noisy digital control lines
- Keep the audio ground path sensible
- Keep left and right channel paths reasonably matched
- Avoid unnecessary vias if possible

## Symptoms of Too Much Audio Level

If the attenuation is not strong enough, possible symptoms include:

- Distortion during loud scenes
- Harsh audio
- Crackling
- Clipping
- Muddy sound
- Bluetooth output sounding worse than wired output
- Audio sounding acceptable at low volume but bad during loud sounds

## Symptoms of Too Much Attenuation

If the attenuation is too strong, possible symptoms include:

- Audio is too quiet
- Bluetooth headphones need to be turned up too high
- Background noise becomes more noticeable
- Quiet game audio becomes hard to hear
- Volume range feels limited

## What Counts as a Good Result

A good attenuation value should provide:

- Clean audio during loud game scenes
- Comfortable headphone volume
- No obvious clipping
- No major hiss or hum
- Balanced left and right channels
- Reliable behavior across multiple games

## Known Concerns

Items to watch during testing:

- Distortion at high game volume
- Audio being too quiet after attenuation
- Left and right channel imbalance
- Ground noise
- Bluetooth latency
- Headphone compatibility
- Differences between Bluetooth emitter revisions

## Revision Notes

Use this section to track audio attenuation changes.

| Revision | Notes |
|---|---|
| Rev 0.1 | Initial attenuation concept |
| Rev 1.0 | First public/test revision |
| Rev 1.1 | Future resistor value changes |

## Related Documents

- `Documents/03-Interface-Board.md`
- `Documents/08-Testing.md`
- `Hardware/Interface-Board/README.md`
- `Test-Data/README.md`

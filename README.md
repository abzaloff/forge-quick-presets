# Forge Quick Presets

Delta presets for Forge NEO.

Stable local version: `0.1.0` (2026-04-29).

The extension adds a small `Quick Presets` panel below the generation preview. It captures the current UI as a baseline, saves almost any UI field changed after that baseline, and applies those changed fields later without touching Forge's model preset selectors or user-provided media.

Quick Presets are separate from native Forge `UI Preset`s. They do not edit, overwrite, rename, delete, or otherwise modify Forge's built-in preset system.

Excluded by default:

- Forge UI Preset
- Checkpoint
- VAE / Text Encoder
- Diffusion dtype
- prompts
- image, mask, gallery, upload fields
- generate/interrupt/skip controls
- ControlNet `Control Type` filter state

Typical flow:

1. Choose a native Forge `UI Preset`.
2. Change any settings you want to bundle: generation settings, Refiner, ControlNet units, ADetailer, Scripts, extension fields, denoise, CFG, steps, and similar UI controls.
3. Press `Save Changed`.
4. Later choose the native Forge preset again, then apply the saved quick preset.

To revise an existing quick preset:

1. Select and apply the preset.
2. Adjust the UI fields you want to change.
3. Press `Update` and confirm.

Notes:

- `Apply` and `Reset` preserve the user's scroll position.
- Programmatic dropdown selections are hidden to avoid page jumps and large dropdown flashes.
- Native Forge `UI Preset`s are not modified; quick presets are stored separately.
- ControlNet image, mask, gallery, and upload fields are intentionally ignored.
- ControlNet `Control Type` is treated as a filter, not a saved generation parameter; quick presets reset it to `All` before selecting saved models and preprocessors.

Presets are stored in `presets/user_presets.json`.

## License

Forge Quick Presets is free for non-commercial use and redistribution with attribution. It may not be sold or included in paid products, bundles, subscriptions, or commercial distributions, including modified versions. If you want to monetize it in any way, including paid builds or paid bundles, contact the author first and obtain written permission. See [LICENSE.md](LICENSE.md).

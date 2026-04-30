# Changelog

## 0.1.0 - 2026-04-29

Stable local version.

- Added delta quick presets for txt2img/img2img UI fields.
- Added apply, reset, delete, save changed, and update selected preset flows.
- Preserved user-provided images, masks, galleries, uploads, prompts, checkpoints, VAE/Text Encoder, and native Forge UI preset selectors.
- Added ControlNet support for enable state, model, preprocessor, weights, timestep range, sliders, checkboxes, and radio fields.
- Treated ControlNet `Control Type` as a transient filter: quick presets apply through `All` instead of saving Tile/Instant-ID/Style filter state.
- Improved dropdown application so Gradio internal values are updated, not just visible text.
- Hid programmatic dropdown option lists to avoid large visual flashes and page layout jumps.
- Preserved scroll position during apply/reset, including ControlNet and Scripts presets.
- Added `Update` to overwrite the selected preset with the current changed fields.
- Limited `user_presets.json.bak-*` retention to the latest three backups.

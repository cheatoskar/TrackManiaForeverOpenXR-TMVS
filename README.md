# TrackMania Forever OpenXR + TM Vibrant Shaders

This is a fork of [jiink/TrackManiaForeverOpenXR](https://github.com/jiink/TrackManiaForeverOpenXR), the VR mod for TrackMania Nations/United Forever, with one patch: it lets [TM Vibrant Shaders](https://github.com/cheatoskar/TM-Vibrant-Shaders) run in VR. Everything else is jiink's mod: for installation, settings and help see the [original README](https://github.com/jiink/TrackManiaForeverOpenXR#readme).

The patch is by [wial663](https://github.com/wial663) and is offered to the original mod as a pull request. Once it is merged there, use the original.

## What the patch does

Under VR, TM Vibrant Shaders never saw the game's graphics device, so its menu and effects stayed off. With the patch the VR mod hands the device over:

- **Default:** the TM Vibrant Shaders menu (`F8`) shows in the headset and its keys work. Its effects stay off; the VR image is not changed.
- **`AttachVibrantShaders=2`** under `[Compatibility]` in `Documents\TrackMania\TMFOXR.ini`: TM Vibrant Shaders shades each eye. Experimental.
- **`AttachVibrantShaders=0`:** the hand-over is off.

Both mods have to be installed with the mod loader, and TM Vibrant Shaders has to be a version with the VR hand-over.

## Where the code is

The patch changes `src/d3d9_proxy.cpp` and `TMFOXR.defaults.ini`. `master` is jiink's code with the patch and this README; the branch [`tmvs-handover`](https://github.com/cheatoskar/TrackManiaForeverOpenXR-TMVS/tree/tmvs-handover) is the same patch without this README, for the pull request.

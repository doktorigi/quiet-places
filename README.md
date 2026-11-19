# Quiet Places

A free, open-source meditation inside real 360° photos, for Meta Quest (2, 3, 3S, Pro) and any modern browser.

**Use it:** open <https://doktorigi.github.io/quiet-places/> in the Quest browser, choose a place and a length. No install, no account, no tracking.

Six places: a mountain top, a lake at sunrise, misty pines, a secluded beach, a forest stream and the Milky Way. In VR, pull the trigger or pinch to move to the next place. Wind, waves and stream sounds are synthesised and swell at a slow breathing pace (4s in, 2s hold, 6s out). A bell marks the start and the end.

Sister apps: [Quiet Orb](https://github.com/doktorigi/quiet-orb), [Quiet Summit](https://github.com/doktorigi/quiet-summit).

## Photos

The photos are 360° panoramas from [Poly Haven](https://polyhaven.com/hdris), released into the public domain (CC0): Table Mountain 1, Lakeside Sunrise, Misty Pines, Secluded Beach and Rogland Clear Night by Greg Zaal (with Rico Cilliers and Jarod Guest), and Lauter Waterfall by Andreas Mischok. Thank you.

Each photo is in `photos/` as `<id>_8k.jpg` (8192x4096), `<id>_4k.jpg` and `<id>_preview.jpg`. The app picks 8K when the device supports it; add `?res=4k` to the URL to force the smaller one.

To add a place: put the three sizes of any equirectangular photo in `photos/` and add a line to `PLACES` at the top of the script in `index.html`.

## Develop

It is one file, `index.html`, with no build step. three.js loads from a CDN.

    python -m http.server 8767

Open <http://localhost:8767/>. Add `#test` to the URL to run the self-check (the tab title becomes "tests ok").

WebXR needs HTTPS, so to try changes in a headset, push to GitHub Pages.

## License

Code: MIT. Photos: CC0 (public domain).

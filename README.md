# Quiet Places

A free, open-source meditation inside real 360° photos, for Meta Quest (2, 3, 3S, Pro) and any modern browser.

**Use it:** open <https://doktorigi.github.io/quiet-places/> in the Quest browser, choose a place and a length. No install, no account, no tracking.

Eighteen places, among them a mountain top, a canyon at sunset, an alpine meadow, lakes, a beach and a rocky coast, six kinds of forest, two gardens, snow, and two night skies. In VR, pull the trigger or pinch for the next place and squeeze the grip for the previous one. Wind, waves and stream sounds are synthesised and swell at a slow breathing pace (4s in, 2s hold, 6s out). A bell marks the start and the end.

Sister apps: [Quiet Orb](https://github.com/doktorigi/quiet-orb), [Quiet Summit](https://github.com/doktorigi/quiet-summit).

## Photos

The photos are 360° panoramas from [Poly Haven](https://polyhaven.com/hdris), released into the public domain (CC0). Thank you to the photographers:

- Greg Zaal: Table Mountain 1, Lakeside Sunrise, Lakeside Night, Misty Pines, Secluded Beach, Rogland Clear Night, Kiara 1 Dawn, Cannon, Ninomaru Teien (with Rico Cilliers and Jarod Guest on some)
- Andreas Mischok: Lauter Waterfall, Chinese Garden, Forest Slope, Alps Field
- Alexander Scholten: Autumn Forest 04
- Sergej Majboroda: Winter Lake 01
- Dario Barresi: Valley Of Desolation
- Oliksiy Yakovlyev: Snowy Forest Path 01
- Dimitrios Savva and Jarod Guest: Rainforest Trail

They are ordinary (mono) 360° photos, not stereo 3D: freely licensed stereo 360° photos of nature are hard to find.

Each photo is in `photos/` as `<id>_8k.jpg` (8192x4096), `<id>_4k.jpg` and `<id>_preview.jpg`. The app picks 8K when the device supports it; add `?res=4k` to the URL to force the smaller one.

To add a place: put the three sizes of any equirectangular photo in `photos/` and add a line to `PLACES` at the top of the script in `index.html`.

## Develop

It is one file, `index.html`, with no build step. three.js loads from a CDN.

    python -m http.server 8767

Open <http://localhost:8767/>. Add `#test` to the URL to run the self-check (the tab title becomes "tests ok").

WebXR needs HTTPS, so to try changes in a headset, push to GitHub Pages.

## License

Code: MIT. Photos: CC0 (public domain).

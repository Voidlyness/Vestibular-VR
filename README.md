# Vestibular VR Lab

A WebXR prototype for vestibular and visual-vestibular exercises: fixation, pursuit/saccades, optokinetic stimulation, and a dynamic visual-acuity (DVA) self-test.

## Run locally

Open `index.html` through a local web server. WebXR requires a secure context when used on a headset, so the published GitHub Pages URL is the preferred way to launch it in VR.

## Publish to GitHub Pages

The included workflow deploys the root of this repository whenever changes are pushed to `main`.

1. Create an empty GitHub repository and add it as `origin`.
2. Push the `main` branch.
3. In the repository's **Settings → Pages**, set the source to **GitHub Actions** if GitHub has not selected it automatically.
4. When the **Deploy GitHub Pages** workflow succeeds, open the URL shown in its deployment details. It will normally be `https://<account>.github.io/<repository>/`.

The page loads Three.js from jsDelivr, so an internet connection is currently required.

## Safety note

This is an uncalibrated prototype intended for self-guided experimentation, not a medical device or clinical diagnostic tool.

# Vestibular VR Lab

A WebXR prototype for vestibular and visual-vestibular exercises: fixation, pursuit/saccades, optokinetic stimulation, a dynamic visual-acuity (DVA) self-test, and a gentle guided starter session.

## Guided session and local data

The guided starter session uses a short, low-intensity sequence with a rest period, symptom check-ins, pause/stop controls, and local session records. Records are stored only in the browser's local storage until the user explicitly exports them as JSON.

The session schema records protocol events and sampled head-motion data. It also reserves a clearly marked, inactive `eyeTracking` field for a future validated hardware integration; this prototype does not calculate or diagnose nystagmus, VOR gain, or any vestibular condition.

## Dynamic visual acuity (DVA) self-test

The DVA mode runs practice trials, a static baseline, then separate rightward and leftward head-movement blocks. The Landolt C flashes for 150 ms only while the head turns at 120–180°/s in the block's direction and points roughly at the target. Each block uses an adaptive staircase (1-down/1-up to the first reversal, then 2-down/1-up), and the result is the loss in logMAR from static to each direction.

Symptoms are rated 0–10 before starting and after finishing, and there is a rest break before the leftward block where the run can be stopped. Stopped runs are saved too. Runs are stored locally and can be exported as JSON.

## Run locally

Open `index.html` through a local web server. WebXR requires a secure context when used on a headset, so the published GitHub Pages URL is the preferred way to launch it in VR.

## Publish to GitHub Pages

The included workflow deploys the root of this repository whenever changes are pushed to `main`.

1. Push the `main` branch.
2. In the repository's **Settings → Pages**, set the source to **GitHub Actions** if GitHub has not selected it automatically.
3. When the **Deploy GitHub Pages** workflow succeeds, open the URL shown in its deployment details.

The page loads Three.js from jsDelivr, so an internet connection is currently required.

## Safety note

This is an uncalibrated prototype intended for self-guided experimentation, not a medical device or clinical diagnostic tool. Any future clinical or research use requires protocol validation, appropriate consent, and data-governance procedures.

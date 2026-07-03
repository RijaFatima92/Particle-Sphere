# Particle Sphere

A single-file, framework-free 3D particle sphere (3,000 points) that responds to hand gestures in real time via your webcam — built with **Three.js** and **MediaPipe Hands**.

No build step, no dependencies to install. Open it in a browser and it just works.


## Gestures

| Gesture | Effect |
|---|---|
| One hand | Moves the sphere and rotates it as your hand drifts |
| Pinch (thumb + index) and hold | Fills a charge ring — release at 100% to explode the particles across the screen, then watch them reform |
| Two hands, spread / bring together | Grows / shrinks the sphere |
| Finger count (0–5) | Changes particle color |
| Button (top right) | Toggles the webcam as a fullscreen background |


## Running it

Camera access requires a proper origin (`file://` won't work in most browsers), so serve it locally:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/particle-sphere.html` and grant camera permission.

## Stack

- [Three.js](https://threejs.org/) r128 — WebGL particle rendering
- [MediaPipe Hands](https://developers.google.com/mediapipe) — real-time hand landmark tracking
- Vanilla JS, HTML, CSS — no frameworks, no bundler

## Notes

Gesture thresholds (pinch distance, finger-extension detection) are tuned heuristically and may need adjusting depending on lighting and camera quality.

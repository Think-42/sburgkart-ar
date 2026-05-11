# sburgkart-ar

A tiny web AR prototype that places a human pelvis on a flat surface — anatomical scale, as if a patient were lying on the table. Useful for sketching what a C-arm or CT scan might show.

## How it works

- Single HTML page using Google's `<model-viewer>`
- iOS: Quick Look (`.usdz`)
- Android: Scene Viewer / WebXR (`.glb`)
- Desktop: in-page 3D viewer + QR code so you can hop to a phone

## Local preview

Static page — open `index.html` in any browser. For AR you need a phone (iOS Safari or Android Chrome) and HTTPS, so deploy via GitHub Pages.

## Model

`models/pelvis.glb` is from the NIH 3D Print Exchange. To add iOS Quick Look support, export a `.usdz` (Reality Composer on macOS) and drop it next to the `.glb`.

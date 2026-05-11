# AR Pelvis — Model Files

Put two files here:

- `pelvis.glb` — used by Android (Scene Viewer / WebXR) and the desktop 3D viewer
- `pelvis.usdz` — used by iOS Quick Look (optional but recommended)

If only `.glb` is here, iPhones still show the 3D viewer in the browser but won't open the full AR overlay.

## Where to get a free pelvis model

**NIH 3D (best for medical / anatomically correct):** https://3d.nih.gov
Search "pelvis". Many are CT-segmentation derived and licensed CC0 / public domain. Download `.stl` or `.glb`.

**Sketchfab:** https://sketchfab.com/search?q=pelvis&type=models
Filter "Downloadable" + license "CC Attribution" or "CC0". Download in glTF format → you get a `.glb`.

**BodyParts3D / Anatomography:** https://lifesciencedb.jp/bp3d/
Free anatomical models from the Japanese DBCLS, usable for educational prototypes.

## Converting between formats

- **STL → GLB:** open in Blender (File → Import → STL), then File → Export → glTF Binary (.glb).
- **GLB → USDZ (for iOS):** open the `.glb` in Apple's **Reality Composer** (free, on Mac) and export as `.usdz`. Or use the CLI tool `usd-from-gltf`.

## Scale matters

`ar-scale="fixed"` in the HTML respects the model's actual size. A pelvis should be ~30 cm across. If it appears giant or tiny on the table, fix the scale in Blender (Object → Apply → Scale) before exporting.

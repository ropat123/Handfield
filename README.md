# Handfield

Hand-tracked 3D particle sculptures for iPhone, running in Safari (no app install).

| Page | What it is |
|---|---|
| `index.html` | Launcher |
| `ar.html` | Zapbox headset, 6DoF: rear main camera passthrough, side-by-side stereo with lens pre-distortion, position tracking from the printed ArUco board fused with the gyro, MediaPipe hand tracking mapped into the world in metres |
| `3dof.html` | Zapbox headset, 3DoF: same rendering and hands, rotation from the gyro only; hold both open palms up to recenter |
| `handheld.html` | Original phone-in-hand version with the front camera |
| `handfield-marker-board.pdf` | 2×2 ARUCO_MIP_36h12 board (ids 0–3, 80 mm squares); print at 100% |

Camera and motion sensors only work on HTTPS, which GitHub Pages provides. Libraries load from jsDelivr (three.js, MediaPipe Tasks Vision, js-aruco2); the hand model loads from Google's MediaPipe model bucket. Camera frames are processed on the phone and never uploaded.

Lens settings (spacing, distortion, view size) are stored in the browser per site and shared between `ar.html` and `3dof.html`.

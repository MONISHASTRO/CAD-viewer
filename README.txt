# STP Viewer — Offline Setup Guide
=========================================

## Folder Structure Required
```
stp-viewer/
├── index.html          ← The viewer (this file)
└── libs/
    ├── three.module.js
    ├── OrbitControls.js
    ├── occt-import-js.js
    └── occt-import-js.wasm   ← ~10 MB, most important!
```

## Step 1 — Download the 4 Library Files
Open your browser and download each file to the `libs/` folder:

### File 1 — Three.js (3D rendering engine)
URL: https://unpkg.com/three@0.160.0/build/three.module.js
Save as: libs/three.module.js

### File 2 — OrbitControls (mouse rotate/pan/zoom)
URL: https://unpkg.com/three@0.160.0/examples/jsm/controls/OrbitControls.js
Save as: libs/OrbitControls.js

### File 3 — OCCT Import JS (STEP parser)
URL: https://unpkg.com/occt-import-js@0.0.17/dist/occt-import-js.js
Save as: libs/occt-import-js.js

### File 4 — OCCT WebAssembly Engine (~10 MB)
URL: https://unpkg.com/occt-import-js@0.0.17/dist/occt-import-js.wasm
Save as: libs/occt-import-js.wasm

## Step 2 — Open in Browser Correctly
⚠️ IMPORTANT: You CANNOT just double-click index.html
   Modern browsers block local file loading for security.

### Option A — Use VS Code Live Server (Recommended)
1. Open the stp-viewer folder in VS Code
2. Right-click index.html → "Open with Live Server"
3. Browser opens at http://127.0.0.1:5500

### Option B — Python (if installed)
1. Open terminal/cmd in the stp-viewer folder
2. Run: python -m http.server 8080
3. Open browser → http://localhost:8080

### Option C — Node.js (if installed)
1. Run: npx serve .
2. Open browser → http://localhost:3000

## Step 3 — Export from CATIA
1. Open your part/assembly in CATIA
2. File → Save As → Format: STEP (*.stp)
3. Click Save

## Step 4 — Load the Model
1. Drag & drop your .stp file onto the viewer
2. Or click the sidebar upload area

## Controls
- Left mouse drag  → Rotate
- Right mouse drag → Pan
- Scroll wheel     → Zoom
- F key            → Fit to view
- T key            → Top view
- Y key            → Front view

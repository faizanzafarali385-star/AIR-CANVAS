# Air Canvas Pro: Horizon Spatial Studio

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-00897B?style=for-the-badge&logo=google&logoColor=white)
![WebGL](https://img.shields.io/badge/WebGL-990000?style=for-the-badge&logo=webgl&logoColor=white)

**Air Canvas Pro** is a cutting-edge spatial 3D voxel creation studio powered by in-browser computer vision and real-time hand tracking. Build, sculpt, and interact with 3D structures directly in mid-air using your webcam, or seamlessly switch to mouse and keyboard controls.

---

## ✨ Features

- **Spatial Air Gestures (MediaPipe Hands)**:
  - **Index Aim**: Direct 3D air cursor aiming with adaptive lerp smoothing.
  - **Pinch (Thumb + Index)**: Real-time voxel construction or destruction.
  - **Fist Gesture**: Orbit, rotate, and navigate around your 3D creation in 360°.
  - **2-Hand Hybrid Mode**: Aim with your primary hand while triggering actions or locking depth with your secondary hand.
  - **Air Dwell Ring**: Dwell on UI buttons and menus to click them hands-free without touching the keyboard or mouse.

- **Creative 3D Engine (Three.js)**:
  - **Modular Voxel Engine**: Grid-snapped 3D building with surface-normal alignment.
  - **Multiple Brush Sizes**: Expand construction with `1x1`, `2x2`, or `3x3` clusters.
  - **Mirror Symmetry**: Automatic bilateral reflection across the X or Z planes.
  - **Material Shaders**:
    - **STD**: Classic matte solid finish.
    - **GLOW**: Emissive neon voxel lighting.
    - **GLAS**: Translucent holographic glass shader.
    - **METL**: High-specular reflective chrome metal.
  - **Color Palette & Eyedropper**: 10 preset cyberpunk neon colors, full custom RGB color picker, and a 3D color pipette (eyedropper).

- **Studio & Environment Controls**:
  - **AR Camera Mode & Studio Void Mode**: Toggle between an augmented reality camera backdrop and an immersive dark space studio.
  - **Lighting Atmospheres**: Switch between *Cyberpunk*, *Sunset Gold*, *Deep Void*, and *Clean Studio* lighting setups.
  - **Turntable Presentation**: Auto-rotating display mode for showcasing completed models.
  - **Hand Skeleton Visualization**: High-precision landmark tracking visualizer with toggle support.

- **Productivity & Export**:
  - **Clear Canvas**: Dedicated quick-clear option with a non-blocking confirmation dialog and full undo protection.
  - **History (Undo / Redo)**: Complete undo/redo stack (`Ctrl+Z`, `Ctrl+Y`).
  - **3D Model Export (.OBJ)**: Export your voxels directly into standard `.OBJ` format for Blender, Unity, Unreal Engine, or 3D printing.
  - **Project Save & Load**: Save and restore entire scenes as lightweight `.json` files.
  - **High-Res Snapshots**: Capture clean PNG snapshots without UI overlays.
  - **Procedural 3D Templates**: Instant pre-built models including *Cyber Spaceship*, *Cyber Katana*, *Castle Watchtower*, *Bonsai Tree*, *Step Pyramid*, and *Pixel Heart*.
  - **Synthesizer SFX**: Dynamic spatial audio feedback built on the Web Audio API.

---

## 🚀 Getting Started

No build tools or package managers required! Air Canvas Pro runs entirely in the browser using modern ES modules.

### Option 1: Direct File Opening
Double-click `Air_Canvas.html` or open it with any modern web browser (Google Chrome, Microsoft Edge, Brave, or Safari recommended for MediaPipe web camera support).

### Option 2: Local HTTP Server (Recommended)
Running through a local web server ensures optimal camera permissions:

```bash
# Using Python
python -m http.server 8000

# Using Node.js npx
npx serve .
```
Then navigate to `http://localhost:8000/Air_Canvas.html`.

---

## 🎮 Controls & Shortcuts

| Action | Hand Gesture | Mouse / Keyboard |
| :--- | :--- | :--- |
| **Aim Cursor** | Point index finger | Mouse Move |
| **Build Block** | Pinch (Thumb + Index) in Construct Mode | Left Click |
| **Erase Block** | Pinch in Destroy Mode | Left Click in Destroy Mode |
| **Orbit Camera** | Make a Fist & move hand | Right-Click Drag |
| **Zoom View** | Move closer/further from camera | Mouse Scroll Wheel |
| **Construct Mode** | Dwell on *Construct* tab | **`B`** |
| **Destroy Mode** | Dwell on *Destroy* tab | **`E`** |
| **Orbit Mode** | Dwell on *Orbit View* tab | **`O`** |
| **Mirror Symmetry** | Dwell on *Mirror* button | **`M`** |
| **Turntable Mode** | Dwell on *Turntable* button | **`T`** |
| **Color Pipette** | Dwell on *Pipette* button | **`I`** |
| **Clear Canvas** | Dwell on *Clear Canvas* button | **`C`** or **`Delete`** |
| **Undo** | Dwell on *Undo* button | **`Z`** or **`Ctrl+Z`** |
| **Redo** | Dwell on *Redo* button | **`Y`** or **`Ctrl+Y`** |
| **Toggle Skeleton**| Dwell on *Skeleton* button | **`H`** |
| **Quick Colors** | Dwell on Color Swatches | **`1`** – **`9`** |
| **Close Modals** | Dwell on Close / Cancel | **`Escape`** |

---

## 🛠️ Tech Stack

- **[Three.js](https://threejs.org/)** (v0.160.0) – 3D scene graph, camera projection, shadows, and custom materials.
- **[Google MediaPipe](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker)** – 21-point 3D hand landmark recognition running client-side.
- **HTML5 Canvas & WebGL** – Multi-layer rendering for tracking skeleton, 3D world, and futuristic HUD reticles.
- **Web Audio API** – Procedural dynamic sound synthesis for clicks, placements, and deletions.

---

## 📄 License

This project is licensed under the MIT License - feel free to build, customize, and extend it!

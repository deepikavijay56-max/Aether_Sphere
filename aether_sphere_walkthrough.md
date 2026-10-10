# Aether Sphere — 3D Real-Time Hand Responsive Particles

A self-contained, single-file interactive 3D WebGL particle sphere engineered with Three.js and MediaPipe Hands.

![Aether Sphere View](/C:/Users/mutha/.gemini/antigravity-ide/brain/61671ded-8112-4f33-989c-196a55cf4612/localhost_3000_view_1791624968190.png)

---

## 🌟 Features Implemented

### 1. 3D Particle Sphere (3,000 Particles)
- Generated via a **Fibonacci lattice** on a sphere for uniform particle density.
- Dynamic breathing undulations using spherical harmonic noise.
- Rendered with an additive blending shader and custom radial glowing point sprites.

### 2. MediaPipe Hands Sensor & Real-Time Gestures
- **Single Hand**: 
  - **Position**: Follows palm coordinates smoothly across 3D space with cubic lerp interpolation.
  - **Rotation**: Hand tilt and yaw angles dynamically rotate the particle lattice.
- **Pinch & Hold to Explode**: 
  - Pinching index finger + thumb activates an on-screen glowing SVG charge ring.
  - Generates a rising frequency synthesized audio hum via Web Audio API.
  - On release, triggers a supernova burst explosion where particles scatter outwards across the viewport, before spring damping smoothly pulls them back to reform the pristine sphere.
- **Two Hands (Scale Manipulation)**:
  - Spreading two hands apart expands the sphere up to $2.5\times$ scale.
  - Bringing hands closer shrinks the sphere to a compact $0.45\times$ scale.
- **Finger Count (0–5 Chromatics)**:
  - ✊ **0 Fingers (Fist)**: Magma Crimson (`#ff3344`)
  - ☝️ **1 Finger**: Cyan Ray (`#00f0ff`)
  - ✌️ **2 Fingers**: Neon Emerald (`#10ff88`)
  - 🤟 **3 Fingers**: Solar Amber (`#ffb703`)
  - 🖖 **4 Fingers**: Cyber Orchid (`#f72585`)
  - 🖐️ **5 Fingers (Open Palm)**: Ultra Violet (`#7209b7`)
  - All color transitions interpolate smoothly across vertex buffers.

### 3. Webcam Backdrop & Interface
- **Webcam Backdrop Button**: Toggles the live mirrored webcam feed as a fullscreen cinematic backdrop with balanced brightness and contrast filters.
- **Serif Branding**: Top-left typography in *Cormorant Garamond* with live sensor status badge.
- **Sensor PIP & HUD**: Live picture-in-picture sensor view, telemetry counters, and gesture guidance dock.
- **Fallback Desktop Controls**: Mouse click & drag to rotate/move, click+hold to pinch-charge, scroll wheel to scale, and keys `0`–`5` to shift colors.

---

## 🚀 How to Run

Open [index.html](file:///c:/Users/mutha/OneDrive/Desktop/3D%20sphere/index.html) in any modern browser (Chrome, Edge, Brave, Firefox) or serve it locally:

```bash
# Optional local serve
npx serve .
# Or simply double click index.html
```

# ✨ NEON HOLOGRAM — Gesture Controlled Particle Simulation

A real-time **gesture-controlled particle system** built with Three.js and MediaPipe.

This project transforms your hand movements into a dynamic, cinematic particle experience — where particles behave like living energy, reacting to gestures with rotation, zoom, and explosive transitions.

---

## 🚀 Overview

NEON HOLOGRAM is an **interactive physics-driven visual system** where:

* Particles behave like a **gas cloud**
* They **assemble into structured forms**
* They can be **charged and released into explosions**
* All controlled using **hand gestures in real time**

---

## 🎮 Features

### 🖐️ Gesture Controls (MediaPipe Hands)

* **Rotation** → Move your index finger
* **Zoom** → Pinch gesture (thumb + index)
* **Charge Mode** → Make a fist
* **Blast / Release** → Open your hand

---

### 🌌 Particle System

* ~45,000 particles rendered using GPU acceleration
* Additive blending for neon glow effect
* Organic motion using **velocity + friction physics**

---

### ⚡ Simulation States

The system runs on a **state machine**:

1. **Gas Mode**

   * Brownian motion (random movement)
   * Free-floating particles inside a boundary

2. **Assembly Mode**

   * Particles get pulled toward target shapes
   * Uses "viscous suction" physics

3. **Charge & Blast Cycle**

   * Fist → particles destabilize (charging)
   * Release → explosion impulse
   * Gradual reassembly with cinematic timing

---

### 🔷 Procedural Shapes

Switch between multiple particle formations:

* Saturn (planet + rings)
* Galaxy (spiral arms)
* Sphere
* Vortex
* Helix (double strand)
* HyperCube (random volume)

---

### 🎨 Visual Effects

* ✨ Unreal Bloom (glow effect)
* 🌊 Afterimage Trails (motion persistence)
* 🌬️ Organic “breathing” motion using sine waves
* 🎯 Smooth camera interpolation (rotation + zoom)

---

## 🧠 How It Works

### 1. Gesture Recognition

* Uses **MediaPipe Hands**
* Tracks 21 hand landmarks
* Calculates:

  * Finger distance → zoom
  * Finger position → rotation
  * Hand openness → state trigger

---

### 2. Physics Engine

Each particle has:

* Position
* Velocity
* Target position

Core logic:

* **Assembly**

  * Velocity += (target - position) × suction
  * Velocity *= friction

* **Gas Mode**

  * Random forces (Brownian motion)
  * Boundary collision

---

### 3. Transition System

* Time-based cinematic transitions
* Smooth interpolation using easing curves
* Multi-phase animation cycle

---

## 🛠️ Tech Stack

* **Three.js** → 3D rendering
* **WebGL** → GPU acceleration
* **MediaPipe Hands** → gesture detection
* **JavaScript (ES Modules)**
* **Postprocessing Effects**

  * EffectComposer
  * UnrealBloomPass
  * AfterimagePass

---

## ▶️ How to Run

### ✅ Easiest Way (Recommended)

1. Download the project (or just the HTML file)
2. Open the file:

```id="runhtml"
Z30-FINAL.html
```

3. It will run directly in your browser 🎉

> ⚠️ Make sure to allow **camera access** when prompted (required for gesture control)

---

### 🧠 Alternative (If browser blocks features)

Some browsers may restrict modules or camera access when opened directly.

In that case, use a simple local server:

```bash id="altserver"
# Python
python -m http.server

# OR Node
npx serve
```

Then open:

```id="localurl"
http://localhost:8000
```

---

## 🎮 Controls (Mouse Fallback)

If no hand is detected:

* Drag → Rotate
* Scroll → Zoom

---

## ⚙️ Configuration

Inside the code:

```js id="configblock"
const CONFIG = {
    count: 45000,
    size: 0.18,
    color: 0x00ffcc,
    bloomStrength: 1.4,
    trail: 0.6 
};
```

You can tweak:

* Particle count
* Glow intensity
* Trail length
* Particle size

---

## 🔥 Highlights

* Real-time **gesture → physics → rendering pipeline**
* Smooth cinematic transitions (not abrupt changes)
* High particle count with optimized rendering
* Fully browser-based (no backend)

---

## 🧪 Future Improvements

* Multi-hand interaction
* Custom gesture mapping
* Audio-reactive particles
* VR / AR integration
* Mobile optimization

---

## 📸 Demo

<img width="1670" height="1199" alt="Screenshot 2026-05-03 203940" src="https://github.com/user-attachments/assets/25c43b58-24b6-425e-9457-2ad3b2b124fc" />
<img width="1662" height="1199" alt="Screenshot 2026-05-03 204012" src="https://github.com/user-attachments/assets/b2e7b87d-1997-4cff-bd5b-2e03e22e8fa8" />

---

## 📄 License

MIT License




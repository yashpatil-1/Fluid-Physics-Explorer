# 🌊 Fluid Physics Explorer

### Interactive 3D Fluid Simulation with Real-Time Hand Tracking

Fluid Physics Explorer is an interactive, browser-based 3D fluid simulation that combines particle physics, real-time graphics, and computer vision. Users can manipulate a container of simulated liquid using webcam-based hand gestures, creating an immersive way to explore fluid behaviour.

The simulation runs directly in the browser using **JavaScript, WebGL2, and MediaPipe Hand Landmarker**, without requiring specialised hardware beyond a webcam.

## ✨ Features

- **Real-Time Fluid Physics:** Simulates approximately 3,600 particles using gravity, pressure, viscosity, and wall collisions.
- **Gesture-Based Interaction:** Uses webcam hand tracking to control the simulation.
- **3D Visualisation:** Displays translucent red liquid inside an orange wireframe cube.
- **GPU Rendering:** Uses WebGL2 for fluid rendering and visual effects.
- **Background Physics Processing:** Uses a Web Worker to keep physics calculations separate from the main rendering thread.
- **Interactive Camera Controls:** Rotate and zoom using hand movements or mouse controls.
- **Browser-Based Experience:** Runs locally without a separate backend service or API key.

## 🖐️ Controls

| Interaction | Action |
|---|---|
| Move one hand | Tilt, rotate, and move the container |
| Spread two hands apart | Zoom in |
| Bring two hands together | Return towards default zoom |
| No hand detected | Container tumbles automatically |
| Mouse drag | Rotate the container |
| Mouse wheel | Zoom in or out |
| `R` | Reset the liquid simulation |

## 🛠️ Technology Stack

- **Frontend:** HTML5, CSS3, JavaScript
- **3D Graphics:** WebGL2
- **Computer Vision:** Google MediaPipe Hand Landmarker
- **Physics Simulation:** Custom JavaScript particle simulation
- **Parallel Processing:** Web Workers
- **Local Development Server:** Node.js

## 🚀 Getting Started

### Prerequisites

- Node.js 18 or newer
- A modern browser with WebGL2 support
- A webcam
- An internet connection to load the MediaPipe library and hand-tracking model when required

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/yashpatil-1/Fluid-Physics-Explorer.git
cd Fluid-Physics-Explorer
```

**2. Install the project dependencies**

```bash
npm install
```

The project does not declare external npm dependencies, so installation is primarily for setting up the local environment.

**3. Start the development server**

```bash
npm run dev
```

**4. Open the application**

Open the local URL printed in your terminal, usually:

`http://localhost:5173`

Allow camera access when prompted to enable hand tracking.

> **Note:** Webcam access generally requires `localhost` or HTTPS. MediaPipe resources may require an internet connection.

## 🧠 How It Works

The application combines three main components:

1. **Hand Tracking:** MediaPipe detects hand landmarks from the webcam feed.
2. **Physics Simulation:** The simulation updates particle positions and velocities based on fluid forces and container collisions.
3. **3D Rendering:** WebGL2 renders the liquid and wireframe container while a Web Worker handles physics calculations separately.

Together, these components create an interactive experience where hand movements influence the container and the simulated liquid responds dynamically.

## 📁 Project Structure

```text
Fluid-Physics-Explorer/
├── index.html   # Application structure
├── style.css    # Visual styling
├── app.js       # Hand tracking and rendering
├── sim.js       # Fluid physics simulation
├── worker.js    # Background physics calculations
├── server.js    # Local development server
├── package.json # Project scripts and metadata
├── package-lock.json
├── README.md
└── LICENSE
```

## 🎯 Potential Applications

- Interactive demonstrations of fluid dynamics
- Computer vision and gesture-control experiments
- Browser-based 3D visualisation
- Educational demonstrations of physics concepts
- Exploration of real-time graphics and simulation performance

## 🔮 Future Improvements

- Add adjustable viscosity, gravity, and particle density.
- Introduce multiple fluid colours and simulation presets.
- Add performance statistics and simulation controls.
- Improve mobile and touch-screen compatibility.
- Provide educational explanations of the physics behind the simulation.

## 📚 Credits and Attribution

This project is based on the original **Fluid Particle Simulator** created by [tubakhxn](https://github.com/tubakhxn).

- **Original repository:** https://github.com/tubakhxn/fluid-particle-simulator
- **MediaPipe:** https://ai.google.dev/edge/mediapipe

This repository is an organised portfolio version of the original project. The original implementation and applicable license remain acknowledged. Please review the included `LICENSE` before redistributing or modifying the project.

## 👨‍💻 Maintained By

**Yash Patil**

GitHub: [@yashpatil-1](https://github.com/yashpatil-1)

---

*Exploring the intersection of physics, computer vision, and interactive 3D technology.*

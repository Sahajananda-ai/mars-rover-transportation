# Mars Rover — Transportation System 🚀

Designed for the Transportation role of the Mars Rover Project.
This repository contains the full proof of work including chassis 
design, motor control code, and Mars terrain simulation.

---

## 1. Chassis CAD Design
- **Tool used:** Zoo Design Studio (zoo.dev) with Zookeeper AI
- **Design:** 6-wheel rocker-bogie inspired layout
- **Chassis dimensions:** 500mm × 250mm × 15mm
- **Wheel specs:** 50mm radius × 25mm width (100mm diameter)
- **Ground clearance:** 80mm for terrain traversal
- **Features:** Motor mount brackets, corner mounting holes, parametric KCL model

### CAD Screenshots
![Chassis ISO View](chassis_iso.png)
![Chassis Front View](chassis_front.png)
![Chassis Top View](chassis_top.png)

---

## 2. Motor Control System
- **Microcontroller:** Arduino Uno
- **Motor Driver:** L298N Dual H-Bridge
- **Motors:** 2× 12V DC Geared Motors (100–200 RPM)
- **Control method:** PWM differential steering
- **Steering principle:** Same as NASA Mars rovers — 
  speed difference between left/right banks controls direction

### Code Functions
- `moveForward(speed)` — both sides equal speed
- `turnLeft(speed)` — right side faster than left
- `turnRight(speed)` — left side faster than right  
- `moveBackward(speed)` — both sides reverse
- `stopMotors()` — cuts all motor signals

---

## 3. Mars Terrain Simulation — Jezero Crater
- **Tool used:** Marble AI (World Labs) — marble.worldlabs.ai
- **Location simulated:** Jezero Crater — actual Perseverance landing site
- **Terrain zones modelled:**
  - Open lakebed plains
  - Basalt boulder fields
  - Ancient river delta edge
  - Sand ripple dunes
  - Shallow impact craters
- **Purpose:** Visual validation of wheel clearance, 
  rocker-bogie suspension requirements and terrain traversability
- **3D file:** PLY point cloud imported into Blender 4.5

### Simulation Screenshots
![Jezero Crater Wide View](jezero_crater_1.png)
![Jezero Crater Ground Level](jezero_crater_2.png)
![Blender Import](blender_import.png)

---

## 4. Proposed Transportation System Design

> "The transportation system uses a 6-wheel rocker-bogie inspired 
> layout on a 500×250mm chassis. Wheels are 100mm diameter, driven 
> individually by 12V DC geared motors controlled via PWM through an 
> L298N motor driver. The chassis sits 80mm above ground for terrain 
> clearance. The design was modelled parametrically in Zoo Design 
> Studio using KCL, allowing dimensions to be updated without 
> rebuilding from scratch."

### Key Design Decisions
| Component | Choice | Reason |
|---|---|---|
| Wheel count | 6 wheels | Standard Mars rover configuration |
| Suspension | Rocker-bogie | Stability on uneven terrain |
| Steering | Differential | No steering servo needed |
| Motors | 12V DC Geared | High torque at low RPM |
| Chassis material | Aluminium sheet | Lightweight + rigid |

---

## 5. Tools Used
| Tool | Purpose |
|---|---|
| Zoo Design Studio | Parametric CAD modelling |
| Marble AI | Mars terrain simulation |
| Blender 4.5 | 3D file import and rendering |
| Arduino IDE | Motor control code |
| L298N + Arduino | Hardware motor driver setup |

---

## Reference
NASA's Perseverance rover successfully completed AI-planned drives 
at Jezero Crater in 2025 — the exact terrain this transportation 
system is designed for.  

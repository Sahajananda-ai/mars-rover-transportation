# Mars Rover — Transportation System 🚀

Designed for the Transportation role of the Mars Rover Project.

---

## 1. Chassis CAD Design
- **Tool:** Zoo Design Studio (zoo.dev)
- **Layout:** 6-wheel rocker-bogie
- **Chassis:** 500mm × 250mm × 15mm
- **Wheels:** 50mm radius × 25mm width
- **Ground clearance:** 80mm

![Chassis ISO View](chassis_iso.png)
![Chassis Front View](chassis_front.png)

---

## 2. Motor Control System
- **Microcontroller:** Arduino Uno
- **Motor Driver:** L298N Dual H-Bridge
- **Motors:** 2× 12V DC Geared Motors
- **Control:** PWM differential steering

### Code Functions
- `moveForward(speed)` — both sides equal speed
- `turnLeft(speed)` — right side faster
- `turnRight(speed)` — left side faster
- `moveBackward(speed)` — both sides reverse
- `stopMotors()` — stops everything

---

## 3. Mars Terrain Simulation — Jezero Crater
- **Tool:** Marble AI (World Labs)
- **Location:** Jezero Crater — Perseverance landing site
- **Terrain zones:**
  - Open lakebed plains
  - Basalt boulder fields
  - Ancient river delta edge
  - Sand ripple dunes
  - Shallow impact craters

![Jezero Crater View 1](jezero_crater_1.png)
![Jezero Crater View 2](jezero_crater_2.png)
![Blender Import](blender_import.png)

---

## 4. Design Summary

The transportation system uses a 6-wheel rocker-bogie layout
on a 500×250mm chassis. Wheels are 100mm diameter, driven by
12V DC geared motors controlled via PWM through an L298N driver.
Chassis sits 80mm above ground for terrain clearance. Modelled
parametrically in Zoo Design Studio using KCL.

| Component | Choice | Reason |
|---|---|---|
| Wheel count | 6 wheels | Standard Mars rover config |
| Suspension | Rocker-bogie | Stability on uneven terrain |
| Steering | Differential | No steering servo needed |
| Motors | 12V DC Geared | High torque at low RPM |

---

## 5. Tools Used
| Tool | Purpose |
|---|---|
| Zoo Design Studio | CAD modelling |
| Marble AI | Mars terrain simulation |
| Blender 4.5 | 3D file import |
| Arduino + L298N | Motor control hardware |

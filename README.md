# 🧊 SAR Iceberg Lab (Version 2.0)

An interactive, browser-based simulator that combines **high-fidelity buoyancy physics** with **Synthetic Aperture Radar (SAR)** backscatter modeling. 

Draw a custom iceberg and watch it stabilize in real-time while observing how its geometry creates unique radar signatures.

## 🚀 [Live Demo on GitHub Pages](INSERT_YOUR_LINK_HERE)

---

## 🛠 Features

### 1. Advanced Physics Engine
This lab goes beyond simple bounding boxes to simulate real fluid dynamics:
* **Lumped Mass Point Analysis:** 250 mass points are distributed within the polygon to calculate an accurate Center of Mass.
* **Rotational Inertia:** Calculates the Moment of Inertia based on the drawn geometry to simulate realistic rocking and stabilization.
* **Turf.js Integration:** Uses spatial analysis for precise clipping of submerged areas to calculate buoyant force based on displaced volume.

### 2. SAR Remote Sensing Simulator
The simulator models how a side-looking radar satellite interacts with the ice:
* **Dynamic Shadowing:** Shadows are calculated geometrically based on the incidence angle and the "freeboard" (height above water).
* **Scattering Mechanisms:**
    * **Specular:** Smooth surfaces reflecting energy away (appears dark).
    * **Diffuse:** Rough surface scattering returning energy to the sensor (appears grey).
    * **Double-Bounce:** High-intensity returns from the intersection of vertical ice walls and the sea surface (appears as bright "glints").
    * **Volume Scattering:** Backscatter from internal ice structures, particularly visible in **HV Polarization**.

### 3. Morphological Classification
The engine analyzes your drawing to categorize the iceberg into standard international shapes:
* **Tabular:** Flat-topped with high aspect ratios.
* **Drydock:** U-shaped notched icebergs (modeled as corner reflectors).
* **Pinnacle/Spire:** Steep-sided shapes prone to radar layover and deep shadows.
* **Dome/Blocky/Wedge:** Various other standard classifications based on asymmetry and flatness.

---

## 🛰 Educational Value
This tool demonstrates why radar interpretation of the cryosphere is complex. By adjusting sliders for **Incidence Angle**, **Roughness**, and **Dielectric Constant**, users can see how the same physical object can look completely different depending on the satellite's sensor configuration.

---

## 💻 Tech Stack
* **Language:** JavaScript (ES6+)
* **Libraries:** [jQuery](https://jquery.com/), [Turf.js](https://turfjs.org/) (Geospatial analysis)
* **Rendering:** HTML5 Canvas API

---

## 📖 How to Use
1. **Draw:** Click or touch the top canvas to plot points.
2. **Complete:** Click "Finish Iceberg" to trigger the physics engine and classification.
3. **Analyze:** Use the "SAR Simulation" panel to change the satellite's perspective.
4. **Learn:** Open the **Physics Guide** or **Shape Physics** panels for a breakdown of the scattering mechanics.

---
*Created as an educational tool for the Earth Observation and SAR community.*

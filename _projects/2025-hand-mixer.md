---
layout: project
title: Hand Mixer System Dynamics Analysis
description: System modeling, dissection, and dynamic characterization of a mechanical hand mixer.
technologies: [System Dynamics, MATLAB, Mechanical Design, Modeling]
image: /assets/images/hand-mixer-thumbnail.png
permalink: /projects/2025-hand-mixer/
---

For this System Dynamics project, I performed a complete mechanical dissection and dynamic analysis of a commercial hand mixer. The objective was to identify internal components, extract their functional relationships, build a mathematical model of the drivetrain, and validate it using measured rotational speed data.

👉 **[Download Full System Dynamics Report (PDF)]({{ "/assets/Hand_Mixer_Project.pdf" | relative_url }})**

This report includes component diagrams, free-body analyses, gears and transmission characterization, state-space modeling, and comparison of predicted vs. experimental mixer speeds at multiple power levels.

---

## Project Objectives

- Disassemble a hand mixer and identify all mechanical and electrical subsystems  
- Model torque transmission through the gear train  
- Construct a dynamic model relating motor voltage to whisk rotation speed  
- Analyze steady-state and transient behavior using differential equations and MATLAB  
- Validate the model using high-speed video measurements (750 fps)  

---

## System Overview

The hand mixer contains several key dynamic elements:

- **DC brushed motor** → electrical input converted to rotational torque  
- **Multi-stage plastic gear train** → reduces speed & increases torque  
- **Output shafts / beaters** → load with drag proportional to fluid viscosity  
- **Switching mechanism** → discrete speed increments  
- **Housing constraints** → fixed supports and bearings  

![Hand mixer internal components]({{ "/assets/images/hand-mixer-thumbnail.png" | relative_url }})

(If you'd like, I can edit or create a better thumbnail image from your photos.)

---

## Mathematical Modeling

A dynamic model was developed using Newton’s laws for rotational systems:

\[
J \dot{\omega} + b\omega + \tau_\text{load} = \tau_\text{motor}
\]

Where:

- \(J\) = equivalent rotational inertia (motor + gears + beaters)  
- \(b\) = viscous damping coefficient  
- \(\omega\) = output shaft rotational speed  
- \(\tau_\text{load}\) = torque from fluid drag  
- \(\tau_\text{motor}\) = motor torque mapped from input voltage  

Gear ratios were computed from tooth counts, allowing transformation between motor shaft speed and beater speed:

\[
\omega_\text{out} = \frac{\omega_\text{motor}}{N}
\]

where \(N\) is the total speed reduction.

Static and dynamic tests were performed to estimate:

- Motor constant \(K_t\)  
- Damping coefficient  
- Equivalent inertia  
- Load torque at different speeds  

---

## Experimental Validation

Velocity data was captured using a **750 fps high-speed camera** and analyzed frame-by-frame. Playback at 20 fps required a conversion factor:

\[
t_\text{actual} = \frac{750}{20} t_\text{playback}
\]

The measured transient speed curves were compared to the model, showing strong agreement at medium and high mixer settings.

Key experimental results include:

- Speed rise time  
- Final steady-state speed  
- Damping behavior  
- Gear noise frequency characteristics  

---

## Summary of Key Findings

| Aspect                      | Result |
|----------------------------|--------|
| Gear reduction ratio       | Determined from tooth counts |
| Motor constant \(K_t\)    | Estimated experimentally |
| Final mixer speed (setting 5) | ~1,450 RPM |
| Damping ratio              | Low (<0.1), resulting in lightly damped exponential behavior |
| Model accuracy             | Within ~5–10% of measured values |

The analysis successfully tied physical dissection to formal system modeling, demonstrating how real household appliances can be represented using classical dynamic system equations.

---

To see all diagrams, derivations, MATLAB scripts, and the full analysis, download the full PDF above.


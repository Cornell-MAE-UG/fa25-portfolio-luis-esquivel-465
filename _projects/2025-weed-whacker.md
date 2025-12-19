---
layout: project
title: Weed Whacker Carburetor Fluid Mechanics Analysis
description: Dissection and fluid-mechanics analysis of a small-engine carburetor, focusing on Venturi-driven fuel metering and mixture formation.
technologies: [Fluid Mechanics, Carburetors, Bernoulli, Venturi Effect, Control Volumes]
image: /assets/images/weed-whacker-thumbnail.png
permalink: /projects/2025-weed-whacker-carburetor/
---

For this Fluid Mechanics project, my team and I dissected a small two-stroke weed whacker and analyzed how its **carburetor** meters fuel into the airflow using the **Venturi effect**. The objective was to connect the physical components (throttle plate, venturi throat, jets, and fuel passages) to the governing fluid mechanics: pressure–velocity relationships, losses, and mixture formation.

---

## Video Walkthrough (YouTube)

[Watch the full dissection + analysis on YouTube](https://www.youtube.com/watch?v=ayXWChBD-kg)

---

## System Overview

A typical small-engine diaphragm carburetor (common on weed whackers) includes:

- **Air inlet + filter** (sets upstream conditions)
- **Throttle plate** (controls mass flow rate)
- **Venturi throat** (increases velocity, lowers static pressure)
- **Main jet / nozzle** (fuel metering into low-pressure region)
- **Diaphragm pump & regulator** (maintains fuel delivery without a float bowl)
- **Mixing region** (atomization + air–fuel mixture formation)

![Weed whacker carburetor overview]({{ "/assets/images/weed-whacker-thumbnail.png" | relative_url }})

---

## Key Fluid Mechanics Concepts

### 1) Venturi Effect and Pressure Drop

As air accelerates through the throat, static pressure drops. A simplified relationship (neglecting elevation change) is:

\[
p_1 + \frac{1}{2}\rho V_1^2 \approx p_2 + \frac{1}{2}\rho V_2^2 + \Delta p_{\text{loss}}
\]

where:

- \(p_1, V_1\): upstream pressure and velocity  
- \(p_2, V_2\): throat pressure and velocity  
- \(\Delta p_{\text{loss}}\): losses due to contraction, friction, and turbulence  

The **pressure difference** \(p_1 - p_2\) is what drives fuel through the metering jet.

---

### 2) Continuity and Mass Flow

For incompressible flow at low Mach number:

\[
\dot{m} = \rho A V
\]

When \(A\) decreases at the throat, \(V\) increases, which strengthens suction and increases fuel draw (up to limits set by jets and diaphragm regulation).

---

### 3) Fuel Metering Through the Jet

Fuel flow through the main jet can be approximated using an orifice model:

\[
\dot{m}_f = C_d A_j \sqrt{2\rho_f \Delta p}
\]

where:

- \(C_d\): discharge coefficient  
- \(A_j\): jet area  
- \(\rho_f\): fuel density  
- \(\Delta p = p_{\text{fuel}} - p_{\text{throat}}\)

This explains why changes in throat pressure (from throttle position or engine speed) change the fuel rate.

---

## Throttle Position and Mixture Behavior

The throttle plate upstream of the venturi acts as the primary flow control.

- **Low throttle:** smaller mass flow, weaker suction → lower fuel draw  
- **High throttle:** higher mass flow, higher throat velocity → stronger suction → more fuel entrainment  

This interaction makes the carburetor a coupled fluid system: throttle changes airflow, airflow changes throat pressure, throat pressure changes fuel flow, and the mixture changes engine power (which further affects airflow).

---

## Losses and Real-World Effects

In practice, the pressure drop is not purely Bernoulli due to:

- Sudden contraction/expansion losses  
- Surface roughness and boundary layer effects  
- Turbulence in the mixing region  
- Pulsating intake flow from the two-stroke cycle  
- Diaphragm pump dynamics (fuel delivery is unsteady)

A more realistic expression includes a loss coefficient \(K\):

\[
\Delta p_{\text{loss}} = K\left(\frac{1}{2}\rho V^2\right)
\]

---

## Summary

This dissection showed how a compact carburetor uses fluid mechanics to regulate mixture:

- Air accelerates through a venturi → static pressure drops  
- The resulting \(\Delta p\) pulls fuel through jets and passages  
- Throttle position changes airflow, which changes suction and fuel metering  
- Real losses and unsteady engine intake flow strongly influence performance  

This project connected real hardware to foundational concepts in **continuity**, **Bernoulli**, **orifice flow**, and **head losses**, demonstrating how fluid mechanics directly enables fuel delivery and combustion in small engines.

---

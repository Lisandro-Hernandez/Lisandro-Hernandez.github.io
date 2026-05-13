# Dynamic Simulation of the Moving Boundary Method

## 🧠 Overview
This project presents a computational exploration of the **moving boundary method**, a classical electrochemical technique used to determine ionic transport numbers. The simulation captures the dynamic evolution of the interface between two electrolyte solutions, moving beyond static descriptions to demonstrate how boundaries physically form and maintain themselves under an applied electric field.

The system illustrates the fundamental competition between:
*   **Diffusion**, which acts to blur and dissipate the interface.
*   **Electromigration**, which acts as a restorative force to sharpen the boundary.

This leads to the emergence of a **non-equilibrium steady state** where a sharp traveling wave propagates through the electrolyte.

---

## 🔬 Key Physical Additions

### Self-Sharpening Mechanism
The core of the moving boundary method is the **restorative electromigration** driven by a conductivity gradient. In the model, the migration velocity is coupled to the local concentration to mimic the physical reality of the experiment:

$$v(c) = v_{\text{lead}} + (v_{\text{trail}} - v_{\text{lead}})c$$

where:
*   $v_{\text{trail}}$ is the velocity in the trailing (higher resistance) solution.
*   $v_{\text{lead}}$ is the velocity in the leading (lower resistance) solution.

This ensures that lagging ions are "kicked" forward by the higher electric field, while leading ions that diffuse too far forward slow down, maintaining a sharp interface.

---

### Concentration Gradient Analysis
The "sharpness" of the system is quantified by analyzing the spatial derivative of the concentration profile:

$$\text{Sharpness} = \left| \frac{\partial c}{\partial x} \right|_{\max}$$

This allows for quantitative tracking of the boundary's evolution from an initially blurred state to its optimized steady-state width.

---

## 📊 Boundary Evolution Regimes

The simulation demonstrates the life cycle of a moving boundary, progressing through distinct phases:

*   **Focusing Phase (Initial Sharpening)**
    *   Electromigration dominates the initial high-entropy (blurred) state.
    *   The concentration gradient increases rapidly as ions are forced into the self-regulating boundary structure.

*   **Steady-State Displacement**
    *   A dynamic equilibrium is reached where diffusion and migration fluxes balance.
    *   The boundary maintains a constant width and shape as it translates across the spatial domain.

*   **Kohlrausch Adjustment**
    *   The trailing solution concentration adjusts to satisfy the regulating function, ensuring the interface velocity remains uniform.

<img src="./moving_boundary_evolution.png" width="700"/>

---

## 📈 Dimensionless Framework

The stability and sharpness of the boundary are governed by the balance of transport mechanisms, characterized by the grid-based **Péclet number**:

$$\mathrm{Pe} = \frac{vL}{D}$$

where:
*   $v$ is the characteristic migration velocity.
*   $L$ is the characteristic length scale of the interface.
*   $D$ is the ionic diffusion coefficient.

High Péclet numbers in the simulation correspond to the exceptionally sharp boundaries observed in laboratory experiments.

---

## 🛠 Numerical Methodology

The governing equation is a non-linear advection-diffusion PDE:

$$\frac{\partial c}{\partial t} + v(c)\frac{\partial c}{\partial x} = D\frac{\partial^2 c}{\partial x^2}$$

The system is implemented using a **stable vectorized solver** in Python:
*   **Spatial Discretization:** Central difference for diffusion and upwind schemes for migration to ensure numerical stability.
*   **Stability Control:** Automated time-step ($dt$) selection based on the CFL (Courant–Friedrichs–Lewy) condition.
*   **Vectorization:** Optimized NumPy slicing to mimic high-performance array operations.

---

## 🔑 Key Insight

This model demonstrates that the Moving Boundary Method is more than just a measurement tool; it is a **self-organizing system**. 
*   Even when starting with a heavily blurred interface, the physics of the electric field gradient forces the system into a sharp, stable configuration.
*   The simulation successfully replicates the visual phenomena recorded in laboratory observations (e.g., KCl/KNO₃ systems).

---

## 🚀 Next Extensions

This simulation provides a foundation for modeling complex transport phenomena, including:
*   Integration of the **Hittorf Method** for comparative transport analysis.
*   Multi-component ionic transport using the full **Nernst-Planck** equations.
*   Coupling with **Joule heating** effects and thermal convection analysis.
*   Implementation in **COMSOL Multiphysics** for 2D/3D interface stability modeling.

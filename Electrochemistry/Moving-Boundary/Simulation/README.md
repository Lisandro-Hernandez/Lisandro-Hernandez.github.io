# Dynamic Simulation of the Moving Boundary Method

## 🧠 Overview
This project presents a computational simulation of the **moving boundary method**, exploring how ionic interfaces physically form and maintain themselves under an applied electric field. Moving beyond static textbook descriptions, this model demonstrates the real-time transition from a blurred initial state to a sharp, stable traveling wave.

The system captures the fundamental competition between:
*   **Diffusion**, which naturally dissipates concentration gradients.
*   **Restorative Electromigration**, which acts as a "focusing" force to maintain a distinct boundary.

---

## 🔬 Key Physical Mechanisms

### Profile Dynamical Model 
The interface evolution is described by a non-linear advection-diffusion equation that governs the local concentration $c$ over time $t$:

![Advection-Diffusion Equation](https://latex.codecogs.com/svg.image?\frac{\partial%20c}{\partial%20t}%20&plus;%20v(c)\frac{\partial%20c}{\partial%20x}%20=%20D\frac{\partial^2%20c}{\partial%20x^2})

where the second term on the left represents **advection** (the physical displacement and sharpening of the boundary), and the term on the right represents **diffusion** (the natural mixing and dissipation of the gradient).

### The Self-Sharpening Effect
The core of this model is the implementation of a velocity gradient across the interface. By coupling the local migration velocity to the concentration, we simulate the higher electric field found in the trailing solution:

![Velocity Gradient](https://latex.codecogs.com/svg.image?v(c)%20=%20v_{\text{lead}}%20&plus;%20(v_{\text{trail}}%20-%20v_{\text{lead}})c)

where ![Inequality](https://latex.codecogs.com/svg.image?v_{\text{trail}}%20&gt;%20v_{\text{lead}}).

This velocity differential ensures that ions lagging behind the boundary are accelerated forward, while those diffusing too far ahead slow down. This "squeezing" effect creates the distinct interface characteristic of laboratory experiments. While the physical dependence of velocity on concentration is non-linear, this linear interpolation captures the essential restorative physics while avoiding the high computational cost of solving the full Poisson equation for the electric field at every time step.

---

## 📊 Observed Dynamics

The simulation successfully captures the two key features of electrochemical boundary evolution: **sharpening** and **displacement**. As the simulation progresses, the initially diffuse gradient "tightens" into a steady-state profile that translates uniformly across the domain.

<img src="./moving_boundary_evolution.png" width="700"/>

---

## 🛠 Numerical Methodology

The simulation solves the transport equations using a **stable vectorized solver** developed in Python:

*   **Vectorized Processing:** Utilizing NumPy array slicing to perform updates across the entire spatial domain simultaneously, mirroring the efficiency of high-performance C++/Fortran operations.
*   **Stability Constraints:** Time integration is governed by a dynamic stability check (**CFL condition**) to prevent numerical oscillations or "explosions" at the sharp interface.
*   **Upwind Discretization:** Employing an upwind scheme for the migration term to ensure the traveling wave remains physically accurate and numerically stable.

---

## 🔑 Key Insight

This project demonstrates that the Moving Boundary Method is a **self-organizing system**. The sharpening observed in the lab is not a lucky coincidence of layering, but a mathematical necessity of the electric field gradient. The simulation bridges the gap between the theoretical Nernst-Planck framework and the visual evidence captured in experimental photography.

<!-- 
---

## 🚀 Future Extensions

*   **Multi-Species Modeling:** Expanding the flux equations to include multiple cations and anions.
*   **Hittorf Method Comparison:** Developing a secondary module to simulate concentration changes in electrode compartments.
*   **Thermal Coupling:** Modeling the impact of Joule heating on the stability and shape of the moving boundary.
-->

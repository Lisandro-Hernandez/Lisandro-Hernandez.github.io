# Simulation of Phase Equilibria

## 🧠 Overview
This project investigates the thermodynamic information extracted from cubic equations of state (EoS) to model phase transitions and stability. By solving the conditions for phase equilibrium, these analyses characterize the transition from abstract molecular models to observable physical phenomena.

## 🔬 Core Analyses
* **Isotherms & Criticality:** Mapping $P-V$ behavior and identifying the critical point.
* **Coexistence Properties:** Calculation of liquid-vapor densities and orthobaric pressures.
* **Thermal Properties:** Derivation of the latent heat of vaporization ($\Delta H_{vap}$) as a function of temperature.

---

## 📊 Available Results

### Pure Component Systems
Select a model below to view the computational results for single-component phase behavior:

* **[van der Waals Model](./van%20der%20Waals/)** *Initial results and qualitative analysis of molecular attraction and excluded volume.*
* **[Redlich-Kwong Model](./Redlich%20Kwong/)** *Improved density predictions and enhanced accuracy in liquid-vapor equilibrium calculations.*

### Binary Mixtures
* **[Binary Mixtures Phase Diagram](./Binary%20Mixtures/)** *Temperature-composition ($T-x-y$) diagrams showcasing vapor-liquid equilibrium (VLE) for nearly ideal mixtures.*

---

## 🛠 Methodology
The simulations rely on finding the roots of the cubic polynomials to determine molar volumes and utilizing the **Maxwell Construction** (or fugacity coefficient equality) to locate the phase boundaries. For binary systems, equilibrium is determined by the equality of chemical potentials across phases.

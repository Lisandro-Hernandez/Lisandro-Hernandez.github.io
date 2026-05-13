# Thermodynamic Modeling of Unsteady-State Tank Filling

## 🧠 Overview
This project investigates the transient thermodynamics of a high-pressure gas filling process. While textbook problems often focus on steady-state systems, this model explores the **unsteady-state open system**, where mass and energy accumulate within a control volume. The simulation demonstrates a critical thermodynamic principle: the adiabatic filling of a vessel results in a temperature rise significantly higher than the source temperature due to the conversion of **flow work** into internal energy.

---

## 🔬 Thermodynamic Derivation

### 1. The Energy Balance (First Law)
For a rigid, adiabatic tank being filled from a supply line, the rate of change of internal energy ($U$) is governed by the enthalpy ($\hat{H}$) of the incoming stream. Neglecting kinetic and potential energy:

$$\frac{dU}{dt} = \dot{m}_{in}\hat{H}_{in}$$

Integrating from the initial state ($i$) to the final state ($f$):
$$U_f - U_i = (m_f - m_i)\hat{H}_{in}$$

### 2. Differential Temperature Evolution
By substituting $U = m\hat{C}_V T$ and $\hat{H} = \hat{C}_P T$, we derive the relationship between mass accumulation and temperature change. The governing differential equation is:

$$m dT = (\gamma T_{in} - T)dm$$

where $\gamma = \bar{C}_P / \bar{C}_V$. Integrating this expression allows us to determine the temperature $T_f$ at the exact moment the valve is closed. For an ideal gas like Argon ($\bar{C}_P = 5R/2$, $\bar{C}_V = 3R/2$):

$$T_f = T_i \left( \frac{\bar{C}_P}{R} \right) \left[ \frac{\bar{C}_V}{R} + \frac{P_i}{P_f} \right]^{-1}$$

Using $T_i = 298$ K, $P_i = 10$ bar, and $P_f = 50$ bar, the final temperature reaches **438 K**.

---

## 📊 Long-Term Thermalization & Equilibrium

Once the valve is closed, the system undergoes a slow isochoric (constant volume) cooling process as it reaches thermal equilibrium with the storage environment.

### Energy Dissipation
The heat transferred to the surroundings during this cooling phase is calculated via the change in specific internal energy:

$$\hat{q} = \Delta \hat{u} = \hat{C}_V(T_{final} - T_f)$$

For Argon ($M = 40$ kg/kmol):
$$\hat{q} = \frac{3}{2} \left( \frac{8.3145}{40} \right) (298 - 438) = -43.65 \text{ kJ/kg}$$

### Pressure Regression
As the kinetic energy of the particles decreases, the pressure drops linearly with temperature. The final stable pressure in the tank is:

$$P_{final} = P_f \left( \frac{T_{final}}{T_f} \right) = 50 \text{ bar} \left( \frac{298 \text{ K}}{438 \text{ K}} \right) = 34.02 \text{ bar}$$

---

## 🛠 Numerical Implementation

This analytical framework serves as the basis for a **Python-based transient solver** that can handle non-ideal scenarios:

*   **Real Gas Correction:** Implementation of the **Compressibility Factor ($Z$)** and residual enthalpies to account for non-ideal behavior at high pressures (50+ bar).
*   **Time-Dependent Flow:** Modeling the mass flow rate $\dot{m}$ as a function of the pressure differential ($P_{supply} - P_{tank}$) using orifice flow equations.
*   **Heat Integration:** Transitioning from an adiabatic assumption to a polytropic model by including a heat transfer coefficient ($h$) for the tank walls.

---

## 🔑 Key Insight
This model proves that **temperature is not just a measure of thermal contact, but a reflection of work performed.** Even though the supply line is at room temperature, the gas inside the tank heats up by 140 K because the environment is performing work to "shove" the gas into the rigid container. This has significant implications for the safety and material integrity of high-pressure storage systems.

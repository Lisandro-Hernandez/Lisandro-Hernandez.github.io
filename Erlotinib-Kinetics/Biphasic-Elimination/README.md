# Multi-Pathway Decay Model

## 🧪 Model Overview
This sub-project provides a detailed simulation of Erlotinib transport through a compartmental system characterized by competitive first-order reactions and zero-order systemic elimination. The primary focus is the **Sequential Metabolic Flux** case, where the drug moves from the gastrointestinal tract to the bloodstream, accompanied by parallel degradation pathways.

---

## 📝 Analytical Solution
The system is modeled with first-order absorption and degradation rates, coupled with zero-order elimination in the bloodstream. The exact analytical solutions describing the concentration of each component as a function of time are given by:

![Equation 1](https://latex.codecogs.com/svg.image?C_A(t)=C_{A0}e^{-(k_1+k_3)t})

![Equation 2](https://latex.codecogs.com/svg.image?C_B(t)=\frac{k_1C_{A0}}{k_1+k_3}\left(1-e^{-(k_1+k_3)t}\right)-k_2t)

![Equation 3](https://latex.codecogs.com/svg.image?C_C(t)=k_2t)

![Equation 4](https://latex.codecogs.com/svg.image?C_D(t)=\frac{k_3C_{A0}}{k_1+k_3}\left(1-e^{-(k_1+k_3)t}\right))

These equations capture the dual behavior of the drug where exponential intake transitions into linear elimination.

---

## 📊 Simulation Results

The simulation profiles the concentrations of the drug in each compartment over a 10-hour window, assuming an initial dose $C_{A0} = 1.0 \text{ mol/L}$.



### Key Observations
1. **The Absorption Phase:** The drug in the stomach ($C_A$) decays exponentially, transferring mass to the bloodstream and undergoing competitive degradation.
2. **The Circulation Peak:** The blood concentration ($C_B$) reaches its maximum at $t_{max}$, determined by the rate at which intake balances the zero-order elimination rate $k_2$.
3. **Accumulation Limits:** The gastric degradation product ($C_D$) approaches an asymptotic upper bound, while systemic metabolites ($C_C$) increase linearly over time.

---

## 🛠 Methodology
The concentrations are calculated using the analytical solutions derived from the coupled mass balance. The Python implementation uses `numpy` for vectorized calculations and `matplotlib` for high-fidelity visualization.

### Parameter Set

| Parameter | Description | Value |
| :--- | :--- | :--- |
| $k_1$ | Rate constant (Stomach → Bloodstream) | $0.5 \text{ hr}^{-1}$ |
| $k_2$ | Zero-order elimination rate | $0.05 \text{ mol}/(\text{L}\cdot\text{hr})$ |
| $k_3$ | First-order gastric degradation rate | $0.1 \text{ hr}^{-1}$ |
| $C_{A0}$ | Initial concentration | $1.0 \text{ mol/L}$ |

---

## 🚀 Run Simulation
To regenerate these plots locally:

```bash
python erlotinib_kinetics_sim.py

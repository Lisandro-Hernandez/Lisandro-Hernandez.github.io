# Multi-Pathway Decay Model

## 🧪 Model Overview
This sub-project provides a detailed simulation of drug transport through a compartmental system characterized by competitive first-order reactions. The primary focus is the **Kinetic Resonance** case, where the total exit rate from the stomach is identical to the total exit rate from the blood circulation.

## 📝 Analytical Solution
For a system where ![Resonance Condition](https://latex.codecogs.com/svg.image?k_1&plus;k_4=k_2&plus;k_3=\lambda), the concentration of the drug in the bloodstream does not follow a standard bi-exponential decay. Instead, it is described by a gamma-distribution profile:

![Cr Equation](https://latex.codecogs.com/svg.image?C_R(t)=k_1C_{A_0}te^{-\lambda&space;t})

This represents a **critically damped** system, providing the maximum possible peak concentration for a given set of rate constants.

## 📊 Simulation Results

The plot below illustrates the concentration profiles over a 5-hour window, assuming an initial dose ![CA0](https://latex.codecogs.com/svg.image?C_{A,0}=100).

![Pharmacokinetics Decay Plot](./pharmacokinetics_decay_plot.png)

### Key Observations
1. **The Absorption Phase:** The drug in the stomach (![CA](https://latex.codecogs.com/svg.image?C_A)) decays purely exponentially, reaching near-zero levels within 2 hours.
2. **The Circulation Peak:** The blood concentration (![CR](https://latex.codecogs.com/svg.image?C_R)) reaches its maximum at ![t_max](https://latex.codecogs.com/svg.image?t=1/\lambda). In this simulation (![lambda=3](https://latex.codecogs.com/svg.image?\lambda=3)), the peak occurs at **20 minutes**.
3. **Bioavailability Plateau:** The final accumulation in the tumor (![CS](https://latex.codecogs.com/svg.image?C_S)) levels off at approximately **22.2%**. This value is determined by the "branching ratio" of the competitive pathways:
   ![Bioavailability Formula](https://latex.codecogs.com/svg.image?\text{Bioavailability}=\frac{k_1k_2}{(k_1+k_4)(k_2+k_3)})

## 🛠 Methodology
The concentrations are calculated using the analytical solutions derived from the coupled ODE system. The Python implementation uses `numpy` for vectorized calculations and `matplotlib` for high-fidelity visualization.

### Parameter Set
| Parameter | Description | Value |
| :--- | :--- | :--- |
| ![k1](https://latex.codecogs.com/svg.image?k_1) | Stomach → Blood | 2.0 hr⁻¹ |
| ![k4](https://latex.codecogs.com/svg.image?k_4) | Stomach Degradation | 1.0 hr⁻¹ |
| ![k2](https://latex.codecogs.com/svg.image?k_2) | Blood → Target | 1.0 hr⁻¹ |
| ![k3](https://latex.codecogs.com/svg.image?k_3) | Systemic Loss | 2.0 hr⁻¹ |

## 🚀 Run Simulation
To regenerate these plots locally:
```bash
python pharmacokinetics_sim.py

# Kinetics of Erlotinib Distribution and Degradation

## 🧠 Overview
This project investigates the metabolic pathways of the anticancer drug Erlotinib following oral administration. By modeling the transition from the gastrointestinal tract to the bloodstream, the simulation accounts for competitive degradation by gastric processes and bacterial attack. The model specifically addresses the transition from first-order absorption to zero-order systemic elimination, characterizing the drug's residence time and therapeutic availability.

---

## 🔬 Core Analyses
* **Sequential Metabolic Flux:** Mapping the conversion of Erlotinib from the stomach ($C_A$) to the bloodstream ($C_B$), while accounting for parallel degradation ($C_D$).
* **Zero-Order Elimination Dynamics:** Analyzing the systemic clearance of Erlotinib ($C_C$), which follows a zero-order rate law, creating a distinct linear decay profile once absorption diminishes.
* **Peak Plasma Concentration:** Determining the critical time ($t_{max}$) and magnitude ($C_{B,max}$) of the drug in the bloodstream to establish the effective therapeutic window.
* **Accumulation Limits:** Quantifying the irreversible accumulation of degraded metabolites and identifying why gastric degradation ($C_D$) lacks a local maximum.

---

## 📊 Available Results

### Pharmacokinetic Models
Select a model below to view the computational results for Erlotinib behavior:

* **Biphasic Elimination Model:** Analysis of the transition between the absorption-dominant phase and the zero-order elimination phase.
* **Degradation Sensitivity:** Study of how the gastric degradation rate ($k_3$) impacts the total bioavailability of Erlotinib in the blood.

### System Parameters
* **Residence Time Profiles:** Detailed sketches of concentration gradients for components A, B, C, and D based on relative rate constants ($k_3 < k_1$, $k_1 > k_2$).
* **Saturation Limits:** Calculation of the asymptotic behavior of metabolites as $t \to \infty$.

---

## 🛠 Methodology
The simulation uses the exact analytical solutions derived from the mass balance $C_A + C_B + C_C + C_D = C_{A0}$, incorporating first-order kinetics for absorption and degradation, along with zero-order kinetics for systemic metabolism:

$$C_A(t) = C_{A0} e^{-(k_1+k_3)t}$$

$$C_B(t) = \frac{k_1 C_{A0}}{k_1 + k_3} \left(1 - e^{-(k_1+k_3)t}\right) - k_2 t$$

$$C_C(t) = k_2 t$$

$$C_D(t) = \frac{k_3 C_{A0}}{k_1 + k_3} \left(1 - e^{-(k_1+k_3)t}\right)$$

The analytical solution accounts for two distinct regimes:
1. **Absorption Phase:** Where $C_A$ provides a sufficient influx to the bloodstream.
2. **Depletion Phase:** Where the zero-order elimination ($k_2$) dominates as $C_A$ approaches zero.

---

## 🚀 Usage
To run the Erlotinib distribution simulation and generate the concentration profiles, execute the following script:

```bash
python erlotinib_kinetics_sim.py

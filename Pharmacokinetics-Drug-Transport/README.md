# Kinetics of Drug Delivery and Accumulation

## 🧠 Overview
This project investigates the multi-compartment kinetic behavior of a drug following oral administration. By solving the coupled mass balance equations for absorption, systemic distribution, and competitive degradation, the simulation characterizes the transition of the drug from the stomach to the bloodstream and its eventual accumulation at target tumor sites.

## 🔬 Core Analyses
* **Transient Compartmental Response:** Mapping the rise and fall of drug concentration in the blood ($C_R$) and its depletion from the stomach ($C_A$).
* **Kinetic Resonance:** Analyzing the "critically damped" state where absorption and elimination rates are matched ($k_1 + k_4 = k_2 + k_3$), leading to a gamma-distribution profile.
* **Bioavailability & Accumulation:** Quantifying the total fraction of the drug that successfully reaches the target tumor ($S$) versus the fraction lost to degradation ($W$ and $T$).

---

## 📊 Available Results

### Pharmacokinetic Models
Select a model below to view the computational results for drug distribution behavior:

* **[Multi-Pathway Decay Model](./Multi-Pathway-Decay/)** Analysis of systemic distribution with simultaneous competitive degradation: ![Inlet](https://latex.codecogs.com/svg.image?C_A(t)=C_{A_0}e^{-(k_1+k_4)t})
* **[Critical Resonance Analysis](./Critical-Resonance/)** Study of the system behavior when input and output rates are mathematically balanced.

### System Parameters
* **[Bioavailability Studies](./Bioavailability/)** *Sensitivity analysis of rate constants on the final therapeutic accumulation in target tissues.*

## 🛠 Methodology
The simulations rely on solving the system of first-order linear differential equations derived from the compartmental mass balance:

![Differential Equation](https://latex.codecogs.com/svg.image?\begin{align*}\frac{dC_A}{dt}&=-(k_1+k_4)C_A\\ \frac{dC_R}{dt}&=k_1C_A-(k_2+k_3)C_R\end{align*})

The analytical solution is implemented in Python, accounting for the unique case of identical roots in the characteristic equation. The model highlights the **Therapeutic Window**, identifying the time to peak concentration ($t_{max}$) and the duration of effective drug presence in the bloodstream.

## 🚀 Usage
To run the pharmacokinetic simulation and generate the distribution plots, execute the main script:
```bash
python pharmacokinetics_sim.py

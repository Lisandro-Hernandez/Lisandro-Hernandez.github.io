# Aqueous Acid–Base Multi-Equilibrium Systems

## 🧠 Overview
This project focuses on the rigorous modeling of chemical equilibria in aqueous solutions. Unlike simplified approximations (such as the Henderson-Hasselbalch equation), these simulations solve the full system of non-linear equations—incorporating charge balance, mass balance, and water self-ionization—to provide numerically exact descriptions of ionic concentrations and pH behavior.

## 🔬 Core Analyses
* **Exact Titration Curves:** Solving for pH as a function of titrant volume without neglecting auto-protolysis or minor ionic species.
* **Speciation Modeling:** Calculating the fractional distribution ($\alpha$ values) of protonated and deprotonated species across the pH scale.
* **Heterogeneous Equilibrium:** Modeling the dissolution and titration of solid-phase carbonates in the presence of atmospheric or dissolved $CO_2$.

---

## 📊 Available Results

### 🧪 Acid-Base Titrations
Numerical solutions for the titration of various acid systems with a strong base (e.g., $NaOH$). Results include pH curves and derivative plots for endpoint detection.

* **[Acid-Base Titration Curves](./Acid-Base%20Titrations/)**
    * *Strong Acids:* Modeling the sharp transition of $HCl$.
    * *Weak & Polyprotic Acids:* Exact solutions for $KHP$ and Maleic acid, accounting for multiple dissociation constants ($K_{a1}, K_{a2}$).

### 💊 Antacid Analysis
Investigation of the buffering capacity and neutralization profile of calcium carbonate.

* **[Calcium Carbonate Titration](./Antacid%20Analysis/)** *Simulation of the titration of $CaCO_3$, incorporating the carbonate/bicarbonate equilibrium and the effects of $CO_2$ solubility.*

---

## 🛠 Methodology
The simulations utilize a **Charge Balance** approach. For any system, the sum of cationic charges must equal the sum of anionic charges:

$$\sum [Cationic\ Charges] = \sum [Anionic\ Charges]$$

By substituting mass balance expressions and acid dissociation constants ($K_a$) into the charge balance equation, the system is reduced to a polynomial in $[H^+]$. These polynomials (ranging from cubic to high-order for polyprotic systems) are solved numerically using root-finding algorithms to generate exact titration curves.

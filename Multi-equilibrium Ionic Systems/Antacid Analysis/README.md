# 📊 Antacid Analysis: Calcium Carbonate Systems

## 🧠 Overview
This repository provides a rigorous numerical analysis of the **direct titration** of Calcium Carbonate ($CaCO_3$) using both strong ($HCl$) and weak ($KHP$) acids. Unlike simplified models, these results are derived by solving the full system of coupled equilibrium equations, accounting for:
* **Heterogeneous Equilibrium:** The solubility product ($K_{sp}$) of $CaCO_3(s)$.
* **Carbonate Speciation:** The multi-stage equilibria of the $CO_2/HCO_3^-/CO_3^{2-}$ system.
* **Solvent Autoprotolysis:** The self-ionization of water.

## 📈 Visualizations

<img src="Titration_CaCO3_and_Ca.png" alt="Titration of CaCO3 showing pH and Ca2+ dissolution" width="600">

<img src="Titration_CaCO3_and_CO2Gas.png" alt="CO2 gas/aqueous ratio during titration" width="600">

<img src="Titration_CaCO3_Comparison.png" alt="Comparison between CaCO3 and NaOH titration curves" width="600">

## 🔍 Section Descriptions
* **$CaCO_3$ Buffering & Calcium Dissolution:** The first figure illustrates the $pH$ profile and the corresponding increase in $[Ca^{2+}]$ as the mineral phase dissolves. The calcium concentration reaches its plateau exactly when the solid phase is fully consumed.
* **$CO_2$ Phase Distribution:** The second figure tracks the evolution of dissolved $CO_2(aq)$ into the gas phase ($CO_2(g)$) as the solution acidifies. It quantifies the rapid shift in equilibrium where $CO_2(g)$ becomes the dominant species.
* **Comparative Neutralization:** The third figure overlays the titration curves of $CaCO_3$ and $NaOH$ against $HCl$ for equivalent molar amounts, highlighting the differences in buffering regions and the convergence at the equivalence point.

## 💡 Key Insights
* **Robust Buffering:** $CaCO_3(s)$ in water acts as a high-capacity, slightly basic buffer. The stoichiometric dissolution is completed at the point of maximum $[Ca^{2+}]$, providing a clear marker for the phase transition.
* **Degassing Dynamics:** As $HCl$ is added, the system quickly generates $CO_2$. After just a few milliliters of titrant, the partial pressure of $CO_2(g)$ results in a concentration nearly 50 times greater than that of the aqueous $CO_2$.
* **Foundation for Back Titration:** The convergence of the $CaCO_3$ and $NaOH$ curves post-equivalence point demonstrates that the final $pH$ is governed solely by excess $HCl$. This justifies the **back titration method** commonly used in analytical chemistry to determine the neutralization capacity of antacids.

## 🛠 Methodology
The underlying solutions utilize numerical root-finding to solve the charge balance equation of the multi-component system. The Python code for these simulations is available upon request.

# Bioavailability & Sensitivity Analysis

## 🎯 Optimization Goal
The ultimate success of a pharmacokinetic system is measured by its **Bioavailability**: the fraction of the initial dose that successfully reaches the target site ($S$). In this model, the target accumulation competes with gastric degradation ($W$) and systemic protein-binding or loss ($T$).

## 📊 Sensitivity Analysis
The plot below demonstrates how the final distribution of the drug shifts as a function of the targeting rate constant (![k2](https://latex.codecogs.com/svg.image?k_2)), while maintaining a constant systemic elimination rate sum.

![Bioavailability Sensitivity Plot](./bioavailability_sensitivity_plot.png)

### Distribution Breakdown
As ![time](https://latex.codecogs.com/svg.image?t\to\infty), the system reaches a steady state where all of the drug has been distributed into one of the three "sink" compartments. The final percentages are calculated using the branching ratios of the competitive pathways:

* **Target Bioavailability (![fS](https://latex.codecogs.com/svg.image?f_S)):** ![fs_eq](https://latex.codecogs.com/svg.image?f_S=\frac{k_1}{k_1+k_4}\cdot\frac{k_2}{k_2+k_3})
* **Systemic Loss (![fT](https://latex.codecogs.com/svg.image?f_T)):** ![ft_eq](https://latex.codecogs.com/svg.image?f_T=\frac{k_1}{k_1+k_4}\cdot\frac{k_3}{k_2+k_3})
* **Gastric Loss (![fW](https://latex.codecogs.com/svg.image?f_W)):** ![fw_eq](https://latex.codecogs.com/svg.image?f_W=\frac{k_4}{k_1+k_4})

## 🔬 Key Insights
1.  **The Gastric Ceiling:** Regardless of how efficient the blood-to-tumor targeting becomes, the bioavailability is capped by the initial gastric degradation. In this model, with ![k1=2, k4=1](https://latex.codecogs.com/svg.image?k_1=2,k_4=1), at least **33.3%** of the drug is lost before it even enters the circulation.
2.  **Targeting Efficiency:** To achieve a bioavailability of >50%, the targeting rate ![k2](https://latex.codecogs.com/svg.image?k_2) must be significantly higher than the systemic loss rate ![k3](https://latex.codecogs.com/svg.image?k_3). 
3.  **Mass Balance Consistency:** The stacked area chart confirms the conservation of mass, as the sum of the three fractions always equals 100% of the initial dose ![CA0](https://latex.codecogs.com/svg.image?C_{A,0}).

## 🛠 Methodology
The sensitivity analysis was performed by sweeping ![k2](https://latex.codecogs.com/svg.image?k_2) from 0.1 to 2.9 hr⁻¹ and calculating the asymptotic limits of the analytical solutions.

## 🚀 Run Sensitivity Study
Execute the script to view the interactive plot and explore different branching ratio scenarios:
```bash
python bioavailability_sensitivity_study.py

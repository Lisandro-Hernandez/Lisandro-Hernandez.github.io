# Moving Boundary Method

## 🧠 Overview

This project explores the **moving boundary method** from both experimental and theoretical perspectives, with emphasis on ionic transport and boundary propagation in electrolyte systems.

The experiment demonstrates the evolution of the interface between two electrolyte solutions, showing both the **displacement** and **sharpening** of the moving boundary over time. The system consists of aqueous **KCl/KNO₃** solutions studied in laboratory experiments conducted in Dr. Hernández’s electrochemistry course at Kettering University.

The moving boundary method provides a classical framework for analyzing:
- ionic mobility,
- transport processes,
- concentration gradients,
- and electrochemical migration phenomena.

The images below illustrate the evolution of the electrolyte boundary during the experiment.

<p align="center">
  <img src="./Picture_1.JPG" width="400"/>
  <img src="./Picture_4.JPG" width="400"/>
</p>

### 📝 Finding Transport Numbers and Ionic Mobilities

To determine the transport properties of the **0.1 M HCl** solution, we utilize the following experimental parameters:
*   **Concentration ($c$):** $0.1\text{ M} = 100\text{ mol/m}^3$
*   **Conductivity ($\sigma$):** $4.2\text{ S/m}$
*   **Current ($I$):** $0.003\text{ A}$
*   **Cross-section ($A$):** $0.3\text{ cm}^2 = 3 \times 10^{-5}\text{ m}^2$
*   **Distance ($L$):** $3.08\text{ cm} = 0.0308\text{ m}$
*   **Time ($t$):** $1\text{ hour} = 3600\text{ s}$

---

#### 1. Transport Number ($t_+$)
The transport number for the cation ($H^+$) is calculated using the volume swept by the boundary ($V = A \cdot L$) and the total charge passed ($Q = I \cdot t$):

![Transport Number Equation](https://latex.codecogs.com/svg.image?t_+%20=%20\frac{z_+%20F%20c%20V}{I%20t}%20=%20\frac{(1)(96485)(100)(3%20\times%2010^{-5}%20\times%200.0308)}{(0.003)(3600)})

**$t_{H^+} \approx 0.825$**

Since ![Sum of Transport Numbers](https://latex.codecogs.com/svg.image?t_+%20+%20t_-%20=%201), the transport number for $Cl^-$ is:
**$t_{Cl^-} = 1 - 0.825 = 0.175$**

---

#### 2. Ionic Mobilities ($u_i$)
The mobility is related to the transport number and the total conductivity of the solution:

![Mobility Relation](https://latex.codecogs.com/svg.image?u_i%20=%20\frac{t_i%20\sigma}{z_i%20F%20c})

*   **For $H^+$:**
    ![Mobility H+](https://latex.codecogs.com/svg.image?u_{H^+}%20\approx%203.59%20\times%2010^{-7}%20\text{%20m}^2\text{V}^{-1}\text{s}^{-1})

*   **For $Cl^-$:**
    ![Mobility Cl-](https://latex.codecogs.com/svg.image?u_{Cl^-}%20\approx%207.61%20\times%2010^{-8}%20\text{%20m}^2\text{V}^{-1}\text{s}^{-1})

---

#### 3. Molar Ionic Conductivities ($\lambda_i$)
The molar ionic conductivity (![Molar Conductivity Relation](https://latex.codecogs.com/svg.image?\lambda_i%20=%20t_i%20\Lambda)) where ![Molar Conductivity Value](https://latex.codecogs.com/svg.image?\Lambda%20=%20\sigma/c%20=%200.042%20\text{%20S%20m}^2\text{mol}^{-1}):

*   **![Lambda H+](https://latex.codecogs.com/svg.image?\lambda_{H^+}%20\approx%203.47%20\times%2010^{-2}%20\text{%20S%20m}^2\text{mol}^{-1})**
*   **![Lambda Cl-](https://latex.codecogs.com/svg.image?\lambda_{Cl^-}%20\approx%207.35%20\times%2010^{-3}%20\text{%20S%20m}^2\text{mol}^{-1})**

---

### 🔑 Key Insight
The high transport number and mobility of the $H^+$ ion ($t_+ \approx 0.83$) compared to $Cl^-$ ($t_- \approx 0.17$) illustrates the unique **Grotthuss mechanism** (proton hopping) in aqueous solutions, which allows protons to move much faster than standard hydrodynamic migration.

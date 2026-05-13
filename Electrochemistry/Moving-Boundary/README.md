# Moving Boundary Method

## 🧠 Overview

This project explores the **moving boundary method** from both experimental and theoretical perspectives, emphasizing ionic transport and boundary propagation in electrolyte systems.

The moving boundary method was investigated through laboratory experiments in Dr. Hernández’s Electrochemistry course at Kettering University. The system shown in the images below corresponds to aqueous KNO<sub>3</sub>/KMnO<sub>4</sub> solutions, illustrating the evolution of the electrolyte boundary during the experiment. The results demonstrate the progression of the interface between two electrolyte solutions, specifically highlighting both the displacement and sharpening of the moving boundary over time.

<p align="center">
  <img src="./Picture_1.JPG" width="400"/>
  <img src="./Picture_4.JPG" width="400"/>
</p>

Experimental Configuration: To ensure gravitational stability, the system was modeled after a U-tube apparatus. The trailing KMnO<sub>4</sub> solution was layered atop the leading KNO<sub>3</sub> in a vertical column, creating a descending boundary. This physical arrangement, combined with the self-sharpening effect, prevents convective mixing and maintains a sharp colorimetric interface for measurement.

The moving boundary method provides a classical framework for analyzing:
*   Ionic mobility
*   Transport processes
*   Concentration gradients
*   Electrochemical migration phenomena

  
### 📝 Finding Transport Numbers and Ionic Mobilities

To determine the transport properties of a **0.1 M HCl** solution, we employed the following experimental conditions:
*   **Concentration ($c$):** $0.1\text{ M} = 100\text{ mol/m}^3$
*   **Conductivity ($\sigma$):** $4.2\text{ S/m}$
*   **Current ($I$):** $0.003\text{ A}$
*   **Cross-section ($A$):** $0.3\text{ cm}^2 = 3 \times 10^{-5}\text{ m}^2$
*   **Distance ($L$):** $3.08\text{ cm} = 0.0308\text{ m}$
*   **Time ($t$):** $1\text{ hour} = 3600\text{ s}$

---

#### 1. Transport Number ($t_+$)
The transport number for the cation ($H^+$) is calculated using the volume swept by the boundary ($V = A \cdot L$) and the total charge passed ($Q = I \cdot t$):

![Transport Number Equation](https://latex.codecogs.com/svg.image?t_%2b%20%3d%20%5cfrac%7bz_%2b%20F%20c%20V%7d%7bI%20t%7d%20%3d%20%5cfrac%7b%281%29%2896485%29%28100%29%283%20%5ctimes%2010%5e%7b-5%7d%20%5ctimes%200.0308%29%7d%7b%280.003%29%283600%29%7d)

**$t_{H^+} \approx 0.825$**

Since ![Sum of Transport Numbers](https://latex.codecogs.com/svg.image?t_%2b%20%2b%20t_-%20%3d%201), the transport number for $Cl^-$ is:
**$t_{Cl^-} = 1 - 0.825 = 0.175$**

---

#### 2. Ionic Mobilities ($u_i$)
The mobility is related to the transport number and the total conductivity of the solution:

![Mobility Relation](https://latex.codecogs.com/svg.image?u_i%20%3d%20%5cfrac%7bt_i%20%5csigma%7d%7bz_i%20F%20c%7d)

*   **For $H^+$:**
    ![Mobility H+](https://latex.codecogs.com/svg.image?u_%7bH%5e%2b%7d%20%5capprox%203.59%20%5ctimes%2010%5e%7b-7%7d%20%5ctext%7b%20m%7d%5e2%5ctext%7bV%7d%5e%7b-1%7d%5ctext%7bs%7d%5e%7b-1%7d)

*   **For $Cl^-$:**
    ![Mobility Cl-](https://latex.codecogs.com/svg.image?u_%7bCl%5e-%7d%20%5capprox%207.61%20%5ctimes%2010%5e%7b-8%7d%20%5ctext%7b%20m%7d%5e2%5ctext%7bV%7d%5e%7b-1%7d%5ctext%7bs%7d%5e%7b-1%7d)

---

#### 3. Molar Ionic Conductivities ($\lambda_i$)
The molar ionic conductivity (![Molar Conductivity Relation](https://latex.codecogs.com/svg.image?%5clambda_i%20%3d%20t_i%20%5cLambda)) where ![Molar Conductivity Value](https://latex.codecogs.com/svg.image?%5cLambda%20%3d%20%5csigma/c%20%3d%200.042%20%5ctext%7b%20S%20m%7d%5e2%5ctext%7bmol%7d%5e%7b-1%7d):

*   **![Lambda H+](https://latex.codecogs.com/svg.image?%5clambda_%7bH%5e%2b%7d%20%5capprox%203.47%20%5ctimes%2010%5e%7b-2%7d%20%5ctext%7b%20S%20m%7d%5e2%5ctext%7bmol%7d%5e%7b-1%7d)**
*   **![Lambda Cl-](https://latex.codecogs.com/svg.image?%5clambda_%7bCl%5e-%7d%20%5capprox%207.35%20%5ctimes%2010%5e%7b-3%7d%20%5ctext%7b%20S%20m%7d%5e2%5ctext%7bmol%7d%5e%7b-1%7d)**

---

### 🔑 Key Insight
The high transport number and mobility of the $H^+$ ion ($t_+ \approx 0.83$) compared to $Cl^-$ ($t_- \approx 0.17$) illustrates the unique **Grotthuss mechanism** (proton hopping) in aqueous solutions, which allows protons to move much faster than standard hydrodynamic migration.

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

### 📝 Exercise Solution: Transport Numbers and Ionic Mobilities

To determine the transport properties of the **0.1 M HCl** solution, we utilize the experimental parameters provided:
*   **Concentration ($c$):** $0.1\text{ M} = 100\text{ mol/m}^3$
*   **Conductivity ($\sigma$):** $4.2\text{ S/m}$
*   **Current ($I$):** $0.003\text{ A}$
*   **Cross-section ($A$):** $0.3\text{ cm}^2 = 3 \times 10^{-5}\text{ m}^2$
*   **Distance ($L$):** $3.08\text{ cm} = 0.0308\text{ m}$
*   **Time ($t$):** $1\text{ hour} = 3600\text{ s}$

---

#### 1. Transport Number ($t_+$)
The transport number for the cation ($H^+$) is calculated using the volume swept by the boundary ($V = A \cdot L$) and the total charge passed ($Q = I \cdot t$):

$$t_+ = \frac{z_+ F c V}{I t} = \frac{(1)(96485)(100)(3 \times 10^{-5} \times 0.0308)}{(0.003)(3600)}$$

**$t_{H^+} \approx 0.825$**

Since $t_+ + t_- = 1$, the transport number for $Cl^-$ is:
**$t_{Cl^-} = 1 - 0.825 = 0.175$**

---

#### 2. Ionic Mobilities ($u_i$)
The mobility is related to the transport number and the total conductivity of the solution:

$$u_i = \frac{t_i \sigma}{z_i F c}$$

*   **For $H^+$:**
    $$u_{H^+} \approx 3.59 \times 10^{-7} \text{ m}^2\text{V}^{-1}\text{s}^{-1}$$

*   **For $Cl^-$:**
    $$u_{Cl^-} \approx 7.61 \times 10^{-8} \text{ m}^2\text{V}^{-1}\text{s}^{-1}$$

---

#### 3. Molar Ionic Conductivities ($\lambda_i$)
The molar ionic conductivity ($\lambda_i = t_i \Lambda$) where $\Lambda = \sigma/c = 0.042 \text{ S m}^2\text{mol}^{-1}$:

*   **$\lambda_{H^+} \approx 3.47 \times 10^{-2} \text{ S m}^2\text{mol}^{-1}$**
*   **$\lambda_{Cl^-} \approx 7.35 \times 10^{-3} \text{ S m}^2\text{mol}^{-1}$**

---

### 🔑 Key Insight
The high transport number and mobility of the $H^+$ ion ($t_+ \approx 0.83$) compared to $Cl^-$ ($t_- \approx 0.17$) illustrates the unique **Grotthuss mechanism** (proton hopping) in aqueous solutions, which allows protons to move much faster than standard hydrodynamic migration.

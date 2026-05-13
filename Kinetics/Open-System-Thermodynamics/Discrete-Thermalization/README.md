# Discrete Thermalization and Dynamical Heat Transfer

## 🧠 Overview
This project explores the transition from discrete thermalization events to continuous dynamical heat transfer. By analyzing a series of successive thermal contacts between two liquid masses at different temperatures, the model demonstrates how a kinetic process—typically described by differential equations—emerges at the limit of infinite discrete thermalization processes.

---

## 📝 Exercise: Sequential Thermal Contact

### 1. Equilibrium of Two Masses
Consider masses ![Mass A](https://latex.codecogs.com/svg.image?m_A) and ![Mass B](https://latex.codecogs.com/svg.image?m_B) of the same liquid at temperatures ![Temperature A](https://latex.codecogs.com/svg.image?T_A) and ![Temperature B](https://latex.codecogs.com/svg.image?T_B), where ![Ta > Tb](https://latex.codecogs.com/svg.image?T_A%20%3E%20T_B). When placed in thermal contact, the heat lost by A is absorbed by B:

![Energy Balance Equation](https://latex.codecogs.com/svg.image?0%20%3D%20m_A%20%5Chat%7BC%7D%20(T%20-%20T_A)%20+%20m_B%20%5Chat%7BC%7D%20(T%20-%20T_B))

Solving for the final temperature ![T](https://latex.codecogs.com/svg.image?T):

![Final Temperature Solution](https://latex.codecogs.com/svg.image?T%20%3D%20%5Cfrac%7Bm_A%7D%7BM%7D%20T_A%20+%20%5Cleft(1%20-%20%5Cfrac%7Bm_A%7D%7BM%7D%5Cright)%20T_B)

where ![Total Mass](https://latex.codecogs.com/svg.image?M%20%3D%20m_A%20+%20m_B).

### 2. Successive Thermalization Events
A large mass ![mB](https://latex.codecogs.com/svg.image?m_B) is thermalized by successive contacts with a much smaller mass ![mA](https://latex.codecogs.com/svg.image?m_A) (always at ![TA](https://latex.codecogs.com/svg.image?T_A)). Let ![x](https://latex.codecogs.com/svg.image?x%20%3D%20m_A/M) and ![Tk](https://latex.codecogs.com/svg.image?T_k) be the temperature after ![k](https://latex.codecogs.com/svg.image?k) contacts. The recurrence relation is:

![Recurrence Relation](https://latex.codecogs.com/svg.image?T_k%20%3D%20x%20T_A%20+%20T_%7Bk-1%7D(1-x))

The resulting temperature can be written as:

![Tk General Expression](https://latex.codecogs.com/svg.image?T_k%20%3D%20R_k%20T_A%20+%20L_k%20T_B)

where:
*   ![Lk Definition](https://latex.codecogs.com/svg.image?L_k%20%3D%20(1-x)%5Ek)
*   ![Rk Definition](https://latex.codecogs.com/svg.image?R_k%20%3D%201%20-%20(1-x)%5Ek)

### 3. The Continuous Limit
In the limit where ![x to 0](https://latex.codecogs.com/svg.image?x%20%5Cto%200), we use the approximation ![ln approximation](https://latex.codecogs.com/svg.image?%5Cln(1-x)%20%5Capprox%20-x):

![Limit derivation](https://latex.codecogs.com/svg.image?%5Clim_%7Bx%20%5Cto%200%7D%20(1-x)%5Ek%20%3D%20%5Clim_%7Bx%20%5Cto%200%7D%20e%5E%7Bk%5Cln(1-x)%7D%20%5Capprox%20e%5E%7B-kx%7D)

The temperature at step ![k](https://latex.codecogs.com/svg.image?k) for very small ![x](https://latex.codecogs.com/svg.image?x) becomes:

![Tk Continuous Form](https://latex.codecogs.com/svg.image?T_k%20%3D%20T_A%20-%20(T_A%20-%20T_B)%20e%5E%7B-kx%7D)

---

## 📊 Numerical Visualization
For ![TA = 400K](https://latex.codecogs.com/svg.image?T_A%20%3D%20400%5Ctext%7B%20K%7D), ![TB = 300K](https://latex.codecogs.com/svg.image?T_B%20%3D%20300%5Ctext%7B%20K%7D), and ![x = 0.1](https://latex.codecogs.com/svg.image?x%20%3D%200.1), the discrete steps (points) are compared against the limiting exponential form (line):

<p align="center">
  <img src="./T_k_plot.png" width="600"/>
</p>

The smaller the ratio ![x](https://latex.codecogs.com/svg.image?x), the greater the agreement between the discrete events and the continuous curve.

---

## 🔑 Key Insight: Connection to Kinetic Models
This exercise demonstrates that a dynamical heat transfer process can be modeled without differential equations by treating it as a limit of discrete events.

By defining the total mass added at time ![t](https://latex.codecogs.com/svg.image?t) as ![mass flow](https://latex.codecogs.com/svg.image?%5Cdot%7Bm%7D_A%20t%20%3D%20k%20m_A), the discrete solution maps directly to the standard kinetic heat transfer model:

![Continuous Kinetic Model](https://latex.codecogs.com/svg.image?T(t)%20%3D%20T_A%20-%20(T_A%20-%20T_B)%20e%5E%7B-(%5Cdot%7Bm%7D/M)t%7D)

**Underlying Assumptions:**
*   **Time Scales:** The rate of thermal equilibration is assumed to be instantaneous compared to the rate of mass addition.
*   **Mass Conservation:** The rate of mass exit must equal the rate of mass addition (![mdot](https://latex.codecogs.com/svg.image?%5Cdot%7Bm%7D_A)) to keep the total system mass ![M](https://latex.codecogs.com/svg.image?M) constant.

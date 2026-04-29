# Dynamics of Chemical Reactors

## 🧠 Overview
This project investigates the transient behavior of an ideal Continuous Stirred-Tank Reactor (CSTR) subjected to time-varying feed conditions. By solving the dynamic mass balance for a first-order irreversible reaction, the simulation characterizes the transition from initial reactor states to a moving steady-state equilibrium governed by inlet decay.

## 🔬 Core Analyses
* **Transient Response:** Mapping the decay of initial reactor concentration $C_{A,0}$ and the "washout" effect.
* **Lead-Lag Dynamics:** Characterizing the temporal shift and concentration "lag" between the inlet feed and the reactor environment.
* **Kinetic Interaction:** Analyzing the coupled effect of the residence time ($\tau$) and the reaction rate constant ($k$) on reactant conversion.

---

## 📊 Available Results

### Reactor System Models
Select a model below to view the computational results for reactor concentration behavior:

* **[Linear Inlet Decay Model](./Linear-Inlet-Decay/)** Analysis of reactor when subjected to a constant ramp down in feed concentration: `C_i = \alpha - \beta t`.
* **[Step Change Response](./Step-Change/)** Classic analysis of the CSTR's transition between two steady states (accessible by setting $\beta = 0$).

### System Parameters
* **[Residence Time Studies](./Residence-Time/)** *Sensitivity analysis of reactor volume and flow rate on the damping of inlet fluctuations.*
## 🛠 Methodology
The simulations rely on solving the first-order linear differential equation derived from the species mass balance:

$$\frac{dC_A}{dt} + \left( \frac{1}{\tau} + k \right) C_A = \frac{C_i(t)}{\tau}$$

The analytical solution is implemented in Python, utilizing an integrating factor to account for the non-homogeneous time-dependent input. The model highlights the **Moving Steady State**, where the reactor's internal concentration attempts to track the inlet concentration but remains offset by a factor of $(k\tau + 1)^{-1}$ and a characteristic temporal lag.


<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$', '$$']],
      processEscapes: true
    }
  };
</script>

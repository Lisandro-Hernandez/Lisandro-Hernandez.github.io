# 📊 Quantum Free Energy from Non-Equilibrium Path Integral Methods

## 🧠 Overview
The graph illustrates the irreversible work distributions for forward and reverse processes across three protocol regimes: quasistatic, finite-rate, and instantaneous. For a harmonic system, these distributions are obtained analytically, although no general closed form exists.

## 📈 Visualization
<img src="variousSpeeds.png" alt="Graph" width="600">

## 🔍 What This Shows
- According to the [Crooks fluctuation theorem](https://en.wikipedia.org/wiki/Crooks_fluctuation_theorem), the free energy change of the process $\Delta F$ is given by the intersection of the forward and reverse distributions.
- The free energy change remains independent of the protocol speed.
- Since these are non-equilibrium adiabatic processes, the system is out of equilibrium at $t > 0$ in all cases.

## 💡 Key Insights
- The [Jarzynski equality](https://en.wikipedia.org/wiki/Jarzynski_equality) and [Crooks fluctuation theorem](https://en.wikipedia.org/wiki/Crooks_fluctuation_theorem) are generalized to quantum systems using imaginary-time path integrals.
- The path-integral representation is isomorphic to the configurational partition function of a classical field theory, which can be associated with a natural but fictitious Hamiltonian dynamics.
- We demonstrate that if this system is prepared in an equilibrium state and a control parameter in the fictitious Hamiltonian is changed over finite time, the Jarzynski and Crooks relations hold, with work defined as the energy change in the fictitious Hamiltonian.
- To address energy divergence in the classical field theory, we introduce two regularization methods that limit the degrees of freedom. The corresponding work distribution cumulants are shown to converge in canonical equilibrium as the degrees of freedom approach infinity.
- The applicability of these methods is demonstrated numerically for a quartic double-well potential and analytically for a harmonic system.

## 📌 Notes
Code available upon request.

# 📊 Quantum Free Energy from Non-Equilibrium Path Integral Methods

## 🧠 Overview
This graph shows the irreversible work distribution for the forward and reverse processes at different protocol speeds: quasistatic, finite process, and instantaneous. The distributions are determined analytically for a harmonic system.

## 📈 Visualization
<img src="variousSpeeds.png" alt="Graph" width="600">

## 🔍 What This Shows
- According to Crooks fluctuation theorem, the free energy change of the process $\Delta F$ is given by the intersection of the forward and reverse distributions.
- The free energy change is independent of process speed.
- Since these are non-equilibrium adiabatic processes, the system is out of equilibrium at $t > 0$ in all cases.

## 💡 Key Insights
- [Jarzynski equality](https://en.wikipedia.org/wiki/Jarzynski_equality) and [Crooks fluctuation theorem](https://en.wikipedia.org/wiki/Crooks_fluctuation_theorem) are generalized to quantum systems in the context of imaginary time path integrals.
- The path-integral representation is isomorphic to the configurational partition function of a classical field theory, to which a natural but fictitious Hamiltonian dynamics can be associated.
- We have shown that if this system is prepared in an equilibrium state, after which a control parameter in the fictitious Hamiltonian is changed in a finite time, then formally the Jarzynski
nonequilibrium work relation and the Crooks fluctuation relation hold, where work is defined as the change in the energy as given by the fictitious Hamiltonian.
- Since the energy diverges for the classical field theory in canonical equilibrium, two regularization methods are introduced which limit the number of degrees of freedom to be finite, and the corresponding distribution cumulants of the work are shown to converge in canonical equilibrium as the number of degrees of freedom go to infinity.
- The applicability of the methods is demonstrated numerically for a quartic double-well potential and analytically for a harmonic system.

## 📌 Notes
Code available upon request

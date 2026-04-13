# 📊 van der Waals Equation of State

## 🧠 Overview
A great deal of infomration can be extracted from equations of state. Here is shown the isotherms, liquid-vapor phase diagram, liquid-vapor densities and heats of vaporization as a function of temperature.

## 📈 Visualization

<img src="isotherms.png" alt="Graph" width="600">

<img src="phase_diagram.png" alt="Graph" width="600">

<img src="densities.png" alt="Graph" width="600">

<img src="argon_vs_exp.png" alt="Graph" width="600">

## 🔍 Description
- The **exact quantum time correlation function** (blue) is computed numerically via Hamiltonian diagonalization.  
- The **quasi-classical (q-class) result** (green) is obtained using the Wigner truncated approximation, which combines an initial Wigner distribution with classical dynamics.  
- The **CMD result** (red) corresponds to a centroid molecular dynamics–type approximation based on a novel phase-space mapping of quantum mechanical operators.  



## 💡 Key Insights
- The three methods agree at **t = 0**, where no dynamics occur and the quantum ensemble is represented exactly.
- As time evolves, both approximate methods (red and green) deviate from the exact quantum dynamics.
- The new phase-space mapping (red) provides improved accuracy over Wigner dynamics (green) due to the use of an effective force rather than a purely classical force.
- As in the Wigner approach, the accuracy of the new mapping can be systematically improved to arbitrary precision with increased computational effort.
- The new phase-space mapping is general and can describe the time evolution of any other operator.
- At high temperatures, both approximate approaches converge to the classical limit.
- In the harmonic limit, both methods reproduce the exact quantum dynamics.

## 📌 Notes
Code is available upon request.

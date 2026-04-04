# 📊 Quantum Time Correlation Function for a Quantum Oscillator

## 🧠 Overview
This project presents the position–position quantum time correlation function of a one-dimensional quantum oscillator at inverse temperature **β = 1.0**.

## 📈 Visualization
![Graph](results_quartic_beta_1.0.png)

## 🔍 Description
- The **exact quantum time correlation function** is computed numerically via Hamiltonian diagonalization.  
- The **quasi-classical (q-class) result** is obtained using the Wigner truncated approximation, which combines an initial Wigner distribution with classical dynamics.  
- The **CMD result** corresponds to a centroid molecular dynamics–type approximation based on a novel phase-space mapping of quantum mechanical operators.  

## 💡 Key Insights
- All methods agree at **time t = 0**, where no dynamics occur and the quantum ensemble is represented exactly.  
- As time evolves, both approximate methods deviate from the exact quantum dynamics.  
- The new phase-space mapping provides improved accuracy compared to Wigner dynamics, due to the use of an effective force rather than a purely classical force.  
- At high temperatures, both approximate approaches converge to the classical limit.  
- In the harmonic limit, both methods reproduce the exact quantum dynamics.  

## 📌 Notes
Code is available upon request.

# Dynamics of Liquid Neon via Ring Polymer Molecular Dynamics

## 🧠 Overview
This project evaluates the accuracy of Ring Polymer Molecular Dynamics (RPMD) in describing the quantum velocity autocorrelation functions of condensed phase systems[cite: 1]. By analyzing a Lennard-Jones fluid parameterized to represent liquid neon at 30 K, the study provides a quantitative assessment of how well RPMD captures dynamical structures and obeys exact quantum mechanical constraints[cite: 1].

## 🔬 Core Analyses
* **Velocity Autocorrelation Functions:** Calculation of the Kubo-transformed velocity autocorrelation function ($C_{vv}^K(t)$) and the thermally symmetrized correlation function ($G_{vv}(0)$)[cite: 1].
* **Constraint Convergence:** Numerical testing of integral constraints to determine the time range over which RPMD remains accurate[cite: 1].
* **Diffusion Coefficient Estimation:** Evaluation of how discrepancies in the correlation function's structure at longer times may lead to overestimations of self-diffusion[cite: 1].

---

## 📊 Available Results

### Algorithmic Performance
* **Path Integral Convergence:** *The thermaly symmetrized static average of the velocity $G_VV(0)$ and the zero-time value of the Kubo transformed velocity qunatum time correlation functions are shown to  be sufficiently converged numericaly at 20 "beads" ($P=20$) in path integral results for liquid neon at 30 K.*

<p align="center">
  <img src="./Liquid-Neon-P-Convergence.jpg" width="700"/>
</p>
  
* **[Integrand Time-Scaling](./integrand-analysis/)** *Quantitative definition of representative times for various integral constraints to pinpoint where RPMD dynamics diverge from exact behavior[cite: 1].*

### Liquid Neon Case Study
Select the analysis below to view the performance of RPMD at cryogenic temperatures:

* **[Quantum vs. Classical Limits](./neon-quantum-limit/)** *Comparison of $C_{vv}^K(0)$ and $G_{vv}(0)$ to quantitatively measure the significance of quantum effects in liquid neon[cite: 1].*
* **[Temporal Accuracy Mapping](./temporal-accuracy/)** *Analysis showing high accuracy for times up to $\beta\hbar$ (approx. 0.26 ps), with a subsequent decrease in reliability as the structure of the correlation function minimum is reached[cite: 1].*

---

## 🛠 Methodology
The simulations utilize **Ring Polymer Molecular Dynamics (RPMD)**, generating Hamiltonian trajectories from initial conditions drawn via Monte Carlo sampling from the Boltzmann distribution[cite: 1]. Trajectories are integrated using a **velocity-Verlet algorithm** with a 4.6-femtosecond time step[cite: 1]. The methodology relies on evaluating three distinct integral constraints to verify the correctness of the correlation function across different time scales relative to the quantum thermal time ($\beta\hbar$)[cite: 1].

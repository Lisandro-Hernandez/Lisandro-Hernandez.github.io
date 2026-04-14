# 📊 Assessment of Approximate Quantum Dynamics via Sum Rules

## 🧠 Overview
This project discusses a rigorous framework for evaluating the accuracy of approximate quantum dynamics using exact sum rules. These identities relate the time-integrals of Kubo-transformed correlation functions to specific thermally symmetrized static averages, providing a powerful diagnostic for approximate quantum dynamical methods.

## 📈 Visualization
<img src="results_quartic_beta_1.0.png" alt="Graph" width="500">


## 🔍 Description
- **Weighting Kernels:** The figure illustrates the various kernels associated with different time-integrals of the Kubo correlation function and their corresponding static averages.
- **Ensemble Averages:** The kernel associated with the standard (ordinary) ensemble average decays rapidly, limiting its ability to probe long-time dynamics.
- **Symmetrized Statics:** The primary kernel associated with thermally symmetrized static averages exhibits a characteristic "bell-shaped" structure, analytically defined by the $\text{sech}^2(x)$ distribution.
- **High-Order Integrals:** Additional higher-order kernels are zero at $t=0$ and exhibit polynomial growth at large times. This allows for a systematic weighting of long-time dynamics during integration, providing a sensitive test for the stability and long-term accuracy of approximate methods.

## 💡 Key Insights
- **Robust Benchmarking:** Sum rules provide a rigorous method for assessing the quality of approximate quantum time correlation functions in non-trivial, multi-dimensional condensed phase systems.
- **Dynamics vs. Statics:** The assessment relies on a direct comparison between dynamic time-integrals and numerically exact static averages. Because these averages contain no dynamical information, they can generally be computed with high accuracy, serving as an absolute reference.
- **Validation of Approximations:** This framework is essential for validating approximate Kubo correlation functions in systems where exact quantum-mechanical results are computationally inaccessible.
- **Global Constraints:** The sum rules represent global dynamical constraints. While they do not provide information regarding specific points in time, they ensure that the integrated dynamics remain physically consistent with the underlying equilibrium thermodynamics.

## 📌 Notes
Code and derivation details are available upon request.

# 📊 Solid state Mössbauer spectra and lattice dynamics

## 🧠 Overview
This graph shows the gamma-ray energy spectrum of Iron-57 in a 1D harmonic lattice at room temperature. The spectrum is fully determined analytically.

## 📈 Visualization

<img src="mossbauer_spectrum.png" alt="Graph" width="600">

- \(E_0 = 14.4 \, \text{keV}\) corresponds to the nuclear excitation energy of iron-57.  
- The line spacing is determined by the lattice vibrational frequency.  
- \(E_R\) represents the recoil kinetic energy of the nucleus.  
- For illustration, the graph depicts a “weakly bound” nucleus with \(E_R > \hbar \omega\); this parameter can be adjusted. In practice, \(E_R \approx \hbar \omega / 2\), leading to fewer spectral lines with larger spacing.


## 🔍 Lattice Dynamics

The spectrum above corresponds to the Fourier transform of the following periodic quantum time correlation function of the lattice dynamics. The correlation function period is 3.17 ps, while the coupling parameter The coupling parameter
$eta2 = (k_photon / (2 * alpha))**2 = 0.750$ and the average number of phonons excited at this temperature is 19.328.

<img src="mossbauer_correlation_function.png" alt="Graph" width="600">



## 💡 Key Insights
- The spectrum illustrates quantum momentum transfer effects in gamma decay.  
- For a free nucleus, the spectrum would be continuous, since the Hamiltonian commutes with the momentum operator.  
- The discrete structure arises from the non-commutativity of the Hamiltonian and momentum operator in a bound system.  
- The spectral maximum is shifted below \(E_0\) (the nominal nuclear excitation energy) due to recoil effects.  
- Relativistic corrections lead to hyperfine line splitting, and can be incorporated analytically.

## 📌 Notes
Code available upon request

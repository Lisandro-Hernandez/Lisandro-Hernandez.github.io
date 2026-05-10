# Electrochemical Transport with Overpotential-Driven Interfacial Kinetics

## 🧠 Overview
This extension of the nonlinear interfacial transport model incorporates a simplified representation of **electrochemical driving forces** at the electrode interface. In addition to Li⁺ diffusion in the electrolyte, the interfacial flux is now modulated by an **overpotential-like term**, introducing a basic coupling between local concentration and electrochemical driving force.

The result is a regime-dependent system in which kinetic effects become significant in reaction-limited conditions, while diffusion-limited behavior remains largely unchanged.

---

## 🔬 Key Physical Additions

### Electrochemical Interface
The interfacial flux is now influenced by an electrochemical driving force through an overpotential term:

\[
\eta = \phi_s - \phi_{eq}
\]

where:
- $\phi_s$ is the (assumed constant) electrode potential
- $\phi_{eq}$ is a simplified equilibrium potential dependent on Li⁺ concentration

A reduced thermodynamic form is used:
\[
\phi_{eq} = \ln(c)
\]

---

### Modified Interfacial Kinetics
The nonlinear interfacial flux is extended to include an electrochemical activation factor:

\[
J = k_0 c^n e^{\eta}
\]

where:
- $c$ is the local Li⁺ concentration at the electrode interface
- $n$ controls nonlinear reaction order
- $\eta$ represents the overpotential driving force

This introduces a simplified representation of electrochemical activation effects commonly associated with charge-transfer reactions.

---

## 📊 Regime Behavior

The system retains the same diffusion-reaction structure but exhibits distinct sensitivity depending on the Damköhler number:

* **Low Damköhler Number (Da ≪ 1): Reaction-Limited Regime**
  - Interfacial kinetics strongly influence concentration profiles
  - Overpotential modification significantly alters boundary behavior
  - Noticeable deviation from purely nonlinear diffusion model

* **Intermediate Regime (Da ~ 1–10): Mixed Control**
  - Diffusion and electrochemical kinetics compete
  - Smooth transition in boundary layer structure
  - Strong coupling between interface and bulk behavior

* **High Damköhler Number (Da ≫ 1): Diffusion-Limited Regime**
  - Transport dominates system behavior
  - Strong boundary layer forms near electrode
  - Kinetic modifications have limited impact on bulk profiles

<img src="./electrochemical_transport_with_Overpotential-Driven_Kinetics" width="700"/>

A key observation is that kinetic modifications primarily affect reaction-limited regimes, while diffusion-limited regimes remain largely unchanged due to transport control at the interface.

---

## 📈 Dimensionless Framework

The Damköhler number continues to govern system behavior:

\[
\mathrm{Da} = \frac{k_0 L}{D}
\]

where:
- $k_0$ is the effective interfacial reaction rate constant  
- $L$ is the system length  
- $D$ is the Li⁺ diffusion coefficient  

This dimensionless ratio quantifies the competition between interfacial reaction kinetics and bulk transport.

---

## 🛠 Numerical Methodology

The governing equation remains a one-dimensional diffusion equation for Li⁺ transport:

\[
\frac{\partial c}{\partial t} = D \frac{\partial^2 c}{\partial x^2}
\]

with a modified nonlinear boundary condition at the electrode interface:

\[
-D \frac{\partial c}{\partial x} = k_0 c^n e^{\eta}
\]

The system is solved using:
- Finite-difference spatial discretization  
- Explicit time stepping scheme  
- Positivity-preserving updates to ensure physically meaningful concentrations  

---

## 🔑 Key Insight

The introduction of an electrochemical overpotential term creates a clear separation of regimes:

- In **reaction-limited systems**, interfacial electrochemical driving forces strongly influence concentration profiles.
- In **diffusion-limited systems**, transport constraints dominate, making the system largely insensitive to kinetic details.

This behavior reflects a fundamental feature of electrochemical systems: **transport-limited regimes suppress sensitivity to interfacial kinetics**.

---

## 🚀 Next Extensions

This model forms the basis for more complete electrochemical descriptions, including:

- Full Butler–Volmer kinetics with symmetric charge-transfer barriers  
- Explicit electrolyte and solid-phase potential fields  
- Coupling to current conservation laws  
- Extension to porous electrode (DFN/P2D) frameworks  

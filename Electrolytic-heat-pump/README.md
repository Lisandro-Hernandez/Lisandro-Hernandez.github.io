# Hydrogen Energy Conversion: Efficiency vs Coefficient of Performance

## 🧠 Overview

This project analyzes how hydrogen, produced via water electrolysis, can be used in two fundamentally different ways:

1. To generate electrical work (fuel cell or battery operation)  
2. To generate heat through combustion  

The goal is to compare **thermodynamic efficiency** and **coefficient of performance (COP)** using Gibbs free energy and enthalpy as the central thermodynamic quantities.

The combustion reaction is:

![Hydrogen Combustion](https://latex.codecogs.com/svg.image?\ce{H2(g)%20+%20\frac{1}{2}O2(g)%20->%20H2O(l)})

At 25°C:

![Thermodynamic Data](https://latex.codecogs.com/svg.image?\Delta%20H_{rxn}%20=%20-285.830%20kJ/mol%20\quad%20,\quad%20\Delta%20G_{rxn}%20=%20-237.141%20kJ/mol)

Using:

![Gibbs relation](https://latex.codecogs.com/svg.image?\Delta%20G%20=%20\Delta%20H%20-%20T\Delta%20S)

we obtain:

![Entropy term](https://latex.codecogs.com/svg.image?T\Delta%20S%20=%20\Delta%20H%20-%20\Delta%20G%20=%20-48.689%20kJ/mol)

This shows that electrolysis requires both **electrical work and heat input**, while combustion releases both.

---

## 🔬 Core Analyses

## ⚡ Hydrogen used to produce electrical work (Efficiency)

The efficiency is defined as:

![Efficiency](https://latex.codecogs.com/svg.image?\eta%20=%20\frac{|w_{out}|}{w_{in}})

### Reversible case:

![Reversible efficiency](https://latex.codecogs.com/svg.image?\eta_{rev}%20=%201)

### Irreversible case:

![Irreversible efficiency](https://latex.codecogs.com/svg.image?\eta_{irr}%20=%20\frac{|\Delta%20G_{rxn}|%20-%20\delta}{|\Delta%20G_{rxn}|%20+%20\epsilon}%20<%201)

👉 Irreversibility always reduces efficiency below 1.

---

## 🔥 Hydrogen used to produce heat (COP)

The coefficient of performance is:

![COP](https://latex.codecogs.com/svg.image?\lambda%20=%20\frac{|\Delta%20H_{rxn}|}{w_{in}})

### Reversible case:

![COP reversible](https://latex.codecogs.com/svg.image?\lambda_{rev}%20=%20\frac{|\Delta%20H_{rxn}|}{|\Delta%20G_{rxn}|})

Numerically:

![COP value](https://latex.codecogs.com/svg.image?\lambda_{rev}%20\approx%201.21)

### Irreversible case:

![COP irreversible](https://latex.codecogs.com/svg.image?\lambda_{irr}%20=%20\frac{|\Delta%20H_{rxn}|}{|\Delta%20G_{rxn}|%20+%20\epsilon}%20<%20\lambda_{rev})

---

## 🔑 Physical Interpretation

Electrolysis heat exchange:

![Heat relation](https://latex.codecogs.com/svg.image?q%20=%20T\Delta%20S)

For this system:

![Numerical heat](https://latex.codecogs.com/svg.image?q%20=%20+48.689%20kJ/mol)

👉 Electrolysis requires both **electrical work and heat absorption** from the environment.

---

## 🔑 Key Insight

This system highlights a fundamental distinction:

- **Efficiency (η)** → conversion of chemical energy into useful **work**
- **COP (λ)** → conversion of chemical energy into useful **heat**

Even though both processes involve the same chemical reaction, their thermodynamic interpretation depends on the energy output form.

---

## 🚀 Extensions

- Temperature-dependent hydrogen energy cycles  
- Fuel cell efficiency under kinetic losses  
- Electrochemical overpotential modeling  
- Multi-stage hydrogen energy storage systems  
- Non-equilibrium thermodynamic cycle optimization

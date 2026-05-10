# Conductivity and Degree of Dissociation of Weak Acids

## 🧠 Overview

This project analyzes the relationship between **electrical conductivity**, **ionic dissociation**, and **chemical equilibrium** in weak electrolytes using acetic acid as a model system. By combining equilibrium thermodynamics with conductivity measurements, the model estimates both the **acid dissociation constant** and the **degree of ionization** as a function of concentration.

The analysis illustrates how macroscopic transport measurements can be used to infer microscopic equilibrium behavior in ionic systems.

---

## 🔬 Equilibrium Model

For a weak acid (such as acetic acid), the equilibrium constant \(K_a\) is related to the degree of dissociation \(\alpha\) through:

![Ka](https://latex.codecogs.com/svg.image?K_a=\frac{x^2}{c_0-x}=\frac{\alpha%20x}{1-\alpha}=\frac{\alpha^2%20c_0}{1-\alpha})

where:

- \(c_0\) is the initial acid concentration  
- \(x\) is the equilibrium concentration of the dissociated anion  
- \(\alpha = x/c_0\) is the degree of dissociation  

This expression can also be written as:

![alpha_relation](https://latex.codecogs.com/svg.image?\frac{1}{\alpha}=1+\frac{\alpha%20c_0}{K_a})

---

## ⚡ Conductivity Relation

The degree of ionization is related to the molar conductivity through:

![conductivity_alpha](https://latex.codecogs.com/svg.image?\alpha=\frac{\Lambda}{\Lambda_0})

where:

- \(\Lambda\) is the molar conductivity at concentration \(c_0\)
- \(\Lambda_0\) is the molar conductivity at infinite dilution

Substitution into the equilibrium expression gives:

![onsager_like](https://latex.codecogs.com/svg.image?\frac{1}{\Lambda}=\frac{1}{\Lambda_0}+\frac{1}{\Lambda_0^2K_a}\Lambda%20c_0)

This linearized form allows determination of:

- \(\Lambda_0\) from the intercept
- \(K_a\) from the slope

A key advantage of this formulation is that although \(\Lambda\) decreases with increasing concentration, the product \(\Lambda c_0\) remains relatively stable, reducing numerical sensitivity.

---

## 📊 Experimental Data

Experimental molar conductivity values for acetic acid are listed below.

| \(c_0\) | \(\Lambda\) |
|---|---|
| 0.0100 | 16.2 |
| 0.0050 | 22.8 |
| 0.0020 | 35.2 |
| 0.0010 | 48.7 |
| 0.0005 | 64.5 |
| 0.0002 | 104.0 |
| \(c_0 \rightarrow 0\) | \(\Lambda_0 = 388.6\) |

<img src="./Inverse_Molar_Conductivity.png" width="700"/>

---

## 📈 Linear Regression Analysis

Linear regression of the transformed conductivity relation yields:

### Infinite Dilution Conductivity

![lambda0_fit](https://latex.codecogs.com/svg.image?\Lambda_0=\frac{1}{\text{intercept}}=\frac{1}{0.00286}=349.7)

Reported experimental value:

![lambda0_exp](https://latex.codecogs.com/svg.image?\Lambda_0=388.6)

---

### Acid Dissociation Constant

![Ka_fit](https://latex.codecogs.com/svg.image?K_a=\frac{(\text{intercept})^2}{\text{slope}}=\frac{(0.00286)^2}{0.3626}=2.26\times10^{-5})

Reported experimental value:

![Ka_exp](https://latex.codecogs.com/svg.image?K_a=1.75\times10^{-5})

The agreement demonstrates that conductivity measurements provide a reliable indirect estimate of equilibrium dissociation properties.

---

## 📉 Degree of Dissociation

The degree of dissociation at each concentration is computed using:

![alpha_lambda](https://latex.codecogs.com/svg.image?\alpha=\frac{\Lambda}{\Lambda_0})

| \(c_0\) | \(\Lambda\) | \(\alpha\) |
|---|---|---|
| 0.0100 | 16.2 | 0.046 |
| 0.0050 | 22.8 | 0.065 |
| 0.0020 | 35.2 | 0.101 |
| 0.0010 | 48.7 | 0.139 |
| 0.0005 | 64.5 | 0.184 |
| 0.0002 | 104.0 | 0.297 |

As expected for weak electrolytes, the degree of dissociation increases strongly with dilution.

---

# 🔄 Alternative Analysis

Assuming the equilibrium constant \(K_a\) is known, the degree of dissociation can be computed directly from:

![alpha_exact](https://latex.codecogs.com/svg.image?\alpha=\frac{1}{2c_0}\left[\sqrt{K_a(K_a+4c_0)}-K_a\right])

---

## ⚡ Conductivity Scaling Relation

Using the conductivity definition:

![sigma_relation](https://latex.codecogs.com/svg.image?\frac{\sigma}{\alpha}=\frac{\Lambda%20c_0}{\Lambda/\Lambda_0}=\Lambda_0%20c_0)

the plot of:

![sigma_plot](https://latex.codecogs.com/svg.image?\sigma/\alpha)

versus concentration \(c_0\) yields a straight line with:

- zero intercept
- slope equal to \(\Lambda_0\)

This provides an alternative method for estimating infinite-dilution conductivity.

---

## 📌 Scaling Interpretation

The degree of dissociation may also be estimated through:

![alpha_scaling](https://latex.codecogs.com/svg.image?\alpha=\frac{\Lambda}{\Lambda_0}=\frac{\sigma}{c_0}\frac{\tilde{c}_0}{\tilde{\sigma}}=\frac{\sigma}{D\tilde{\sigma}})

where:

- \(D = c_0/\tilde{c}_0\) is a concentration scaling factor
- \(\tilde{c}_0\) corresponds to a near-infinite dilution reference concentration

This expression highlights that \(\alpha\) is not uniquely determined from the ratio \(\sigma/\tilde{\sigma}\) alone without concentration normalization.

---

## 🔑 Key Insight

This project demonstrates how equilibrium ionization behavior can be extracted from macroscopic conductivity measurements. The analysis connects:

- ionic transport
- equilibrium thermodynamics
- weak electrolyte dissociation
- conductivity scaling laws

within a unified electrochemical framework.

The results also illustrate how transport measurements can indirectly probe microscopic chemical equilibrium processes in ionic systems.

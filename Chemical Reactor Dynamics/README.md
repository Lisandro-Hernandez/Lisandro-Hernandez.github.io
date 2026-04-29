import numpy as np
import matplotlib.pyplot as plt

# Suggested Parameters
CA0 = 0.5    # Initial concentration in reactor (mol/L)
alpha = 2.0  # Initial inlet concentration (mol/L)
beta = 0.04  # Rate of change of inlet concentration (mol/L/min)
k = 0.1      # Reaction rate constant (1/min)
tau = 5.0    # Mean residence time (min)

# Time range: from 0 until the inlet concentration would theoretically reach zero
t_max = alpha / beta
t = np.linspace(0, t_max, 400)

# Calculate exponential factor (k + 1/tau)
gamma = k + 1/tau
exp_term = np.exp(-gamma * t)

# Implementing the User's derived expression:
# Term 1: Decay of initial concentration
term1 = CA0 * exp_term

# Term 2: Response to the constant part of the inlet (alpha)
term2 = (alpha / (k * tau + 1)) * (1 - exp_term)

# Term 3: Response to the linear ramp part of the inlet (-beta*t)
# Note: (kt + t/tau) is equal to gamma * t
term3 = - (beta * tau / (k * tau + 1)**2) * (gamma * t - 1 + exp_term)

CA_t = term1 + term2 + term3
Ci_t = alpha - beta * t

# Plotting the results
plt.figure(figsize=(10, 6))
plt.plot(t, Ci_t, 'r--', label=r'Inlet $C_i(t) = \alpha - \beta t$')
plt.plot(t, CA_t, 'b-', linewidth=2, label=r'Reactor $C_A(t)$')

plt.xlabel(r'Time $t$ (min)', fontsize=12)
plt.ylabel(r'Concentration (mol/L)', fontsize=12)
plt.title(r'CSTR Concentration Profile: Response to Linear Inlet Decay', fontsize=14)
plt.legend()
plt.grid(True, linestyle='--', alpha=0.7)
plt.tight_layout()

# Save the plot
plt.savefig('cstr_concentration_plot.png')

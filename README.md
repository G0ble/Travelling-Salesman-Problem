## Statistical Mechanics Inspiration for Simulated Annealing

Simulated Annealing (SA) is inspired by Statistical Mechanics.  In equilibrium at temperature **T**, the probability of a system being in state *i* with energy *E_i* is given by the **Boltzmann distribution**:

```math
P(E_i) = \frac{e^{-\beta E_i}}{Z}, \quad Z = \sum_i e^{-\beta E_i}, \quad \beta = \frac{1}{k_B T}
```

If the ground state energy is set to zero (*E = 0*), then as the temperature approaches absolute zero (*T → 0*, hence *β → ∞*), all probabilities vanish except for the ground state. This means the system will always end up in its minimum energy configuration.

This motivates the strategy of simulated annealing:
1. Simulate the system at some initial temperature using a Markov Chain process.  
2. Gradually lower the temperature while letting the system evolve.  
3. At very low temperature, the system is likely to settle near its ground state.  

The key insight is that this method is not limited to physical systems, as it can be applied to any optimization problem by treating the cost function as an “energy” to minimize.

<br>

https://github.com/user-attachments/assets/3983e23d-9648-4177-8c8d-0ccc283b4074

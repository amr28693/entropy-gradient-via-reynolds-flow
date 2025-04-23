# entropy-gradient-via-reynolds-flow
Demonstration of link between the entropy gradient and Reynolds number in some system.
This repository supports the preprint:
Entropy Production Mirrors Reynolds Flow Collapse: The Entropy Gradient as a Generalized Derivative of Reynolds Flow in Discrete Dynamical Collapse Systems  
arXiv:2504.XXXX (update when finalized)

---

## Objective

This simulation tests the hypothesis:
    dS/dt ≈ -d⟨R⟩/dt

The result shows that the negative time derivative of the average Reynolds number acts as a direct signal of entropy production and instability in flow-based systems.

---

## Files

- `entropy-gradient-via-reynolds-flow.ipynb` – simulation notebook
- Plots of ⟨R⟩ (Reynolds) and entropy gradient (–d⟨R⟩/dt)
- Interpretation section linking flow collapse and entropy production

---

## How to Run

1. Open the notebook in Jupyter.
2. Run all cells.
3. Modify the parameters in the `run_entropy_gradient_sim()` call to explore behavior.

Example:

```python
R, E = run_entropy_gradient_sim(
    collapse_threshold=0.28,
    viscosity=3.0,
    resistance_spread=0.5,
    steps=1000,
    seed=42
)

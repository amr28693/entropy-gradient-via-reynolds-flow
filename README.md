# Entropy Gradient via Reynolds Flow  
_A minimal simulation-based framework for collapse detection in discrete systems_

## Overview

This repository contains code supporting the preprint:  
"Entropy Production Mirrors Reynolds Flow Collapse"  
by Anderson M. Rodriguez (arXiv:2025.xxxxx)

We demonstrate that in discrete dynamical systems, the entropy gradient can be approximated by the negative time derivative of an average flow observable:
\[
\frac{dS}{dt} \sim -\frac{dR}{dt}
\]
Here, \( \langle R \rangle \) is a generalized Reynolds-like quantity computed from inverse edge weights on a dynamic network. This minimal formulation links collapse, instability, and entropy production across complex systems without requiring full thermodynamic or continuum models.

## Simulation Description

Nodes: Represent system components
Edges: Represent dynamic, weighted connections (inverse weights ∼ flow)
Collapse threshold: Optional condition to stop growth
Flow observable:  
  \[
  R_t = \frac{1}{|E|} \sum_{(i,j)} \frac{1}{w_{ij}}
  \]
- Entropy gradient:  
  \[
  \frac{dS}{dt} \approx -R_t - R_{t-1})
  \]

Plots are generated for:
- Flow decay over time
- Entropy gradient dynamics

## How to Run

Run the Jupyter Notebook `entropy-gradient-via-reynolds-flow.ipynb`.  
Each cell is annotated and can be adjusted to test collapse or stable regimes.

Key parameters:
- `collapse_threshold`: Float between 0–1
- `viscosity`: Higher values reduce flow (default: 2.0–4.0)
- `resistance_spread`: Variability in edge weights

## Example Regimes

| Regime | Parameters | Behavior |
|--------|------------|----------|
| Laminar Collapse | `collapse_threshold=0.05 to 0.1`| 
| Turbulent Collapse | `collapse_threshold=0.15 to 0.25`| Corresponds to typical Reynolds number values of 2000 to 4000|
| Collapse | `collapse_threshold=0.25`, `viscosity=5.0` | Flow decays sharply, entropy spikes |
| Subcritical | `collapse_threshold=0.37`, `viscosity=3.0` | Flow remains high, entropy gradient oscillates gently |

## Citation

If you use this framework, please cite:

@misc{rodriguez2025entropy, author = {Anderson M. Rodriguez}, title = {Entropy Production Mirrors Reynolds Flow Collapse: The Entropy Gradient as a Generalized Derivative of Reynolds Flow in Discrete Dynamical Collapse Systems}, year = 2025, eprint = {arXiv:25xx.xxxxx}, archivePrefix = {arXiv} }

## License
MIT License


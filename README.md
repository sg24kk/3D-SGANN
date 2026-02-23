# Sequence-Based Evolutionary and Neural Strategies for Reducing Zone Crossings in Toolpaths
---
## Overview

In multi-material 3D printing, frequent transitions between material zones reduce efficiency and print quality. This project introduces a **hybrid AI optimization framework** to minimize zone crossings in Hamiltonian toolpaths.

<img width="1920" height="1080" alt="Pipeline" src="https://github.com/user-attachments/assets/dfd1ced2-557b-449a-9754-79c937bcbebe" />

Our approach combines:

- **Simulated Annealing (SA)** for strong local optimization  
- **Genetic Algorithm (GA)** for global sequence evolution  
- **Neural Network (FusionNet)** to predict efficient operation sequences  

The toolpath is modeled as a **Hamiltonian path on a grid**, and optimized using local reconfiguration operations (flip & transpose).

## Key Idea

Instead of directly modifying paths, we:

1. Start with a **zigzag Hamiltonian path**
2. Apply **local reconfiguration operations**:
   - Flip (2×3 or 3×2 subgrid)
   - Transpose (3×3 subgrid)
3. Optimize using:
   - SA → generate strong solutions  
   - GA → evolve sequences of operations  
   - Neural model → learn and predict best sequences
  


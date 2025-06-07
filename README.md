# HgMAP

# Sensor-Field Reconstruction & 1D Diffusion PINN Tutorials

## Overview

This repository contains two tutorial notebooks:

1. **Sensor-Field Reconstruction with Jacobian-Weighted Adaptive Sampling**  
   Learn how to train a Conv–LSTM–Attention autoencoder to reconstruct a smooth 2D field from sparse sensor readings, then adaptively place sensors using Hessian-based importance sampling.

2. **1D Solute Diffusion PINN Tutorial**  
   Implement a physics-informed neural network (PINN) to solve the 1D diffusion equation under mixed Dirichlet/Neumann conditions, compare against finite-difference and analytical error-function solutions.

Each notebook is self-contained and walks through problem setup, math derivations, code implementation, training/evaluation, and rich visualizations.

## Notebooks

| Name                                                      | Purpose                                                                                 |
| --------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `SensorPlacement.ipynb`                         | Autoencoder design, uniform vs adaptive sampling, MSE/SSIM/EMD metrics, experiment loop |
| `1D_Diffusion.ipynb`                           | PINN architecture, PDE residual derivation, LHS sampling, training, FDM & analytical   |

## Dependencies

Both notebooks require a Python 3.8+ environment with these core packages:

```bash
pip install numpy scipy scikit-image pandas matplotlib torch pyDOE
````

You may also run each notebook in Google Colab without local install.

## Usage

1. Open the desired notebook in Jupyter or Colab.
2. Run each cell in order.
3. For the sensor-field notebook, adjust budgets `k` or model hyperparameters to explore performance trade-offs.
4. For the PINN notebook, tune diffusion coefficient `D`, network widths, or sampling sizes `N_f, N_D, N_N`.

Both notebooks include:

* Math derivations in Markdown
* Fully runnable code cells
* Visualizations of solutions, error maps, and performance metrics

## Project Structure

```
/
├── README.md
├── SensorPlacement.ipynb
├── 1D_Diffusion.ipynb
```

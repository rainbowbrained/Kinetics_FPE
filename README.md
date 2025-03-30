# Entangled Fokker-Planck Equations for Non-Markovian Stochastic Processes

This repository contains code and derivations related to the **Derivation of Entangled Fokker–Planck-like Equations for Non-Markovian Stochastic Processes**. The project implements a functional-calculus approach (inspired by R. Fox, Phys. Rev. A 1986) to derive approximate Fokker–Planck equations for systems driven by colored (exponentially-correlated) noise, and includes numerical simulations to compute the mean first-passage time (MFPT) in a bistable potential.


[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/rainbowbrained/Kinetics_FPE )
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Documentation](https://img.shields.io/badge/docs-up--to--date-blueviolet)](./docs)

---

## Overview

This repository contains the derivation and numerical implementation of entangled Fokker-Planck-like equations for non-Markovian stochastic processes. The project involves both analytical derivations using advanced functional calculus techniques and numerical studies of mean-first passage time (MFPT) in a bistable potential driven by colored, exponentially-correlated noise.

The derivations include:

1. **Review of the non-Markovian FP equations:** A comprehensive survey of existing non-Markovian Fokker-Planck formulations.
2. **Method of functional calculus for the derivation of non-Markovian FP-equation (NMFPE):** Detailed steps using functional calculus to derive the governing equations.
3. **Derivation of the NVFPE for short correlation time of the colored noise:** Analytical reduction under the assumption of short noise correlation time.
4. **Derivation on entangled NVFPE for P₂, P₃, etc.:** Extension of the derivation to higher order probability density functions.
5. **Numerical computation of the MFPT:** Simulations in a bistable potential compared with theoretical predictions from R. Fox (Phys. Rev. A, 1986).

---

## Table of Contents

- [Overview](#overview)
- [Table of Contents](#table-of-contents)
- [Background](#background)
- [Features](#features)
- [Methodology](#methodology)
  - [Review of Non-Markovian FP Equations](#review-of-non-markovian-fp-equations)
  - [Functional Calculus Derivation](#functional-calculus-derivation)
  - [NVFPE Derivation for Short Correlation Time](#nvfpe-derivation-for-short-correlation-time)
  - [Entangled NVFPE for Higher Orders](#entangled-nvfpe-for-higher-orders)
  - [Numerical Computation of MFPT](#numerical-computation-of-mfpt)
- [Results & Comparison](#results--comparison)
- [References](#references)

---

## Background

- **Non-Markovian Dynamics**: In systems where the noise exhibits memory (colored noise), the evolution of the probability density cannot be fully captured by the standard Markovian Fokker–Planck equation.
- **Functional Calculus Approach**: The derivation uses functional derivatives and path integrals to systematically obtain an approximate FPE, which includes corrections in the noise correlation time tau.
- **Entangled Equations**: For a full description of memory effects, the project discusses a hierarchy of coupled (entangled) equations for multi-time probability densities P_1, P_2, P_3, ...
- **Numerical Simulations**: The code simulates the overdamped Langevin equation in a bistable potential 
  
      U(x) = -a/2 x^2 + b/4 x^4,
  
  with colored, exponentially-correlated noise, and computes the first-passage time density, survival probability, and MFPT. These results are then compared with the theoretical predictions from Fox’s work.

The behavior of non-Markovian stochastic systems is notoriously complex due to memory effects. In this project, we employ **functional calculus** to derive generalized Fokker-Planck equations that capture these non-local effects. Special attention is given to:
- **Colored noise:** Specifically, exponentially correlated noise.
- **Bistable potentials:** Providing a rich framework for studying transitions and MFPT.

---

## Features

- **Analytical Derivations**: Derivation of non-Markovian Fokker–Planck equations using the functional-calculus approach.
- **Simulation of Colored Noise SDEs**: Overdamped Langevin dynamics with colored (Ornstein–Uhlenbeck) noise.
- **MFPT Computation**: Calculation of first-passage time density, survival probability, and MFPT in a bistable potential.
- **Theoretical Comparison**: Comparison of numerical results with theoretical predictions based on Fox’s 1986 approximation.

---

## Methodology
### Review of Non-Markovian FP Equations
An in-depth review of the existing formulations provides the groundwork for the derivations presented. Key references include seminal papers on non-Markovian dynamics.
### Functional Calculus Derivation
We utilize functional calculus to systematically derive the non-Markovian FP-equation (NMFPE). The derivation details the manipulation of functional derivatives and path integrals.
### NVFPE Derivation for Short Correlation Time
By assuming a short correlation time for the colored noise, the NVFPE is derived to simplify the analysis while retaining essential memory effects.
### Entangled NVFPE for Higher Orders
Extensions to P₂, P₃, and beyond are derived to capture entangled states within the system, offering a deeper understanding of higher order stochastic interactions.
### Numerical Computation of MFPT
The numerical implementation simulates the MFPT in a bistable potential. Results are compared with theoretical predictions from R. Fox's 1986 study in Phys. Rev. A.
simulate_mfpt.py: Main simulation code that:
1. Defines the bistable potential and its derivative.
2.  Implements the colored noise SDE via an auxiliary Ornstein–Uhlenbeck process.
3.  Collects first-passage times and computes the MFPT.
4.  Compares the numerical results with the theoretical prediction.
5.  Generates plots for the FPT distribution.

---
## Results

---

## References
- R. F. Fox, "Functional‑calculus approach to stochastic differential equations", Phys. Rev. A, 33, 467 (1986).
- K. Furutsu, "On the Statistical Theory of Electromagnetic Waves in a Fluctuating Medium", J. Res. Natl. Bur. Stand. Sect. D, 67, 303 (1963).
- E. A. Novikov, "Functionals and the Random‑Force Method in Turbulence Theory", Sov. Phys. JETP, 20, 1290 (1964).
- Reviews on colored noise and the Unified Colored-Noise Approximation (UCNA) in literature such as works by P. Hänggi et al.
- C. W. Gardiner, Handbook of Stochastic Methods, Springer (1983).
- L. Arnold, Stochastic Differential Equations: Theory and Applications, Wiley-Interscience (1974).


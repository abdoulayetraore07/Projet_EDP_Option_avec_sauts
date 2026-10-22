# Option Pricing under the Merton Jump-Diffusion Model (PDE approach)

Numerical pricing of European options under the Merton jump-diffusion model, by solving the associated partial integro-differential equation (PIDE) with finite difference schemes. Academic project, ENSTA Paris / ENSAE Paris.

## Model

The asset price follows the Merton dynamics
dS_t = S_t ( mu dt + sigma dB_t + (eta - 1) dq_t ),
where dq_t is a Poisson process with intensity lambda and eta > 0 is the relative jump size. The option price V(t, s) solves a PIDE with terminal condition V(T, s) = phi(s), where the jump term appears as a linear integral operator on V.

## Content (questions treated)

- Q1: Boundary behavior near S = 0
- Q2: Change of variable s = K e^x
- Q3: Discretization of the integral (jump) term
- Q4: Explicit schemes (Upwind and centered / DFC)
- Q5: Comparison with the analytical Merton formula and the no-jump (Black-Scholes) model
- Q6: Implicit scheme
- Additional part: pricing of a floating-strike Asian option

## Repository structure

- Projet_EDP_Merton.ipynb : main notebook (theory, schemes, results)
- projet_edp_merton.py : script export of the main notebook
- Pricing_Asiatique_Strike_Flottant.ipynb : floating-strike Asian option pricing
- Rapport_EDP.pdf : project report

## Methods

- Finite difference schemes for the PIDE: explicit (Upwind and centered) and implicit
- Discretization of the jump integral term
- Log-grid and change of variables
- Validation against the closed-form Merton series and the Black-Scholes price

## Authors

Abdoulaye TRAORE, Franck KOUASSI, Mohamed Naceur, Hussein Rammal
ENSTA Paris / ENSAE Paris

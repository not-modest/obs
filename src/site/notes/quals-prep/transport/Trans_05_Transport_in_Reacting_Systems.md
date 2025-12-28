---
{"dg-publish":true,"permalink":"/quals-prep/transport/trans-05-transport-in-reacting-systems/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

## Key definitions

- **External mass transfer limitation**  
  Rate controlled by transport of reactant from bulk fluid to external surface (film resistance).

- **Internal diffusion limitation**  
  Rate controlled by diffusion inside porous catalyst particles.

- **Effectiveness factor, $\eta$**  
  Ratio of actual reaction rate in a particle to the rate if the entire particle were at external surface conditions.

- **Hot spot**  
  Local temperature maximum in a reactor (often a fixed bed) caused by exothermic reaction and limited heat removal.

---

## Core formulas

### 1. External mass transfer to a reacting surface

Flux:
$$
N_A = k_c (C_{A,b} - C_{A,s})
$$

Surface reaction rate (per external area):
$$
-r_{A,\text{surf}} = k_s C_{A,s}^n
$$

At steady state, for a first‑order reaction, equate flux and reaction:
$$
k_c (C_{A,b} - C_{A,s}) = k_s C_{A,s}
$$

Solve for $C_{A,s}$ and define an overall rate; external limitation becomes strong when $k_c \ll k_s$.

### 2. Internal diffusion and effectiveness factor (summary)

Intrinsic first‑order rate in pellet:
$$
-r_A = k C_A
$$

Effective observed rate per particle volume:
$$
-r_{A,\text{obs}} = \eta\, k C_{A,s}
$$

For a spherical pellet:
- Thiele modulus:
  $$
  \Phi = R_p \sqrt{\frac{k}{D_{\text{eff}}}}
  $$
- Effectiveness factor (exact form):
  $$
  \eta = \frac{3}{\Phi} \left(\frac{1}{\tanh \Phi} - \frac{1}{\Phi}\right)
  $$

### 3. Simple energy balance for a hot spot (concept)

In a differential PFR slice:
$$
F C_p \frac{dT}{dV} + (-\Delta H_r) r_A + \frac{dQ}{dV} = 0
$$
with $\dfrac{dQ}{dV} = \dfrac{U A}{V}(T_c - T)$.

Competition between $(-\Delta H_r) r_A$ and heat removal term shapes $T(z)$ profile and hot spots.

---

## Interesting concepts

- **Regime identification**  
  Compare intrinsic rate to mass‑transfer and heat‑transfer capacities (e.g. via Damköhler and Biot numbers) to see whether kinetics, mass transfer, or heat transfer limits.

- **Pellet size and transport**  
  Smaller pellets reduce internal diffusion limitations (smaller $\Phi$), but can increase pressure drop and external transfer importance.

- **Heat and mass transfer coupling**  
  In exothermic reactions, limited heat removal can raise temperature, increasing $k(T)$ and potentially moving system into transport‑limited regimes.

---

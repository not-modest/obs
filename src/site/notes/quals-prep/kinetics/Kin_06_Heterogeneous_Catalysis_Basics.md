---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/kin-06-heterogeneous-catalysis-basics/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

## Key definitions

- **Heterogeneous catalyst**  
  Catalyst in a different phase from reactants (typically solid catalyst, gas or liquid reactants); reaction occurs on the surface.

- **External mass transfer resistance**  
  Resistance to transport of reactant between bulk fluid and external catalyst surface (through the fluid film around the particle).

- **Internal diffusion limitation**  
  Resistance to diffusion of reactant inside catalyst pores; reactant concentration decreases from external surface into the interior.

- **Thiele modulus, $\Phi$ (first‑order, spherical pellet)**  
  Measures relative rates of reaction and diffusion inside a porous catalyst:
  $$
  \Phi = R_p \sqrt{\frac{k}{D_{\text{eff}}}}
  $$
  where $R_p$ is pellet radius, $k$ intrinsic first‑order rate constant, and $D_{\text{eff}}$ effective diffusivity.

- **Effectiveness factor, $\eta$**  
  Ratio of actual reaction rate in the pellet to the rate if the entire pellet were at the external surface concentration:
  $$
  \eta = \frac{\text{actual rate in pellet}}{\text{rate at surface conditions everywhere}}
  $$

- **Langmuir–Hinshelwood (L–H) mechanism**  
  Surface reaction mechanism in which reactants adsorb on surface sites, react on the surface, and products desorb; rate expressions involve adsorption terms and surface coverage.

---

## Core formulas (simple forms)

### 1. External mass transfer (overall rate to surface)

For reactant $A$ at bulk concentration $C_{A,b}$ and surface concentration $C_{A,s}$:
$$
N_A = k_c (C_{A,b} - C_{A,s})
$$
where $k_c$ is the external mass transfer coefficient; the rate per external surface area is often $r_{A,\text{ext}} = N_A$.

### 2. Internal diffusion and effectiveness factor (first‑order, sphere)

Intrinsic rate inside pellet:
$$
-r_A = k C_A
$$

Effectiveness factor (exact analytical form for a sphere):
$$
\eta = \frac{3}{\Phi} \left( \frac{1}{\tanh \Phi} - \frac{1}{\Phi} \right)
$$

Limiting behavior:

- Small $\Phi$ (weak diffusion limitation): $\eta \approx 1$ (reaction‑controlled).  
- Large $\Phi$ (strong diffusion limitation): $\eta \approx \dfrac{3}{\Phi}$ (diffusion‑controlled).

Overall observable rate per external surface area:
$$
-r_{A,\text{obs}} = \eta\, k\, C_{A,s}
$$

### 3. Simple Langmuir–Hinshelwood rate expression (one reactant, non‑dissociative)

Assume:

- One reactant A adsorbs on uniform sites.  
- Surface reaction is rate‑limiting.  
- Adsorption follows Langmuir isotherm.  

Then:
$$
-r_A = \frac{k_r K_A C_A}{1 + K_A C_A}
$$
where $k_r$ is surface reaction rate constant and $K_A$ adsorption equilibrium constant.

For two reactants A and B (qualitative memory form):
$$
-r_A \propto \frac{K_A C_A\, K_B C_B}{\left(1 + K_A C_A + K_B C_B\right)^2}
$$
(up to a constant factor).

---

## Interesting concepts

- **Identifying rate control**  
  - $\eta \approx 1$ and strong dependence of rate on $k$: reaction‑controlled.  
  - $\eta \ll 1$ and weak dependence of rate on $k$: diffusion‑controlled inside the pellet.  

- **External vs internal limitations**  
  External limitations change $C_{A,s}$ relative to $C_{A,b}$; internal limitations change concentration inside the pellet relative to $C_{A,s}$. Both can coexist.

- **Apparent reaction order**  
  L–H expressions often show non‑integer or changing apparent orders (e.g., first‑order at low coverage, zero‑order at high coverage), which is a hallmark of surface kinetics.

- **Using Thiele modulus**  
  Increasing $R_p$ or $k$ (at fixed $D_{\text{eff}}$) increases $\Phi$ and reduces $\eta$; decreasing pellet size or increasing diffusivity moves the system toward intrinsic kinetics.

---


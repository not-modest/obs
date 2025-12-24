---
{"dg-publish":true,"permalink":"/quals-prep/transport/trans-06-links-to-thermo-and-kinetics/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Transport driving forces**  
  Gradients in temperature, concentration, or velocity (equivalently chemical potential) that cause heat, mass, and momentum transfer.

- **Transport‑controlled regime**  
  Overall rate limited by heat or mass transfer rather than intrinsic kinetics.

- **Biot number (mass or heat)**  
  Ratio of internal to external resistance, e.g.
  $$
  \text{Bi}_m = \frac{k_c R_p}{D_{\text{eff}}},\quad
  \text{Bi}_h = \frac{h L_c}{k}
  $$

- **Damköhler number, $\text{Da}$**  
  Ratio of reaction rate to transport rate (or characteristic timescale ratio).

---

## Core links

### 1. Transport vs thermodynamics

- Thermodynamics supplies equilibrium conditions (e.g. saturation, phase equilibrium, equilibrium composition).  
- Transport determines how fast systems approach these equilibria; finite fluxes imply gradients and departures from equilibrium.

Examples:

- VLE: interfacial equilibrium but bulk phases may be far from equilibrium due to finite mass transfer.  
- Heat exchangers: finite $\Delta T$ needed to drive $q$, generating entropy.

### 2. Transport vs kinetics

- Intrinsic rate law:
  $$
  -r_A^{\text{int}} = k(T) f(C_i)
  $$
- Observed rate including transport:
  $$
  -r_A^{\text{obs}} = \eta_{\text{diff}}\, \eta_{\text{heat}}\, r_A^{\text{int}}
  $$
  where $\eta$ factors encode mass‑ and heat‑transfer limitations.

- $\text{Da} \ll 1$: kinetics slow, transport fast (reaction‑controlled).  
- $\text{Da} \gg 1$: kinetics fast, transport slow (transport‑controlled).

---

## Interesting concepts

- **Local equilibrium with global non‑equilibrium**  
  Interfaces may satisfy phase equilibrium while bulk phases show gradients and non‑uniform composition/temperature.

- **Design and scale‑up**  
  Large reactors or equipment often move from kinetic control (lab scale) to transport control (industrial scale), changing optimal conditions and observed reaction orders.

- **Entropy generation as a link**  
  Irreversibilities from finite heat and mass transfer generate entropy, tying transport limitations back to the second law.

---



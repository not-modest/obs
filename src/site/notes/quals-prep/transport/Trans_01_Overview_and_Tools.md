---
{"dg-publish":true,"permalink":"/quals-prep/transport/trans-01-overview-and-tools/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

## Key definitions

- ### Conservation laws  
  - Mass: what goes in – what comes out + generation = accumulation.  
  - Momentum: sum of forces = rate of change of momentum.  
  - Energy: first law applied to a control volume (includes internal, kinetic, potential).

- ### Shell balance  
  Differential balance over a thin “shell” of fluid/solid to derive governing equations (e.g. velocity profile, temperature profile, concentration profile). Some math behind shell balances can be found [[quals-prep/transport/z_Shell_balance\|here!]]

- ### **Transport coefficients**  
  - Momentum: viscosity $\mu$.  
  - Heat: thermal conductivity $k$.  
  - Mass: diffusivity $D$.

- **Dimensionless groups**  
  - Reynolds: $\displaystyle \text{Re} = \frac{\rho v L}{\mu}$  
  - Prandtl: $\displaystyle \text{Pr} = \frac{c_p \mu}{k}$  
  - Schmidt: $\displaystyle \text{Sc} = \frac{\mu}{\rho D}$  
  - Nusselt: $\displaystyle \text{Nu} = \frac{h L}{k}$  
  - Sherwood: $\displaystyle \text{Sh} = \frac{k_c L}{D}$  

---

## Core ideas

- **Analogy of transport**  
  Flux is proportional to gradient of driving force:
  - Momentum: shear stress $\tau \propto \dfrac{du}{dy}$.  
  - Heat: $q \propto -\dfrac{dT}{dx}$.  
  - Mass: $N_A \propto -\dfrac{dC_A}{dx}$.

- **Control volume vs shell**  
  Control volumes give integral balances; shell balances give differential equations suitable for simple geometries.

- **Correlations and similarity**  
  Dimensionless groups allow reuse of empirical correlations for different fluids and scales.

---


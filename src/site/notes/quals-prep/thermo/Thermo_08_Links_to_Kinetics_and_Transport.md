---
{"dg-publish":true,"permalink":"/quals-prep/thermo/thermo-08-links-to-kinetics-and-transport/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Thermodynamic driving force**  
  Often measured by $\Delta G$ or departure from equilibrium; determines how strongly a process “wants” to proceed.

- **Equilibrium conversion**  
  Maximum conversion allowed by thermodynamics for given $T$, $P$, and feed; actual conversion may be lower due to kinetics/transport.

- **Transport limitation**  
  Situation where heat or mass transfer rates restrict approach to the thermodynamically favored state.

---

## Core links to kinetics

### 1. Equilibrium vs kinetic control

- Equilibrium constant $K$ sets the final composition if the system has enough time and no transport limitations.  
- Kinetics (rate laws, $k(T)$, activation energies) determine how fast equilibrium is approached or whether metastable states persist.

### 2. Energy balances in reactors

- Heat of reaction $\Delta H_r$ from thermodynamics appears in reactor energy balances:
  $$
  F C_p (T_0 - T) + (-\Delta H_r) r_A V + Q = 0
  $$
- Changing $T$ changes $k(T)$ and hence reaction rate; thermodynamics and kinetics interact through this coupling.

---

## Core links to transport

### 1. Driving forces and fluxes

- Thermodynamic gradients (temperature, chemical potential, concentration) drive transport:
  - Heat flux $\propto -\nabla T$.  
  - Mass flux $\propto -\nabla$ (chemical potential or concentration).  

- When transport is slow, systems remain far from thermodynamic equilibrium locally.

### 2. Dimensionless groups

- Damköhler numbers compare reaction to transport timescales.  
- Biot numbers compare internal and external transport resistances.  
These numbers indicate whether kinetics or transport dominates the approach to thermodynamic equilibrium.

---

## Interesting concepts

- **Local vs global equilibrium**  
  A reacting system may be in local equilibrium with respect to some variables (e.g. phase equilibrium) while being far from equilibrium for overall reaction progress.

- **Design implications**  
  In reactor and separation design, thermodynamics defines what is possible; kinetics and transport determine what is practical within given size, time, and energy constraints.

---


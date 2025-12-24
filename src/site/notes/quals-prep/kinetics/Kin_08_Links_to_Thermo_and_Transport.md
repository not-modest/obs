---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/kin-08-links-to-thermo-and-transport/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Thermodynamic control**  
  Reaction outcome governed by equilibrium; product distribution determined by minimum Gibbs free energy, not by how fast products form.

- **Kinetic control**  
  Reaction outcome governed by rates and activation barriers; product distribution reflects fastest pathway on the experiment timescale.

- **Damköhler number, $\text{Da}$**  
  Dimensionless ratio of reaction rate to transport rate (or reaction time to transport time); used to classify reaction‑ vs transport‑controlled regimes.

- **Biot number for mass/heat transfer, $\text{Bi}$**  
  Ratio of internal to external transport resistance (e.g. inside pellet vs film).

---

## Core links to thermodynamics

### 1. Equilibrium vs rate

- Thermodynamics sets the **maximum conversion** or equilibrium composition; kinetics determines how fast a system approaches that equilibrium, or if it effectively never reaches it.  
- For reversible reactions, the equilibrium constant $K$ comes from thermodynamics; the individual rate constants $k_f$ and $k_r$ satisfy $K = k_f/k_r$.

### 2. Driving force

- Thermodynamic driving force (e.g. $\Delta G$, $\Delta \mu$, departure from equilibrium composition) interacts with kinetics: larger driving force usually increases the rate until transport or surface saturation becomes limiting.  
- Near equilibrium, forward and reverse rates almost cancel; net rate becomes small even if individual rates remain large.

### 3. Energy and nonisothermal behavior

- Heat of reaction $\Delta H_r$ (thermodynamic quantity) couples to kinetics via the energy balance; changing temperature alters $k(T)$ and can cause runaway or extinction.  
- In exothermic systems, higher $T$ increases rates (kinetics) but may also shift equilibrium to lower conversion (thermodynamics).

---

## Core links to transport

### 1. Reaction vs transport timescales

Typical Damköhler number form:
$$
\text{Da} = \frac{\text{reaction rate scale}}{\text{transport rate scale}}
\sim \frac{\text{characteristic transport time}}{\text{characteristic reaction time}}
$$

- $\text{Da} \ll 1$: reaction‑controlled (transport is fast).  
- $\text{Da} \gg 1$: transport‑controlled (reaction is fast relative to transport).

### 2. Internal vs external transport (Biot number)

For a porous pellet or heat‑transfer problem, a Biot number compares internal to external resistance, e.g.
$$
\text{Bi}_m = \frac{k_c R_p}{D_{\text{eff}}}
$$

- Small Bi: external film resistance dominates.  
- Large Bi: internal diffusion dominates.

Kinetics uses the **observed** rate, which already includes these transport limitations.

### 3. Effective rate constants

When transport is limiting, the observed rate can still be written in a form that looks kinetic, but with an **effective** rate constant $k_{\text{eff}}$ that depends on transport coefficients (e.g. $k_c$, $D_{\text{eff}}$, $U$).  
Design and scale‑up must distinguish intrinsic $k$ from $k_{\text{eff}}$.

---

## Interesting concepts

- **Kinetic vs thermodynamic product**  
  Conditions with short residence times or low temperatures often favor the kinetic product (lower barrier, less stable), while long times or higher temperatures favor the thermodynamic product (more stable).  

- **Hidden transport limitations**  
  Observed orders and activation energies can change when external or internal transport becomes limiting, leading to misinterpretation of intrinsic kinetics if transport is ignored.  

- **Dimensionless maps**  
  Plots in terms of Damköhler, Biot, and other groups organize regimes: purely kinetic, mixed kinetic–transport, or fully transport‑controlled.

---

 

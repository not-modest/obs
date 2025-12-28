---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/z-reactive-extraction/","tags":["2021_Jan"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

# 1. Core Idea and Equilibrium

- Two liquid phases: typically aqueous (feed) and organic (extractant in diluent).
- Solute A (e.g. acid) reacts with extractant S in organic phase or at interface to form a complex:
  $$
  \text{A}_{(aq)} + \nu\,\text{S}_{(org)} \rightleftharpoons \text{A}\cdot\text{S}_\nu{}_{(org)}
  $$
- Apparent **distribution coefficient**:
  $$
  D = \frac{C_{A,org}}{C_{A,aq}}
  $$
  can be orders of magnitude larger than for physical extraction because A is bound in a complex.

Equilibrium expression (example, 1:1 complex):
$$
K_{\text{ex}} = \frac{C_{A\cdot S,org}}{C_{A,aq}\,C_{S,org}}
$$

Overall extraction efficiency depends on:
- Complexation equilibrium (extraction constant, stoichiometry).
- Acid–base equilibrium (speciation of A in water).
- Phase ratio (organic/aqueous volume).
- Diluent effects (polarity, H-bonding, solvating power).

---

# 2. Reactor / Contacting Device Types

Reactive extraction is implemented in **reactors + contactors** where reaction and phase transfer occur together:

- **Batch mixer–settlers**:  
  - Strong mixing for reaction + mass transfer, then quiescent settling.  
- **Continuous stirred tanks (CSTR extractors)**:  
  - Good for kinetic control, multiple stages in series for higher separation.
- **Packed columns / pulsed columns**:  
  - Countercurrent flow, high interfacial area, suitable for near-equilibrium operation.
- **Rotating disc contactors / RDC**:  
  - Enhanced mass transfer and controllable dispersion.
- **Membrane-supported reactive extraction**:  
  - Phases separated by a membrane; reaction at/inside membrane pores.

Choice depends on:
- Reaction kinetics vs mass transfer rates.
- Phase ratio and density/viscosity.
- Fouling / emulsion issues.
- Required approach to equilibrium.

---

# 3. Equilibrium Limitations

Even with fast kinetics, **equilibrium sets an upper bound** on what you can extract in one stage.

For a given system at equilibrium:

- Distribution coefficient $D(C_A, C_S, T)$ and phase ratio $\phi = V_{org}/V_{aq}$ determine **single-stage extraction**:
  $$
  E = \frac{\text{moles of A transferred to organic}}{\text{moles of A fed}}
  =
  \frac{D \phi}{1 + D \phi}
  $$

Key limitations:

- **Finite extractant loading**:  
  - Complex formation saturates at high A; loading ratio:
    $$
    Z = \frac{C_{A,org}}{C_{S,org,0}}
    $$
  - As $Z \to$ stoichiometric limit, marginal gain in extraction drops.
- **Aqueous speciation** (for acids/bases/metals):  
  - Only certain species (e.g., undissociated acid HA or anionic form A⁻) are extractable.  
  - pH or complexing agents strongly affect equilibrium.

Equilibrium alone can make complete extraction in one stage impossible; **multi-stage countercurrent** or **recycling** is then needed.

---

# 4. Rate and Mass Transfer Considerations

In many systems, overall rate is controlled by:

1. Diffusion of solute from bulk aqueous to interface.  
2. Interfacial reaction/complexation with extractant.  
3. Diffusion of complex into organic phase.

Frequently modeled with **two-film theory**:

- Flux of A:
  $$
  N_A = k_L (C_{A,bulk} - C_{A,i})
  $$
  with reaction at or very near interface:
  $$
  \text{A}_{(aq)} + \nu S_{(org)} \rightleftharpoons \text{complex}_{(org)}
  $$

For “fast reaction” cases, **Hatta number** and **enhancement factors** from gas–liquid theory have analogs in reactive liquid–liquid systems.

Design needs to check:

- Are we **equilibrium-limited** (mass transfer fast, reaction fast)?  
- Or **kinetically limited** (reaction or diffusion slow)?  

This guides whether to prioritize higher interfacial area / mixing vs more residence time or higher extractant concentration.

---

# 5. Reactor/Process Design Considerations

## 5.1 Solvent / Extractant / Diluent selection

- High distribution coefficient $D$ and selectivity for target A over other species.  
- Chemical stability, regenerability, low volatility (loss), low toxicity.  
- Phase disengagement: low emulsion tendency, sufficiently large density difference.  
- Diluent controls viscosity, phase behavior, and sometimes reaction stoichiometry.

## 5.2 Stoichiometry, Loading, and Regeneration

- Ensure extractant concentration $C_{S,org,0}$ and phase ratio $\phi$ provide required capacity with reasonable $Z$.  
- Regeneration step:
  - Back-extraction (stripping) using another reagent, or
  - Decomposition of complex (pH swing, temperature, or displacement), or
  - Distillation if volatile species.

Design must close the **solvent loop**: extraction → regeneration → recycle.

## 5.3 Hydrodynamics and Mass-Transfer Area

- Sufficient interfacial area $a$ (droplet dispersion, packing, membrane area).  
- Control of drop size distribution; avoid stable emulsions.  
- Residence time distribution (RTD) must allow both reaction and mass transfer to approach desired extent.

Link to volumetric rate:
$$
N_A V = k_L a V \,\Delta C_{\text{eff}}
$$

Increasing $k_L a$ (agitation, packing, internals) can reduce stage count or column height.

## 5.4 Reactor Types for Reactive Extraction

- **Equilibrium-oriented design**:
  - Aim for near-equilibrium in each stage: high $k_L a$, sufficient residence time, modest throughput per stage.
- **Kinetics-oriented design**:
  - If reaction is slow, need reactors (stirred tanks, loop reactors) with good mixing and controlled temperature.  
  - For highly exothermic complexation, temperature control is crucial (equilibrium and kinetics are temperature dependent).

---

# 6. Typical Design Workflow (High-Level)

1. **Equilibrium characterization**  
   - Measure/specify $K_{\text{ex}}(T)$, loading behavior, $D(C_A, C_S, T)$.  
   - Identify speciation (pH, complexing agents).

2. **Kinetic and mass-transfer studies**  
   - Determine whether process is mass-transfer-controlled or reaction-controlled.  
   - Evaluate $k_L a$ and interfacial reaction rates at expected hydrodynamics.

3. **Stagewise design / column sizing**  
   - Use McCabe–Thiele-type constructions or rigorous equilibrium-stage/nonequilibrium-stage models.  
   - For continuous columns: integrate equilibrium and rate expressions along height.

4. **Solvent regeneration and recycle**  
   - Design back-extraction or stripping section.  
   - Solve overall mass balance for A and solvent; include energy balance if needed.

5. **Sensitivity and operability**  
   - Analyze effect of feed composition, pH, temperature, and phase ratio on extraction efficiency and loading.  
   - Check robustness against phase separation issues (third phase, emulsions).

---

# 7. Why Reactive Extraction is Powerful

- In-situ binding of solute in organic phase **shifts liquid–liquid equilibrium**, enabling:
  - High recovery from dilute aqueous solutions.
  - Avoidance of energy-intensive evaporation.
  - High selectivity even when physical distribution is poor.

- In **reactive separation** contexts, coupling reaction and extraction (or reaction + extraction + distillation) can:
  - Break equilibrium limitations in synthesis (Le Chatelier: remove product as formed).  
  - Increase overall conversions and simplify downstream purification.

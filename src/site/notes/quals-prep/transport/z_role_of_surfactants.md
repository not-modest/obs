---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-role-of-surfactants/","tags":["2019_Jan"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

# Role of Surfactants in Fluid Flow and Dynamics

Surfactants adsorb at interfaces and change **surface tension** and **interfacial rheology**, which in turn modifies flow patterns, drop/bubble dynamics, and mass transfer.

---

## 1. Interfacial Tension and Marangoni Effects

- Surfactant surface excess $\Gamma$ lowers surface tension:
  $$
  \sigma = \sigma(\Gamma), \quad \frac{d\sigma}{d\Gamma} < 0
  $$
- Non-uniform $\Gamma(s,t)$ along an interface creates **surface-tension gradients**:
  $$
  \frac{\partial \sigma}{\partial s} \neq 0
  $$
  leading to **Marangoni stresses** (tangential stresses along the interface).

Tangential stress balance at interface (simplified):
$$
\mu \left( \frac{\partial u_t}{\partial n} \right)_{\text{interface}}
=
\frac{\partial \sigma}{\partial s}
$$
where:
- $u_t$ = tangential velocity along interface  
- $n$ = normal direction  
- $s$ = coordinate along the interface  

Gradients in $\sigma$ drive tangential flows (Marangoni flows) that redistribute surfactant and fluid.

---

## 2. Impact on Drops, Bubbles, and Threads

### 2.1 Deformation and breakup

Lower $\sigma$ → lower capillary pressure:
$$
\Delta p \sim \frac{\sigma}{R}
$$
so for a given inertial or viscous stress, interfaces deform more easily.

Relevant dimensionless groups:
$$
\mathrm{Ca} = \frac{\mu U}{\sigma}, \quad
\mathrm{We} = \frac{\rho U^2 L}{\sigma}
$$

- Decreasing $\sigma$ → increases $\mathrm{Ca}$ and $\mathrm{We}$ → promotes drop/bubble deformation and breakup.

### 2.2 Coalescence and film drainage

Surfactant adsorption at thin films between approaching drops/bubbles:

- Creates **Marangoni stresses** that oppose drainage (immobilizes interface), stabilizing films and **suppressing coalescence**.  
- Can produce repulsive disjoining pressures (electrostatic, steric) via the adsorbed layer.

Result: more stable emulsions and foams; coalescence times increase.

---

## 3. Slug / Taylor Flow and Microfluidics

In microchannels with gas–liquid or liquid–liquid slug flow:

- Surfactants control **drop/slug size** by tuning $\sigma$, influencing regime transitions (dripping ↔ jetting ↔ stable slugs).  
- Interfacial mobility:
  - **Clean (low surfactant)** interface → mobile, strong recirculation inside slugs, high mass-transfer rates.  
  - **Surfactant-covered** interface → partially immobilized, weaker recirculation, modified film thickness around bubbles.

Interfacial area per volume in a capillary (slug flow, rough estimate):
$$
a_{GL} \sim \frac{4}{D}
$$
Decreasing $\sigma$ can shrink drop size and alter $a_{GL}$, impacting volumetric mass transfer $k_L a_{GL}$.

---

## 4. Interfacial Rheology

Surfactant-laden interfaces can have **2D viscosity and elasticity**:

- Interfacial shear viscosity $\eta_s$  
- Interfacial dilatational (extensional) modulus $E_s$

These modify the dynamic boundary conditions:

- Highly viscoelastic interfaces behave more like “elastic skins,” resisting area change and shear.  
- This affects:
  - Capillary wave damping.  
  - Drop oscillations and breakup modes.  
  - Foam/emulsion stability.

---

## 5. Practical Consequences

- **Control of drop/bubble size** in mixers, atomizers, reactors, microfluidics via $\sigma$ and Marangoni effects.  
- **Stabilization** of foams and emulsions (detergents, food, enhanced oil recovery) by suppressing coalescence.  
- **Modified mass transfer**:
  - Lower $\sigma$ and smaller drops → higher interfacial area.  
  - But interfacial immobilization and Marangoni flows can reduce local renewal and change effective $k_L$.  

Overall, surfactants couple **interface thermodynamics** (adsorption and $\sigma(\Gamma)$) with **fluid dynamics** (stresses, flow near interfaces), providing powerful levers to tune multiphase flow behavior.

---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-permeability/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

#2021_Jan 
Permeability quantifies how easily a fluid passes through a material or barrier. In ChemE it appears in two main contexts:

1. **Porous media permeability** (Darcy-type flow through rocks, catalysts, filters)  
2. **Membrane permeability** (mass transfer through dense or porous membranes)

[[#6. Summary Table]]

---

## 1. Porous Media Permeability (Darcy’s Law)

**Intrinsic permeability** $k$ is a property of the porous solid only; it measures the ability of the medium to transmit fluid, independent of fluid properties.

### Darcy’s Law (1D, incompressible, laminar)

For flow through a porous slab of length $L$ and cross-sectional area $A$:
$$
Q = -\,\frac{k\,A}{\mu}\,\frac{\Delta p}{L}
$$

- $Q$ = volumetric flow rate  
- $\mu$ = fluid viscosity  
- $\Delta p$ = pressure drop  

Superficial (Darcy) velocity [[quals-prep/transport/z_Interfacial_Area_Superficial_velocity\|(more details)]]:
$$
u = \frac{Q}{A}
= -\,\frac{k}{\mu}\,\frac{\Delta p}{L}
$$

Units:
- $k$ typically in m² (SI); often reported in darcy (1 darcy ≈ $10^{-12}$ m²).

### Hydraulic conductivity (groundwater, soil)

Often you see:
$$
u = - K \,\frac{\Delta h}{L}
$$

- $K$ = hydraulic conductivity, includes both medium and fluid:
  $$
  K = \frac{k \rho g}{\mu}
  $$

---

## 2. Effective Permeability, Porosity, Tortuosity

Permeability depends on pore geometry:

- **Porosity** $\varepsilon$: fraction of void space.  
- **Tortuosity** $\tau$: how “twisted” flow paths are (effective path length > geometric length).

Empirical relations (Kozeny–Carman type):

$$
k \sim \frac{\varepsilon^3}{S_v^2 (1-\varepsilon)^2}
$$

where $S_v$ is specific surface area (area per unit volume of solid). Increasing tortuosity or decreasing porosity generally lowers $k$.

---

## 3. Membrane Permeability and Permeance

For a flat membrane of thickness $l$ separating two gases or liquids, the **flux** $N$ of species $i$ is often written:

### Linear driving-force form

$$
N_i = \Pi_i \,\Delta p_i
$$

- $\Pi_i$ = **permeance** (mol·m⁻²·s⁻¹·Pa⁻¹)  
- $\Delta p_i$ = transmembrane partial pressure difference of $i$

Permeability $P_i$ relates to permeance via membrane thickness:
$$
P_i = \Pi_i\, l
$$

So:
$$
N_i = \frac{P_i}{l}\,\Delta p_i
$$

Permeability $P_i$ has units like mol·m·m⁻²·s⁻¹·Pa⁻¹ = mol·m·m⁻¹·s⁻¹·Pa⁻¹, often reported in **Barrer** for gases.

---

## 4. Permeability vs Permeance vs Selectivity

- **Permeability $P_i$**:  
  - Intrinsic property of material + specific permeant.  
  - Scales with membrane thickness.

- **Permeance $\Pi_i$**:  
  - System-level property for a given membrane module (material + thickness).  
  - Directly proportional to flux for given $\Delta p_i$.

- **Ideal selectivity** (for species $i$ over $j$):
  $$
  \alpha_{ij} = \frac{P_i}{P_j} = \frac{\Pi_i}{\Pi_j}
  $$

High $P_i$ and high $\alpha_{ij}$ are desired in separations.

---

## 5. Gas Permeability in Polymers

In dense polymer membranes, permeability is often modeled as:
$$
P_i = D_i\,S_i
$$

- $D_i$ = diffusivity of $i$ in polymer  
- $S_i$ = solubility of $i$ in polymer  

Thus flux:
$$
N_i = \frac{D_i S_i}{l} \,\Delta p_i
$$

Permeability reflects both how easily the gas dissolves in the polymer and how fast it diffuses.

---

## 6. Summary Table

| Quantity        | Context             | Basic definition / relation                                  | Depends on                         |
|----------------|---------------------|--------------------------------------------------------------|------------------------------------|
| $k$            | Porous medium       | $u = -\dfrac{k}{\mu}\dfrac{\Delta p}{L}$                    | Pore structure (porosity, tortuosity, size) |
| $K$            | Hydraulic flow      | $K = \dfrac{k \rho g}{\mu}$                                 | $k$ and fluid properties           |
| $P_i$          | Membrane material   | $N_i = \dfrac{P_i}{l}\Delta p_i$                            | Material + permeant (D and S)      |
| $\Pi_i$        | Membrane/module     | $N_i = \Pi_i \Delta p_i$, $\Pi_i = P_i/l$                   | $P_i$ and $l$                      |
| $\alpha_{ij}$  | Membrane selectivity| $\alpha_{ij} = P_i/P_j = \Pi_i/\Pi_j$                       | Differential sorption + diffusion  |

Use $k$ (Darcy) for flow through **porous media**, and $P_i$, $\Pi_i$ for **membrane transport** problems.

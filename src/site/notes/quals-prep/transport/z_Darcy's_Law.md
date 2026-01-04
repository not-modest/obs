---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-darcy-s-law/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

# Darcy’s Law – Math and Key Concepts

Darcy’s law is the **momentum balance for slow flow through porous media**: it says that superficial velocity is proportional to the **negative pressure gradient**, with the proportionality determined by permeability and viscosity.

---

## 1. Core Equation (1D and Vector Form)

### 1D linear flow (length $L$, cross-sectional area $A$)

Volumetric flow rate:
$$
Q = -\,\frac{k A}{\mu}\,\frac{\Delta p}{L}
$$

Superficial (Darcy) velocity:
$$
u = \frac{Q}{A}
= -\,\frac{k}{\mu}\,\frac{\Delta p}{L}
$$

- $k$ = intrinsic permeability [m²] (property of the porous solid) 
- $\mu$ = dynamic viscosity [Pa·s]   [[quals-prep/transport/z_Viscosity#Dynamic (absolute) viscosity, $ mu$\|more info]]
- $\Delta p = p_2 - p_1$ (pressure drop from 1 to 2)

### Differential / vector form

Let $\mathbf{u}$ be Darcy velocity, $p(\mathbf{x})$ pressure field:

$$
\boxed{
\mathbf{u} = -\,\frac{k}{\mu}\,\nabla p
}
$$

Sometimes porosity $\varepsilon$ is made explicit; then **average pore velocity** is $\mathbf{v} = \mathbf{u}/\varepsilon$.

---

## 2. Physical Meaning

- Linear relation: **flux ∝ driving force** (pressure gradient), analogous to:
  - Ohm’s law (current ∝ voltage gradient),
  - Fick’s law (molar flux ∝ concentration gradient).
- $k$ encodes the **geometric ease of flow** (pore size, connectivity, tortuosity).  
- $\mu$ encodes **fluid friction**: higher viscosity → lower velocity for a given gradient.

Darcy’s law is valid when:

- Flow is **laminar in the pores**, Reynolds number in pores $Re_p \lesssim O(1)$.
- Medium is **fully saturated** and permeability is “homogenizable”.

---

## 3. Connection to Poiseuille Flow (Intuition)

Laminar flow in a single cylindrical pore (Hagen–Poiseuille):

For pore radius $R$:
$$
Q_{\text{pore}}
=
-\,\frac{\pi R^4}{8\mu}\,\frac{\Delta p}{L}
$$

Define an equivalent Darcy form:
$$
Q = -\frac{k A}{\mu} \frac{\Delta p}{L}
$$

If the porous medium consists of many pores, homogenization shows that, roughly,
$$
k \sim \frac{\varepsilon R^2}{C(\text{geometry})}
$$
so $k$ can be interpreted as an upscaled “effective $R^2$” over the pore network.

---

## 4. Hydraulic Conductivity and Head Form

In groundwater / soil mechanics, Darcy’s law is often written using **hydraulic head** $h$:

Hydraulic head:
$$
h = \frac{p}{\rho g} + z
$$

Darcy velocity:
$$
\mathbf{u}
=
-\,K\,\nabla h
$$

- $K$ = hydraulic conductivity [m/s], combining $k$ and fluid properties:
  $$
  K = \frac{k \rho g}{\mu}
  $$

Relating forms:
$$
\mathbf{u}
=
-\,\frac{k}{\mu}\,\nabla p
=
-\,\frac{k \rho g}{\mu}\,\nabla \left(\frac{p}{\rho g}\right)
=
-\,K\,\nabla h
$$

---

## 5. Validity and “Darcy Reynolds Number”

Flow in pores has its own Reynolds number, e.g.:

$$
Re_D = \frac{\rho u d_p}{\mu}
$$

or forms involving $\sqrt{k}$; a common rule:

- For $Re_D \lesssim 1$–10: Darcy’s law holds (laminar, linear).  
- At higher $Re_D$, inertial effects appear; you need **Forchheimer / Ergun**-type corrections:

$$
- \nabla p
=
\mu \frac{1}{k} \mathbf{u}
+ \beta \rho |\mathbf{u}| \mathbf{u}
$$

Darcy = first term only; the second term is inertial (quadratic in velocity).

---

## 6. Darcy’s Law + Continuity → Diffusion-Type PDE

For incompressible, single-phase flow in a homogeneous medium:

1. Darcy’s law:
   $$
   \mathbf{u} = -\frac{k}{\mu}\,\nabla p
   $$
2. Mass conservation (no sources/sinks):
   $$
   \nabla \cdot \mathbf{u} = 0
   $$

Combine:
$$
\nabla \cdot \left( -\frac{k}{\mu}\,\nabla p \right) = 0
$$

If $k/\mu$ constant:
$$
\nabla^2 p = 0
$$

In compressible or transient cases (e.g., reservoir engineering), coupling Darcy’s law with accumulation terms leads to the **diffusivity equation** for pressure.

---

## 7. Where Darcy’s Law is Used in ChemE

- **Reservoir engineering**: oil/gas/water flow in porous rock; base of diffusivity equation.  
- **Packed-bed reactors**: idealized low-Re flow through catalyst beds (before using Ergun at higher Re).  
- **Groundwater hydrology**: aquifer flow, drawdown around wells.  
- **Filtration and membranes (porous)**: transmembrane flow through porous supports.  
- **Porous media modeling**: basis for Darcy, Darcy–Brinkman, and Darcy–Forchheimer models in CFD.

In short, Darcy’s law is the **Ohm’s law of porous flow**: flux is linearly related to gradient, with permeability/viscosity as the “resistance” term.

---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/z-slug-flow-reactor/","tags":["2019_Jan"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

# Slug Flow Reactors 
![../src/Pasted image 20251228154531.png|400](/img/user/quals-prep/src/Pasted%20image%2020251228154531.png)

Slug flow reactors can be modeled as **plug-flow reactors** with enhanced interphase mass/heat transfer due to Taylor slugs. Below are the main equations and derivations.

## 1. What is Slug Flow?

- Flow pattern: Sequence of **liquid slugs** and **gas bubbles** (or two immiscible liquid slugs) moving down a channel.
- Each “unit cell” ≈ gas bubble + liquid slug + thin film around bubble.
- Typically seen in **microreactors** and **capillaries** at appropriate flow rates.

Key features:
- Bullet-shaped “Taylor bubbles” spanning the channel cross-section.
- Thin liquid film between bubble and wall.
- Recirculating vortices inside liquid slugs → strong radial mixing, weak axial dispersion.

---

## 2. Hydrodynamics and Residence Time

- Superficial velocities: $u_G$, $u_L$ for gas and liquid; mixture velocity $u_{mix}$ sets residence time:
  $$
  \tau = \frac{L}{u_{mix}}
  $$
- Residence time distribution (RTD) is close to **plug flow** because:
  - Each unit cell moves at nearly constant velocity.
  - Internal mixing within a slug is fast compared to axial convection.

Slugs are characterized by:
- Slug length $L_s$ (liquid), bubble length $L_b$ (gas).
- Void fraction (gas holdup) and film thickness.

---

## 3. Mass Transfer and Heat Transfer

Slug flow strongly enhances interphase transport compared with laminar single-phase flow:

- Large interfacial area per volume (gas–liquid or liquid–liquid).
- Internal recirculation in liquid slugs constantly renews concentration at the interface.
- Thin films around bubbles add extra interfacial area and short diffusion paths.

Effective volumetric mass-transfer coefficient:
$$
k_L a_{\text{slug}} \gg k_L a_{\text{single-phase}}
$$

Similarly, heat transfer is improved:
- Higher Nusselt/Sherwood numbers relative to laminar pipe flow.
- Approximate plug flow with strong radial mixing → efficient temperature control.

---

## 4. Reactor Modeling (Slug Flow as PFR + Enhancement)

At the macro scale, a slug flow reactor is often modeled as a **plug flow reactor (PFR)** with enhanced mass/heat transfer:

- Species balance for liquid-phase component $A$:
  $$
  \frac{dF_{A,L}}{dz}
  = r_{A,L}^{\text{rxn}}(z) + N_A^{\text{int}}(z)\,A
  $$
  where $N_A^{\text{int}}$ is interfacial flux (gas → liquid, or phase 1 → phase 2).

- Interfacial flux (gas–liquid example):
  $$
  N_A^{\text{int}} = k_L a_{\text{slug}} \left(C_{A}^{*} - C_{A,L}\right)
  $$
  with $C_A^{*}$ the equilibrium concentration corresponding to gas-phase composition.

- If reaction is fast in the liquid slug, the overall rate is often controlled by:
  - Gas–liquid mass transfer,
  - Slug hydrodynamics (lengths, velocities, film thickness).

---

## 5. Design Considerations

### 5.1 Advantages

- Near plug-flow behavior with good radial mixing → high selectivity for kinetically controlled reactions.
- High mass and heat transfer → suitable for:
  - Gas–liquid and liquid–liquid reactions,
  - Highly exothermic reactions,
  - Mass-transfer-limited systems.
- Small volume, high surface-to-volume ratio → **process intensification**.

### 5.2 Key design variables

- Channel diameter and geometry (circular, square, T-junction generation).
- Gas and liquid flow rates → control slug/bubble length and regime.
- Physical properties: viscosity, density, surface tension → determine slug regime (via Re, Ca, We).
- Pressure drop and operating pressure (important for gas solubility).

### 5.3 Limitations / Challenges

- Narrow operating window for stable slug flow; at higher velocities, flow may transition to churn/annular regimes.
- Scale-up is non-trivial: often done by **numbering-up** (many parallel channels).
- Sensitivity to fouling, wetting changes, or particle presence (e.g., crystallization).

---

## 6. Typical Applications

- Gas–liquid microreactors (e.g., hydrogenations, oxidations).  
- Liquid–liquid reaction–extraction systems in microchannels.  
- Slug-flow crystallizers: controlled nucleation and growth under well-mixed conditions.  
- Plasma, photocatalytic, or electrochemical reactors with gas–liquid contact.

In summary, a slug flow reactor is essentially a **segmented-flow plug-flow reactor** that leverages Taylor slugs to dramatically enhance mass and heat transfer while maintaining narrow residence time distributions.

---

# Math
## 1. Geometry and Hydrodynamics

Consider a capillary of diameter $D$, total length $L$, carrying alternating **liquid slugs** and **gas bubbles**.

- Superficial velocities:
  $$
  u_L = \frac{Q_L}{A}, \quad
  u_G = \frac{Q_G}{A}
  $$
- Cross-sectional area:
  $$
  A = \frac{\pi D^2}{4}
  $$
- Mixture superficial velocity:
  $$
  u_{mix} = u_L + u_G
  $$

Residence time of a fluid element:
$$
\tau = \frac{L}{u_{mix}}
$$

Define unit-cell length (one bubble + one liquid slug):
$$
L_{cell} = L_b + L_s
$$

Gas holdup (void fraction in channel):
$$
\varepsilon_G = \frac{L_b}{L_{cell}}, \quad
\varepsilon_L = 1 - \varepsilon_G = \frac{L_s}{L_{cell}}
$$

---

## 2. Ideal Plug-Flow Approximation

Under near-ideal Taylor flow:

- Axial dispersion is small → plug-flow assumption for each phase.
- For species $A$ in the **liquid phase**, define molar flow:
  $$
  F_{A,L}(z) = C_{A,L}(z)\,u_L A
  $$

General 1D mole balance (steady state, differential segment $dz$):

$$
\frac{dF_{A,L}}{dz}
=
\text{(net production by reaction)}
+
\text{(net transfer from gas)}
$$

or:
$$
\frac{dF_{A,L}}{dz}
=
(1)\ \nu_A r_{rxn} V_{L,seg}
+
(2)\ N_A^{int} A_{int,seg}
$$

In differential form (per reactor volume basis), we usually write:

$$
\boxed{
\frac{dF_{A,L}}{dz}
=
R_{A,L}(z) + N_A^{int}(z)\,A
}
$$

where:
- $R_{A,L}(z)$ = net rate of production of A in liquid (mol·s⁻¹·m⁻¹)  
- $N_A^{int}(z)$ = interfacial flux of A from gas to liquid (mol·m⁻²·s⁻¹)

Expanding $F_{A,L}=C_{A,L}u_L A$:

$$
u_L A \frac{dC_{A,L}}{dz}
=
R_{A,L}(z) + N_A^{int}(z) A
$$

---

## 3. Interfacial Mass Transfer

Using a two-film-like model for gas–liquid mass transfer:

Interfacial flux of A:
$$
N_A^{int}
=
k_L a_{GL} \big( C_A^{*} - C_{A,L} \big)
$$

- $k_L$ = liquid-side mass-transfer coefficient  
- $a_{GL}$ = interfacial area per reactor volume  
- $C_A^{*}$ = equilibrium dissolved concentration corresponding to gas composition (Henry/Raoult)  

So the species balance becomes:

$$
u_L A \frac{dC_{A,L}}{dz}
=
R_{A,L}(z) + k_L a_{GL}(z)\,A \big( C_A^{*}(z) - C_{A,L}(z) \big)
$$

Divide by $u_L A$:

$$
\frac{dC_{A,L}}{dz}
=
\frac{R_{A,L}(z)}{u_L A}
+
\frac{k_L a_{GL}(z)}{u_L} \big( C_A^{*}(z) - C_{A,L}(z) \big)
$$

If reaction occurs only in the liquid and has rate $r_{A,L}$ per unit liquid volume:

$$
R_{A,L}(z) = r_{A,L}(z)\,A \varepsilon_L
$$

giving:

$$
\boxed{
\frac{dC_{A,L}}{dz}
=
\frac{\varepsilon_L r_{A,L}(z)}{u_L}
+
\frac{k_L a_{GL}(z)}{u_L}
\big( C_A^{*}(z) - C_{A,L}(z) \big)
}
$$

This is the core PFR equation for A in the liquid slugs.

---

## 4. Gas-Phase Balance (if needed)

For gas species A:

Molar flow:
$$
F_{A,G}(z) = y_A(z)\, Q_G \frac{p}{RT}
$$

Gas-phase mole balance (assuming reaction only in liquid, so gas loses A only by transfer):

$$
\frac{dF_{A,G}}{dz}
=
- N_A^{int}(z)\,A
$$

Using $N_A^{int} = k_L a_{GL}(C_A^{*} - C_{A,L})$:

$$
\boxed{
\frac{dF_{A,G}}{dz}
=
- k_L a_{GL}(z)\,A \big( C_A^{*}(z) - C_{A,L}(z) \big)
}
$$

Coupled with Henry’s law or other equilibrium relation at interface, you can solve for $C_A^{*}$ and gas composition along $z$.

---

## 5. Interfacial Area in Slug Flow

A simple estimate for interfacial area per volume $a_{GL}$ in a channel:

- Each unit cell has bubble–liquid interfacial area $\approx \pi D L_b$ (neglecting end caps, or use more refined geometry).
- Volume of one unit cell: $V_{cell} = A L_{cell}$.

So:
$$
a_{GL}
\approx
\frac{\text{interfacial area per cell}}{\text{volume per cell}}
=
\frac{\pi D L_b}{A L_{cell}}
=
\frac{\pi D L_b}{(\pi D^2 /4) L_{cell}}
=
\frac{4 L_b}{D L_{cell}}
$$

For high gas holdup ($L_b \sim L_{cell}$), this gives $a_{GL} \sim 4/D$.  
Smaller $D$ → larger $a_{GL}$.

---

## 6. Dimensionless Groups and Regime Identification

### 6.1 Reynolds, Capillary, and Weber numbers (for slug flow formation)

- Reynolds number:
  $$
  Re = \frac{\rho u_{mix} D}{\mu}
  $$
- Capillary number:
  $$
  Ca = \frac{\mu u_{mix}}{\sigma}
  $$
- Weber number:
  $$
  We = \frac{\rho u_{mix}^2 D}{\sigma}
  $$

Slug/Taylor flow typically occurs in a window of $Re$ and $Ca$ where:

- Interface spans the channel.
- Slugs remain coherent without breaking into churn or bubbly flow.

---

## 7. Effective Axial Dispersion (if non-ideal PFR)

If deviations from ideal plug flow exist, one can add an axial dispersion term:

Species balance in axial coordinate:

$$
u_{\text{eff}} \frac{\partial C_{A,L}}{\partial z}
=
D_{\text{ax,eff}} \frac{\partial^2 C_{A,L}}{\partial z^2}
+ \varepsilon_L r_{A,L}
+ k_L a_{GL} ( C_A^{*} - C_{A,L} )
$$

- $D_{\text{ax,eff}}$ is the effective axial dispersion coefficient (often small in well-formed slug flow).

In many microreactor slug flows, $D_{\text{ax,eff}}$ is small enough to neglect, justifying plug-flow modeling.

---

## 8. Summary of Key Equations

**Hydrodynamics and RTD**
- $u_{mix} = u_L + u_G$  
- $\tau = L / u_{mix}$  
- Hydraulic Diameter #2019_Jan : $$ D_h = \frac{4\cdot\text{Cross-sectional Area}}{\text{Wetted Perimeter}} $$

**Liquid-phase species balance (PFR + mass transfer + reaction)**
$$
\frac{dC_{A,L}}{dz}
=
\frac{\varepsilon_L r_{A,L}(z)}{u_L}
+
\frac{k_L a_{GL}(z)}{u_L}
\big( C_A^{*}(z) - C_{A,L}(z) \big)
$$

**Gas-phase species balance**
$$
\frac{dF_{A,G}}{dz}
=
- k_L a_{GL}(z)\,A \big( C_A^{*}(z) - C_{A,L}(z) \big)
$$

**Interfacial area estimate**
$$
a_{GL}
\approx
\frac{4 L_b}{D L_{cell}}
\quad (\text{slug–bubble unit cell})
$$

**Regime characterization**
$$
Re = \frac{\rho u_{mix} D}{\mu},
\quad
Ca = \frac{\mu u_{mix}}{\sigma},
\quad
We = \frac{\rho u_{mix}^2 D}{\sigma}
$$

These relations give a compact yet mathematically explicit toolkit for modeling and designing slug flow reactors.

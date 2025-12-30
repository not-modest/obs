---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-viscosity/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

[[quals-prep/transport/Trans_02_Momentum_Transport\|Trans_02_Momentum_Transport]]
Viscosity quantifies **internal friction** in a fluid, i.e., resistance to shear or flow.

---

## 1. Dynamic vs Kinematic Viscosity

### Dynamic (absolute) viscosity, $\mu$ 

Newton’s law of viscosity (simple shear):
$$
\tau = \mu \frac{du}{dy}
$$
- $\tau$ = shear stress  
- $du/dy$ = velocity gradient (shear rate)

Units:
- SI: Pa·s = kg·m⁻¹·s⁻¹  

**Newtonian fluid**: $\mu$ independent of shear rate.  
**Non-Newtonian**: $\mu_{\text{eff}}$ depends on $\dot{\gamma}$, time, etc.

### Kinematic viscosity, $\nu$

Ratio of dynamic viscosity to density:
$$
\nu = \frac{\mu}{\rho}
$$

Units:
- SI: m²·s⁻¹  

Interpreted as “momentum diffusivity,” analogous to thermal diffusivity $\alpha$ and mass diffusivity $D$.

---

## 2. Viscosity shows up in these concepts:

### 2.1 Momentum balance / Navier–Stokes

For incompressible Newtonian fluid:
$$
\rho \left( \frac{\partial \mathbf{v}}{\partial t}
+ \mathbf{v}\cdot\nabla \mathbf{v} \right)
=
- \nabla p + \mu \nabla^2 \mathbf{v} + \rho \mathbf{g}
$$

Viscous term $\mu \nabla^2 \mathbf{v}$ controls **momentum diffusion** and laminar flow patterns.

### 2.2 Dimensionless groups ([[quals-prep/Dimensionless#Reynolds number, Re\|Re]], [[quals-prep/Dimensionless#Prandtl number, Pr\|Pr]], [[quals-prep/Dimensionless#Schmidt number, Sc\|Sc]])

- Reynolds number:
  $$
  Re = \frac{\rho U L}{\mu} = \frac{U L}{\nu}
  $$
  Inertia vs viscosity → laminar vs turbulent.

- Prandtl number (heat):
  $$
  Pr = \frac{\nu}{\alpha} = \frac{\mu c_p}{k}
  $$

- Schmidt number (mass):
  $$
  Sc = \frac{\nu}{D} = \frac{\mu}{\rho D}
  $$

Viscosity links **momentum** to **heat and mass transfer** via these analogies.

### 2.3 Pipe / channel flow [[quals-prep/transport/z_Velocity Profiles and Boundary Layers\|(here)]]

Fully developed laminar flow (Hagen–Poiseuille):
$$
\Delta p = \frac{32 \mu U L}{D^2}
$$
or friction factor
$$
f = \frac{64}{Re}
$$

Viscosity determines pressure drop, pump/compressor sizing, and flow regime.

### 2.4 Packed beds ([[quals-prep/transport/z_Ergun_equation\|Ergun equation]])

Pressure drop:
$$
\frac{\Delta p}{L}
=
\frac{150\,\mu (1-\varepsilon)^2}{d_p^2 \varepsilon^3}\,u_s
+
\frac{1.75\,\rho (1-\varepsilon)}{d_p \varepsilon^3}\,u_s^2
$$

First (linear) term is purely viscous; scales with $\mu$.

### 2.5 Mass and heat transfer coefficients ([[quals-prep/Dimensionless#2. Heat transfer\|Nu]], [[quals-prep/Dimensionless#Sherwood number, Sh\|Sh]])

Correlations like:
$$
Nu = f(Re, Pr), \quad Sh = f(Re, Sc)
$$

Because $Re$, $Pr$, $Sc$ depend on $\mu$, viscosity indirectly controls:
- $h$ (heat-transfer coefficient) via $Nu$.  
- $k_L$ (mass-transfer coefficient) via $Sh$.

---

## 3. Non-Newtonian Viscosity (Very Brief)

Many industrial fluids (polymer melts, slurries, blood, emulsions):

- Power-law (Ostwald–de Waele):
  $$
  \tau = K \dot{\gamma}^n
  $$
  Apparent viscosity:
  $$
  \mu_{\text{app}} = K \dot{\gamma}^{n-1}
  $$

- Bingham, Herschel–Bulkley, viscoelastic models extend this idea (yield stress, elasticity), changing flow, mixing, and scale-up.

---

## 4. Temperature and Composition Effects

Empirical correlations, e.g. Arrhenius-like:
$$
\mu(T) = \mu_0 \exp\left(\frac{E_\mu}{R T}\right)
$$

Or for liquids, log-linear forms (e.g. Andrade or Vogel–Fulcher–Tammann) are common.  
Mixtures: viscosity often estimated by mixing rules (e.g. logarithmic blending), but strong non-ideality possible.

---

## 5. Summary Table

| Quantity           | Symbol | Basic relation                     | Units      |
|--------------------|--------|-------------------------------------|------------|
| Dynamic viscosity  | $\mu$  | $\tau = \mu\,du/dy$                | Pa·s       |
| Kinematic viscosity| $\nu$  | $\nu = \mu / \rho$                 | m²/s       |
| Reynolds number    | $Re$   | $Re = \rho U L / \mu = UL/\nu$     | –          |
| Prandtl number     | $Pr$   | $Pr = \nu/\alpha = \mu c_p/k$      | –          |
| Schmidt number     | $Sc$   | $Sc = \nu/D = \mu/(\rho D)$        | –          |

Viscosity is the **bridge** from microscopic momentum exchange to macroscopic flow, and it appears everywhere in ChemE: pressure drop, flow regime, mixing, transport coefficients, and non-Newtonian rheology.

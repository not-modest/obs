---
{"dg-publish":true,"permalink":"/quals-prep/transport/trans-02-momentum-transport/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Newtonian fluid**  
  Shear stress proportional to velocity gradient:
  $$
  \tau_{xy} = \mu \frac{\partial u_x}{\partial y}
  $$

- **Viscosity, $\mu$**  
  Measure of fluid resistance to shear; units Pa·s (kg m$^{-1}$ s$^{-1}$).

- **Fully developed laminar flow in a circular pipe**  
  Velocity profile and pressure drop are constant with axial distance; no entrance effects.

- **Friction factor, $f$**  
  Dimensionless measure of pressure drop in pipes.

---

## Core formulas

### 1. Laminar flow in a circular pipe

Velocity profile:
$$
u(r) = 2 u_{\text{avg}} \left(1 - \frac{r^2}{R^2}\right)
$$

Average velocity:
$$
u_{\text{avg}} = \frac{R^2}{8\mu} \left(-\frac{dP}{dz}\right)
$$

Pressure drop over length $L$:
$$
\Delta P = \frac{32 \mu L u_{\text{avg}}}{D^2}
$$
with $D = 2R$.

For laminar flow ($\text{Re} < 2100$):
$$
f = \frac{64}{\text{Re}},\quad
\Delta P = f \frac{L}{D} \frac{\rho u_{\text{avg}}^2}{2}
$$

### 2. Major and minor losses

Total head loss:
$$
\Delta P = \left(f \frac{L}{D} + \sum K_i\right) \frac{\rho u^2}{2}
$$
where $K_i$ are loss coefficients for fittings, bends, valves.

### 3. Very brief external flow

Drag force on a body:
$$
F_D = \frac{1}{2} C_D \rho u_\infty^2 A
$$
where $C_D$ is drag coefficient and $A$ is reference area.

---

## Interesting concepts

- **Laminar vs turbulent**  
  Low Re: viscous forces dominate, predictable parabolic profiles. High Re: turbulence, flatter velocity profile, larger friction factor.

- **Entrance length**  
  Fully developed flow occurs after some entrance distance; for many exam problems, pipe is assumed fully developed.

- **Use of Moody chart**  
  For turbulent flow, friction factor depends on Re and relative roughness; read from Moody chart or correlations.


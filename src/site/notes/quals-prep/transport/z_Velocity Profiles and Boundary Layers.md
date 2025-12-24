---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-velocity-profiles-and-boundary-layers/"}
---

[[quals-prep/transport/Trans_02_Momentum_Transport\|Trans_02_Momentum_Transport]]
#2025_Jan 
Velocity profiles describe how fluid velocity varies across a flow cross-section. They depend on flow regime (laminar vs turbulent), geometry, and boundary conditions (e.g., no-slip at walls).

---

## Boundary Layer Concept

When a fluid flows past a solid surface:

- **No-slip condition** at the wall:
  $$
  \mathbf{u}(y=0) = 0
  $$
- Away from the wall, velocity approaches the free-stream value $U_\infty$.

The **boundary layer** is the thin region near the wall where viscous effects are significant and velocity changes from 0 to (approximately) $U_\infty$.

- Boundary layer thickness $\delta(x)$ grows with distance $x$ from the leading edge.  
- Outside the boundary layer, the flow is often approximated as inviscid and nearly uniform.

---

## Laminar vs Turbulent Boundary Layers

- **Laminar boundary layer**:
  - Flow is orderly, layered; velocity profile is smooth, with strong curvature near the wall.  
  - Example (Blasius solution over a flat plate): steep gradient at the wall, gradual approach to $U_\infty$.

- **Turbulent boundary layer**:
  - Flow has eddies and fluctuations; profile near the wall is fuller (less curved), higher velocity near the wall compared to laminar.  
  - Often described by empirical “law of the wall” forms (e.g., logarithmic profiles).

Transition from laminar to turbulent is usually characterized by a critical Reynolds number based on distance from the leading edge:
$$
\text{Re}_x = \frac{\rho U_\infty x}{\mu}
$$

---

## Internal Flow: Pipe / Channel

For fully developed flow in a circular pipe of radius $R$:

### Laminar Flow (Hagen–Poiseuille)

Steady, incompressible, fully developed, laminar flow driven by pressure gradient has a **parabolic** profile:
$$
u(r) = u_{\max}\left(1 - \frac{r^2}{R^2}\right)
$$
where:
- $r$ = radial coordinate from centerline  
- $u_{\max}$ = centerline velocity  

Average velocity:
$$
\bar{u} = \frac{1}{A}\int_A u\,dA = \frac{u_{\max}}{2}
$$

Shear stress is highest at the wall and zero at the centerline.

### Turbulent Flow in a Pipe

Fully developed turbulent pipe flow has a **flatter (“fuller”) velocity profile**:

- Velocity is almost uniform over most of the cross-section, dropping sharply near the wall.  
- Near the wall, empirical forms like the **1/7th power law** are sometimes used:
  $$
  \frac{u(r)}{u_{\max}} \approx \left(1 - \frac{r}{R}\right)^{1/n}, \quad n \approx 7 \text{ (for moderate Re)}
  $$

- The near-wall region is often decomposed into:
  - Viscous sublayer (very close to wall).  
  - Buffer layer.  
  - Log-law region (where $u^+ \sim \frac{1}{\kappa}\ln y^+ + B$ in wall units).

---

## Plug Flow Approximation
[[quals-prep/kinetics/Kin_03_Batch_CSTR_PFR\|Kin_03_Batch_CSTR_PFR]]

In many engineering models (e.g., ideal plug flow reactors, high-Re pipe flow), velocity is taken as uniform across the cross-section:

- **Plug flow assumption**:
  $$
  u(r) \approx \bar{u}
  \quad \text{for } 0 \le r < R
  $$

Physically:

- Real velocity profiles are never perfectly flat due to no-slip at walls.  
- However, in high-Re turbulent flow, the core region is nearly uniform, and plug flow is a reasonable approximation for:
  - Residence time calculations  
  - 1D mass/energy balances  

Boundary layers still exist near walls, but their effect on bulk mixing can be small compared to turbulent mixing.

---

## Entrance Region vs Fully Developed Flow

In internal flows:

- **Entrance region**:
  - Velocity profile evolves from uniform (e.g., at pipe inlet) to the characteristic fully developed shape.  
  - Boundary layers grow from the walls until they merge at the centerline.

- **Fully developed region**:
  - Axial velocity profile no longer changes with axial position:
    $$
    \frac{\partial u}{\partial x} \approx 0
    $$
  - Pressure gradient balances viscous/turbulent shear.

The entrance length depends on Reynolds number and flow regime; laminar entrance length scales differently from turbulent.

---

## Summary of Typical Profiles

- **External laminar** (flat plate): thin, growing boundary layer; sharp gradient at wall, gradual rise to $U_\infty$.  
- **External turbulent**: thicker boundary layer; fuller profile near wall, more momentum near the wall.  
- **Laminar pipe**: parabolic profile, $u_{\max} = 2\bar{u}$.  
- **Turbulent pipe**: fuller profile, $u_{\max} \approx 1.1–1.3\,\bar{u}$, steep drop near wall.  
- **Plug flow model**: idealized uniform profile, useful for simplified reactor/transport calculations.

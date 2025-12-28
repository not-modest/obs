---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-surface-tension/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

#2024_Jan 
Surface tension is the tendency of a liquid surface to minimize its area due to cohesive intermolecular forces, making the surface behave like a stretched elastic membrane.

---

## Thermodynamic Definition

Thermodynamically, surface tension γ is the increase in Gibbs free energy per unit increase in interfacial area at constant T and p:
$$
\gamma = \left(\frac{\partial G}{\partial A}\right)_{T,p,\{n_i\}}
$$
It is the reversible work required to create unit area of new surface. Units: N/m.

---

## Mechanical Definition

Mechanically, surface tension is the tangential force per unit length acting along a line in the interface:
$$
\gamma = \frac{F}{L}
$$
- $F$ = force along the surface  
- $L$ = length over which the force acts  

This relates directly to ring and plate methods for measuring γ.

---

## Young–Laplace Equation (Curved Interfaces)

For a fluid–fluid interface with principal radii of curvature $R_1$ and $R_2$, the pressure jump across the interface is:
$$
\Delta p = p_{\text{inside}} - p_{\text{outside}} = \gamma \left(\frac{1}{R_1} + \frac{1}{R_2}\right)
$$

Special cases:

- Spherical droplet/bubble:
  $$
  \Delta p = \frac{2\gamma}{R}
  $$
- Cylindrical interface:
  $$
  \Delta p = \frac{\gamma}{R}
  $$

Small droplets therefore have higher internal pressure; capillary effects are stronger at small length scales.

---

## Contact Angle and Wetting (Young’s Equation)

For a liquid on a solid in a gas:
$$
\gamma_{\text{SG}} = \gamma_{\text{SL}} + \gamma_{\text{LG}} \cos\theta
$$
or:
$$
\gamma_{\text{SG}} - \gamma_{\text{SL}} = \gamma_{\text{LG}} \cos\theta
$$

Where:
- $\gamma_{\text{SG}}$ = solid–gas surface energy  
- $\gamma_{\text{SL}}$ = solid–liquid interfacial energy  
- $\gamma_{\text{LG}}$ = liquid–gas surface tension  
- $\theta$ = contact angle  
![quals-prep/src/Pasted image 20251224164344.png|400](/img/user/quals-prep/src/Pasted%20image%2020251224164344.png) 
Interpretation:
![quals-prep/src/Pasted image 20251224164501.png](/img/user/quals-prep/src/Pasted%20image%2020251224164501.png)
- $\theta \approx 0^\circ$: good wetting (hydrophilic).  
- $\theta \approx 180^\circ$: poor wetting (hydrophobic).
---

## Molecular Picture and Temperature Dependence

- Bulk molecules experience isotropic attractions; surface molecules have fewer neighbors, so the surface is a higher-energy region.  
- Creating more surface moves molecules from bulk to surface, costing energy → positive γ.  
- Surface tension generally decreases with temperature and tends to zero near the critical point.

---

## Practical Consequences

- Capillary rise or depression in narrow tubes due to balance between surface tension and gravity.  
- Nearly spherical shape of small droplets and bubbles (surface area minimization at fixed volume).  
- Control of wetting, spreading, foams, emulsions, coatings, and detergency by adjusting γ (e.g., surfactants lower surface tension).

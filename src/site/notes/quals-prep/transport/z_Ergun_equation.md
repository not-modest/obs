---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-ergun-equation/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

#2021_Jan 
# Ergun Equation (Packed-Bed Pressure Drop)

The Ergun equation relates **pressure drop** across a packed bed to **fluid properties**, **packing geometry**, and **superficial velocity**, combining viscous (laminar) and inertial (turbulent) contributions.

---

## 1. Standard Form

For a packed bed of length $L$ with spherical particles of diameter $d_p$ and void fraction $\varepsilon$, carrying fluid of density $\rho$, viscosity $\mu$, and superficial velocity $u_s$:

$$
\frac{\Delta p}{L}
=
\frac{150\,\mu\,(1-\varepsilon)^2}{d_p^2\,\varepsilon^3}\,u_s
+
\frac{1.75\,\rho\,(1-\varepsilon)}{d_p\,\varepsilon^3}\,u_s^2
$$

- First term: **viscous** (linear in $u_s$)  
- Second term: **inertial** (quadratic in $u_s$)

Superficial velocity:
$$
u_s = \frac{Q}{A}
$$

---

## 2. Physical Interpretation

- At **low Reynolds number** (small $u_s$): first term dominates → linear dependence on velocity (Darcy-like).  
- At **high Reynolds number**: second term dominates → quadratic dependence on velocity (inertial losses).

Void fraction $\varepsilon$ and particle size $d_p$ sharply affect resistance:

- Lower $\varepsilon$ (denser packing) → higher $\Delta p/L$.  
- Smaller $d_p$ → higher $\Delta p/L$ (more surface area, narrower pores).

---

## 3. Connection to Darcy–Forchheimer Form

The Darcy–Forchheimer equation for flow in porous media:

$$
\frac{\Delta p}{L}
=
\frac{\mu}{k}\,u_s
+
\beta \rho u_s^2
$$

Comparing with Ergun:

- **Viscous permeability** $k$:
  $$ 
  k = \frac{d_p^2}{150}\,\frac{\varepsilon^3}{(1-\varepsilon)^2}
  $$

- **Inertial coefficient** $\beta$:
  $$
  \beta = \frac{1.75\,(1-\varepsilon)}{d_p\,\varepsilon^3}
  $$

So the Ergun equation effectively provides empirical expressions for $k$ and $\beta$ for packed beds of (roughly) spherical particles.

---

## 4. Dimensionless Form (Packed-Bed Friction Factor)

Define a **particle Reynolds number** based on superficial velocity:

$$
Re_p = \frac{\rho u_s d_p}{\mu}
$$

Packed-bed friction factor $f_p$ can be written as:

$$
f_p
=
\frac{\Delta p}{L}\,
\frac{d_p}{\rho u_s^2}
\left(
\frac{\varepsilon^3}{1-\varepsilon}
\right)
$$

Using the Ergun equation, this gives:

$$
f_p
=
\frac{150}{Re_p (1-\varepsilon)}
+
1.75
$$

- At low $Re_p$: $f_p \approx \dfrac{150}{Re_p (1-\varepsilon)}$ (viscous regime).  
- At high $Re_p$: $f_p \approx 1.75$ (inertial regime).

---

## 5. Usage Notes

- Applicable to **flow through packed beds** of roughly uniform spherical particles over a broad range of Reynolds numbers.  
- For non-spherical particles, an effective diameter based on **sphericity** is typically used.  
- Common in design of **packed-bed reactors**, **adsorbers**, **fixed-bed catalytic reactors**, and **packed columns**.  
- For very low velocities (purely laminar), the first term reduces to the Carman–Kozeny type correlation.  

In practice:

1. Compute $Re_p$.  
2. Evaluate both terms; check whether viscous or inertial term dominates.  
3. Use $\Delta p$ to size pumps/compressors, evaluate feasibility, or estimate minimum fluidization (when combined with weight of particles) in fluidization problems.

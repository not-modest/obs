---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-navier-stokes/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

# 1. What Navier–Stokes *means*

- Treat the fluid as a continuum with:
  - Velocity field $\mathbf{u}(\mathbf{x},t)$
  - Density $\rho(\mathbf{x},t)$
- At each point, apply **force balance** to a tiny fluid element.

Forces per unit volume:
- **Inertial** (left-hand side): $\rho\,D\mathbf{u}/Dt$  
- **Pressure** (normal stress): $-\nabla p$  
- **Viscous** (tangential stress): “smeared out friction” $\nabla\cdot\boldsymbol{\tau}$  
- **Body forces** (e.g., gravity): $\rho\mathbf{g}$  

So the conceptual statement is:
$$
\text{Inertia} = \text{pressure forces} + \text{viscous forces} + \text{body forces}
$$

The Navier–Stokes equations are the **PDE realization** of this statement once you supply a **constitutive law** for viscous stress.

---

# 2. Mass Conservation (Continuity)

For an incompressible fluid:
$$
\nabla \cdot \mathbf{u} = 0
$$

This says there is no local volume change; what flows in must flow out.

---

# 3. General Momentum Balance (Before Choosing Fluid Type)

Start with Newton’s 2nd law on a differential element:

- Momentum per volume: $\rho\mathbf{u}$  
- Material derivative:
  $$
  \frac{D\mathbf{u}}{Dt}
  =
  \frac{\partial \mathbf{u}}{\partial t}
  + \mathbf{u}\cdot\nabla \mathbf{u}
  $$

Local momentum balance:
$$
\rho \frac{D\mathbf{u}}{Dt}
=
\nabla \cdot \boldsymbol{\sigma}
+ \rho \mathbf{g}
$$

- $\boldsymbol{\sigma}$ = Cauchy stress tensor (all surface stresses).  

Decompose:
$$
\boldsymbol{\sigma}
= -p \mathbf{I} + \boldsymbol{\tau}
$$
- $-p\mathbf{I}$: isotropic pressure  
- $\boldsymbol{\tau}$: viscous (deviatoric) stress

Thus:
$$
\rho \frac{D\mathbf{u}}{Dt}
=
-\nabla p
+ \nabla \cdot \boldsymbol{\tau}
+ \rho \mathbf{g}
\tag{1}
$$

So far: **general Newton’s law for any fluid**; not yet “Navier–Stokes” until we define $\boldsymbol{\tau}$.

---

# 4. Newtonian Fluid Assumption (Constitutive Law)

A **Newtonian fluid** has viscous stress proportional to rate of strain:

Rate-of-strain tensor:
$$
\mathbf{D}
=
\frac{1}{2}
\left[
\nabla \mathbf{u} + (\nabla \mathbf{u})^T
\right]
$$

General isotropic Newtonian form:
$$
\boldsymbol{\tau}
=
2\mu \mathbf{D}
+ \lambda (\nabla\cdot\mathbf{u})\,\mathbf{I}
$$

- $\mu$ = shear (dynamic) viscosity  
- $\lambda$ = second viscosity

For **incompressible** flow, $\nabla\cdot\mathbf{u} = 0$, so:
$$
\boldsymbol{\tau}
=
2\mu \mathbf{D}
=
\mu\left[
\nabla \mathbf{u} + (\nabla \mathbf{u})^T
\right]
$$

Its divergence simplifies (for constant $\mu$) to:
$$
\nabla\cdot\boldsymbol{\tau}
=
\mu \nabla^2 \mathbf{u}
$$

This is **momentum diffusion**: viscous forces behave like a Laplacian of velocity.

---

# 5. Incompressible Newtonian Navier–Stokes (Final Form)

Substitute into (1):

$$
\rho \frac{D\mathbf{u}}{Dt}
=
-\nabla p
+ \mu \nabla^2 \mathbf{u}
+ \rho \mathbf{g}
$$

with
$$
\frac{D\mathbf{u}}{Dt}
=
\frac{\partial \mathbf{u}}{\partial t}
+ \mathbf{u}\cdot\nabla \mathbf{u},
\quad
\nabla\cdot\mathbf{u} = 0
$$

Expanded:

$$
\rho
\left(
\frac{\partial \mathbf{u}}{\partial t}
+ \mathbf{u}\cdot\nabla \mathbf{u}
\right)
=
- \nabla p
+ \mu \nabla^2 \mathbf{u}
+ \rho \mathbf{g}
$$

This is **the Navier–Stokes equation** for an incompressible Newtonian fluid:

- LHS: local + convective acceleration (inertia)  
- RHS: pressure gradient + viscous diffusion + body forces  

---

# 6. Dimensionless form and Reynolds number

Introduce characteristic $U, L$ and scale:

- $\mathbf{u}' = \mathbf{u}/U$, $x' = x/L$, $t' = t U/L$, $p' = p / (\rho U^2)$  

Then you get:
$$
\frac{\partial \mathbf{u}'}{\partial t'}
+
\mathbf{u}'\cdot\nabla' \mathbf{u}'
=
- \nabla' p'
+
\frac{1}{Re} \nabla'^2 \mathbf{u}'
+ \mathbf{f}'
$$

where
$$
Re = \frac{\rho U L}{\mu}
$$

- $Re \ll 1$ → Stokes (viscous-dominated) flow  
- $Re \gg 1$ → inertia-dominated, potential turbulence

---

---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-shell-balance/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

# Shell Balances in Chemical Engineering 

Shell (or differential) balances apply conservation laws (mass, species, momentum, energy) on a **small differential volume** to derive PDEs. The structure is always:

- Accumulation = In − Out + Generation − Consumption

Below are the standard forms and typical derivations.

---

## 1. General Conservation Statement

For a conserved quantity per unit volume, $\Phi(\mathbf{r},t)$ (e.g., total mass, species mass, momentum component, energy):

$$
\frac{\partial \Phi}{\partial t}
= - \nabla \cdot \mathbf{J}_\Phi + S_\Phi
$$

where:
- $\mathbf{J}_\Phi$ = flux vector of $\Phi$
- $S_\Phi$ = volumetric source (positive for generation, negative for consumption)

This is obtained by applying:

$$
\frac{d}{dt} \int_V \Phi \, dV
=
- \int_A \mathbf{J}_\Phi \cdot \mathbf{n} \, dA
+ \int_V S_\Phi \, dV
$$

to an arbitrary fixed control volume $V$, then shrinking to a differential element and using the divergence theorem.

---

## 2. Shell Balances in Rectangular Coordinates

Consider a rectangular differential element with sides $dx, dy, dz$.

### 2.1. Total Mass Balance (Continuity)

Let $\rho$ be density, $\mathbf{v} = (u,v,w)$ velocity.

Total mass per volume:
$$
\Phi = \rho
$$

Flux (mass flux by convection):
$$
\mathbf{J}_m = \rho \mathbf{v}
$$

No sources ($S_\Phi = 0$):

$$
\frac{\partial \rho}{\partial t}
= - \nabla \cdot (\rho \mathbf{v})
$$

In rectangular coordinates:

$$
\frac{\partial \rho}{\partial t}
+ \frac{\partial (\rho u)}{\partial x}
+ \frac{\partial (\rho v)}{\partial y}
+ \frac{\partial (\rho w)}{\partial z}
= 0
$$

For incompressible flow ($\rho$ constant):

$$
\frac{\partial u}{\partial x}
+ \frac{\partial v}{\partial y}
+ \frac{\partial w}{\partial z}
= 0
$$

### 2.2. Species Balance (Diffusion + Convection + Reaction)

Let $c_A$ be concentration of species A. Take:

- Accumulation:
  $$
  \frac{\partial c_A}{\partial t}
  $$
- Convective flux:
  $$
  \mathbf{J}_{A,\text{conv}} = c_A \mathbf{v}
  $$
- Diffusive flux (Fick’s law):
  $$
  \mathbf{J}_{A,\text{diff}} = - D_{AB} \nabla c_A
  $$
Total flux:
$$
\mathbf{J}_A = c_A \mathbf{v} - D_{AB} \nabla c_A
$$

Volumetric reaction rate (consumption of A) = $r_A$ (negative if consumption, positive if generation). Then:

$$
\frac{\partial c_A}{\partial t}
= - \nabla \cdot \mathbf{J}_A + r_A
$$

In rectangular coordinates:

$$
\frac{\partial c_A}{\partial t}
=
- \left[
\frac{\partial}{\partial x}(c_A u - D_{AB} \frac{\partial c_A}{\partial x})
+
\frac{\partial}{\partial y}(c_A v - D_{AB} \frac{\partial c_A}{\partial y})
+
\frac{\partial}{\partial z}(c_A w - D_{AB} \frac{\partial c_A}{\partial z})
\right]
+ r_A
$$

For 1D steady diffusion with reaction in $x$ (no convection, $u=0$):

- Accumulation = 0
- Convective flux = 0

Balance reduces to:

$$
\frac{d}{dx}
\left(
- D_{AB} \frac{d c_A}{dx}
\right)
+ r_A = 0
$$

---

## 3. Shell Balances in Cylindrical Coordinates

Coordinates: $(r, \theta, z)$ with corresponding unit vectors. Consider a differential shell of dimensions $dr$, $r d\theta$, $dz$.

### 3.1. Continuity Equation

For incompressible flow:

$$
\frac{1}{r} \frac{\partial}{\partial r}(r v_r)
+ \frac{1}{r} \frac{\partial v_\theta}{\partial \theta}
+ \frac{\partial v_z}{\partial z}
= 0
$$

### 3.2. Species Balance (General Form)

Concentration $c_A$, flux:

$$
\mathbf{J}_A =
c_A \mathbf{v}
- D_{AB} \nabla c_A
$$

Gradient in cylindrical coordinates:

$$
\nabla c_A
=
\hat{e}_r \frac{\partial c_A}{\partial r}
+
\hat{e}_\theta \frac{1}{r} \frac{\partial c_A}{\partial \theta}
+
\hat{e}_z \frac{\partial c_A}{\partial z}
$$

Divergence of flux:

$$
\nabla \cdot \mathbf{J}_A
=
\frac{1}{r} \frac{\partial}{\partial r}
\left(
r J_{A,r}
\right)
+
\frac{1}{r} \frac{\partial J_{A,\theta}}{\partial \theta}
+
\frac{\partial J_{A,z}}{\partial z}
$$

Balance:

$$
\frac{\partial c_A}{\partial t}
= - \nabla \cdot \mathbf{J}_A + r_A
$$

---

### 3.3. Typical 1D Shell Balance: Radial Diffusion + Reaction

Example: steady diffusion and reaction of A in a long cylinder (no $\theta$, no $z$ variation, no convection):

- $c_A = c_A(r)$
- Only radial flux $J_{A,r} = - D_{AB} \frac{d c_A}{d r}$

Shell between $r$ and $r + dr$, length $L$:

- In: $J_{A,r}(r) \cdot (2\pi r L)$
- Out: $J_{A,r}(r+dr) \cdot [2\pi (r+dr) L]$
- Generation: $r_A \cdot (\text{volume}) = r_A \cdot (2\pi r L dr)$
- Steady state: accumulation = 0

Balance:

$$
0 =
J_{A,r}(r) (2\pi r L)
- J_{A,r}(r+dr) [2\pi (r+dr) L]
+ r_A (2\pi r L dr)
$$

Divide by $2\pi L$ and take $dr \to 0$:

$$
\frac{d}{dr}(r J_{A,r})
+ r r_A
= 0
$$

Substitute $J_{A,r} = - D_{AB} \frac{d c_A}{d r}$:

$$
\frac{d}{dr}
\left(
- r D_{AB} \frac{d c_A}{d r}
\right)
+ r r_A
= 0
$$

Assuming $D_{AB}$ constant:

$$
\frac{1}{r} \frac{d}{dr}
\left(
r \frac{d c_A}{d r}
\right)
- \frac{r_A}{D_{AB}} = 0
$$

For first-order consumption $r_A = -k c_A$:

$$
\frac{1}{r} \frac{d}{dr}
\left(
r \frac{d c_A}{d r}
\right)
- \frac{k}{D_{AB}} c_A
= 0
$$

---

## 4. Shell Balances in Spherical Coordinates

Coordinates: $(r,\theta,\phi)$.

### 4.1. Continuity Equation (Incompressible)

In full generality:

$$
\frac{1}{r^2} \frac{\partial}{\partial r}(r^2 v_r)
+ \frac{1}{r \sin\theta} \frac{\partial}{\partial \theta}(v_\theta \sin\theta)
+ \frac{1}{r \sin\theta} \frac{\partial v_\phi}{\partial \phi}
= 0
$$

For purely radial, spherically symmetric flow: $v_\theta = v_\phi = 0$, $v_r = v_r(r)$:

$$
\frac{1}{r^2} \frac{d}{dr}(r^2 v_r) = 0
$$

---

### 4.2. Species Balance: Spherical Symmetry

Assume $c_A = c_A(r)$, no convection:

- Radial flux:
  $$
  J_{A,r} = - D_{AB} \frac{d c_A}{d r}
  $$

Shell between $r$ and $r+dr$:

- Surface area at $r$: $4\pi r^2$
- In: $J_{A,r}(r) \cdot 4\pi r^2$
- Out: $J_{A,r}(r+dr) \cdot 4\pi (r+dr)^2$
- Generation: $r_A \cdot (4\pi r^2 dr)$

Steady state:

$$
0 =
J_{A,r}(r) 4\pi r^2
- J_{A,r}(r+dr) 4\pi (r+dr)^2
+ r_A 4\pi r^2 dr
$$

Divide by $4\pi$ and take $dr \to 0$:

$$
\frac{d}{dr}
\left(
r^2 J_{A,r}
\right)
+ r^2 r_A
= 0
$$

Substitute $J_{A,r} = - D_{AB} \frac{d c_A}{d r}$:

$$
\frac{d}{dr}
\left(
- r^2 D_{AB} \frac{d c_A}{d r}
\right)
+ r^2 r_A
= 0
$$

Assuming constant $D_{AB}$:

$$
\frac{1}{r^2} \frac{d}{dr}
\left(
r^2 \frac{d c_A}{d r}
\right)
- \frac{r_A}{D_{AB}}
= 0
$$

For first-order reaction $r_A = -k c_A$:

$$
\frac{1}{r^2} \frac{d}{dr}
\left(
r^2 \frac{d c_A}{d r}
\right)
- \frac{k}{D_{AB}} c_A
= 0
$$

---

## 5. Common Starting Forms (Rectangular / Cylindrical / Spherical)

These are the **standard Laplacian and divergence** forms used when writing shell balances.

### 5.1. Rectangular (Cartesian) Coordinates

Gradient:
$$
\nabla \phi
=
\hat{i} \frac{\partial \phi}{\partial x}
+ \hat{j} \frac{\partial \phi}{\partial y}
+ \hat{k} \frac{\partial \phi}{\partial z}
$$

Divergence:
$$
\nabla \cdot \mathbf{J}
=
\frac{\partial J_x}{\partial x}
+ \frac{\partial J_y}{\partial y}
+ \frac{\partial J_z}{\partial z}
$$

Laplacian:
$$
\nabla^2 \phi
=
\frac{\partial^2 \phi}{\partial x^2}
+ \frac{\partial^2 \phi}{\partial y^2}
+ \frac{\partial^2 \phi}{\partial z^2}
$$

---

### 5.2. Cylindrical Coordinates $(r,\theta,z)$

Gradient of scalar $\phi$:
$$
\nabla \phi
=
\hat{e}_r \frac{\partial \phi}{\partial r}
+ \hat{e}_\theta \frac{1}{r} \frac{\partial \phi}{\partial \theta}
+ \hat{e}_z \frac{\partial \phi}{\partial z}
$$

Divergence of vector $\mathbf{J} = (J_r, J_\theta, J_z)$:
$$
\nabla \cdot \mathbf{J}
=
\frac{1}{r} \frac{\partial}{\partial r}(r J_r)
+ \frac{1}{r} \frac{\partial J_\theta}{\partial \theta}
+ \frac{\partial J_z}{\partial z}
$$

Laplacian of scalar $\phi$:
$$
\nabla^2 \phi
=
\frac{1}{r} \frac{\partial}{\partial r}
\left(
r \frac{\partial \phi}{\partial r}
\right)
+ \frac{1}{r^2} \frac{\partial^2 \phi}{\partial \theta^2}
+ \frac{\partial^2 \phi}{\partial z^2}
$$

For axisymmetric, fully developed 1D radial problems ($\partial/\partial \theta = 0$, $\partial/\partial z = 0$):

$$
\nabla^2 \phi
=
\frac{1}{r} \frac{d}{dr}
\left(
r \frac{d \phi}{d r}
\right)
$$

---

### 5.3. Spherical Coordinates $(r,\theta,\phi)$

Gradient:
$$
\nabla \phi
=
\hat{e}_r \frac{\partial \phi}{\partial r}
+ \hat{e}_\theta \frac{1}{r} \frac{\partial \phi}{\partial \theta}
+ \hat{e}_\phi \frac{1}{r \sin\theta} \frac{\partial \phi}{\partial \phi}
$$

Divergence:
$$
\nabla \cdot \mathbf{J}
=
\frac{1}{r^2} \frac{\partial}{\partial r}(r^2 J_r)
+ \frac{1}{r \sin\theta} \frac{\partial}{\partial \theta}(J_\theta \sin\theta)
+ \frac{1}{r \sin\theta} \frac{\partial J_\phi}{\partial \phi}
$$

Laplacian of scalar $\phi$:
$$
\nabla^2 \phi
=
\frac{1}{r^2} \frac{\partial}{\partial r}
\left(
r^2 \frac{\partial \phi}{\partial r}
\right)
+ \frac{1}{r^2 \sin\theta} \frac{\partial}{\partial \theta}
\left(
\sin\theta \frac{\partial \phi}{\partial \theta}
\right)
+ \frac{1}{r^2 \sin^2\theta} \frac{\partial^2 \phi}{\partial \phi^2}
$$

For spherically symmetric 1D problems ($\partial/\partial \theta = 0$, $\partial/\partial \phi = 0$):

$$
\nabla^2 \phi
=
\frac{1}{r^2} \frac{d}{dr}
\left(
r^2 \frac{d \phi}{d r}
\right)
$$

---

## 6. Typical “Shell Balance” Templates

You can think in this generic pattern for any coordinate system:

- Accumulation in shell:
  $$
  \frac{\partial (\text{quantity})}{\partial t} \times (\text{shell volume})
  $$
- Influx through faces − outflux through faces, expressed using:
  - Rectangular: $\partial/\partial x, \partial/\partial y, \partial/\partial z$
  - Cylindrical: $1/r \, \partial/\partial r (r \cdot)$, etc.
  - Spherical: $1/r^2 \, \partial/\partial r (r^2 \cdot)$
- Plus any volumetric source term.

Then divide by shell volume and take limit to get the differential equation.

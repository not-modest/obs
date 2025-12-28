---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-fick-s-2nd-law/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

#2021_Jan 

Fick’s second law describes **time-dependent diffusion**, relating how concentration changes in time due to spatial gradients.

---

## 1. Starting Point: Conservation of Species

Consider 1D diffusion of species A in $x$ (no reaction, no convection).  
Take a differential slab between $x$ and $x+dx$.

- Accumulation in slab:
  $$
  \text{Accumulation} =
  \frac{\partial C_A}{\partial t}\,dx
  $$
- Net flux in − out:
  $$
  \text{Net in} =
  J_A(x)\, -\, J_A(x+dx)
  $$

Conservation (no generation/consumption):
$$
\text{Accumulation} = \text{Net in}
$$

So:
$$
\frac{\partial C_A}{\partial t}\,dx =
J_A(x) - J_A(x+dx)
$$

Expand $J_A(x+dx)$ in Taylor series:
$$
J_A(x+dx) \approx J_A(x) + \frac{\partial J_A}{\partial x} dx
$$

Then:
$$
J_A(x) - J_A(x+dx)
\approx
J_A(x) - \left[
J_A(x) + \frac{\partial J_A}{\partial x} dx
\right]
= -\frac{\partial J_A}{\partial x} dx
$$

Thus:
$$
\frac{\partial C_A}{\partial t}\,dx
=
- \frac{\partial J_A}{\partial x} dx
$$

Divide by $dx$:
$$
\frac{\partial C_A}{\partial t}
=
- \frac{\partial J_A}{\partial x}
$$

This is the **unsteady species balance** in 1D.

---

## 2. Constitutive Relation: Fick’s First Law

Fick’s first law (1D) for diffusion in $x$:

$$
J_A = - D_{AB} \frac{\partial C_A}{\partial x}
$$

- $D_{AB}$ = diffusion coefficient (assume constant in space and time).

---

## 3. Deriving Fick’s Second Law (1D)

Substitute $J_A$ into the species balance:

$$
\frac{\partial C_A}{\partial t}
=
- \frac{\partial}{\partial x}
\left(
- D_{AB} \frac{\partial C_A}{\partial x}
\right)
$$

With constant $D_{AB}$:

$$
\frac{\partial C_A}{\partial t}
=
D_{AB} \frac{\partial^2 C_A}{\partial x^2}
$$

This is **Fick’s second law in 1D**.

---

## 4. General 3D Form

For 3D diffusion with position vector $\mathbf{r}$:

- Fick’s first law (vector form):
  $$
  \mathbf{J}_A = - D_{AB} \nabla C_A
  $$

- Species balance:
  $$
  \frac{\partial C_A}{\partial t}
  = - \nabla \cdot \mathbf{J}_A
  $$

Combine:
$$
\frac{\partial C_A}{\partial t}
=
- \nabla \cdot (- D_{AB} \nabla C_A)
= D_{AB} \nabla^2 C_A
$$

So the **general Fick’s second law** (constant $D_{AB}$):

$$
\frac{\partial C_A}{\partial t}
=
D_{AB} \nabla^2 C_A
$$

- $\nabla^2$ is the Laplacian operator (sum of second derivatives in space).

---

## 5. With Reaction or Source Term

If there is a volumetric reaction rate $r_A$ (positive for generation, negative for consumption):

Species balance becomes:
$$
\frac{\partial C_A}{\partial t}
= - \nabla \cdot \mathbf{J}_A + r_A
$$

With Fick’s law:
$$
\frac{\partial C_A}{\partial t}
=
D_{AB} \nabla^2 C_A + r_A
$$

Example in 1D:
$$
\frac{\partial C_A}{\partial t}
=
D_{AB} \frac{\partial^2 C_A}{\partial x^2}
+ r_A(x,t)
$$

---

## 6. Physical Interpretation

- Left-hand side: **time rate of change** of concentration.  
- Right-hand side: **spatial curvature** of concentration (scaled by $D$), plus any source/sink.

Regions where $C_A$ is “curved” (nonlinear vs $x$) drive diffusion; $D_{AB}$ sets how fast these gradients relax. Over time, Fick’s second law tends to **smooth out concentration gradients**.

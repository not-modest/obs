---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-maxwell-stefan-and-driving-force/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

#2024_Jan [[quals-prep/transport/Trans_04_Mass_Transfer\|Trans_04_Mass_Transfer]]
Maxwell–Stefan equations describe multicomponent diffusion by balancing driving forces (chemical potential gradients) against frictional interactions between pairs of species.

---

## Maxwell–Stefan Equation (General Form)

For an $n$-component mixture, the Maxwell–Stefan equation for species $i$ is:
$$
-\nabla \mu_i = \sum_{j \ne i} \frac{\mu_i - \mu_j}{\tilde{D}_{ij}} ( \mathbf{v}_i - \mathbf{v}_j )
$$
More commonly in engineering form, using mole fractions and fluxes, one writes (for isothermal, isobaric conditions):
$$
-\,\frac{x_i}{RT}\,\nabla \mu_i
=
\sum_{j \ne i}
\frac{x_i x_j}{\mathcal{D}_{ij}} \left( \mathbf{u}_i - \mathbf{u}_j \right)
$$
where:
- $x_i$ = mole fraction of species $i$  
- $\mu_i$ = chemical potential of species $i$  
- $\mathbf{u}_i$ = diffusion velocity of species $i$ (relative to a reference frame)  
- $\mathcal{D}_{ij}$ = Maxwell–Stefan diffusivity between $i$ and $j$ (symmetric in $i,j$)  
- $R$ = gas constant, $T$ = temperature  

Left side: **driving force** per mole of species $i$ (chemical potential gradient).  
Right side: sum of **friction forces** between $i$ and all other species $j$.

---

## Driving Force: Chemical Potential vs Concentration

The true thermodynamic driving force is the **gradient of chemical potential**:
$$
-\nabla \mu_i
$$

For an ideal gas mixture:
$$
\mu_i = \mu_i^\circ(T) + RT \ln x_i
\quad \Rightarrow \quad
\nabla \mu_i = RT \nabla \ln x_i
$$

For non-ideal mixtures (with activity $a_i = \gamma_i x_i$):
$$
\mu_i = \mu_i^\circ(T) + RT \ln a_i
= \mu_i^\circ(T) + RT \ln(\gamma_i x_i)
$$
so:
$$
\nabla \mu_i = RT \nabla \ln(\gamma_i x_i)
= RT \left( \nabla \ln x_i + \nabla \ln \gamma_i \right)
$$

Thus the driving force includes both **composition gradients** and **non-ideality (activity coefficient) gradients**, as well as possible $T$ or $p$ variations if not constant.

---

## Maxwell–Stefan in Terms of Fluxes

Define:
- Total molar flux:
  $$
  \mathbf{N}_i = c x_i \mathbf{u}_i
  $$
  where $c$ is total molar concentration.
- In a frame where the molar-average velocity is zero (no net diffusion of the mixture), one often rewrites Maxwell–Stefan as:
  $$
  -\,\frac{x_i}{RT}\,\nabla \mu_i
  =
  \sum_{j \ne i}
  \frac{x_j}{c\,\mathcal{D}_{ij}}
  \left(\mathbf{N}_i - \mathbf{N}_j\right)
  $$

For a **binary mixture** (1–2, isothermal, isobaric, ideal), this reduces to:
$$
-\,\frac{x_1}{RT}\,\nabla \mu_1
=
\frac{x_1 x_2}{\mathcal{D}_{12}}(\mathbf{u}_1 - \mathbf{u}_2)
$$
and since:
$$
\nabla \mu_1 = RT \nabla \ln x_1
$$
you get:
$$
-\,x_1 \nabla \ln x_1
=
\frac{x_1 x_2}{\mathcal{D}_{12}}(\mathbf{u}_1 - \mathbf{u}_2)
$$

This can be rearranged to produce a **Fick-like** form for binary diffusion, showing how Fick’s law emerges as a special case.

---

## Relation to Fick’s Law (Binary Ideal Case)

For a binary ideal mixture, isothermal, isobaric, and with the molar-average velocity as reference, the Maxwell–Stefan equation reduces to Fick’s law:
$$
\mathbf{N}_1 = -c D_{12}\,\nabla x_1
$$
with an effective Fick diffusivity $D_{12}$ related to the Maxwell–Stefan diffusivity $\mathcal{D}_{12}$.  

Key point:  
- **Fick’s law** uses concentration (or mole fraction) gradient as *apparent* driving force.  
- **Maxwell–Stefan** uses chemical potential gradients and is strictly valid for **multicomponent, non-ideal** systems.

---

## Multicomponent Coupling

In mixtures with more than two species:

- Each species’ flux **depends on gradients of all species**.  
- Cross-diffusion effects appear: a gradient in species $j$ can drive flux of species $i$ (even if $\nabla x_i = 0$).  

Mathematically:

- One obtains a **matrix system**:
  $$
  \mathbf{B} \cdot \mathbf{N} = -\mathbf{C}\,\nabla \boldsymbol{\mu}
  $$
  where $\mathbf{B}$ involves the Maxwell–Stefan diffusivities $\mathcal{D}_{ij}$, and $\mathbf{C}$ involves compositions and total concentration.

This coupling is crucial for accurate modeling of diffusion in:
- Multicomponent gas mixtures  
- Non-dilute liquid mixtures  
- Membranes, porous media, and reacting systems with strong composition gradients.

---

## Driving Forces in Other Practical Forms

For engineering use (especially in gas mixtures), one often expresses driving forces in terms of other variables:

- **Partial pressure gradients** (ideal gases):
  $$
  -\nabla \mu_i \sim -RT \nabla \ln p_i
  $$
- **Activity gradients** in liquid mixtures:
  $$
  -\nabla \mu_i \sim -RT \nabla \ln a_i
  $$
- In thermodynamic driving-force form:
  $$
  \text{Driving force} \sim -\nabla \left(\frac{\mu_i}{RT}\right)
  $$

The Maxwell–Stefan framework is flexible: one chooses the most convenient thermodynamic variable (activity, partial pressure, fugacity) as long as its relationship to $\mu_i$ is known.

---

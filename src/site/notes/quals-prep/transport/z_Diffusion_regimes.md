---
{"dg-publish":true,"permalink":"/quals-prep/transport/z-diffusion-regimes/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

# Diffusion Regimes
![../src/Pasted image 20251226125548.png|600](/img/user/quals-prep/src/Pasted%20image%2020251226125548.png)

Diffusion describes transport driven by random molecular motion and gradients in chemical potential or concentration. Different **regimes** are identified based on geometry, time scales, and interactions.

---
## Random Walk Theory of Diffusion

Diffusion can be viewed as a **random walk** of particles (Brownian motion). This leads to the Einstein relation for the diffusion coefficient.

### Simple 1D random walk

Consider:

- Particle takes steps of length $\ell$.
- At each time interval $\Delta t$, it moves either $+ \ell$ or $- \ell$ with equal probability $1/2$.
- After $N$ steps, total time:
  $$
  t = N \Delta t
  $$

Position after $N$ steps:
$$
x_N = \ell \sum_{k=1}^{N} s_k
$$
where each $s_k$ is +1 or −1 with probability 1/2.

Mean:
$$
\langle x_N \rangle = 0
$$

Mean-square displacement:
$$
\langle x_N^2 \rangle
=
\ell^2 \left\langle \left( \sum_{k=1}^{N} s_k \right)^2 \right\rangle
=
\ell^2 N
$$

Since $N = t / \Delta t$:
$$
\langle x^2 \rangle = \ell^2 \frac{t}{\Delta t}
$$

Compare with Fickian diffusion result in 1D:
$$
\langle x^2 \rangle = 2 D t
$$

Thus:
$$
D = \frac{\ell^2}{2 \Delta t}
$$

This is the **random-walk expression** for the diffusion coefficient in 1D.

### Extension to 3D

In three dimensions, for isotropic random walk:

$$
\langle r^2 \rangle = 6 D t
$$

So:
$$
D = \frac{\ell^2}{6 \Delta t}
$$

where $r^2 = x^2 + y^2 + z^2$.

### Einstein relation (Brownian particle in fluid)

For a spherical Brownian particle (radius $a$) in a fluid with viscosity $\mu$ at temperature $T$, the diffusion coefficient is given by the **Einstein–Stokes relation**:

$$
D = \frac{k_B T}{6 \pi \mu a}
$$

- $k_B$ = Boltzmann constant.

This links macroscopic diffusion coefficient $D$ to microscopic friction coefficient (hydrodynamic drag) and thermal energy.

## Diffusion Regimes 

### Bulk diffusion

- Random molecular motion dominates.
- Mean-square displacement proportional to time:
  $$
  \langle x^2 \rangle = 2 D t \quad (1\text{D})
  $$
- Flux given by Fick’s law.

### Knudsen diffusion

Occurs in narrow pores where:
$$
\lambda \gtrsim d_{\text{pore}}
$$
($\lambda$ = mean free path, $d_{\text{pore}}$ = pore diameter)

- Molecule–wall collisions dominate over molecule–molecule collisions.
- Effective Knudsen diffusivity (for gas species $i$):
  $$
  D_{K,i} = \frac{2}{3} r_p \sqrt{\frac{8 R T}{\pi M_i}}
  $$
  where $r_p$ is pore radius, $M_i$ molar mass.

### Transition / combined regimes

When both molecular and Knudsen diffusion are significant:

- Use **series resistance** form for effective diffusivity:
  $$
  \frac{1}{D_{\text{eff}}}
  =
  \frac{1}{D_{AB}} + \frac{1}{D_K}
  $$

### Effective diffusion in porous media

Porous medium with porosity $\varepsilon$ and tortuosity $\tau$:

$$
D_{\text{eff}} = \frac{\varepsilon}{\tau} D
$$

- $D$ is either molecular, Knudsen, or combined diffusion coefficient.

---



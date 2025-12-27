---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/z-leonard-jones-potential/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

#2021_Jan 
# Lennard–Jones Potential (LJ Potential)

The Lennard–Jones potential is a simple pairwise model for intermolecular interactions, capturing **short-range repulsion** and **long-range attraction** between neutral atoms/molecules.

---

## 1. Functional Form

For two particles separated by distance $r$:

$$
U(r) = 4\varepsilon \left[ \left( \frac{\sigma}{r} \right)^{12}
- \left( \frac{\sigma}{r} \right)^{6} \right]
$$

- $\varepsilon$: depth of the potential well (interaction strength).  
- $\sigma$: distance where $U(r) = 0$ (effective size parameter).  

As $r \to \infty$, $U(r) \to 0$ (no interaction).

![../src/Pasted image 20251226224416.png](/img/user/quals-prep/src/Pasted%20image%2020251226224416.png)
---

## 2. Physical Interpretation

- Repulsive term:
  $$
  U_{\text{rep}}(r) = 4\varepsilon \left( \frac{\sigma}{r} \right)^{12}
  $$
  Dominates at very short distances (overlap of electron clouds).

- Attractive term (dispersion / van der Waals):
  $$
  U_{\text{att}}(r) = -4\varepsilon \left( \frac{\sigma}{r} \right)^{6}
  $$
  Dominates at intermediate distances.

Total $U(r)$ has a minimum at some $r = r_{\text{min}}$ where attraction and repulsion balance.

---

## 3. Location and Value of the Minimum

Set derivative to zero:

$$
\frac{dU}{dr} = 0
$$

Compute derivative:

$$
\frac{dU}{dr}
=
4\varepsilon
\left[
-12 \frac{\sigma^{12}}{r^{13}}
+ 6 \frac{\sigma^6}{r^7}
\right]
=
\frac{24\varepsilon \sigma^6}{r^{13}}
\left(
-2 \sigma^6 + r^6
\right)
$$

Set bracket term zero:

$$
-2 \sigma^6 + r^6 = 0
\quad\Rightarrow\quad
r^6 = 2 \sigma^6
\quad\Rightarrow\quad
r_{\text{min}} = 2^{1/6} \sigma
$$

Value at minimum:

$$
U(r_{\text{min}})
=
4\varepsilon \left[ \left( \frac{\sigma}{2^{1/6}\sigma} \right)^{12}
- \left( \frac{\sigma}{2^{1/6}\sigma} \right)^{6} \right]
=
4\varepsilon \left[ \left(2^{-1/6}\right)^{12} - \left(2^{-1/6}\right)^{6} \right]
$$

Note:
$$
(2^{-1/6})^{6} = 2^{-1}, \quad (2^{-1/6})^{12} = 2^{-2}
$$

So:
$$
U(r_{\text{min}})
=
4\varepsilon \left( 2^{-2} - 2^{-1} \right)
=
4\varepsilon \left( \frac{1}{4} - \frac{1}{2} \right)
=
4\varepsilon \left( -\frac{1}{4} \right)
= -\varepsilon
$$

So:
- Minimum at $r_{\text{min}} = 2^{1/6}\sigma$  
- $U(r_{\text{min}}) = -\varepsilon$

---

## 4. Force Between Particles

Force is minus gradient of potential:

$$
F(r) = -\frac{dU}{dr}
$$

From derivative above:

$$
F(r)
=
-4\varepsilon
\left[
-12 \frac{\sigma^{12}}{r^{13}}
+ 6 \frac{\sigma^6}{r^7}
\right]
=
4\varepsilon
\left[
12 \frac{\sigma^{12}}{r^{13}}
- 6 \frac{\sigma^6}{r^7}
\right]
$$

Factor:
$$
F(r)
=
\frac{24\varepsilon}{r}
\left[
2 \left( \frac{\sigma}{r} \right)^{12}
-
\left( \frac{\sigma}{r} \right)^6
\right]
$$

- $F(r) > 0$: repulsive (pushing apart).  
- $F(r) < 0$: attractive (pulling together).  

At $r = r_{\text{min}}$, $F(r) = 0$ (equilibrium separation).

---

## 5. Reduced (Dimensionless) Form

Define reduced variables:

$$
r^* = \frac{r}{\sigma}, \quad
U^* = \frac{U}{\varepsilon}
$$

Then:

$$
U^*(r^*)
=
4\left[ \frac{1}{(r^*)^{12}} - \frac{1}{(r^*)^{6}} \right]
$$

Minimum at $r^* = 2^{1/6}$ with $U^* = -1$.

This nondimensional form is widely used in simulations/figures.

---

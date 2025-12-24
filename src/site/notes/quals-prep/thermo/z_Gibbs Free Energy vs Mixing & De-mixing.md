---
{"dg-publish":true,"permalink":"/quals-prep/thermo/z-gibbs-free-energy-vs-mixing-and-de-mixing/","dgShowToc":true}
---

#2025_Jan [[quals-prep/thermo/Thermo_05_Mixtures_and_Solutions\|Thermo_05_Mixtures_and_Solutions]]

For a binary mixture (components A and B), mixing or de-mixing is governed by the molar Gibbs free energy $G$ as a function of composition $x_B$ at fixed $T,P$. The system adopts the state (single phase or two phases) that minimizes $G$.

---

## Gibbs Free Energy of Mixing

Change in molar Gibbs free energy on mixing:
$$
\Delta G_{\text{mix}} = \Delta H_{\text{mix}} - T\,\Delta S_{\text{mix}}
$$

For an ideal solution (no enthalpy of mixing, $\Delta H_{\text{mix}} = 0$):
$$
\Delta G_{\text{mix}}^{\text{ideal}} = RT\left[x_A \ln x_A + x_B \ln x_B\right]
$$
with $x_A + x_B = 1$. This is always negative, so the mixture is fully miscible.

Total molar Gibbs free energy of the mixed phase:
$$
G(x_B) = x_A G_A^0 + x_B G_B^0 + \Delta G_{\text{mix}}(x_B)
$$
where $G_A^0, G_B^0$ are molar Gibbs free energies of pure A and B.

---

## Regular Solution Model (Non-ideal Mixing)

For non-ideal mixing, introduce an interaction parameter $\Omega$ (regular solution theory):
$$
\Delta G_{\text{mix}} = RT\left[x_A \ln x_A + x_B \ln x_B\right] + \Omega x_A x_B
$$

- $\Omega > 0$: unfavorable A–B interactions → tendency to de-mix.  
- $\Omega < 0$: favorable A–B interactions → strong mixing.

At high $T$ (or small $\Omega/RT$), $\Delta G_{\text{mix}}$ has a single minimum → stable, homogeneous mixture. At low $T$ (large $\Omega/RT$), $\Delta G_{\text{mix}}(x_B)$ can develop a **double-well** shape → phase separation possible.

---

## Mixing vs De-mixing Criterion (Common Tangent)

Graphically, plot $G(x_B)$ vs $x_B$ at fixed $T,P$:

- **Stable single phase**: Curve has one minimum; no straight line between two compositions lies below the curve.  
- **Phase separation**: If a straight line (common tangent) touches $G(x_B)$ at two compositions $x_1$ and $x_2$ and lies below $G(x_B)$ everywhere between them, then the system lowers its Gibbs free energy by splitting into two phases with compositions $x_1$ and $x_2$.

Mathematically, for coexisting phases at $x_1$ and $x_2$:
$$
\left.\frac{\partial G}{\partial x_B}\right|_{x_1}
=
\left.\frac{\partial G}{\partial x_B}\right|_{x_2}
=
\frac{G(x_2) - G(x_1)}{x_2 - x_1}
$$
which expresses equality of chemical potentials (common tangent construction).
![../src/Pasted image 20251223145607.png](/img/user/quals-prep/src/Pasted%20image%2020251223145607.png)

---


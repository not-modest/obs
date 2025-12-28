---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/z-packed-bed-reactors/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

# Key Concepts and Equations

Packed-bed reactors are fixed beds of solid particles (often catalysts) through which fluid reactants flow. They are widely used in heterogeneous catalysis and adsorption.

---

## 1. Basic Structure and Assumptions

- Cylindrical column packed with particles (catalyst pellets, adsorbent, inert packing).  
- Fluid phase (gas, liquid, or two-phase) flows through void spaces.  
- Common assumptions for modeling:
  - Steady state.
  - 1D plug flow in axial direction (no radial gradients).
  - Constant temperature (or specified $T(z)$ profile).
  - Constant pressure or known $p(z)$ from Ergun equation.
  - Negligible axial dispersion (for ideal plug-flow model).

Bed void fraction:
$$
\varepsilon_b = \frac{V_{\text{void}}}{V_{\text{bed}}}
$$

Superficial velocity:
$$
u_s = \frac{Q}{A}
$$

Interstitial (pore) velocity:
$$
u_{\text{int}} = \frac{u_s}{\varepsilon_b}
$$

---

## 2. Mole Balance for a Species (Plug-Flow Form)

Consider species A, stoichiometric coefficient $\nu_A$ in reaction. Let:

- $F_A(z)$ = molar flow of A [mol/s] at axial position $z$.  
- $r_A'$ = reaction rate per catalyst volume [mol/(m³ of catalyst·s)].  

For a differential bed element of volume $dV$:

**Differential mole balance:**
$$
\frac{dF_A}{dV} = r_A'
$$

If the reaction rate is expressed per mass of catalyst $r_A$ [mol/(kg·s)], with bulk catalyst density $\rho_{cat}$:

$$
r_A' = \rho_{cat} r_A
$$

Then:
$$
\frac{dF_A}{dV} = \rho_{cat} r_A
$$

Relate $V$ to axial coordinate $z$:
$$
V = (1 - \varepsilon_b) A z
\quad \Rightarrow \quad
\frac{dV}{dz} = (1 - \varepsilon_b) A
$$

So:
$$
\frac{dF_A}{dz}
=
(1 - \varepsilon_b) A \rho_{cat} r_A
$$

If $r_A$ depends on fluid-phase concentration $C_A$:
$$
F_A = C_A u_s A
\quad \Rightarrow \quad
C_A = \frac{F_A}{u_s A}
$$

and $r_A = r_A(C_A, T, \dots)$.

---

## 3. Isothermal PBR with First-Order Reaction

Example: $A \to \text{products}$, rate:
$$
r_A = -k C_A
$$

Mole balance:
$$
\frac{dF_A}{dV} = \rho_{cat} (-k C_A)
$$

Using $F_A = C_A u_s A$,
$$
C_A = \frac{F_A}{u_s A}
$$

Thus:
$$
\frac{dF_A}{dV}
=
-\rho_{cat} k \,\frac{F_A}{u_s A}
$$

Rearrange:
$$
\frac{dF_A}{F_A}
=
-\frac{\rho_{cat} k}{u_s A} \, dV
$$

Integrate from inlet ($F_{A0}$ at $V=0$) to $F_A$ at $V$:
$$
\ln\left(\frac{F_A}{F_{A0}}\right)
=
-\frac{\rho_{cat} k}{u_s A} V
$$

Define **space time**:
$$
\tau = \frac{V}{u_s A}
$$

Then:
$$
\frac{F_A}{F_{A0}}
=
\exp(-\rho_{cat} k \tau)
$$

Conversion of A:
$$
X_A = 1 - \frac{F_A}{F_{A0}} = 1 - \exp(-\rho_{cat} k \tau)
$$

---

## 4. Pressure Drop – Ergun Equation Coupling

For gas-phase reactions, pressure drop along the bed is often significant and affects concentration via $C_A = y_A p / (RT)$.

Ergun equation:
$$
\frac{dp}{dz}
=
-\left[
\frac{150\,\mu\,(1-\varepsilon_b)^2}{d_p^2\,\varepsilon_b^3} u_s
+
\frac{1.75\,\rho\,(1-\varepsilon_b)}{d_p\,\varepsilon_b^3} u_s^2
\right]
$$

- $d_p$ = particle diameter  
- $\rho$ = fluid density  
- $\mu$ = viscosity  

Coupled PBR model typically solves:

- Mole balance: $\dfrac{dF_A}{dz} = (1-\varepsilon_b) A \rho_{cat} r_A$  
- Energy balance (if non-isothermal)  
- Ergun (momentum balance): $\dfrac{dp}{dz} = \dots$

---

## 5. Internal Diffusion and Effectiveness Factor

When reaction occurs inside porous catalyst pellets, internal diffusion can limit rate. Intrinsic rate per catalyst volume $r_{A,\,int}$ is reduced to an **observed rate** $r_A'$:

$$
r_A' = \eta r_{A,\,int}
$$

- $\eta$ = **effectiveness factor** $0 < \eta \le 1$  
- Often function of **Thiele modulus** $\phi$:
  $$
  \phi^2 = \frac{k L_p^2}{D_{eff}}
  $$
  where $L_p$ is characteristic pellet length (e.g., radius), $D_{eff}$ effective diffusivity.

In the PBR mole balance, use:
$$
r_A = r_A' = \eta r_{A,\,int}
$$

---

## 6. External Mass Transfer Limitations

If gas–solid reaction requires transport from bulk fluid to pellet surface:

- External mass-transfer coefficient $k_g$  
- External resistance can be important at high reaction rates.

Flux at pellet surface:
$$
N_A = k_g (C_{A,bulk} - C_{A,s})
$$

At pseudo steady state (surface equals consumption inside pellet),

- Solve external + internal resistances to express overall rate as function of bulk $C_A$.  
- Then plug effective $r_A$ into PBR balance.

---

## 7. Summary of Key Relations

**Geometry & Flow**
- Bed volume: 
  $$
  V = (1 - \varepsilon_b) A L
  $$
- Superficial velocity: 
  $$
  u_s = \frac{Q}{A}
  $$
- Interstitial velocity:
  $$
  u_{\text{int}} = \frac{u_s}{\varepsilon_b}
  $$

**Mole balance (general PFR/PBR form)**
- In terms of $V$:
  $$
  \frac{dF_A}{dV} = r_A'
  $$
- In terms of $z$:
  $$ 
  \frac{dF_A}{dz} = (1 - \varepsilon_b) A \rho_{cat} r_A
  $$

**Ideal gas concentration**
$$
C_A = \frac{y_A p}{RT}
$$

**Ergun pressure drop**
$$
\frac{dp}{dz}
=
-\left[
\frac{150\,\mu\,(1-\varepsilon_b)^2}{d_p^2\,\varepsilon_b^3} u_s
+
\frac{1.75\,\rho\,(1-\varepsilon_b)}{d_p\,\varepsilon_b^3} u_s^2
\right]
$$

**Effectiveness factor**
$$
r_A = \eta r_{A,\,int}
$$

**Thiele modulus (example, 1st order)**
$$
\phi^2 = \frac{k L_p^2}{D_{eff}}
$$

This set gives you a compact PBR “toolbox” for modeling and quick reference in your notes.

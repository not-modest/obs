---
{"dg-publish":true,"permalink":"/quals-prep/thermo/z-maxwell-relations/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

# Maxwell Relations 

Maxwell relations are a set of **exact partial-derivative identities** that follow from the thermodynamic potentials. They connect **entropy** (hard to measure) with **P, V, T** (easy to measure), letting you rewrite ugly derivatives in terms of measurable quantities.

---

## 1. Thermodynamic Potentials and Natural Variables

Write the four main potentials in differential form:

- Internal energy:
  $$
  dU = T\,dS - P\,dV
  \quad\Rightarrow\quad U = U(S,V)
  $$
- Enthalpy:
  $$
  dH = T\,dS + V\,dP
  \quad\Rightarrow\quad H = H(S,P)
  $$
- Helmholtz free energy:
  $$
  dA = -S\,dT - P\,dV
  \quad\Rightarrow\quad A = A(T,V)
  $$
- Gibbs free energy:
  $$
  dG = -S\,dT + V\,dP
  \quad\Rightarrow\quad G = G(T,P)
  $$

From these, identify partial derivatives:
- $T = \left(\dfrac{\partial U}{\partial S}\right)_V$,   $-P = \left(\dfrac{\partial U}{\partial V}\right)_S$  
- $T = \left(\dfrac{\partial H}{\partial S}\right)_P$,   $V  = \left(\dfrac{\partial H}{\partial P}\right)_S$  
- $-S = \left(\dfrac{\partial A}{\partial T}\right)_V$,  $-P = \left(\dfrac{\partial A}{\partial V}\right)_T$  
- $-S = \left(\dfrac{\partial G}{\partial T}\right)_P$,  $V  = \left(\dfrac{\partial G}{\partial P}\right)_T$

---

## 2. Deriving a Maxwell Relation (Example)

Take internal energy $U(S,V)$:

Total differential in math form:
$$
dU = \left(\frac{\partial U}{\partial S}\right)_V dS +
      \left(\frac{\partial U}{\partial V}\right)_S dV
$$

Compare with thermodynamic form:
$$
dU = T\,dS - P\,dV
$$

Thus:
$$
T = \left(\frac{\partial U}{\partial S}\right)_V,
\quad
-P = \left(\frac{\partial U}{\partial V}\right)_S
$$

Now use equality of mixed second derivatives (exact differential property):
$$
\frac{\partial}{\partial V}
\left(\frac{\partial U}{\partial S}\right)_V
=
\frac{\partial}{\partial S}
\left(\frac{\partial U}{\partial V}\right)_S
$$

Substitute $T$ and $-P$:

Left-hand side:
$$
\left(\frac{\partial T}{\partial V}\right)_S
$$

Right-hand side:
$$
\frac{\partial}{\partial S}(-P)\Big|_V
=
-\left(\frac{\partial P}{\partial S}\right)_V
$$

So the **first Maxwell relation** is:
$$
\boxed{
\left(\frac{\partial T}{\partial V}\right)_S
=
-\left(\frac{\partial P}{\partial S}\right)_V
}
$$

The other three follow analogously from $H$, $F$, and $G$.

---

## 3. The Four Common Maxwell Relations

Starting from the four potentials above:

1. From $U(S,V)$:
   $$
   \left(\frac{\partial T}{\partial V}\right)_S
   =
   -\left(\frac{\partial P}{\partial S}\right)_V
   $$

2. From $H(S,P)$:
   $$
   \left(\frac{\partial T}{\partial P}\right)_S
   =
   \left(\frac{\partial V}{\partial S}\right)_P
   $$

3. From $A(T,V)$:
   $$
   \left(\frac{\partial S}{\partial V}\right)_T
   =
   \left(\frac{\partial P}{\partial T}\right)_V
   $$

4. From $G(T,P)$:
   $$
   \left(\frac{\partial S}{\partial P}\right)_T
   =
   -\left(\frac{\partial V}{\partial T}\right)_P
   $$

These are the “standard” Maxwell relations; more exist if you include additional variables (e.g., composition, fields).

---

## 4. Why They Matter (Physical/Practical Meaning)

### 4.1 Entropy from measurable properties

Entropy is hard to measure directly. Maxwell relations allow replacing derivatives like
$$
\left(\frac{\partial S}{\partial P}\right)_T
$$
with ones in terms of **V, P, T** that are easier to measure:
$$
\left(\frac{\partial S}{\partial P}\right)_T
=
-\left(\frac{\partial V}{\partial T}\right)_P
$$

Example: change in entropy between $(T,P_1)$ and $(T,P_2)$ at fixed $T$:
$$
\Delta S_T
=
\int_{P_1}^{P_2}
\left(\frac{\partial S}{\partial P}\right)_T dP
=
- \int_{P_1}^{P_2}
\left(\frac{\partial V}{\partial T}\right)_P dP
$$

Right-hand side uses $V(T,P)$ data (equation of state / PVT measurements) instead of entropy.

### 4.2 Connecting response functions

Maxwell relations connect thermodynamic **response functions** (heat capacities, compressibility, expansivity, etc.). For example, starting from:
$$
\left(\frac{\partial S}{\partial V}\right)_T
=
\left(\frac{\partial P}{\partial T}\right)_V
$$
and identities like:
$$
C_V = T\left(\frac{\partial S}{\partial T}\right)_V
$$
you can derive relations between $C_P$, $C_V$, thermal expansion coefficient $\alpha$, and isothermal compressibility $\kappa_T$.

---

## 5. Conceptual Summary

- Mathematically: Maxwell relations are consequences of **exact differentials** and the symmetry of mixed partial derivatives of thermodynamic potentials.
- Physically: they are **bridges** that express difficult derivatives (especially entropy derivatives) in terms of **measurable quantities** (P, V, T).
- Practically: used to:
  - Derive new thermodynamic identities.  
  - Compute entropy/enthalpy changes from PVT data.  
  - Relate response functions and derive equations of state consequences.

They significantly reduce the “bookkeeping” of thermodynamics: once the potentials are known as functions of their natural variables, Maxwell relations provide a systematic way to extract all other properties.

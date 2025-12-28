---
{"dg-publish":true,"permalink":"/quals-prep/thermo/z-raoult-s-law/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

#2021_Jan [[quals-prep/thermo/Thermo_06_Phase_Equilibria_VLE\|Thermo_06_Phase_Equilibria_VLE]]
# Raoult’s Law 

Raoult’s law describes the vapor–liquid equilibrium (VLE) of **ideal solutions** by relating the partial pressure of each component in the vapor to its mole fraction in the liquid and its pure-component saturation pressure.

---

## 1. Basic Statement (Isothermal, Isobaric VLE)

For a component $i$ in an **ideal liquid solution** in equilibrium with an ideal vapor:
$$
p_i = x_i P_i^{\text{sat}}(T)
$$
where:
- $p_i$ = partial pressure of $i$ in the gas phase  
- $x_i$ = mole fraction of $i$ in the liquid phase  
- $P_i^{\text{sat}}(T)$ = saturation pressure of pure $i$ at temperature $T$  

Total pressure:
$$
P = \sum_i p_i = \sum_i x_i P_i^{\text{sat}}(T)
$$

Gas-phase mole fraction:
$$
y_i = \frac{p_i}{P}
= \frac{x_i P_i^{\text{sat}}(T)}{\sum_j x_j P_j^{\text{sat}}(T)}
$$

This gives the **$y$–$x$ relationship** used in binary VLE diagrams.

---

## 2. Chemical Potential Derivation

### 2.1. Gas phase (ideal)

For an ideal gas mixture:
$$
\mu_i^{(g)}(T,P,y_i)
=
\mu_i^{\circ (g)}(T,P^\circ)
+ RT \ln\left(\frac{y_i P}{P^\circ}\right)
$$
where $P^\circ$ is a reference pressure (often 1 bar or 1 atm).

### 2.2. Pure liquid at saturation

For pure liquid $i$ in equilibrium with its vapor at $P_i^{\text{sat}}(T)$:
$$
\mu_i^{(\ell,pure)}(T,P_i^{\text{sat}})
=
\mu_i^{\circ (g)}(T,P^\circ)
+ RT \ln\left(\frac{P_i^{\text{sat}}}{P^\circ}\right)
$$

By definition of saturation, $\mu_i^{(\ell,pure)} = \mu_i^{(g,pure)}$ at $P_i^{\text{sat}}$.

### 2.3. Ideal solution – liquid phase

For an **ideal solution**:
$$
\mu_i^{(\ell)}(T,P,x_i)
=
\mu_i^{(\ell,pure)}(T,P)
+ RT \ln x_i
$$
(Here, the activity $a_i = x_i$, and the activity coefficient $\gamma_i = 1$.)

### 2.4. Equating Chemical Potentials at VLE 

At VLE:
$$
\mu_i^{(\ell)}(T,P,x_i) = \mu_i^{(g)}(T,P,y_i)
$$

Liquid (ideal solution):
$$
\mu_i^{(\ell)} = \mu_i^{(\ell,pure)}(T,P) + RT \ln x_i
$$

Approximate pure-liquid chemical potential at system pressure by that at saturation (incompressible liquid, modest pressure range):
$$
\mu_i^{(\ell,pure)}(T,P) \approx \mu_i^{(\ell,pure)}(T,P_i^{\text{sat}})
$$

Gas (ideal mixture):
$$
\mu_i^{(g)} = \mu_i^{\circ (g)}(T,P^\circ) + RT \ln\!\left(\frac{y_i P}{P^\circ}\right)
$$

Pure-component saturation equilibrium:
$$
\mu_i^{(\ell,pure)}(T,P_i^{\text{sat}}) =
\mu_i^{\circ (g)}(T,P^\circ) + RT \ln\!\left(\frac{P_i^{\text{sat}}}{P^\circ}\right)
$$

Set liquid and gas chemical potentials equal:
$$
\mu_i^{(\ell,pure)}(T,P_i^{\text{sat}}) + RT \ln x_i
=
\mu_i^{\circ (g)}(T,P^\circ) + RT \ln\!\left(\frac{y_i P}{P^\circ}\right)
$$

Substitute the pure-liquid relation:
$$
\mu_i^{\circ (g)}(T,P^\circ) + RT \ln\!\left(\frac{P_i^{\text{sat}}}{P^\circ}\right)
+ RT \ln x_i
=
\mu_i^{\circ (g)}(T,P^\circ) + RT \ln\!\left(\frac{y_i P}{P^\circ}\right)
$$

Cancel $\mu_i^{\circ (g)}(T,P^\circ)$ and divide by $RT$:
$$
\ln\!\left(\frac{P_i^{\text{sat}}}{P^\circ}\right) + \ln x_i
=
\ln\!\left(\frac{y_i P}{P^\circ}\right)
$$

Combine logarithms:
$$
\ln\!\left(\frac{x_i P_i^{\text{sat}}}{P^\circ}\right)
=
\ln\!\left(\frac{y_i P}{P^\circ}\right)
$$

Exponentiate:
$$
\frac{x_i P_i^{\text{sat}}}{P^\circ}
=
\frac{y_i P}{P^\circ}
$$

So:
$$
y_i P = x_i P_i^{\text{sat}}
$$

i.e. Raoult’s law:
$$
p_i = y_i P = x_i P_i^{\text{sat}}(T)
$$


---

## 3. Activity and Non-Ideality (Raoult vs Modified Raoult)

For a **real liquid mixture**, define liquid-phase activity:
$$
a_i = \gamma_i x_i
$$
with activity coefficient $\gamma_i$.

A more general VLE relation is:
$$
y_i P \, \phi_i^{(g)} = a_i \, f_i^{\text{sat}}(T)
$$
where:
- $\phi_i^{(g)}$ = fugacity coefficient in gas  
- $f_i^{\text{sat}}$ = fugacity of pure saturated liquid  

Assuming ideal gas and $f_i^{\text{sat}} \approx P_i^{\text{sat}}$:
$$
y_i P = a_i P_i^{\text{sat}} = \gamma_i x_i P_i^{\text{sat}}
$$

So the **modified Raoult’s law** is:
$$
p_i = y_i P = \gamma_i x_i P_i^{\text{sat}}(T)
$$

- **Ideal solution**: $\gamma_i = 1$ → reduces to Raoult’s original law.  
- **Non-ideal solution**: $\gamma_i \neq 1$; deviations from Raoult’s law describe **positive or negative deviations** (leading to azeotropy, etc.).

---

## 4. Comparison with Henry’s Law (Solutes vs Solvents)

At low $x_i$ (dilute solute region) many systems follow **Henry’s law**:
$$
p_i = H_i x_i
$$
while at $x_i \to 1$ (solvent region) they follow **Raoult’s law**:
$$
p_i = x_i P_i^{\text{sat}}
$$

Thermodynamically:
- Henry’s law corresponds to using a **Henry standard state** for the solute at infinite dilution.  
- Raoult’s law corresponds to the **pure-liquid standard state** at $x_i \to 1$.  

For a component behaving ideally as both solute and solvent:
- $H_i \to P_i^{\text{sat}}$.

---

## 5. Temperature Dependence – Pure Component Saturation Pressure

The temperature dependence of $P_i^{\text{sat}}(T)$ is usually described by an Antoine or Clausius–Clapeyron relation.

**Antoine equation**:
$$
\log_{10} P_i^{\text{sat}}(T) = A_i - \frac{B_i}{T + C_i}
$$

**Clausius–Clapeyron (approximate)**:
$$
\ln P_i^{\text{sat}}(T) \approx -\frac{\Delta H_{\text{vap},i}}{R}\frac{1}{T} + \text{constant}
$$

Thus Raoult’s law inherits this **exponential temperature dependence** through $P_i^{\text{sat}}(T)$.

---

## 6. Binary VLE and y–x–P or y–x–T Relationships

For a binary mixture (1–2) at fixed $T$:

- Partial pressures:
  $$
  p_1 = x_1 P_1^{\text{sat}}(T), \quad
  p_2 = x_2 P_2^{\text{sat}}(T)
  $$
- Total pressure:
  $$
  P = x_1 P_1^{\text{sat}} + x_2 P_2^{\text{sat}}, \quad x_2 = 1 - x_1
  $$
- Vapor composition:
  $$
  y_1 = \frac{p_1}{P}
      = \frac{x_1 P_1^{\text{sat}}}{x_1 P_1^{\text{sat}} + (1 - x_1) P_2^{\text{sat}}}
  $$

At fixed $P$, one can solve for $T$ and $y_i$ as functions of $x_i$ by satisfying:
$$
P = \sum_i x_i P_i^{\text{sat}}(T)
$$

These relations generate:
- **Bubble-point curve**: $T$ vs $x$ (liquid composition where first bubble forms).  
- **Dew-point curve**: $T$ vs $y$ (vapor composition where first drop condenses).

---

## 7. Ideal Solution Criteria (When Raoult’s Law Holds)

A solution is **ideal** (and obeys Raoult’s law) when:

- Intermolecular interactions are similar:
  $$
  A\!-\!A \approx B\!-\!B \approx A\!-\!B
  $$
- Enthalpy of mixing is zero:
  $$
  \Delta H_{\text{mix}} = 0
  $$
- Volume of mixing is zero:
  $$
  \Delta V_{\text{mix}} = 0
  $$

Then the **excess Gibbs energy** $G^E$ is zero, and activity coefficients are unity:
$$
G^E = 0 \quad \Rightarrow \quad \gamma_i = 1
$$

Common near-ideal examples:
- Mixtures of chemically similar species (e.g., benzene–toluene, n-hexane–n-heptane).

---

## 8. Connection to Excess Functions and Azeotropy

When Raoult’s law fails (non-ideal solution), we introduce excess Gibbs energy $G^E$:

- $G^E \neq 0 \Rightarrow \gamma_i \neq 1$.
- Excess models (e.g., Margules, Wilson, NRTL, UNIQUAC) provide $\ln \gamma_i$ as a function of $x$ and $T$.

Then:
$$
p_i = \gamma_i x_i P_i^{\text{sat}}(T)
$$

Strong positive or negative deviations (large $\gamma_i$ or $\gamma_i < 1$) can cause **azeotropes**, where:
$$
x_i = y_i
$$
and bubble and dew curves meet. Pure Raoult’s law (ideal solution) **cannot** produce azeotropes.

---

## 9. Summary – Conceptual Hierarchy

1. **Most general**: equality of fugacities via chemical potentials:
   $$
   f_i^{(g)} = f_i^{(\ell)}
   $$
2. **Ideal gas, real liquid**:
   $$
   y_i P = a_i P_i^{\text{sat}} \quad (a_i = \gamma_i x_i)
   $$
3. **Ideal solution (Raoult’s law)**:
   $$
   y_i P = x_i P_i^{\text{sat}}(T)
   $$
4. **Dilute solute (Henry)**:
   $$
   y_i P = H_i x_i
   $$

Raoult’s law thus sits as the **ideal-solution limit** of a more general activity/fugacity-based VLE framework, with non-ideal behavior captured by activity coefficients and excess Gibbs energy models.

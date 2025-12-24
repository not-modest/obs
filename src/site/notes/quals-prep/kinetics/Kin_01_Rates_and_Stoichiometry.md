---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/kin-01-rates-and-stoichiometry/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Reaction rate, $r$**  
  Speed of reaction per unit volume (or per catalyst volume), based on a chosen reference species and sign convention.

- **Rate of reaction of species $i$, $r_i$**  
  Moles of $i$ produced per unit volume per unit time (negative for reactants).

- **Stoichiometric coefficients, $\nu_i$**  
  For reaction $\sum_i \nu_i A_i = 0$, reactants have $\nu_i < 0$, products $\nu_i > 0$.

- **Extent of reaction, $\xi$**  
  Amount of reaction that has occurred; links mole changes and stoichiometry:
  $$
  dN_i = \nu_i\, d\xi
  $$

- **Conversion of A, $X_A$**  
  Fraction of key reactant A that has reacted:
  $$
  X_A = \frac{N_{A0} - N_A}{N_{A0}}
  $$

- **Power‑law / empirical rate law**  
  Example for a single reaction:
  $$
  -r_A = k C_A^{\alpha} C_B^{\beta}
  $$
  where $\alpha,\beta$ are empirical reaction orders (not necessarily integers).

---

## Core formulas

### 1. Species rates and stoichiometry

For a single reaction with stoichiometric coefficients $\nu_i$ and scalar rate $r$:
$$
r_i = \nu_i\, r
$$

Example: $A + 2B \to 3C$  
- $\nu_A = -1$, $\nu_B = -2$, $\nu_C = +3$  
- If $r$ is defined based on $A$:
  $$
  r_A = -r,\quad r_B = -2r,\quad r_C = 3r
  $$

### 2. Conversion and flow rates

For steady flow with molar flow rates $F_i$:
$$
X_A = \frac{F_{A0} - F_A}{F_{A0}}
$$

For a single reaction and constant volumetric flow, concentrations relate to conversion via:
$$
C_A = C_{A0} (1 - X_A)
$$
(similar relations can be written for other species using stoichiometry).

### 3. Elementary vs non‑elementary

- **Elementary step**: rate law follows stoichiometry (e.g. unimolecular or bimolecular):
  - $A \to$ products: $-r_A = k C_A$  
  - $A + B \to$ products: $-r_A = k C_A C_B$  

- **Non‑elementary reaction**: observed rate law does not match stoichiometric exponents; requires mechanism or empirical fit.

---

## Interesting concepts

- **Choice of reference species**  
  Any species in the reaction can define the scalar rate $r$; all species rates are proportional via $\nu_i$. *Preferable to base the total reaction in terms of **limiting reactant** #2025_Jan 

- **Reaction order vs molecularity**  
  For elementary steps, order equals molecularity; for overall reactions or complex mechanisms, empirical orders can be fractional or non‑integer.

- **Extent of reaction as a global progress variable**  
  $\xi$ is the same for all species in a single reaction; it simplifies material balances and links directly to conversion.  
---


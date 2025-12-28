---
{"dg-publish":true,"permalink":"/quals-prep/thermo/thermo-04-properties-and-eos/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

## Key definitions

- **Equation of state (EOS)**  
  Relation between $P$, $V$ (or $v$), $T$, and composition (e.g. ideal gas, cubic EOS).

- **Ideal gas EOS**  
  $$
  PV = nRT,\quad Pv = RT
  $$

- **Compressibility factor, $Z$**  
  Measures non‑ideality:
  $$
  Z = \frac{PV}{nRT} = \frac{Pv}{RT}
  $$
  $Z = 1$ for ideal gas.

- **Residual properties**  
  Difference between real‑fluid property and ideal‑gas property at same $T$ and $P$ (e.g. $h^{R} = h - h^{\text{ig}}$).

---

## Core formulas

### 1. Cubic EOS (schematic)

Generic cubic form:
$$
P = \frac{RT}{v - b} - \frac{a}{v^2 + u b v + w b^2}
$$
(Specific forms: van der Waals, Redlich–Kwong, Peng–Robinson, etc.)

### 2. Compressibility factor from EOS

For given $T$ and $P$, solve EOS for $v$ or directly for $Z$:

- Ideal gas: $Z = 1$.  
- Real gas: $Z$ from cubic EOS or generalized $Z$ charts.

### 3. Enthalpy/entropy departures (concept level)

Property difference between real and ideal gas:
$$
M h(T,P) = M h^{\text{ig}}(T) + R T\, Z_h^{\text{dep}}(T,P)
$$
(similar for $s$). For most quals, know that charts/tables or EOS‑based correlations give these corrections.

---

## Interesting concepts

- **When ideal gas is acceptable**  
  Low pressure and moderate temperature (far from phase change) $\Rightarrow Z \approx 1$, use ideal gas EOS.

- **Using $Z$ charts**  
  Generalized compressibility charts collapse many gases onto the same curves when using reduced pressure and temperature.

- **Roots of cubic EOS**  
  Multiple real roots correspond to liquid‑ and vapor‑like volumes; phase stability and VLE calculations select appropriate root.

---


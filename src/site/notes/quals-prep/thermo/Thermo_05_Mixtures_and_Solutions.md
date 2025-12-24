---
{"dg-publish":true,"permalink":"/quals-prep/thermo/thermo-05-mixtures-and-solutions/"}
---

## Key definitions

- **Mole fraction, $x_i$ (liquid), $y_i$ (vapor)**  
  $$
  x_i = \frac{n_i}{\sum_j n_j},\quad y_i = \frac{n_i}{\sum_j n_j}
  $$

- **Partial molar property, $\bar{M}_i$**  
  Contribution of component $i$ to an extensive property $M$ of a mixture:
  $$
  \bar{M}_i = \left(\frac{\partial M}{\partial n_i}\right)_{T,P,n_{j\neq i}}
  $$

- **Gibbs–Duhem relation** (concept)  
  Links changes in partial molar properties within a mixture; for chemical potentials:
  $$
  \sum_i n_i\, d\mu_i = 0
  $$

- **Fugacity, $f_i$**  
  Effective pressure that accounts for non‑ideality; for an ideal gas, $f_i = y_i P$.

- **Activity, $a_i$**  
  Dimensionless measure of “effective concentration”; for liquids often written as:
  $$
  a_i = \gamma_i x_i
  $$
  where $\gamma_i$ is activity coefficient.

---

## Core formulas

### 1. Fugacity for ideal and real gases

- Ideal gas (component $i$ in mixture):
  $$
  f_i = y_i P
  $$

- Real gases (sketch):
  $$
  f_i = \phi_i y_i P
  $$
  where $\phi_i$ is the fugacity coefficient from EOS.

### 2. Liquid activity (VLE context)

For a subcooled liquid mixture:
$$
a_i = \gamma_i x_i
$$

For an ideal solution (Raoult’s law region), $\gamma_i \approx 1 \Rightarrow a_i \approx x_i$.

### 3. Excess properties 

Excess property $M^E$:
$$
M^E = M - M^{\text{ideal}}
$$
Used to build activity‑coefficient models; many exams only require knowing that $M^E$ captures deviation from ideal mixing.

### 4. Ideal Solutions 

An ideal solution is a liquid mixture where intermolecular interactions between unlike molecules are effectively the same as those between like molecules, so mixing does not introduce any extra enthalpic or volumetric effects beyond ideal behavior.
#### Key Characteristics

- Obeys Raoult’s law for all components and all compositions:
  $$
  p_i = x_i p_i^\ast
  $$
  where $p_i$ is the partial vapor pressure of component $i$, $x_i$ its mole fraction, and $p_i^\ast$ the pure-component vapor pressure.

- Enthalpy and volume of mixing are zero:
  $$
  \Delta H_{\text{mix}} = 0, \quad \Delta V_{\text{mix}} = 0
  $$
  so the driving force for mixing is purely entropic.

- Gibbs free energy of mixing for a binary ideal solution at constant $T,P$:
  $$
  \Delta G_{\text{mix}} = RT\left(x_A \ln x_A + x_B \ln x_B\right)
  $$
  with $x_A + x_B = 1$ and $0 < x_A, x_B < 1$, which makes $\Delta G_{\text{mix}} < 0$ and ensures complete miscibility.


---

## Interesting concepts

- **Ideal solution vs nonideal**  
  Ideal solutions obey Raoult’s law closely; strong deviations (large $\gamma_i$) occur with specific interactions or size differences.

- **Activity vs concentration**  
  Thermodynamics “sees” activity; concentration is a convenient observable. Activity coefficients correct concentration to activity.

- **Partial molar interpretation**  
  Partial molar properties can be visualized as slopes of mixture property vs composition curves.

---

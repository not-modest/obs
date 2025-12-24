---
{"dg-publish":true,"permalink":"/quals-prep/thermo/thermo-07-chemical-reaction-equilibrium/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Gibbs free energy, $G$**  
  $$
  G = H - TS
  $$
  At constant $T$ and $P$, spontaneous change proceeds toward lower $G$.

- **Standard Gibbs energy change of reaction, $\Delta G_r^\circ$**  
  Computed from standard Gibbs energies of formation:
  $$
  \Delta G_r^\circ = \sum_i \nu_i G_{f,i}^\circ
  $$

- **Equilibrium constant, $K$**  
  Defined from activities $a_i$:
  $$
  K = \prod_i a_i^{\nu_i}
  $$

- **Reaction quotient, $Q$**  
  Same form as $K$ but with current activities; direction of reaction follows whether $Q<K$ or $Q>K$.

---

## Core formulas

### 1. $\Delta G_r^\circ$ and $K$

At temperature $T$:
$$
\Delta G_r^\circ = -RT \ln K
$$
so
$$
K = \exp\!\left(-\frac{\Delta G_r^\circ}{RT}\right)
$$

### 2. Van’t Hoff equation (temperature dependence of $K$) 

#2025_Jan 
For approximate constant $\Delta H_r^\circ$:
$$
\frac{d\ln K}{dT} = \frac{\Delta H_r^\circ}{RT^2}
$$

Integrated between $T_1$ and $T_2$:
$$
\ln\left(\frac{K_2}{K_1}\right)
= \frac{\Delta H_r^\circ}{R}
\left(\frac{1}{T_1} - \frac{1}{T_2}\right)
$$
### 3. Gibbs Helmholtz Equation
#2025_Jan 
$$\left( \frac{\partial (G/T)}{\partial T} \right)_p = -\frac{H}{T^2}$$
$$\frac{\Delta G^\circ(T_2)}{T_2} - \frac{\Delta G^\circ(T_1)}{T_1} = \Delta H^\circ \left( \frac{1}{T_2} - \frac{1}{T_1} \right)
$$

---

### 4. Equilibrium composition (simple gas‑phase example)

For reaction
$$
\nu_1 A_1 + \nu_2 A_2 \rightleftharpoons \nu_3 A_3 + \cdots
$$

In ideal‑gas mixture at $T$ and $P$, activities $\approx$ partial pressures:
$$
a_i \approx \frac{y_i P}{P^\circ}
$$

Solve:
$$
K = \prod_i \left(\frac{y_i P}{P^\circ}\right)^{\nu_i}
$$
together with material balances and $\sum_i y_i = 1$ to obtain equilibrium composition.

---
## Interesting concepts

- **Spontaneity and direction**  
  If $Q < K$, reaction proceeds forward (products favored); if $Q > K$, it proceeds backward until $Q = K$.

- **Exothermic vs endothermic**  
  For exothermic reactions ($\Delta H_r^\circ < 0$), increasing $T$ usually decreases $K$; for endothermic, increasing $T$ increases $K$.

- **Equilibrium vs kinetics**  
  Equilibrium gives the ultimate limit; actual reactors may be far from equilibrium due to kinetic or transport limitations.

---

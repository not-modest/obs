---
{"dg-publish":true,"permalink":"/quals-prep/thermo/thermo-06-phase-equilibria-vle/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Phase equilibrium**  
  At equilibrium, chemical potential of each component is equal in all coexisting phases.

- **Phase rule** (for non‑reactive systems)
  $$
  F = C - P + 2
  $$
  where $F$ is degrees of freedom, $C$ components, $P$ phases.
![../src/Pasted image 20251223145242.png|400](/img/user/quals-prep/src/Pasted%20image%2020251223145242.png)

- **K‑value (equilibrium ratio)**  
  $$
  K_i = \frac{y_i}{x_i}
  $$
  for component $i$ in vapor–liquid equilibrium.

- **Bubble point**  
  Temperature (or pressure) at which first bubble of vapor forms from liquid of known composition.

- **Dew point**  
  Temperature (or pressure) at which first drop of liquid forms from vapor of known composition.

---

## Core formulas

### 1. Raoult’s law (ideal solution, low–moderate $P$)

For component $i$ in VLE:
$$
y_i P = x_i P_i^{\text{sat}}(T)
$$
or
$$
K_i = \frac{P_i^{\text{sat}}}{P}
$$

### 2. Modified Raoult’s law (nonideal liquid)

$$
y_i P = x_i \gamma_i P_i^{\text{sat}}(T)
$$

### 3. Bubble and dew point equations (binary sketch)

- Bubble point (given $x_i$, find $T$ or $P$):
  $$
  \sum_i y_i = 1,\quad y_i = \frac{x_i \gamma_i P_i^{\text{sat}}(T)}{P}
  $$

- Dew point (given $y_i$, find $T$ or $P$):
  $$
  \sum_i x_i = 1,\quad x_i = \frac{y_i P}{\gamma_i P_i^{\text{sat}}(T)}
  $$

### 4. Flash calculation (isothermal, isobaric, binary concept)

Overall material balance and equilibrium:
- $z_i$ feed composition, vapor fraction $\beta$:
  $$
  z_i = \beta y_i + (1-\beta) x_i,\quad y_i = K_i x_i
  $$
Combine to solve for $\beta$ and phase compositions.

---

## Interesting concepts

- **Shape of $P$–$x$–$y$ and $T$–$x$–$y$ diagrams**  
  Liquid and vapor composition curves; azeotropes appear where $x_i = y_i$ and bubble/dew lines meet.

- **Azeotropes and separation limits**  
  At an azeotrope, simple distillation cannot surpass that composition; other separations or conditions are needed.

- **Ideal vs nonideal behavior**  
  Large deviations in $\gamma_i$ lead to strong nonideality and azeotrope formation.

---

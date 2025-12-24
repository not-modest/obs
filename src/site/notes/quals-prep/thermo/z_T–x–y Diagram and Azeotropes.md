---
{"dg-publish":true,"permalink":"/quals-prep/thermo/z-t-x-y-diagram-and-azeotropes/","dgShowToc":true}
---

[[quals-prep/thermo/Thermo_06_Phase_Equilibria_VLE\|Thermo_06_Phase_Equilibria_VLE]]
#2025_Jan 

A T–x–y diagram shows how temperature depends on composition for a binary mixture at fixed pressure, along with liquid (x) and vapor (y) compositions in phase equilibrium.

Two primary curves:

1. **Bubble-point curve** (liquid line, x):
   - Temperatures at which the **first bubble** of vapor forms when heating a liquid of composition $x_1$.
   - Typically the **lower** curve on the T–x–y diagram.

2. **Dew-point curve** (vapor line, y):
   - Temperatures at which the **first drop** of liquid forms when cooling a vapor of composition $y_1$.
   - Typically the **upper** curve on the T–x–y diagram.

Between these curves, **liquid and vapor coexist**.
![../src/Pasted image 20251223152314.png|400](/img/user/quals-prep/src/Pasted%20image%2020251223152314.png)

---

## Phase Equilibrium and Reading Compositions

At a given temperature within the two-phase region:

- A horizontal isotherm cuts:
  - Bubble curve at liquid composition $x_1$.
  - Dew curve at vapor composition $y_1$.

These represent equilibrium compositions satisfying:
- $y_i\,P = x_i\,\gamma_i\,P_i^{\text{sat}}(T)$ (non-ideal, activity coefficient $\gamma_i$).  
- For ideal solutions, $\gamma_i \approx 1$ and Raoult’s law applies:
  $$
  y_i P = x_i P_i^{\text{sat}}(T)
  $$

---

## Lever Rule (Phase Fractions)

Within the two-phase region, the **lever rule** gives phase amounts:

- Let overall feed composition be $z_1$.  
- For a horizontal tie line at temperature $T$:
  - Liquid comp: $x_1$ (on bubble curve).  
  - Vapor comp: $y_1$ (on dew curve).

Then:
$$
\text{Vapor fraction} = \frac{z_1 - x_1}{y_1 - x_1}
$$
$$
\text{Liquid fraction} = \frac{y_1 - z_1}{y_1 - x_1}
$$

---

## Distillation Interpretation

On a T–x–y diagram at fixed $P$:

- Heating a liquid of overall composition $z_1$ to the bubble point gives the first vapor of composition $y_1$ (more volatile component enriched in vapor).  
- Cooling a vapor to the dew point condenses liquid of composition $x_1$ (less volatile component enriched in liquid).  

This compositional difference between $x_1$ and $y_1$ is the basis of **separation by distillation**.

---

## Azeotropes: 

An **azeotrope** is a mixture that boils at a constant temperature and composition, so the vapor and liquid have the **same composition**:
$$
x_1 = y_1
$$

At an azeotropic point in a T–x–y diagram, the bubble and dew curves **touch or cross**, and the mixture behaves as if it were a pure component (no separation by simple distillation at that pressure).

---

## Minimum- and Maximum-Boiling Azeotropes

On a T–x–y diagram:

1. **Minimum-boiling azeotrope**:
   - Azeotrope at a **local minimum** in $T$ vs composition.
   - Boils at a lower temperature than either pure component.
   - Bubble and dew curves dip down and meet at the minimum.  
   - Example behavior: strongly positive deviation from Raoult’s law.

2. **Maximum-boiling azeotrope**:
   - Azeotrope at a **local maximum** in $T$ vs composition.
   - Boils at a higher temperature than either pure component.
   - Bubble and dew curves bulge upward and meet at the maximum.  
   - Example behavior: strongly negative deviation from Raoult’s law.

At the azeotrope:
- Distillation cannot pass through the azeotropic composition at that pressure; both liquid and vapor remain at the azeotropic composition.

![../src/Pasted image 20251223152619.png](/img/user/quals-prep/src/Pasted%20image%2020251223152619.png)

---

## Ideal vs Non-Ideal Behavior

- **Ideal mixtures** (Raoult’s law, no azeotrope):
  - Bubble and dew curves do not cross; no constant-boiling mixture.
  - Separation by distillation is, in principle, possible across the whole composition range.

- **Non-ideal mixtures**:
  - Strong deviations from Raoult’s law can create azeotropes.
  - Activity coefficients $\gamma_i \neq 1$; non-ideality encoded in T–x–y shape.

---



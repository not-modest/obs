---
{"dg-publish":true,"permalink":"/quals-prep/thermo/thermo-07-chemical-reaction-equilibrium/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
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


## Exergonic and Endergonic Reactions 
#2024_Jan 

Exergonic and endergonic describe reactions in terms of **Gibbs free energy change** ($\Delta G$), i.e., whether a reaction releases usable energy or requires it.
### Gibbs Free Energy and Spontaneity

Gibbs free energy change at constant $T,P$:
$$
\Delta G = \Delta H - T \Delta S
$$
where:
- $\Delta H$ = enthalpy change  
- $\Delta S$ = entropy change  
- $T$ = absolute temperature  

Spontaneity criterion:
- $\Delta G < 0$: reaction is **spontaneous** (can proceed without external energy input).  
- $\Delta G > 0$: reaction is **nonspontaneous** (requires energy input).  
- $\Delta G = 0$: system at **equilibrium**.

---

### Exergonic Reactions

**Definition**: Exergonic reactions **release free energy** and have a **negative** Gibbs free energy change.  

Key points:
- $\Delta G < 0$ (energy “exits” the system).  
- Products have **lower** free energy than reactants:
  $$
  \Delta G = G_{\text{products}} - G_{\text{reactants}} < 0
  $$
- Thermodynamically **spontaneous** under given conditions.  
- In biology, often correspond to **catabolic** processes (breaking down molecules, e.g., ATP hydrolysis, glucose oxidation).

Energy released can be harnessed to perform work (transport, synthesis, etc.).
### Endergonic Reactions

**Definition**: Endergonic reactions **require an input of free energy** and have a **positive** Gibbs free energy change.  

Key points:
- $\Delta G > 0$ (energy “enters” the system).  
- Products have **higher** free energy than reactants:
  $$
  \Delta G = G_{\text{products}} - G_{\text{reactants}} > 0
  $$
- Thermodynamically **nonspontaneous** as written; will not proceed unless driven by an external energy source.  
- In biology, often correspond to **anabolic** processes (building complex molecules, e.g., protein synthesis, active transport).

---
### Coupling Exergonic and Endergonic Reactions

Cells and engineered systems often **couple** reactions so that an overall process becomes exergonic:

Example idea:
- Reaction 1 (exergonic): $\Delta G_1 < 0$  
- Reaction 2 (endergonic): $\Delta G_2 > 0$  

If they are coupled such that the **overall** reaction is:
$$
\Delta G_{\text{overall}} = \Delta G_1 + \Delta G_2 < 0
$$
then the combined process is spontaneous.

Classic biochemical example:  
- ATP hydrolysis (exergonic) is coupled to an endergonic biosynthetic step.  
- The net $\Delta G$ becomes negative, so the synthesis can proceed.
![../src/Pasted image 20251224161932.png](/img/user/quals-prep/src/Pasted%20image%2020251224161932.png)
---

#### Exergonic vs Exothermic (and Endergonic vs Endothermic)

- **Exergonic/endergonic**: about **free energy** ($\Delta G$) and **spontaneity**, includes both enthalpy and entropy effects.  
- **Exothermic/endothermic**: about **heat** ($\Delta H$) only.  

A reaction can be:
- Exothermic but not exergonic at certain temperatures if the $-T\Delta S$ term is large and positive.  
- Endothermic but still exergonic if there is a large, positive entropy change making $\Delta G < 0$.

Thus, exergonic vs endergonic is the more general classification for spontaneity at constant $T,P$.


## 4. Equilibrium composition (simple gas‑phase example)

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
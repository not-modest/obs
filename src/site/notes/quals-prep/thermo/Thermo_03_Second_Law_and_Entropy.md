---
{"dg-publish":true,"permalink":"/quals-prep/thermo/thermo-03-second-law-and-entropy/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

## Key definitions

- **Second law of thermodynamics**  
  - Kelvin–Planck statement: no heat engine operating in a cycle can convert all heat from a single reservoir into work.  
  - Clausius statement: heat cannot spontaneously flow from a colder to a hotter body.

- **Entropy, $S$**  
  State function measuring energy dispersal and unavailable energy; for a reversible process:
  $$
  dS = \frac{\delta Q_{\text{rev}}}{T}
  $$

- **Entropy production, $S_{\text{gen}}$**  
  Non‑negative quantity that measures irreversibility; zero for reversible processes, positive for real processes.

- **Thermal efficiency of a heat engine**
  $$
  \eta = \frac{W_{\text{net,out}}}{Q_H}
  $$
  where $Q_H$ is heat input from hot reservoir.

- **Carnot efficiency** (maximum possible between $T_H$ and $T_C$)
  $$
  \eta_{\text{Carnot}} = 1 - \frac{T_C}{T_H}
  $$

---

## Core formulas

### 1. Entropy balance (control mass)

For a closed system:
$$
\Delta S = \int \frac{\delta Q}{T} + S_{\text{gen}}
$$
with $S_{\text{gen}} \ge 0$.

### 2. Entropy balance (control volume, steady state)

For a control volume with mass flow:
$$
\dot S_{\text{in}} - \dot S_{\text{out}} + \dot S_{\text{gen}} = \frac{\dot Q}{T_{\text{b}}}
$$
where $T_{\text{b}}$ is the boundary temperature at which heat $\dot Q$ crosses.

At steady state with no shaft work or accumulation:
- $S_{\text{gen}} \ge 0$; equality only for reversible operation.

### 3. Heat engines and refrigerators

- Heat engine:
  $$
  \eta = \frac{W_{\text{net,out}}}{Q_H}
  = 1 - \frac{Q_C}{Q_H}
  $$
  For a reversible engine between $T_H$ and $T_C$:
  $$
  \frac{Q_C}{Q_H} = \frac{T_C}{T_H}
  \Rightarrow
  \eta_{\text{rev}} = 1 - \frac{T_C}{T_H}
  $$

- Refrigerator coefficient of performance (COP):
  $$
  \text{COP}_R = \frac{Q_C}{W_{\text{net,in}}}
  $$

- Heat pump COP:
  $$
  \text{COP}_{\text{HP}} = \frac{Q_H}{W_{\text{net,in}}}
  $$

---

## Interesting concepts

- **Direction of spontaneous processes**  
  For isolated systems, spontaneous processes occur in the direction of increasing entropy; equilibrium corresponds to maximum entropy.

- **Irreversibility and lost work**  
  Entropy generation quantifies lost potential to do work; more $S_{\text{gen}}$ implies lower achievable efficiency for a given $Q$.

- **Reversible vs real cycles**  
  Reversible cycles (Carnot) are ideal upper bounds; real engines and refrigerators always have lower efficiency/COP due to friction, finite temperature differences, and other irreversibilities.

---


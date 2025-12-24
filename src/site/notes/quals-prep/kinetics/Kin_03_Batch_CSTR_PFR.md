---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/kin-03-batch-cstr-pfr/","dgShowToc":true}
---

## Key definitions

- **Rate of reaction, $r_A$**  
  Rate of disappearance of A per unit reactor volume (or catalyst volume); negative for a reactant. By convention $-r_A > 0$ for reactant A.

- **Conversion, $X_A$**  
  Fraction of A reacted:  
  $$
  X_A = \frac{F_{A0} - F_A}{F_{A0}}
  $$
  for flow systems, or  
  $$
  X_A = \frac{N_{A0} - N_A}{N_{A0}}
  $$
  for batch.

- **Space time, $\tau$**  
  Time to process one reactor volume of fluid at inlet volumetric flow rate:
  $$
  \tau = \frac{V}{\dot V_0}
  $$

- **Space velocity, $s$**  
  $$
  s = \frac{1}{\tau}
  $$

- **Ideal batch reactor**  
  Closed, perfectly mixed, no flow; composition uniform in space, changing with time.

- **Ideal CSTR**  
  Open, well mixed, steady state; outlet conditions equal to reactor contents.

- **Ideal PFR**  
  Steady flow, no axial mixing; properties uniform over cross‑section, varying only along length.

---

## Core formulas (conversion form), isothermal, constant density, $A \to$ products

### Batch reactor

Mole balance:
$$
\frac{dN_A}{dt} = r_A V
$$

Using $N_A = N_{A0}(1 - X_A)$:
$$
t = \int_{0}^{X_A} \frac{N_{A0}}{-r_A V}\, dX_A
$$

### CSTR

Steady‑state mole balance:
$$
F_{A0} - F_A + r_A V = 0
$$

Using $F_A = F_{A0}(1 - X_A)$ and $-r_A$ at outlet:
$$
V = \frac{F_{A0} X_A}{-r_A}
$$

### PFR

Differential mole balance:
$$
dF_A = r_A\, dV
$$

Using conversion:
$$
V = \int_{0}^{X_A} \frac{F_{A0}}{-r_A}\, dX_A
$$

---

## Special case: first‑order liquid reaction, $-r_A = k C_A$, $C_A = C_{A0}(1 - X_A)$

### Batch

$$
t = \int_{0}^{X_A} \frac{dX_A}{k(1 - X_A)}
  = \frac{1}{k}\,\ln\!\left(\frac{1}{1 - X_A}\right)
$$

### CSTR

$$
\tau = \frac{V}{\dot V_0}
     = \frac{X_A}{k(1 - X_A)}
$$

### PFR

$$
\tau = \int_{0}^{X_A} \frac{dX_A}{k(1 - X_A)}
     = \frac{1}{k}\,\ln\!\left(\frac{1}{1 - X_A}\right)
$$

---

## Interesting concepts

- **Where $-r_A$ is evaluated**  
  - Batch: varies with time; integrate over $X_A$.  
  - CSTR: evaluated at outlet conditions.  
  - PFR: varies along reactor; integrate over $X_A$.

- **Relative volume/space‑time**  
  For rate decreasing with conversion (e.g. first order):  
  - PFR (and batch) need less volume than CSTR at the same conversion.  
  - As $X_A \to 1$, $\tau_{\text{CSTR}}$ grows faster than $\tau_{\text{PFR}}$.

- **Scaling with $k$**  
  For first order, $t$ or $\tau$ is proportional to $1/k$; doubling $k$ halves required time/space time at fixed conversion.

- **Reaction Performance**: yield, selectivity, energy input... #2025_Jan 

---


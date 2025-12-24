---
{"dg-publish":true,"permalink":"/quals-prep/transport/trans-03-heat-transfer/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Fourier’s law of conduction**  
  $$
  q_x = -k A \frac{dT}{dx}
  $$

- **Newton’s law of cooling (convection)**  
  $$
  q = h A (T_s - T_\infty)
  $$

- **Thermal conductivity, $k$**  
  Material property relating temperature gradient to heat flux.

- **Heat transfer coefficient, $h$**  
  Effective parameter capturing convection and boundary‑layer behavior.

---

## Core formulas

### 1. 1D steady conduction in a plane wall

Wall of thickness $L$, area $A$, thermal conductivity $k$, $T_1$ and $T_2$ at faces:
$$
q = k A \frac{T_1 - T_2}{L}
$$

### 2. Cylindrical wall

Inner radius $r_1$, outer radius $r_2$, length $L$:
$$
q = \frac{2\pi k L (T_1 - T_2)}{\ln(r_2/r_1)}
$$

### 3. Thermal resistance network

General form:
$$
q = \frac{\Delta T}{R_{\text{total}}}
$$

Examples:

- Conduction through wall: $R_{\text{cond}} = \dfrac{L}{kA}$.  
- Convection: $R_{\text{conv}} = \dfrac{1}{hA}$.

Series layers:
$$
R_{\text{total}} = \sum_i R_i
$$

### 4. Dimensionless numbers and correlations (typical)

- Nusselt:
  $$
  \text{Nu} = \frac{h L}{k}
  $$

Typical forms (memory level):

- Laminar flow, constant wall heat flux in tube:
  $\text{Nu} \approx 4.36$.  
- Turbulent internal flow (Dittus–Boelter type):
  $\text{Nu} = 0.023 \text{Re}^{0.8} \text{Pr}^n$ with $n \approx 0.3 - 0.4$.

---

## Boiling and condensation (exam level)

- **Boiling**  
  Characterized by high $h$; pool boiling curve with nucleate, transition, and film‑boiling regimes; critical heat flux marks burnout.

- **Condensation**  
  Film condensation on vertical surface: overall $h$ from Nusselt film model; dropwise condensation has much higher $h$ but is hard to maintain.

---

## Interesting concepts

- **Thermal resistance analogy**  
  Series of conduction and convection layers behaves like resistors in series; aids quick estimation of $q$.

- **Biot number for transient problems**  
  $\displaystyle \text{Bi} = \dfrac{h L_c}{k}$; small Bi allows lumped capacitance ($T$ uniform inside object).

- **Coupling with fluid flow**  
  $h$ depends on flow regime and properties; strong link with momentum transport via Re and Pr.

---

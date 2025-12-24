---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/kin-04-reaction-networks-and-selectivity/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## Key definitions

- **Parallel reactions**  
  One reactant forms two or more products by different pathways, e.g.  
  $A \to B$, $A \to C$.

- **Series reactions**  
  Product of one step is reactant for the next, e.g.  
  $A \to B \to C$.

- **Yield of desired product**  
  $$Y_B = \frac{\text{moles of B formed}}{\text{moles of A fed}}$$

- **Selectivity** (desired vs undesired)  
  For desired $B$ and undesired $C$:  
  $$S_{B/C} = \frac{\text{moles of B formed}}{\text{moles of C formed}}$$  

- **Instantaneous selectivity**  
  Ratio of instantaneous rates, e.g.  
  $$S_{B/C}^{\text{inst}} = \frac{r_B}{r_C}$$  

---

## Core formulas

### 1. Simple parallel, isothermal, liquid, power‑law

$A \to B$ with $-r_{A,1} = k_1 C_A^{n_1}$  
$A \to C$ with $-r_{A,2} = k_2 C_A^{n_2}$  

Instantaneous selectivity:
$$
S_{B/C}^{\text{inst}} = \frac{r_B}{r_C}
= \frac{k_1 C_A^{n_1}}{k_2 C_A^{n_2}}
= \frac{k_1}{k_2} \, C_A^{\,n_1 - n_2}
$$

Implications:

- If $n_1 > n_2$: higher $C_A$ favors B.  
- If $n_1 < n_2$: lower $C_A$ favors B.

Reactor choice (qualitative):

- High $C_A$ (batch, PFR) favors pathway with higher order in $C_A$.  
- Lower $C_A$ (CSTR) favors pathway with lower order.

### 2. Simple series: $A \to B \to C$ (first order)

$-r_A = k_1 C_A$, $-r_B = k_2 C_B - k_1 C_A$.  

Batch, initial $C_{A0}$, $C_B(0)=0$:

- $$C_A(t) = C_{A0} e^{-k_1 t}$$  
- $$C_B(t) = \frac{k_1 C_{A0}}{k_2 - k_1}
\left(e^{-k_1 t} - e^{-k_2 t}\right)$$  

Desired intermediate B has a maximum at
$$
t_{\text{max},B} = \frac{1}{k_2 - k_1} \ln\left(\frac{k_2}{k_1}\right)
$$

---

## Interesting concepts

- **Using reactor type for parallel reactions**  
  For $n_1 > n_2$ (desired has higher order): use reactors with high $C_A$ (PFR, batch, or plug‑flow sections).  
  For $n_1 < n_2$ (desired has lower order): use CSTRs or recycle to keep $C_A$ lower.

- **Temperature effects on selectivity**  
  If $E_{a,1} \neq E_{a,2}$, changing $T$ changes $k_1/k_2$; higher $E_a$ pathway is more sensitive to $T$.

- **Series reactions and “reactor severity”**  
  For $A \to B \to C$, too low residence time: little B formed; too high: B over‑reacts to C. There is an optimal conversion or residence time maximizing B.

- **Recycling intermediates**  
  In $A \to B \to C$, using CSTRs in series or recycle can help maintain B at useful levels while limiting over‑reaction to C.

---


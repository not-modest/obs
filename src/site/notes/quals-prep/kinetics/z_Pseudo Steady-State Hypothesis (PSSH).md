---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/z-pseudo-steady-state-hypothesis-pssh/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

#2025_Jan [[quals-prep/kinetics/Kin_01_Rates_and_Stoichiometry\|Kin_01_Rates_and_Stoichiometry]]

[Micheles-Menten](https://chem.libretexts.org/Bookshelves/Biological_Chemistry/Supplemental_Modules_(Biological_Chemistry)/Enzymes/Enzymatic_Kinetics/Michaelis-Menten_Kinetics) #2024_Jan 

The pseudo steady-state hypothesis (PSSH), also called the quasi-steady-state approximation, assumes that the concentration of a reactive intermediate changes so slowly (or is so small) that its net rate of production is approximately zero over the time scale of interest.
## Basic Idea

Consider a mechanism involving an intermediate I:
- Formation: $\text{Reactants} \rightarrow \text{I}$
- Consumption: $\text{I} \rightarrow \text{Products}$

PSSH assumes:
$$
\frac{dC_I}{dt} \approx 0
$$

So the rate of formation of I equals its rate of consumption:
$$
r_{\text{form},I} \approx r_{\text{cons},I}
$$

This allows solving algebraically for $C_I$ and substituting back into the rate law to obtain an effective rate expression in terms of stable species only.

---

## Typical Application: Single Intermediate

For a simple sequence:
$$
A \xrightarrow{k_1} I \xrightarrow{k_2} P
$$

Material balance on I:
$$
\frac{dC_I}{dt} = k_1 C_A - k_2 C_I
$$

PSSH: set $\dfrac{dC_I}{dt} \approx 0$:
$$
0 \approx k_1 C_A - k_2 C_I
\quad\Rightarrow\quad
C_I \approx \frac{k_1}{k_2} C_A
$$

Overall rate of product formation:
$$
r_P = k_2 C_I \approx k_2 \left(\frac{k_1}{k_2} C_A\right) = k_1 C_A
$$

So the observable rate law is first order in $A$, independent of $k_2$ in this limit.

---

## Applicability Conditions (Qualitative)

PSSH is reasonable when:

- The intermediate is **highly reactive** and remains at **low concentration** compared to reactants and products.
- The intermediate is formed and consumed on a **faster time scale** than the slow, overall reaction progress.
- The system is not in the very initial transient where $C_I$ is still building up from zero.

Heuristically, one often checks that:

- $C_I \ll C_{\text{reactants}}$ and $C_I \ll C_{\text{products}}$ over most of the reaction.  
- The characteristic time for intermediate adjustment is much shorter than that for bulk concentration changes.

---

## When PSSH May Fail

PSSH may be inappropriate when:

- The intermediate accumulates to **comparable levels** as reactants/products.  
- There are **multiple comparable time scales**, so no clear separation between “fast intermediate” and “slow bulk” dynamics.  
- Initial conditions or boundary layers (e.g., at very early times or near interfaces) dominate the behavior.  

In such cases, the full set of differential equations for all species, including intermediates, should be solved without imposing PSSH.

---



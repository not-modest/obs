---
{"dg-publish":true,"permalink":"/quals-prep/thermo/z-le-chatelier-s/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

[[quals-prep/thermo/Thermo_07_Chemical_Reaction_Equilibrium\|Thermo_07_Chemical_Reaction_Equilibrium]]

Le Chatelier’s principle states that when a system at equilibrium is subjected to a change in conditions (concentration, pressure, or temperature), it responds by shifting its equilibrium position in the direction that tends to counteract that change.

---

## Equilibrium and Reaction Quotient

For a general reaction:
$$
aA + bB \rightleftharpoons cC + dD
$$

The equilibrium constant:
$$
K = \frac{[C]^c [D]^d}{[A]^a [B]^b}
$$

The reaction quotient (at any moment):
$$
Q = \frac{[C]^c [D]^d}{[A]^a [B]^b}
$$

- If $Q < K$: reaction shifts **forward** (to products).  
- If $Q > K$: reaction shifts **backward** (to reactants).  

Le Chatelier’s principle qualitatively predicts the direction of this shift after a disturbance.

---

## Effect of Concentration

If the concentration of a species is changed:

- Adding a reactant (e.g., $A$): increases $[A]$, typically makes $Q < K$, so the system shifts **towards products** to consume the added reactant.  
- Removing a reactant: makes $Q > K$, system shifts **towards reactants** (consuming products) to replenish it.  
- Adding a product: drives shift **towards reactants**.  
- Removing a product: drives shift **towards products**.

The equilibrium constant $K$ does **not** change with concentration; only the equilibrium composition changes.

---

## Effect of Pressure (Gases)

For gas-phase equilibria, changing total pressure (by changing volume) affects the side with more/less moles of gas.

Example:
$$
\text{N}_2(g) + 3\text{H}_2(g) \rightleftharpoons 2\text{NH}_3(g)
$$

- Total moles of gas: left = 4, right = 2.  

Rules:

- Increase pressure (decrease volume): equilibrium shifts toward the side with **fewer moles of gas** (here, toward NH$_3$).  
- Decrease pressure (increase volume): equilibrium shifts toward the side with **more moles of gas**.  
- If gas moles are equal on both sides, pressure changes have negligible effect on equilibrium composition (ignoring non-idealities).

Again, $K$ for the given $T$ is unchanged; only partial pressures adjust.

---

## Effect of Temperature

Temperature changes **do** change the equilibrium constant $K$.

For a reaction with standard enthalpy change $\Delta H^\circ$:

- If the reaction is **exothermic** ($\Delta H^\circ < 0$):  
  - Heat can be viewed as a “product”.  
  - Increasing $T$ shifts equilibrium **toward reactants** (reduces $K$).  
  - Decreasing $T$ shifts equilibrium **toward products** (increases $K$).

- If the reaction is **endothermic** ($\Delta H^\circ > 0$):  
  - Heat acts like a “reactant”.  
  - Increasing $T$ shifts equilibrium **toward products** (increases $K$).  
  - Decreasing $T$ shifts equilibrium **toward reactants** (reduces $K$).

Quantitatively, the van ’t Hoff equation relates $K$ and $T$ #2025_Jan :
$$
\frac{d\ln K}{dT} = \frac{\Delta H^\circ}{RT^2}
$$
---

## Effect of Catalysts

A catalyst:

- Lowers the activation energy for both forward and reverse reactions by the same factor.  
- Speeds up the approach to equilibrium but does **not** change the equilibrium position or the value of $K$.  

Thus, catalysts do **not** shift equilibrium; they only affect how fast equilibrium is reached.

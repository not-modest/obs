---
{"dg-publish":true,"permalink":"/quals-prep/thermo/z-henry-s-law/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

#2021_Jan [[quals-prep/thermo/Thermo_06_Phase_Equilibria_VLE\|Thermo_06_Phase_Equilibria_VLE]]
Henry’s law relates the equilibrium solubility of a gas in a liquid to its partial pressure in the gas phase, assuming dilute solution and no chemical reaction.

---

## Statement

For a gas $A$ dissolved in a liquid at constant temperature:
$$
p_A = H_A\, x_A
$$
where:
- $p_A$ = gas-phase partial pressure of $A$  
- $x_A$ = mole fraction of $A$ in the liquid  
- $H_A$ = Henry’s law constant (pressure units, e.g. Pa or atm)  

Interpretation:
- At fixed $T$, dissolved concentration is **proportional** to gas partial pressure.  
- Larger $H_A$ → gas is **less soluble** (needs higher pressure for same $x_A$).

Alternative concentration form:
$$
C_A = k_H\, p_A
$$
where:
- $C_A$ = dissolved concentration (e.g. mol/m³)  
- $k_H$ = Henry constant in (mol·m⁻³·Pa⁻¹)  

---

## Relation to Chemical Potential and Activities

In thermodynamic form, equilibrium implies equal chemical potentials in gas and liquid:
$$
\mu_A^{(g)} = \mu_A^{(l)}
$$

Using standard-state conventions:

- Gas phase (ideal):
  $$
  \mu_A^{(g)} = \mu_A^{\circ (g)} + RT \ln\left(\frac{p_A}{p^\circ}\right)
  $$

- Liquid phase (very dilute, Henry’s-law standard state):
  $$
  \mu_A^{(l)} = \mu_A^{\circ (H)} + RT \ln a_A
  $$
  with activity $a_A = \gamma_A x_A$ (for solute $A$).

At infinite dilution, $\gamma_A$ is often taken as 1 in Henry’s scale, giving:
$$
\frac{p_A}{x_A} = H_A
$$
where $H_A$ encapsulates the reference-state difference between gas and liquid.

---

## Henry vs Raoult Behavior

- **Raoult’s law**: applies to solvents / major components in ideal solutions:
  $$
  p_i = x_i P_i^{\text{sat}}(T)
  $$
- **Henry’s law**: applies to **dilute solutes** (gases or low-concentration species):
  $$
  p_A = H_A x_A
  $$

In real mixtures:
- The solvent often follows Raoult’s law near $x \approx 1$.  
- The solute follows Henry’s law near $x \approx 0$.

---

## Temperature Dependence

Henry’s law constant depends on temperature. A van ’t Hoff–type relation is often used:
$$
\frac{d\ln H_A}{dT} = \frac{\Delta H_{\text{sol}}}{RT^2}
$$
where $\Delta H_{\text{sol}}$ is an effective enthalpy of solution (sign and magnitude depend on the gas–solvent system).

Practical trend:
- For many gases in water, solubility **decreases** with increasing $T$, so $H_A$ **increases** as temperature rises.

---

## Dimensionless Henry’s Constant

A dimensionless form $H_A^\ast$ often relates gas fugacity (or partial pressure scaled by a reference) to liquid-phase activity:
$$
H_A^\ast = \frac{f_A}{x_A}
$$
or, for ideal gas and Henry’s standard state choices:
$$
H_A^\ast = \frac{p_A}{x_A p^\circ}
= \frac{H_A}{p^\circ}
$$
where $p^\circ$ is a reference pressure (often 1 atm or 1 bar).

This is convenient when coupling phase equilibria with activity models.

---

## Conditions and Limitations

Henry’s law is valid when:

- Solute is **dilute** in the liquid (infinite-dilution limit).  
- No strong chemical reaction with solvent (no significant dissociation or complexation).  
- Pressure is not so high that gas or liquid deviate strongly from ideal behavior (or corrections via fugacity/activity are applied).  

Examples where deviations occur:

- Strongly reactive gases (e.g., CO₂ in water with significant acid–base chemistry).  
- Very high solute concentrations or non-ideal solvents (need more advanced models).

---

## Example Use in Mass Transfer

In gas–liquid mass transfer:
- Interfacial equilibrium is often described by Henry’s law:
  $$
  p_{A,i} = H_A x_{A,i}
  $$
- This relates the interfacial gas partial pressure to interfacial liquid mole fraction, entering overall mass-transfer relations and defining the equilibrium line for absorption/stripping design.


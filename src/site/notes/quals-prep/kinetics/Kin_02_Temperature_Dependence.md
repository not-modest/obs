---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/kin-02-temperature-dependence/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

## Key definitions

- **Rate constant, $k$**  
  Proportionality factor in the rate law (e.g. $-r_A = k C_A^n$ for a power‑law model). Depends strongly on temperature and weakly on pressure (for most liquid‑phase reactions).  

- **Activation energy, $E_a$**  
  Effective energy barrier that reacting molecules must overcome to form products. Higher $E_a$ means stronger sensitivity of $k$ to temperature.  

- **Pre‑exponential factor, $A$**  
  Also called frequency factor; captures collision frequency and orientation effects in the Arrhenius equation.  

- **Arrhenius equation**  
  Empirical relation between $k$ and temperature:
  $$
  k = A \exp\!\left(-\frac{E_a}{RT}\right)
  $$

- **Arrhenius plot**  
  Plot of $\ln k$ versus $1/T$; gives a straight line with slope $-E_a/R$ and intercept $\ln A$.  

---

## Core formulas

### Arrhenius in linear form

$$
\ln k = \ln A - \frac{E_a}{R}\,\frac{1}{T}
$$

From two data points $(k_1,T_1)$ and $(k_2,T_2)$:
$$
\ln\left(\frac{k_2}{k_1}\right)
= -\frac{E_a}{R}\left(\frac{1}{T_2} - \frac{1}{T_1}\right)
$$

Solve for $E_a$:
$$
E_a
= -R\,\frac{\ln(k_2/k_1)}{(1/T_2 - 1/T_1)}
$$

Predict $k_2$ at new temperature $T_2$:
$$
k_2 = k_1 \exp\!\left[
-\frac{E_a}{R}\left(\frac{1}{T_2} - \frac{1}{T_1}\right)
\right]
$$

### Rate law with temperature dependence

For a power‑law rate:
$$
-r_A = k(T)\, C_A^{\alpha} C_B^{\beta}
$$
with
$$
k(T) = A \exp\!\left(-\frac{E_a}{RT}\right)
$$

In design equations (batch, CSTR, PFR), substitute $k(T)$ wherever $k$ appears.

---

## Interesting concepts

- **Sensitivity to temperature**  
  For larger $E_a$, a small increase in $T$ causes a large increase in $k$ and hence in reaction rate. For low $E_a$, rate is comparatively insensitive to $T$.  

- **Rule‑of‑thumb behavior**  
  Many real reactions approximately “double rate per $10^\circ\text{C}$ rise” in some range; this corresponds to a moderate activation energy and is useful for quick estimates.  

- **Log‑linear fitting**  
  Experimental $k$ vs $T$ data are often processed by plotting $\ln k$ vs $1/T$ and using straight‑line regression to extract $E_a$ and $A$.  

- **Connection to energy barriers**  
  Arrhenius behavior reflects that only a fraction $\exp(-E_a/RT)$ of molecular encounters have enough energy to cross the barrier; as $T$ rises, that fraction increases sharply.  

---


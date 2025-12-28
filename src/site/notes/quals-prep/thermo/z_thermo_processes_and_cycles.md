---
{"dg-publish":true,"permalink":"/quals-prep/thermo/z-thermo-processes-and-cycles/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

[[#Quick Summary Table Key Equations]]
# Basic Thermodynamic Processes (Ideal Gas)

| Process type  | Condition          | Key relations (ideal gas, quasi-static)                                        | $p\!-\!V$ work $W$ (system)                      |
|---------------|--------------------|---------------------------------------------------------------------------------|-----------------------------------------------|
| Isothermal    | $T = \text{const}$ | $pV = \text{const}$; $U = \text{const}$; $Q = W$                               | $W = \int p\,dV = nRT \ln\frac{V_2}{V_1}$     |
| Isobaric      | $p = \text{const}$ | $V \propto T$ (Charles); $Q = n c_p (T_2 - T_1)$                               | $W = p(V_2 - V_1)$                             |
| Isochoric     | $V = \text{const}$ | $p \propto T$ (Gay-Lussac); $W = 0$; $Q = n c_v (T_2 - T_1)$                   | $W = 0$                                       |
| Adiabatic     | $Q = 0$            | $pV^\gamma = \text{const}$; $TV^{\gamma-1} = \text{const}$; $p^{1-\gamma} T^\gamma = \text{const}$ | $W = \frac{p_2 V_2 - p_1 V_1}{1 - \gamma}$    |
| Polytropic    | $pV^n = \text{const}$ | Generalization; $n=1$ isoT, $n=\gamma$ adiabatic, $n\to\infty$ isoV         | $W = \frac{p_2 V_2 - p_1 V_1}{1 - n}$ (if $n\ne1$) |

- $\gamma = c_p / c_v$ is the heat capacity ratio.
- For isothermal ideal gas, $\Delta U = 0$, so $Q = W$.
- For adiabatic, $Q = 0$, so $\Delta U = -W$.

---

# Major Thermodynamic Cycles

| Aspect                     | [[#1. Carnot Cycle (Reversible, Ideal Benchmark)\|Carnot cycle]] | [[#2. Rankine Cycle (Basic Steam Power Cycle)\|Rankine cycle]]                         |
| -------------------------- | ---------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Purpose                    | Ideal, theoretical benchmark for maximum efficiency              | Practical steam power cycle used in turbines                                           |
| Working fluid model        | Ideal gas or idealized fluid with reversible processes           | Real water/steam with phase change                                                     |
| Heat addition              | Isothermal at $T_H$                                              | Isobaric in boiler (liquid → saturated/superheated vapor)                              |
| Heat rejection             | Isothermal at $T_C$                                              | Isobaric in condenser (vapor → saturated liquid)                                       |
| Expansion process          | Reversible isothermal + reversible adiabatic                     | Ideally isentropic expansion in turbine                                                |
| Compression process        | Reversible isothermal + reversible adiabatic                     | Ideally isentropic pumping of (nearly) incompressible liquid                           |
| Practical implementability | Not realizable as a real engine                                  | Widely used in power plants (steam cycles)                                             |
| Efficiency expression      | $\eta = 1 - T_C/T_H$                                             | $\eta = \dfrac{w_{\text{net}}}{q_{\text{in}}}$, depends on $h$’s and irreversibilities |
| Irreversibilities assumed  | None (fully reversible)                                          | Present in turbine, pump, boiler, condenser, and fluid flows                           |
| Use in design              | Theoretical upper bound; benchmark for any heat engine           | Basis for real plant design, optimization, and modifications                           |

## 1. Carnot Cycle (Reversible, Ideal Benchmark)

Four internally reversible steps between $T_H$ (hot) and $T_C$ (cold):

1. **Isothermal expansion at $T_H$**:  
   - Heat in: $Q_H = n R T_H \ln(V_2/V_1)$  
   - Work out: $W_{1\to2} = Q_H$

2. **Adiabatic expansion**:  
   - $T_H \to T_C$; $pV^\gamma = \text{const}$  
   - $Q = 0$; work out, temperature drops.

3. **Isothermal compression at $T_C$**:  
   - Heat out: $Q_C = n R T_C \ln(V_4/V_3)$  
   - Work in: $W_{3\to4} = Q_C$

4. **Adiabatic compression**:  
   - $T_C \to T_H$; $Q = 0$; returns to initial state.

Net work:
$$
W_{\text{net}} = Q_H - Q_C
$$

Thermal efficiency:
$$
\eta_{\text{Carnot}} = 1 - \frac{Q_C}{Q_H}
= 1 - \frac{T_C}{T_H}
$$

- Upper bound for any heat engine between $T_H$ and $T_C$.
- Fully reversible; entropy change over full cycle of working fluid is zero, but reservoirs exchange entropy.

---

## 2. Rankine Cycle (Basic Steam Power Cycle)

States (one common numbering):

1. **Pump inlet**: saturated liquid at condenser pressure ($p_L$).  
2. **Pump outlet**: compressed liquid at boiler pressure ($p_H$).  
3. **Turbine inlet**: saturated or superheated steam at $p_H$.  
4. **Turbine outlet**: wet/superheated mixture at $p_L$.

Processes:

1. **1→2: Isentropic pumping (liquid)**  
   - $s_1 \approx s_2$  
   - Pump work (approx):  
     $$
     w_p \approx v_1 (p_2 - p_1)
     $$
   - $h_2 \approx h_1 + w_p$

2. **2→3: Constant-pressure heat addition (boiler)**  
   - $p = p_H$  
   - Heat in:  
     $$
     q_{\text{in}} = h_3 - h_2
     $$

3. **3→4: Isentropic expansion (turbine)**  
   - $s_3 = s_4$  
   - Turbine work:  
     $$
     w_t = h_3 - h_4
     $$

4. **4→1: Constant-pressure heat rejection (condenser)**  
   - $p = p_L$  
   - Heat out:  
     $$
     q_{\text{out}} = h_4 - h_1
     $$

Net work:
$$
w_{\text{net}} = w_t - w_p = (h_3 - h_4) - (h_2 - h_1)
$$

Thermal efficiency:
$$
\eta_{\text{Rankine}} =
\frac{w_{\text{net}}}{q_{\text{in}}}
=
\frac{(h_3 - h_4) - (h_2 - h_1)}{h_3 - h_2}
$$

---

# Reversible vs Irreversible Work, Exergy

| Concept             | Meaning (high level)                                                      | Main formula (closed system, reference $T_0, p_0$)                             |
|---------------------|---------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Useful work $W_u$   | Actual work minus boundary work against environment                      | $W_u = W - p_0 (V_2 - V_1)$                                                    |
| Reversible work $W_{\text{rev}}$ | Maximum possible useful work between given states (no irreversibilities) | For process to dead state: $W_{\text{rev}} = \text{exergy change}$            |
| Irreversibility $I$ | Lost work potential (exergy destruction) due to irreversibilities        | $I = W_{\text{rev,out}} - W_{u,\text{out}}$ (work-producing device)           |
| Exergy $X$          | Maximum useful work relative to environment (dead state)                 | For simple system: $X = (U - U_0) + p_0 (V - V_0) - T_0 (S - S_0)$            |

- **Reversible work** is the benchmark: what you would get (or need) in a fully reversible process.
- **Actual useful work** is always less favorable:
  - For turbines: $W_{u,\text{act}} < W_{\text{rev}}$  
  - For compressors/pumps: $W_{u,\text{act}} > W_{\text{rev}}$ (more input required)

Irreversibility (per unit mass) can be related to entropy generation $S_{\text{gen}}$:
$$
I = T_0 S_{\text{gen}}
$$

- $T_0$ = environment temperature.  
- $S_{\text{gen}} > 0$ for real processes (2nd law), so $I > 0$.

---

## Reversible and Irreversible Work Examples

### 1. Reversible adiabatic expansion of ideal gas (closed system)

For a reversible adiabatic (isentropic) process:
- $Q = 0$, $S = \text{const}$, $pV^\gamma = \text{const}$.

Work (per mole):
$$
W_{\text{rev}} = \frac{p_2 V_2 - p_1 V_1}{1 - \gamma}
= \frac{R (T_2 - T_1)}{1 - \gamma}
$$

This is both **actual** and **reversible** work if the process is truly reversible (no irreversibilities).

### 2. Irreversible expansion with same end states

If the same initial and final states are reached via an irreversible path (e.g., with friction), the actual useful work $W_u$ will be **less** than $W_{\text{rev}}$:

$$
I = W_{\text{rev}} - W_u > 0
$$

For heat engines operating between $T_H$ and $T_C$, the **Carnot efficiency** gives the reversible benchmark; any real engine has lower efficiency, and the difference directly reflects irreversibilities.

---

# Quick Summary Table: Key Equations

| Topic                    | Key equation(s)                                                                 |
|--------------------------|----------------------------------------------------------------------------------|
| Ideal gas law           | $pV = nRT$                                                                       |
| Isothermal work         | $W = nRT \ln(V_2/V_1)$                                                           |
| Adiabatic ideal gas     | $pV^\gamma = \text{const}$, $TV^{\gamma-1} = \text{const}$                      |
| Carnot efficiency       | $\eta_{\text{Carnot}} = 1 - T_C/T_H$                                             |
| Rankine net work        | $w_{\text{net}} = (h_3 - h_4) - (h_2 - h_1)$                                    |
| Rankine efficiency      | $\eta_{\text{Rankine}} = \dfrac{(h_3 - h_4) - (h_2 - h_1)}{h_3 - h_2}$          |
| Useful work             | $W_u = W - p_0 (V_2 - V_1)$                                                      |
| Irreversibility         | $I = W_{\text{rev,out}} - W_{u,\text{out}} = T_0 S_{\text{gen}}$                |
| Exergy (simple system)  | $X = (U-U_0) + p_0 (V-V_0) - T_0 (S-S_0)$                                       |

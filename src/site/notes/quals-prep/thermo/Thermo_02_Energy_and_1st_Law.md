---
{"dg-publish":true,"permalink":"/quals-prep/thermo/thermo-02-energy-and-1st-law/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

## Key definitions

- **Internal energy, $U$**  
  Energy associated with microscopic modes (translation, rotation, vibration, electronic, etc.) of molecules.

- **Enthalpy, $H$**  
  Defined as
  $$
  H = U + PV
  $$
  Convenient for open systems with flow work.

- **Work, $W$** and **heat, $Q$**  
  Energy transfers across the system boundary:
  - Work: organized transfer (e.g. shaft work, electrical work).  
  - Heat: transfer driven solely by temperature difference.

- **Flow work** (open systems)  
  $PV$ work associated with pushing mass into or out of a control volume.

- **First law of thermodynamics**  
  Energy is conserved: change in energy of a system equals net heat added minus net work done by the system.

---

## Core formulas

### 1. Closed system (simple compressible)

Differential form:
$$
\delta Q - \delta W = dU
$$

For only boundary (P–V) work:
$$
\delta W = P\,dV
$$
so
$$
\delta Q = dU + P\,dV
$$

For a finite process:
$$
Q - W = \Delta U
$$

### 2. Open system (steady flow, one inlet, one outlet)

Total energy per unit mass:
$$
e = u + \frac{V^2}{2} + gz
$$

Steady‑flow energy equation:
$$
\dot Q - \dot W_s = \dot m
\left[
\left(h_2 - h_1\right)
+ \frac{V_2^2 - V_1^2}{2}
+ g(z_2 - z_1)
\right]
$$

Common simplifications:

- Pumps/turbines: focus on $h$ and shaft work.  
- Heat exchangers: neglect shaft work, focus on $Q$ and enthalpy change.  
- Throttling valves: $\dot Q \approx 0$, $\dot W_s \approx 0$, negligible kinetic/potential changes $\Rightarrow h_1 \approx h_2$.

### 3. Specific heats and enthalpy changes (approximate)

For ideal gases:
$$
\Delta h \approx c_p \Delta T,\quad \Delta u \approx c_v \Delta T
$$

For incompressible liquids:
$$
\Delta h \approx \Delta u \approx c_p \Delta T
$$

---

## Interesting concepts

- **Shaft work vs flow work**  
  In open systems, enthalpy $h$ already includes internal energy plus flow work; shaft work is what appears explicitly in the steady‑flow equation.

- **Energy vs temperature**  
  Temperature is often proportional to internal energy for simple systems but not always (phase changes, mixtures).

- **Adiabatic vs isothermal**  
  Adiabatic: $Q = 0$ but temperature can change via work; isothermal: $T$ constant but heat and work can both be nonzero.

---


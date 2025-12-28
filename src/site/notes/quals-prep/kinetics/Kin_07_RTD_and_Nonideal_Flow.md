---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/kin-07-rtd-and-nonideal-flow/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---

## Key definitions

- **Residence time distribution (RTD)**  
  Describes how long fluid elements spend in the reactor.

- **$E(t)$ function**  
  Probability density of residence time:  
  $E(t)\,dt$ = fraction of exiting fluid with residence time between $t$ and $t + dt$.  
  Normalization:  
  $$
  \int_0^\infty E(t)\,dt = 1
  $$

- **Mean residence time, $\bar t$**  
  $$
  \bar t = \int_0^\infty t\,E(t)\,dt
  $$

- **Space time, $\tau$**  
  For a single‑phase reactor with volume $V$ and volumetric flow $\dot V$:  
  $$
  \tau = \frac{V}{\dot V}
  $$

- **Variance of RTD, $\sigma_t^2$**  
  Measure of spread:
  $$
  \sigma_t^2 = \int_0^\infty (t - \bar t)^2 E(t)\,dt
  $$

- **Ideal reactor RTDs**  
  - Ideal CSTR: $E(t) = \dfrac{1}{\tau} e^{-t/\tau}$, $t \ge 0$.  
  - Ideal PFR: $E(t) = \delta(t - \tau)$ (all fluid elements have the same residence time).

---
![../src/Pasted image 20251224143547.png|700](/img/user/quals-prep/src/Pasted%20image%2020251224143547.png)

## Core formulas

### 1. Conversion and RTD (single reaction, first order, concept form)

For a first‑order reaction with rate constant $k$, nonideal reactor conversion can be written as:
$$
X = 1 - \int_0^\infty e^{-k t} E(t)\,dt
$$
This is the exit‑age distribution weighted by the decay of $A$ along each trajectory.

### 2. Tanks‑in‑series model

A nonideal reactor approximated as $N$ equal‑volume CSTRs in series:

- RTD:
  $$
  E(t) = \frac{t^{N-1}}{(N-1)!} \left(\frac{N}{\tau}\right)^N
  \exp\!\left(-\frac{N t}{\tau}\right)
  $$

- Mean residence time: $\bar t = \tau$.  
- Variance: $\sigma_t^2 = \tau^2 / N$.  

Limiting behavior:

- $N = 1$: one CSTR.  
- $N \to \infty$: approaches PFR.

### 3. Dispersion model (brief memory form)

For a tubular reactor with axial dispersion, dimensionless dispersion parameter:
$$
\text{Pe} = \frac{u L}{D_{\text{ax}}}
$$
where $u$ is velocity, $L$ length, $D_{\text{ax}}$ axial dispersion coefficient.

- Large Pe $\Rightarrow$ close to PFR.  
- Small Pe $\Rightarrow$ strong back‑mixing (approaches CSTR behavior).

---

## Interesting concepts

- **Diagnosing nonideal flow**  
  Comparing experimental $E(t)$ to ideal CSTR or PFR shapes reveals dead zones, bypassing, or channeling.

- **Effect on conversion**  
  For a given mean residence time and first‑order reaction, increasing variance (more mixing/back‑mixing) generally lowers conversion relative to PFR.

- **Using simple models**  
  RTD data can be fit with tanks‑in‑series (parameter $N$) or dispersion (parameter Pe) models, then combined with kinetics to predict conversion without full CFD.

- **Short‑circuiting and dead volume**  
  Early peaks in $E(t)$ suggest bypassing/short‑circuiting; long tails suggest stagnant regions with very long residence times.

---


---
{"dg-publish":true,"permalink":"/quals-prep/transport/trans-04-mass-transfer/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true}
---

## Key definitions

- **Fick’s first law (steady diffusion)**  
  $$
  J_A = -D_{AB} \frac{dC_A}{dx}
  $$
  where $J_A$ is molar flux relative to a stationary frame.
- **[[quals-prep/transport/z_Diffusion_regimes\|z_Diffusion_regimes]]**

- **Molar flux with convection**  
  $$
  N_A = J_A + C_A v
  $$

- **Mass transfer coefficient, $k_c$**  
  Relates flux to concentration difference across a film:
  $$
  N_A = k_c (C_{A,b} - C_{A,s})
  $$

- **Dimensionless groups**  
  - Schmidt: $\displaystyle \text{Sc} = \frac{\mu}{\rho D}$  
  - Sherwood: $\displaystyle \text{Sh} = \frac{k_c L}{D}$  

---

## Core formulas

### 1. Steady diffusion through a stagnant film

Film thickness $L$, concentrations $C_{A,1}$ and $C_{A,2}$ at faces, B stagnant:

For dilute A:
$$
N_A = -D_{AB} \frac{C_{A,2} - C_{A,1}}{L}
$$

Define:
$$
k_c = \frac{D_{AB}}{L}
$$
so $N_A = k_c (C_{A,1} - C_{A,2})$.

### 2. Equimolar counter‑diffusion (memory form)

If $N_A = -N_B$ and no net flow:
$$
N_A = -D_{AB} \frac{C_{A,2} - C_{A,1}}{L}
$$
same structure as stagnant film for ideal gases.

### 3. Typical external mass‑transfer correlations

Spherical particle, gas–solid or gas–liquid:
$$
\text{Sh} = 2 + 0.6 \text{Re}^{1/2} \text{Sc}^{1/3}
$$

Flat plate (developing boundary layer, order of magnitude):
$$
\text{Sh}_x \sim 0.332\, \text{Re}_x^{1/2} \text{Sc}^{1/3}
$$

---

## Interesting concepts

- **Film theory picture**  
  A thin stagnant film at the surface controls resistance; bulk is well mixed. #2025_Jan 
 ![../src/Pasted image 20251223143749.png](/img/user/quals-prep/src/Pasted%20image%2020251223143749.png)

- **Analogy with heat transfer**  
  Sherwood and Schmidt play roles analogous to Nusselt and Prandtl; correlations often mirror heat‑transfer forms.

- **Interfacial conditions**  
  At gas–liquid or liquid–solid interfaces, surface concentration $C_{A,s}$ often comes from equilibrium (Henry’s law, solubility).

---
# Mass Transfer Resistance in Series
#2025_Jan 

Mass transfer resistance quantifies how strongly a system opposes mass transport; it is defined as driving force divided by flux.  
- Generic definition: $R = \dfrac{\text{driving force}}{N}$, where $N$ is molar flux.  
- Analogous to Ohmic resistance: larger $R$ means slower mass transfer for a given driving force.  

---

## Resistances in Series: Concept

When a species moves through multiple layers (e.g., gas film → interface → liquid film → porous solid), each layer contributes a resistance, and these add in series.  

- Total resistance:
  $$
  \frac{1}{R_{\text{tot}}} = \sum_i \frac{1}{R_i}
  $$
- Overall flux from bulk 1 to bulk 2:
  $$
  N_A = \dfrac{\Delta(\text{overall driving force})}{R_{\text{tot}}}
  $$

If one $R_i \gg$ others, that step is **rate-controlling** and limits the overall mass transfer rate.  

---

## Two-Film Theory (Gas–Liquid)

In gas–liquid systems, a thin film on each side of the interface controls diffusion, while the bulks are well mixed.  

- Gas film:
  $$
  N_A = k_G \left(p_{A,G} - p_{A,i}\right)
  $$
- Liquid film:
  $$
  N_A = k_L \left(C_{A,i} - C_{A,L}\right)
  $$
  where $k_G, k_L$ are individual film mass transfer coefficients.  

Interface equilibrium links $p_{A,i}$ and $C_{A,i}$, usually via Henry’s law:  
$$
p_{A,i} = m\, C_{A,i}
$$
where $m$ is the equilibrium slope.  

---

## Overall Gas-Phase Coefficient $K_G$

Define an overall gas-phase driving force between gas bulk and *equilibrium* with liquid bulk.  

- Overall flux:
  $$
  N_A = K_G \left(p_{A,G} - p_{A,L}^*\right)
  $$
  where $p_{A,L}^*$ is the gas-phase partial pressure in equilibrium with $C_{A,L}$.  

Relation between overall and individual coefficients:  
$$
\frac{1}{K_G} = \frac{1}{k_G} + \frac{m}{k_L}
$$  

Here:
- $\dfrac{1}{k_G}$ is the gas-film resistance.  
- $\dfrac{m}{k_L}$ is the liquid-film resistance expressed in gas-phase units.  

---

## Overall Liquid-Phase Coefficient $K_L$

Alternatively, use liquid-phase driving force between liquid bulk and *equilibrium* with gas bulk.  

- Overall flux:
  $$
  N_A = K_L \left(C_{A,G}^* - C_{A,L}\right)
  $$
  where $C_{A,G}^*$ is the liquid concentration in equilibrium with $p_{A,G}$.  

Relation between overall and individual coefficients:  
$$
\frac{1}{K_L} = \frac{1}{k_L} + \frac{1}{m\,k_G}
$$  

Again:
- $\dfrac{1}{k_L}$ is the liquid-film resistance.  
- $\dfrac{1}{m\,k_G}$ is the gas-film resistance written in liquid-phase units.  

---

## Fractional Resistances and Rate Control

Because resistances add in series, each film’s contribution to the total resistance is easy to quantify.  

- Gas-side fraction (using $K_G$):
  $$
  \text{fraction gas} = \frac{1/k_G}{1/K_G} = \frac{K_G}{k_G}
  $$
- Liquid-side fraction (using $K_G$):
  $$
  \text{fraction liquid} = \frac{m/k_L}{1/K_G}
  $$
  with $\text{fraction gas} + \text{fraction liquid} = 1$.  

If $1/k_G \gg m/k_L$, gas film controls; if $m/k_L \gg 1/k_G$, liquid film controls.  

---

## Extended Series: Films + Porous Solid

For diffusion through gas film, liquid film, and a porous catalyst or membrane, resistances still add in series.  

- Example total resistance:
  $$
  R_{\text{tot}} = \frac{1}{k_G} + \frac{m}{k_L} + R_{\text{pore}}
  $$  

- Porous solid mass transfer can be described by an effective diffusivity $D_{\text{eff}}$ over a characteristic length $L$:
  $$
  R_{\text{pore}} \sim \frac{L}{D_{\text{eff}}}
  $$  

---

## Design/Analysis Implications

- To increase $N_A$ at fixed driving force, reduce the dominant resistance (increase the corresponding $k$ or $D_{\text{eff}}$).  
- Overall coefficients $K_G$ or $K_L$ allow writing a single flux expression using measurable bulk compositions, avoiding explicit interface terms.  
---
# Partition Coefficient

The partition coefficient describes how a solute distributes itself between two immiscible phases (typically an organic phase and an aqueous phase) at equilibrium. It is a measure of relative solubility and thus of how much the solute “prefers” one phase over the other.

## Definition

For a solute X distributing between phase 1 and phase 2 at constant temperature:
$$
K = \frac{C_1}{C_2}
$$
where:
- $C_1$ = equilibrium concentration of X in phase 1  
- $C_2$ = equilibrium concentration of X in phase 2  

This is often written for an organic (org) and aqueous (aq) phase as:
$$
K = \frac{C_{\text{org}}}{C_{\text{aq}}}
$$


## Thermodynamic Relation

The partition coefficient can be related to the standard Gibbs free energy difference of transferring the solute between the two phases:
$$
\Delta G^\circ = -RT \ln K
$$
A larger $K$ (solute favoring phase 1) corresponds to a more negative $\Delta G^\circ$ for transfer from phase 2 to phase 1.

## Practical Notes

- Assumes immiscible phases and equilibrium.  
- If the solute ionizes or associates in one phase, the simple $K$ may no longer be constant and an effective “distribution coefficient” (including all forms) is used instead.  
---

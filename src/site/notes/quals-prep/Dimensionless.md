---
{"dg-publish":true,"permalink":"/quals-prep/dimensionless/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

## 1. Flow and momentum

### Reynolds number, Re

- **Definition**
  $$
  \text{Re} = \frac{\rho v L}{\mu}
  $$
- **Meaning**  
	- $\large{\frac{\text(inertial forces)}{\text(viscous forces)}}$ #2024_Jan 
	- sets laminar vs turbulent regime and structure of velocity field.
- **Use**  
  Pipe and channel flow, external flow, entry to almost all transport correlations.
- **Connections**  
  - [[quals-prep/transport/Trans_02_Momentum_Transport\|Trans_02_Momentum_Transport]] — friction factor, pressure drop.  
  - [[quals-prep/transport/Trans_03_Heat_Transfer\|Trans_03_Heat_Transfer]], [[quals-prep/transport/Trans_04_Mass_Transfer\|Trans_04_Mass_Transfer]] — appears inside Nu and Sh correlations.  

### Fanning friction factor, $f$

- **Definition (pipe flow)**
  $$
  f = \frac{\Delta P\, D}{2 L \rho v^2}
  $$
- **Meaning**  
  Dimensionless pressure drop.
- **Connections**  
  - [[quals-prep/transport/Trans_02_Momentum_Transport\|Trans_02_Momentum_Transport]] — Moody chart and head loss in piping networks.  

### Froude number, Fr (optional memory)

- **Definition**
  $$
  \text{Fr} = \frac{v^2}{g L}
  $$
- **Meaning**  
  Inertia / gravity; important in free‑surface, open‑channel flows and mixing tanks.  

---

## 2. Heat transfer

### Prandtl number, Pr

- **Definition**
  $$
  \text{Pr} = \frac{c_p \mu}{k}
  $$
- **Meaning**  
  Momentum diffusivity / thermal diffusivity; compares thickness of velocity and thermal boundary layers.
- **Connections**  
  - [[quals-prep/transport/Trans_03_Heat_Transfer\|Trans_03_Heat_Transfer]] — Nu = $f(\text{Re},\text{Pr})$ in convection.  

### Nusselt number, Nu

- **Definition**
  $$
  \text{Nu} = \frac{h L}{k}
  $$
- **Meaning**  
  Convective / conductive heat transfer across a boundary layer.
- **Use**  
  $h = \dfrac{\text{Nu}\,k}{L}$ once Nu is obtained from correlations.
- **Connections**  
  - [[quals-prep/transport/Trans_03_Heat_Transfer\|Trans_03_Heat_Transfer]] — internal and external convection.  
  - [[quals-prep/kinetics/Kin_05_Nonisothermal_Reactors\|Kin_05_Nonisothermal_Reactors]] — wall heat transfer in reactors.  

### Biot number (heat), $\text{Bi}_h$

- **Definition**
  $$
  \text{Bi}_h = \frac{h L_c}{k}
  $$
- **Meaning**  
  Internal conduction resistance / external convection resistance.
- **Use**  
  - $\text{Bi}_h \ll 1$: lumped capacitance (uniform temperature inside solid).  
  - $\text{Bi}_h \gg 1$: significant internal gradients.
- **Connections**  
  - [[quals-prep/transport/Trans_03_Heat_Transfer\|Trans_03_Heat_Transfer]] — transient heating/cooling.  
  - [[quals-prep/kinetics/Kin_05_Nonisothermal_Reactors\|Kin_05_Nonisothermal_Reactors]], [[quals-prep/transport/Trans_05_Transport_in_Reacting_Systems\|Trans_05_Transport_in_Reacting_Systems]] — pellet hot spots.  

### Fourier number (heat), Fo

- **Definition**
  $$
  \text{Fo} = \frac{\alpha t}{L^2},\quad \alpha = \frac{k}{\rho c_p}
  $$
- **Meaning**  
  Dimensionless time in transient conduction (how deeply heat has penetrated).  

### Grashof and Rayleigh (free convection, memory)

- **Grashof**
  $$
  \text{Gr} = \frac{g \beta \Delta T L^3}{\nu^2}
  $$
- **Rayleigh**
  $$
  \text{Ra} = \text{Gr} \,\text{Pr}
  $$
- **Meaning**  
  Buoyancy / viscous and overall strength of natural convection.

---

## 3. Mass transfer

### Schmidt number, Sc

- **Definition**
  $$
  \text{Sc} = \frac{\mu}{\rho D} = \frac{\nu}{D}
  $$
- **Meaning**  
  Momentum diffusivity / mass diffusivity; compares thickness of velocity and concentration boundary layers.
$$ \frac{\text{viscous/momentum diffusion rate}}{\text{mass diffusion rate}} $$
- **Connections**  
  - [[quals-prep/transport/Trans_04_Mass_Transfer\|Trans_04_Mass_Transfer]] — appears in Sh correlations.  

### Sherwood number, Sh

- **Definition**
  $$
  \text{Sh} = \frac{k_c L}{D}
  $$
- **Meaning**  
  Convective / diffusive mass transfer across a boundary layer.
- **Use**  
  $k_c = \dfrac{\text{Sh}\,D}{L}$ from correlations.
- **Connections**  
  - [[quals-prep/transport/Trans_04_Mass_Transfer\|Trans_04_Mass_Transfer]], [[quals-prep/transport/Trans_05_Transport_in_Reacting_Systems\|Trans_05_Transport_in_Reacting_Systems]], [[quals-prep/kinetics/Kin_06_Heterogeneous_Catalysis_Basics\|Kin_06_Heterogeneous_Catalysis_Basics]].  

### Biot number (mass), $\text{Bi}_m$

- **Definition**
  $$
  \text{Bi}_m = \frac{k_c R_p}{D_{\text{eff}}}
  $$
- **Meaning**  
  External film resistance / internal diffusion resistance in particles.
- **Connections**  
  - [[quals-prep/transport/Trans_05_Transport_in_Reacting_Systems\|Trans_05_Transport_in_Reacting_Systems]], [[quals-prep/kinetics/Kin_06_Heterogeneous_Catalysis_Basics\|Kin_06_Heterogeneous_Catalysis_Basics]].  

### Fourier number (mass), $\text{Fo}_m$

- **Definition**
  $$
  \text{Fo}_m = \frac{D t}{L^2}
  $$
- **Meaning**  
  Dimensionless time for diffusion problems (penetration depth vs size).  

### Lewis number, Le

- **Definition**
  $$
  \text{Le} = \frac{\alpha}{D} = \frac{\text{Sc}}{\text{Pr}}
  $$
- **Meaning**  
  Thermal diffusivity / mass diffusivity; important in simultaneous heat–mass transfer (evaporation, drying).  

---

## 4. Convection–diffusion and mixing

### Péclet number, Pe

- **Definition (axial transport)**
  $$
  \text{Pe} = \frac{v L}{D_{\text{ax}}}
  $$
- **Equivalent forms**
  - Heat: $\text{Pe}_h = \text{Re}\,\text{Pr}$.  
  - Mass: $\text{Pe}_m = \text{Re}\,\text{Sc}$. #2025_Jan 
- **Meaning**  
  Convection / axial diffusion; large Pe → convection‑dominated, small Pe → diffusion‑dominated. 
#### Gas vs Liquid

| Aspect                           | Gas phase                                                   | Liquid phase                                              |
| -------------------------------- | ----------------------------------------------------------- | --------------------------------------------------------- |
| Typical molecular diffusivity, D | High (~10⁻⁵ m²/s)                                           | Low (~10⁻⁹ to 10⁻¹⁰ m²/s)                                 |
| Resulting mass Pe for same v, L  | Lower Pe (axial diffusion more significant)                 | Much higher Pe (convection dominates; diffusion weaker)   |
| Axial dispersion importance      | More important; dispersion can noticeably broaden RTD       | Often small except in highly mixed or turbulent systems   |
| Boundary-layer thickness         | Thicker concentration boundary layer at given Re            | Thinner concentration boundary layer at same Re           |
| Typical Sc = ν/D                 | Sc ~ 1 (or order 1)                                         | Sc ≫ 1 (10²–10³ common)                                   |
| Interpretation of Pe = Re·Sc     | Pe not extremely large; both advection and diffusion matter | Pe can be very large; plug‑flow assumption often stronger |
| Design implication               | Need to consider axial dispersion and back‑mixing in models | Can often neglect axial diffusion; use ideal PFR models   |


- **Connections**  
  - [[quals-prep/kinetics/Kin_07_RTD_and_Nonideal_Flow\|Kin_07_RTD_and_Nonideal_Flow]] — dispersion model and RTD shape.  
  - [[quals-prep/transport/Trans_02_Momentum_Transport\|Trans_02_Momentum_Transport]], [[quals-prep/transport/Trans_04_Mass_Transfer\|Trans_04_Mass_Transfer]].  

---

## 5. Reacting systems and reactors

### Damköhler number, Da

- **Definition (generic)**
  $$
  \text{Da} = \frac{\text{reaction timescale}}{\text{transport timescale}}
  \sim \frac{k C^{n-1} L}{v}
  $$
  (exact expression depends on reactor and kinetics).
- **Meaning**  
  Reaction / transport rate; classifies reaction‑controlled vs transport‑controlled operation.
- **Connections**  
  - [[quals-prep/transport/Trans_05_Transport_in_Reacting_Systems\|Trans_05_Transport_in_Reacting_Systems]], [[quals-prep/transport/Trans_06_Links_to_Thermo_and_Kinetics\|Trans_06_Links_to_Thermo_and_Kinetics]].  
  - [[quals-prep/kinetics/Kin_03_Batch_CSTR_PFR\|Kin_03_Batch_CSTR_PFR]], [[quals-prep/kinetics/Kin_05_Nonisothermal_Reactors\|Kin_05_Nonisothermal_Reactors]].  

### Thiele modulus, $\Phi$

- **Definition (first‑order, spherical pellet)**
  $$
  \Phi = R_p \sqrt{\frac{k}{D_{\text{eff}}}}
  $$
- **Meaning**  
  Intrinsic reaction rate / internal diffusion rate in porous catalysts.
- **Connections**  
  - [[quals-prep/kinetics/Kin_06_Heterogeneous_Catalysis_Basics\|Kin_06_Heterogeneous_Catalysis_Basics]], [[quals-prep/transport/Trans_05_Transport_in_Reacting_Systems\|Trans_05_Transport_in_Reacting_Systems]].  

### Effectiveness factor, $\eta$

- **Definition**
  $$
  \eta = \frac{\text{actual rate in particle}}{\text{rate at } C_{A,s},T_s \text{ everywhere}}
  $$
- **Meaning**  
  Dimensionless measure of diffusion/heat limitations at particle scale.
- **Connections**  
  - Used with $\Phi$ and Biot numbers in catalyst and reactor design.  

### Stanton number (optional)

- **Heat transfer**
  $$
  \text{St}_h = \frac{h}{\rho c_p v}
  $$
- **Mass transfer**
  $$
  \text{St}_m = \frac{k_c}{v}
  $$
- **Meaning**  
  Convective transfer / convective capacity; often appears in j‑factor analogies.
---

## 7. Big‑picture grouping

- **Momentum/flow:** Re, Fr, Ma, $f$, Kn.  
- **Heat:** Pr, Nu, Bi$_h$, Fo, Gr, Ra, St$_h$.  
- **Mass:** Sc, Sh, Bi$_m$, Fo$_m$, Le, St$_m$.  
- **Convection–diffusion/mixing:** Pe.  
- **Reactors/kinetics:** Da, $\Phi$, $\eta$.  

Related notes:

- [[quals-prep/transport/Trans_01_Overview_and_Tools\|Trans_01_Overview_and_Tools]], [[quals-prep/transport/Trans_06_Links_to_Thermo_and_Kinetics\|Trans_06_Links_to_Thermo_and_Kinetics]]  
- [[quals-prep/kinetics/Kin_05_Nonisothermal_Reactors\|Kin_05_Nonisothermal_Reactors]], [[quals-prep/kinetics/Kin_06_Heterogeneous_Catalysis_Basics\|Kin_06_Heterogeneous_Catalysis_Basics]], [[quals-prep/kinetics/Kin_07_RTD_and_Nonideal_Flow\|Kin_07_RTD_and_Nonideal_Flow]]  
- [[quals-prep/thermo/Thermo_03_Second_Law_and_Entropy\|Thermo_03_Second_Law_and_Entropy]], [[quals-prep/thermo/Thermo_08_Links_to_Kinetics_and_Transport\|Thermo_08_Links_to_Kinetics_and_Transport]]  

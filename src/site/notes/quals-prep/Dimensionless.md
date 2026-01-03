---
{"dg-publish":true,"permalink":"/quals-prep/dimensionless/","dgHomeLink":true,"dgShowLocalGraph":true,"dgEnableSearch":true,"dgShowToc":true,"dgShowTags":true}
---


[[quals-prep/Dimensionless#Some more Dimensionless Groups!\|Some more special ones]] at the end of this page
## 1. Flow and momentum

### Reynolds number, Re
- The **Reynolds number** essentially answers this question: “Will this fluid flow in smooth layers or will it mix chaotically?”

- **Definition**
  $$
  \text{Re} = \frac{\rho v L}{\mu}
  $$
- **Meaning**  
	- $\large{\frac{\text(inertial forces)}{\text(viscous forces)}}$ #2024_Jan 
	- sets laminar vs turbulent regime and structure of velocity field.
	- **viscous force** is the internal resistance of the fluid to flow and deformation caused by the friction between adjacent fluid layers moving at different velocities. It opposes fluid motion, dampening turbulence and creating velocity gradients (like the boundary layer) near reactor walls
	- **Characteristic Length (L)**:
	    - For pipes: Use the pipe diameter
	    - For non-circular ducts: Use the hydraulic diameter $D_H=\frac{4\cdot A}{P_{\text{wetted}}}$
	    - For flow over flat plates: Use the distance from the leading edge
		    ![Pasted image 20260103160801.png](/img/user/quals-prep/src/Pasted%20image%2020260103160801.png)
	    - For flow around objects: Use the object’s characteristic dimension
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
  - [[quals-prep/transport/Trans_02_Momentum_Transport\|Trans_02_Momentum_Transport]] — [[quals-prep/transport/Trans_02_Momentum_Transport#Interesting concepts\|Moody Chart]]and head loss in piping networks.  

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
	![Pasted image 20260103161034.png](/img/user/quals-prep/src/Pasted%20image%2020260103161034.png)
- **Meaning**  
  - Momentum diffusivity $\nu$ / thermal diffusivity $\alpha$; 
  - Compares thickness of velocity and thermal boundary layers.
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

---

## Some more Dimensionless Groups!
### 1. Hatta Number Ha (Brief)
#2024_Jan #2019_Jan 
#### Physical Meaning

- Ha compares **characteristic reaction rate in the liquid film** to **diffusive transport across the film**.
- Low Ha → reaction is slow relative to diffusion (reaction in bulk).
- High Ha → reaction is fast relative to diffusion (reaction confined to film, “fast reaction” regime).

---

#### Typical Definitions

##### General (m,n)-order reaction in A and B

For:
$$
r_A = k_{m,n} C_A^m C_B^n
$$

A generalized Hatta number is:
$$
Ha = \frac{\sqrt{\frac{2}{m+1}\,k_{m,n}\,C_{A,i}^{\,m-1}\,C_{B,bulk}^n\,D_A}}{k_L}
$$
with $C_{A,i}$ the interfacial concentration of A. 

---

#### Regimes (Qualitative)

- $Ha \ll 1$  
  - Reaction slow; essentially **physical absorption** plus slow reaction in bulk.
- $Ha \approx 1$  
  - Reaction and diffusion comparable; partial enhancement of mass transfer.
- $Ha \gg 1$ (often $Ha > 2$)  
  - **Fast reaction regime**; reaction occurs within the film, bulk A ≈ 0, and flux is proportional to $k_L C_{A,i} Ha$.

Ha is essentially the **square root of a Damköhler number** based on the liquid film and is analogous to the **Thiele modulus** for porous catalysts. 

### 2. Weber number
The **Weber number** measures the ratio of **inertial forces** to **surface tension forces** in a flowing fluid, and is key for droplet/bubble breakup, sprays, and multiphase flows.

For a characteristic length $L$ (e.g., droplet diameter), fluid density $\rho$, velocity $u$, and surface tension $\sigma$:

$$
\mathrm{We} = \frac{\rho u^2 L}{\sigma}
$$

Interpretation:

- **Inertial pressure scale**: $\rho u^2$  
- **Capillary (Laplace) pressure scale**: $\sigma / L$  

So:
$$
\mathrm{We} = \frac{\rho u^2}{\sigma/L}
$$
#### Physical Meaning

- $\mathrm{We} \ll 1$: Surface tension dominates. Droplets/bubbles tend to stay spherical and resist deformation or breakup.  
- $\mathrm{We} \sim 1$: Inertial and surface tension forces comparable; deformation becomes significant.  
- $\mathrm{We} \gg 1$: Inertia dominates; droplets, jets, or bubbles can strongly deform and break up into smaller fragments.

In sprays, atomization, and emulsification, critical Weber numbers indicate onset of different **breakup regimes** (e.g., vibrational, bag, shear/strip breakup).

---
#### Typical Usage

- Designing and analyzing **spray nozzles**, **atomizers**, **emulsification processes**.  
- Classifying **jet breakup** and **droplet breakup** in crossflow.  
- Comparing systems at different scales: if $\mathrm{We}$ is matched, **inertial vs capillary balance** is similar (dynamic similarity for these forces).

Remember:  
- Large $u$, large $L$, or large $\rho$ → higher $\mathrm{We}$ → more deformation/breakup.  
- Large $\sigma$ → lower $\mathrm{We}$ → more stable interfaces.

### 3. Capillary Number (Ca) 

#### Definition

For a fluid of viscosity $\mu$, characteristic velocity $U$, and interfacial tension $\sigma$:

$$
\mathrm{Ca} = \frac{\mu U}{\sigma}
$$

- Viscous stress scale: $\mu U/L$  
- Capillary pressure scale: $\sigma / L$  

So the ratio of characteristic viscous stress to capillary stress is:

$$
\frac{\mu U/L}{\sigma/L} = \frac{\mu U}{\sigma} = \mathrm{Ca}
$$

Units cancel → dimensionless.

---

#### Physical Interpretation

- $\mathrm{Ca} \ll 1$  
  - Surface tension dominates.  
  - Interfaces tend to maintain curvature; droplets/bubbles resist deformation, strong capillary effects (meniscus, capillary rise, etc.).

- $\mathrm{Ca} \sim 1$  
  - Viscous and capillary forces comparable; interface deforms significantly.

- $\mathrm{Ca} \gg 1$  
  - Viscous forces dominate.  
  - Surface tension becomes relatively unimportant; interfaces are strongly stretched and deformed by the flow.

---

#### Relation to Other Dimensionless Groups

Using Reynolds number $\mathrm{Re} = \rho U L / \mu$ and Weber number $\mathrm{We} = \rho U^2 L / \sigma$:

$$
\mathrm{Ca} = \frac{\mu U}{\sigma}
= \frac{\mu}{\rho U L} \cdot \frac{\rho U^2 L}{\sigma}
= \frac{\mathrm{We}}{\mathrm{Re}}
$$

So:

- $\mathrm{Re}$: inertia vs viscosity  
- $\mathrm{We}$: inertia vs surface tension  
- $\mathrm{Ca}$: viscosity vs surface tension

---

#### Typical Uses

- **Microfluidics / droplet generation**:  
  - Controls transition between dripping, jetting, and stable slug/Taylor flow.

- **Multiphase flows in porous media** (enhanced oil recovery, soil flow):  
  - $\mathrm{Ca}$ used to judge whether viscous forces can overcome capillary trapping.

- **Coating, wetting, and dynamic contact angles**:  
  - $\mathrm{Ca}$ appears in correlations for moving contact lines and film thickness.

---

#### Summary

- Formula: $\displaystyle \mathrm{Ca} = \mu U / \sigma$  
- Low Ca → capillary-dominated; high Ca → viscous-dominated.  
- Helps classify and scale flows where **viscosity–surface-tension balance** controls interface shape and dynamics.

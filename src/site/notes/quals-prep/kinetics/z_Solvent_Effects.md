---
{"dg-publish":true,"permalink":"/quals-prep/kinetics/z-solvent-effects/","dgHomeLink":true,"dgShowLocalGraph":true,"dgShowToc":true}
---

#2024_Jan [[quals-prep/kinetics/Kin_06_Heterogeneous_Catalysis_Basics\|Kin_06_Heterogeneous_Catalysis_Basics]]
Solvents influence reaction rates by stabilizing or destabilizing reactants, transition states, and intermediates through solvation, changing the effective activation free energy and sometimes the reaction mechanism itself.

---

## Free Energy and Solvation

The rate constant $k$ is related to the activation free energy $\Delta G^\ddagger$:
$$
k \propto e^{-\Delta G^\ddagger / RT}
$$

Solvent changes $\Delta G^\ddagger$ via differential solvation:

- If the transition state (TS) is **stabilized more** than the reactants, $\Delta G^\ddagger$ decreases → rate increases.  
- If reactants are stabilized more than the TS, $\Delta G^\ddagger$ increases → rate decreases.  

$\Delta G^\ddagger$ includes both enthalpic (specific interactions, H-bonding) and entropic (ordering of solvent) contributions.

---

## Polar vs Nonpolar Solvents

- **Polar solvents**:
  - Strongly stabilize charged or highly polar species (ions, zwitterions, polar TS).  
  - Often accelerate reactions with ionic TS (e.g., SN1, certain polar rearrangements).  

- **Nonpolar solvents**:
  - Provide weaker stabilization of charges and dipoles.  
  - Can favor mechanisms/TS with less charge separation (e.g., SN2 vs SN1, radical pathways).

Rule of thumb: a solvent that better stabilizes the *more polar/charged* state (reactants vs TS) will shift the rate accordingly.

---

## Protic vs Aprotic Solvents

**Protic solvents** (e.g., water, alcohols):

- Donate H-bonds and solvate anions strongly via hydrogen bonding.  
- Strong solvation of nucleophiles/anions can **lower their reactivity** (more tightly “caged” by solvent).  
- Often favor unimolecular, ionization-based mechanisms (e.g., SN1, E1) by stabilizing carbocations and leaving groups.

**Polar aprotic solvents** (e.g., DMSO, DMF, acetonitrile):

- High dielectric constant but poor H-bond donation to anions; cations are more strongly solvated than anions.  
- Anions/nucleophiles are “freer” and more reactive → often **increase** rates of bimolecular reactions like SN2.  

Thus, solvent choice can flip the relative rates of different mechanisms.

---

## Dielectric Constant and Ionic Reactions

The dielectric constant $\varepsilon$ measures the solvent’s ability to screen electrostatic interactions.

Effects:

- High $\varepsilon$:
  - Reduces Coulombic attraction/repulsion.  
  - Stabilizes separated ions, facilitating ionization and charge-separated TSs.  

- Low $\varepsilon$:
  - Less screening; ion pairs are more tightly bound, making ionization steps slower.  

For a reaction generating charge in the TS (e.g., bond heterolysis), increasing solvent polarity (higher $\varepsilon$) lowers $\Delta G^\ddagger$ and increases the rate.

---

## Specific Solvent–Solute Interactions

Beyond bulk polarity:

- **Hydrogen bonding**:
  - Solvent–reactant H-bonds can stabilize or destabilize reactants relative to TS.  
  - Strong H-bonding to a reactant site can “lock” a functional group, reducing reactivity at that site.  

- **π–π and donor–acceptor interactions**:
  - Aromatic and electron-rich solvents can stabilize certain TSs or intermediates (e.g., via π-stacking or charge-transfer).  

- **Solvent acidity/basicity**:
  - Protic/acidic solvents may protonate reactants or intermediates → effectively change the reaction path or rate-limiting step.  
  - Basic solvents may deprotonate or act as nucleophiles, introducing competing reactions.

---

## Solvent Effects on Mechanism

Solvent changes can:

- Shift the **rate-determining step** (e.g., make ionization easier so subsequent step becomes RDS).  
- Change the **dominant mechanism** (SN1 ↔ SN2; E1 ↔ E2; radical vs ionic).  
- Modify **transition state structure** (earlier vs later TS), altering sensitivity to substituents and temperature.

Example pattern:

- Moving from polar protic to polar aprotic often:
  - Speeds up SN2 (stronger nucleophiles).  
  - Slows SN1 (less cation stabilization).

---

## Solvation Shell and Entropy

Solvation changes not only enthalpy but also entropy:

- Strongly ordered solvation shells around ions/polar species reduce entropy.  
- If TS involves desolvation (e.g., nucleophile shedding part of its solvation shell), there may be an entropic penalty.  
- Conversely, if reaction releases tightly bound solvent molecules, this can provide a favorable entropy contribution.

Thus, solvent effects on rate can be subtle balances of enthalpic and entropic solvation changes.

---

## Practical Takeaways

- Choose **polar protic solvents** to stabilize ions and favor mechanisms with charge separation in the TS (SN1, E1, many acid/base catalyzed processes).  
- Choose **polar aprotic solvents** to boost nucleophilicity and accelerate bimolecular polar reactions (SN2, certain addition reactions).  
- For **radical** or nonpolar processes, low-polarity solvents can minimize side ionic reactions and keep barriers low for neutral TSs.  
- Always consider both:  
  - Which species/TS is more polar/charged?  
  - How will the solvent stabilize that species relative to the others?

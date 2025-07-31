# CABSdock-cyclic

**Flexible docking of cyclic peptides to proteins using CABS-dock**

This repository contains docking results used in the manuscript:  
**"Flexible docking of cyclic peptides to proteins using CABS-dock."**

The dataset includes both global and local docking simulations performed with CABS-dock, followed by Rosetta-based refinement.

## Repository Structure

Directories are named using the format:

MODE-CONDITION-CYCLIZATIONTYPE-PDBID

Where:
- MODE is either GLOBAL or LOCAL (docking mode)
- CONDITION is BOUND (holo) or UNBOUND (apo) receptor
- CYCLIZATIONTYPE is either backbone or disulfide
- PDBID refers to the PDB ID of the complex

Example:  
GLOBAL-BOUND-backbone-3av9 — Global docking to bound receptor using a backbone-cyclized peptide from PDB 3AV9.

Each directory contains the Top-10 predicted models in PDB format:

model_0.pdb  
model_1.pdb  
model_2.pdb  
model_3.pdb  
model_4.pdb  
model_5.pdb  
model_6.pdb  
model_7.pdb  
model_8.pdb  
model_9.pdb

## Dataset Overview

- 38 peptide–protein complexes
- Each complex docked using both global and local protocols
- Docking performed for both bound (holo) and unbound (apo) receptor structures
- Includes peptides cyclized via:
  ** Backbone cyclization (head-to-tail)**
  Backbone cyclization of cyclic peptides can be performed using Modeller, which enables the formation of a continuous peptide chain.
  ** Disulfide bonds **

## Methodology

The complete protocol is described in the manuscript and Supporting Information (SI). It includes:

1. Flexible docking using the standalone version of CABS-dock with added distance restraints to preserve cyclic topology
2. All-atom reconstruction of Cα traces using PD2
3. High-resolution refinement using Rosetta FlexPepDock

This pipeline allows for the generation of realistic structural models of cyclic peptides bound to protein receptors without prior knowledge of the binding site (in global mode).

# fgf21-design-exploration
Computational exploration of core-position variants in FGF21 using ProteinMPNN and ColabFold

# Computational redesign of a buried core position in FGF21

Self-directed project exploring whether sequence design and structure 
prediction tools can distinguish stabilizing from destabilizing 
substitutions at a buried position in FGF21.

## Motivation
During my undergraduate research I worked with efruxifermin, an 
engineered Fc-FGF21 fusion protein, as a treatment in a liver 
spheroid model. That raised a question I could not answer from the 
wet lab alone — how are such variants chosen, and can I reason about 
them computationally. This project is my first attempt to do so.

## What I did
- Selected position L98, a buried hydrophobic core residue in FGF21
- Generated variants (L98I, L98V) with ProteinMPNN
- Predicted structures of WT, my variants, and the clinical variant 
  carried by efruxifermin (L98R / P171G / A180E) with ColabFold
- Compared predicted structures and per-residue confidence (pLDDT)

## What I found
All variants folded to nearly identical predicted structures with 
comparable confidence scores. Structure prediction told me whether 
a sequence can fold, but gave no signal about thermal stability or 
aggregation — the properties that actually separate a usable variant 
from a failed one.

## What I learned / next steps
Structure prediction alone cannot answer stability questions. 
Methods such as [FoldX / Rosetta ddG / molecular dynamics] and, 
ultimately, experimental measurement are needed. I would like formal 
training in these.

## Repository contents
- `FGF21_ProteinMPNN_ColabFold.ipynb` — the full workflow
- `/structures` — predicted PDB files
- `/figures` — structure overlays and pLDDT plots

## Tools
ProteinMPNN, ColabFold (AlphaFold2), PyMOL

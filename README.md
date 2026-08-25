[README-2.md](https://github.com/user-attachments/files/31397877/README-2.md)
# Find-a-Gene Project: A Novel RBP4 Homolog in the Basking Shark

Final project for **BIMM 143: Introduction to Bioinformatics** at UC San Diego.

## Overview

This project follows the "find-a-gene" workflow to identify and characterize a novel, previously unannotated gene. Starting from human Retinol-binding protein 4 (RBP4), I used BLAST to search unannotated genomic DNA, identified a novel homolog in the basking shark (*Cetorhinus maximus*) genome, and confirmed its novelty before analyzing its evolutionary relationships, structure, and druggability.

## Query Protein

- **Name:** Retinol-binding protein 4 (RBP4)
- **Species:** *Homo sapiens*
- **Accession:** NP_001310446.1
- **Function:** Lipocalin family protein that transports retinol (vitamin A) through the bloodstream, binding transthyretin in plasma to avoid renal filtration.

## Workflow

1. **tblastn search** against the nucleotide collection (core_nt), restricted to Chondrichthyes, to find unannotated genomic homologs.
2. **Match selection:** A raw genomic hit in *Cetorhinus maximus* chromosome 20 with no functional annotation.
3. **Novel sequence assembly:** Stitched together the three high-scoring pairs (HSPs) into a candidate protein sequence.
4. **Novelty confirmation:** blastp against the nr database showed the closest match at 95.73% identity, below the 100% threshold, confirming novelty.
5. **Multiple sequence alignment** (Clustal Omega) across 7 species, including human, mouse, pig, zebrafish, tundra swan, great white shark, and the novel basking shark sequence.
6. **Phylogenetic tree** built from the alignment to visualize species divergence.
7. **Sequence identity heatmap** generated in R using the Bio3D package.
8. **PDB structural search** using `blast.pdb()` in R/Bio3D to find related solved structures.
9. **AlphaFold2 structural prediction** (ColabFold) for the novel protein, visualized in Mol*.
10. **Binding site and druggability analysis** using CASTpFold for pocket prediction and ChEMBL for known ligand/assay data.

## Key Result

The novel basking shark sequence is a genuine, previously unannotated RBP4 homolog, most closely related to the great white shark RBP4 sequence, consistent with their shared lineage among cartilaginous fish. Structural modeling shows a conserved lipocalin beta-barrel fold with a well-defined retinol-binding pocket, and ChEMBL data on the human ortholog suggest existing ligands could serve as a starting point for exploring this homolog therapeutically.

## Skills Demonstrated

BLAST (tblastn, blastp), sequence alignment, phylogenetics, R programming, Bio3D, AlphaFold/ColabFold, structural visualization (Mol*), pocket prediction (CASTpFold), ChEMBL database searches

## View the Full Project

[View the full analysis](index.html)

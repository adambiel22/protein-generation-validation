# mutation-flows-validation

## Validation metrics

**Foldability** is measured by the sequence pLDDT score, as folded by ESMFold. We report the mean
981 CA pLDDT across all residues of each structure, stratified by sequence length in bins of width 100
 residues.

**Novelty** is evaluated using exhaustive structural search against the whole PDB database.The maximum TM-score across all hits defines the pdb-TM, and structures with pdb-TM < 0.5 are classified as structurally novel.

Diversity is reported as the ratio of distinct clusters to the total number of generated structures using FoldSeek with a TM-score threshold of 0.5.
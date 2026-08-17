# mutation-flows-validation

## Unconstrained sequence generation

### Validation metrics

**Foldability** is measured by the sequence pLDDT score, as folded by ESMFold. We report the mean
981 CA pLDDT across all residues of each structure, stratified by sequence length in bins of width 100
 residues. See [src/mutation_flows_validation/foldability.ipynb]().


**Novelty** is evaluated using exhaustive structural search against the whole PDB database.The maximum TM-score across all hits defines the pdb-TM, and structures with pdb-TM < 0.5 are classified as structurally novel. See [src/mutation_flows_validation/novelty.ipynb]().

**Diversity** is reported as the ratio of distinct clusters to the total number of generated structures using FoldSeek with a TM-score threshold of 0.5. See [src/mutation_flows_validation/diversity.ipynb]().

### Baselines

- [EvoDiff](https://github.com/microsoft/evodiff)
- [DPLM](https://github.com/bytedance/dplm)
- [ESM3](https://github.com/Biohub/esm)
- [SCISOR](https://github.com/baronet2/SCISOR)

ChatGPT proposed the following baselines:

|Type|Name|
|---|---|
|Autoregressive|ProGen2|
|Discrete diffusion|EvoDiff, DPLM|
|Masked iterative generation|ESM3|
|Continuous latent diffusion|DiMA|
|Flow matching|ProtFlow|


### Datasets

- PDB database
- UniRef50

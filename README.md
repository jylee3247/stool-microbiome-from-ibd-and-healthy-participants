[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15342901.svg)](https://doi.org/10.5281/zenodo.15342901)
# Description
- Title: **Gut microbiome study of inflammatory bowel disease in a Korean population cohort**
- Authors: **Hyun Sik Kim, Jae-Yun Lee, Bo-Hyung Kim, and Chang Kyun Lee**
- Year: **2025**

# Contents
- `Data` directory
  - `ASV_table.csv` [comma-separeted table]: Count table of amplicon sequencing variants (ASVs) across the samples. Rows represent ASVs and columns represent samples. This table was generated by [DADA2](https://benjjneb.github.io/dada2/index.html) pipeline through [Qiime2](https://qiime2.org/) platform.
  - `ASV_rep-seqs.fasta` [FASTA]: Sequences of each ASV used for construction of phylogenetic tree or taxonomic assignment of ASVs. This FASTA file was generated from [DADA2](https://benjjneb.github.io/dada2/index.html) pipeline through [Qiime2](https://qiime2.org/) platform.
  - `Phylogenetic_tree.nwk`[Newick]: Phylogenetic tree of ASVs constructed by [q2-fragment-insertion](https://library.qiime2.org/plugins/q2-fragment-insertion/16/) plugin in [Qiime2](https://qiime2.org/) platform.
  - `Taxonomy.csv` [comma-separated table]: Taxonomic assignment of ASVs. Species-level assignments were excluded because this level generally showed low accuracy in V3-V4 16S amplicon data. This data was generated from [Qiime2](https://qiime2.org/) platform and [SILVA](https://www.arb-silva.de/) database.
  - `Metadata.csv` [comma-separated table]: Metadata containing six columns
    - **SampleID** [character]: The unique identifier for each of the 640 samples collected from the study participants.
    - **Group** [categorical]: Indicates the clinical group from which the sample was obtained. This column consists of three categories: ‘CD’, ‘UC’, and ‘Healthy’.
    - **Age** [integer]: The age of the participant at the time of sample collection.
    - **Gender** [categorical]: The biological sex of the participant from whom the sample was obtained. The values include ‘Male’ and ‘Female’.
    - **Disease behavior(CD)** [categorical]: This column contains information on the disease behavior of the patients with CD. It reflects the current severity and pattern of CD, classified as ‘inflammatory’, ‘stricturing’, or ‘penetrating’. For samples from non-CD groups, the value is assigned as ‘None’.
    - **Disease location(UC)** [categorical]: This column records the disease extent in the patients with UC. It describes how extensively the disease has spread. Samples from non-UC groups are assigned the value ‘None’. For UC group, the values include ‘proctitis’, ‘left_sided’, and ‘extensive’.

# Preparation of reference fasta files
1. HA and NA segments were downloaded from GISAID (05-25-2022 to 05-25-2024), including three strains: H5N1, H1N1 and H3N2
2. MSA of each segment of each strain, with `mafft --auto`
3. Variant calling with the consensus sequence as reference (including insertions)

# Tiled amplicons designed with [Olivar](https://github.com/treangenlab/Olivar) (beta version)
 - Amplicon length ranging from 150 to 300, with annealing temperature of 60&deg;C
 - BLAST database: `ref_viruses_rep_genomes` (downloaded from NCBI FTP on May. 18, 2024, BLAST v2.15.0). Influenza A is excluded from BLAST search with `-negative_taxids 11320`
 - NA segment of H1N1 is not included in the design
 - Output primers found in `InfA-tiling.csv` and `InfA-tiling.scheme.bed` (ARTIC format)

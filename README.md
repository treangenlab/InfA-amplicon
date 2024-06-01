# Preparation of reference fasta files
1. HA and NA segments were downloaded from GISAID (05-25-2022 to 05-25-2024), including three strains: H5N1, H1N1 and H3N2
2. MSA of each segment of each strain, with `mafft --auto`
3. Variant calling with the consensus sequence as reference (including insertions)

# Tiled amplicons designed with [Olivar](https://github.com/treangenlab/Olivar)
 - Amplicon length ranging from 150 to 300, with annealing temperature of 60&deg;C
 - NA segment of H1N1 is not included in the design
 - Output primers found in `InfA-tiling.csv` and `InfA-tiling.scheme.bed` (ARTIC format)
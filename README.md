# Amplicon sequencing for Influenza A
A total of 45 tiled amplicons are designed with [Olivar](https://github.com/treangenlab/Olivar) (beta version), covering latest HA segment of H5N1, H1N1 and H3N2, and NA segment of H5N1 and H3N2. This beta version of Olivar can take sequences as input and support multiple targets. 

For more details, check [README.pdf](README.pdf)

## Multiple sequence alignment (MSA) and variant calling
1. Latest HA and NA segments were downloaded from GISAID, including three strains: H5N1, H1N1 and H3N2. 
2. MSA was made for each segment of each strain, with `mafft --auto` (version 7.525). All sequences were included for MSA. 
3. A consensus sequence was made for each MSA (gaps removed). 
4. Variant calling was done with a customized module of Olivar, using the consensus sequence as reference. 
5. Lists of variant location and frequency, as well as consensus sequences were used for downstream Olivar design. 

Reference sequences and lists of variations can be found in [References](References). 

## Design of tiled amplicons
 - Amplicon length set as 150 to 300, since shorter amplicons have better sensitivity for fragmented wastewater DNA/RNA. Annealing temperature set as 60°C. 
 - BLAST database: `ref_viruses_rep_genomes` (downloaded from NCBI FTP on May. 18, 2024, BLAST v2.15.0). Influenza A is excluded from BLAST search with `-negative_taxids 11320`
 - NA segment of H1N1 is not included in the design
 - Output primers found in [InfA-tiling.csv](InfA-tiling.csv) and [InfA-tiling.scheme.bed](InfA-tiling.scheme.bed) (ARTIC format)
 - Interactive html figures found in the [Figures](Figures/) folder. Download html files and view in browser. Refer to Fig1 of [Olivar manuscript](doi.org/10.1101/2023.02.11.528155) for details. 

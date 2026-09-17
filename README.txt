
# Overview  

This Toolkit contains a pixi.toml file which will create a project with following tools:

| Purpose | Tool |
|----------|----------|
| Read QC | NanoPack |
| Polishing tool | Medaka |
| Polishing tool | Racon |
| FASTQ manipulation | SeqKit |
| FASTQ manipulation | SeqTK |
| Read filtering | Fastp |
| Assembly | Flye |
| Read mapping | Minimap2 |
| BAM handling | Samtools |
| Sequence similarity search | BLAST+ |
| Assembly quality assessment | QUAST |
| Compression | Pigz |
| Flow management system | Snakemake |
| Flow management system | Nextflow |
| Parallel execution | GNU Parallel |

Once pixi is installed on your system use following command in the folder of the pixi.toml file to recreate the environment:

pixi install


For more extensive information look here: https://passelma42.github.io/Field-Sequencing/

# Adding NGspeciesID  

If you want to add NGspeciesID to the setup Read this info:

NGSpeciesID now recommends installing its dependencies through Conda/Bioconda and then installing NGSpeciesID with `pip --no-deps`. This workflow can be reproduced with Pixi because Pixi uses the Conda ecosystem. 

## Recommended minimal Pixi Setup

```bash
pixi init

pixi add -c conda-forge -c bioconda \
    python=3.12 \
    medaka \
    spoa \
    racon \
    minimap2 \
    samtools \
    pip

pixi shell

pip install --no-deps NGSpeciesID
```
The key part is that ```---no-deps``` avoids pip trying to build/reinstall parasail and edlib, a common source of installation problems on Apple Silicon Macs.  

!!! Note
    If you already built the nanopore toolkit you only need to add the SPOA to the project environment before running the pip install command to install NGSpeciesID with no dependencies.

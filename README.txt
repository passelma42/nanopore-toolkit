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

Overview
--------

This pipeline is an extension to the AMRplusplus pipeline (https://github.com/cdeanj/amrplusplus) and it's goal is to improve "species-level" identification using a custom kraken database followed by using BLAST and the nr/nt database. 

The custom kraken database includes refseq's genomes for bacteria, archaea, and viruses. Additionally,prior to database creation the plasmid sequences in reference genomes were isolated and classified to their own taxa ID. 

Please reach out if you'd like access to the custom database:edoster@colostate.edu
We are currently working on creating an automated script for making the custom database and this will be added soon.

## Example command:
nextflow main.nf --reads "PATH/to/files/*_R{1,2}_001.fastq.gz " --kraken_db $krakendir --output $outputDir --threads 1 -w $workingDIR --host $HOSTFASTA -profile local -species "Salmonella enterica"


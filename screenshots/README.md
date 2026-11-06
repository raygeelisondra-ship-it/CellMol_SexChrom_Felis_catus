This document outlines the step-by-step bioinformatics workflow  to retrieve genomic data, map reads, and compute coverage statistics for *Felis catus* (WGS run `SRR25054052`).

## Step-by-Step Galaxy Process

1. **Reference Genome & Data Retrieval**
   * Downloaded the reference genomic FASTA and assembly report for *Felis catus* (Assembly accession `GCF_018350175.1`).
   * Created a dedicated Galaxy history named `Sex_Dosage_FelisCatus`
   * Imported WGS genomic DNA reads for run `SRR25054052` into the history using the Galaxy SRA import tool.

2. **Quality Control & Read Alignment**
   * Inspected raw read quality using **FastQC**.
   * Aligned paired-end genomic DNA reads against the reference assembly  using **BWA-MEM**

3. **Alignment Processing**
   * Generated a coordinate-sorted and indexed BAM alignment file from the BWA-MEM output.

4. **Coverage Calculation**
   * Executed the **Samtools coverage** tool on the sorted BAM alignment, setting the tabular output option.
   * Configured quality parameters with minimum mapping quality = 20 and minimum base quality = 20 to ensure high-confidence depth measurements.
   * Exported the resulting coverage metrics as `chromosome_coverage.tsv` for downstream R processing.

* **Galaxy Workflow Link:** https://usegalaxy.org/u/ray_gee_lisondra/w/sex-dosage-species

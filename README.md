# Sex-Chromosome Dosage in a Selected Animal Nuclear Genome Using NCBI, Galaxy, and R

## Selected Species & Study Question
* **Species**: *Felis catus* (Domestic cat)
* **Study Question**: Can whole-genome sequencing (WGS) read depth mapping reliably determine the chromosomal sex of *Felis catus*  by calculating normalized sex-to-autosome depth ratios?

## Accession ID
* **Reference Assembly Accession**: GCF_018350175.1
* **Assembly BioSample accession:** SAMN19729387
* **WGS Run Accession**: SRR25054052
* **WGS BioSample accession:** SAMN36026286

## Chromosome Groups & Selection (`chromosome_groups.csv`)
* **Autosomes (Group A)**: 18 primary RefSeq autosomes (NC_058368.1 through NC_058385.1). These were chosen to establish a stable, uniform autosomal baseline mapping depth across the diploid genome.
* **X Chromosome (Group X)**: RefSeq accession NC_058386.1 (Feline X chromosome) designated to evaluate X-linked dosage relative to the autosomal median.
* **Exclusions**: Unplaced genomic scaffolds (NW_*), alternate haplotypes, and mitochondrial DNA (NC_001700.*) were strictly excluded to prevent mapping distortions and coverage anomalies. Y-chromosome reads were absent (NA).

## Questions for the report
1. **What species did you choose, and what evidence supports a diploid XX/XY or ZZ/ZW system?**
   * *Answer*: *Felis catus* was chosen, which utilizes a standard mammalian diploid XX/XY sex-determination system supported by cytogenetic and genomic evidence demonstrating homomorphic XX females and heteromorphic XY males.
2. **What are your assembly accession, WGS run, and both BioSample accessions? Are the donors the same?**
   * *Answer*: Assembly GCF_018350175.1 and WGS run SRR25054052 were analyzed. They were both BioSample accession (assembly:SAMN19729387
, WGS:SAMN36026286) but they were not of the same donors.
3. **Which sequences were used as autosomes and as X or Z? How did you verify their identities?**
   * *Answer*: 18 RefSeq autosomes (NC_058368.1–NC_058385.1) and the X chromosome (NC_058386.1) were used, verified directly against official NCBI RefSeq genome annotations.
4. **What are the median autosomal depth, X:A or Z:A ratio, and inferred sex-chromosome complement?**
   * *Answer*: Median autosome depth = 11.262; X:A ratio = 0.932; Inferred sex-chromosome complement = XX-like (Female).
5. **Does your result agree with the recorded sex of the WGS donor, if reported? Explain any discrepancy or uncertainty.**
   * *Answer*: Yes, the calculated ratio of 0.932 aligns with expected biological female metadata records. Minor deviations from 1.0 stem from normal sequencing and mapping variations.
6. **Why is a chromosome-level assembly alone insufficient for a reliable read-depth sex inference?**
   * *Answer*: A chromosome-level FASTA assembly provides structural reference coordinates but contains no sequencing read data; determining biological sex requires empirical mapping depth data from aligned WGS reads.

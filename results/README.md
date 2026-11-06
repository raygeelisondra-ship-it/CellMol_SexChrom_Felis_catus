## Results Directory: Sex-Chromosome Dosage Analysis
This directory contains the  output files generated for *Felis catus* following read-depth normalization against the median autosomal baseline.

### File Descriptions
* **`sex_inference.txt`**: Summary text file containing the calculated median autosome depth, X/A ratio, Y/A ratio, and the final biological sex-chromosome interpretation.
* **`chromosome_relative_depth.csv`**: Complete tabular dataset listing each chromosome sequence identifier (`rname`), assigned group (`A`, `X`, `Y`), mean read depth (`meandepth`), and normalized relative depth (`relative_depth`).
* **`chromosome_depth.png`**: Bar plot visualizing the normalized depth ratios across all evaluated chromosomes relative to the autosomal median (1.0) and sex-determination thresholds.

### Summary Results
* **Median Autosome Depth ($A$)**: 11.262
* **X / A Ratio**: 0.932[cite: 8]
* **Y / A Ratio**: `NA`[cite: 8]
* **Conclusion**: Together, these quantitative metrics confirm an **XX-like (Female)** chromosomal constitution for specimen `SRR25054052`, consistent with the used WGS record.

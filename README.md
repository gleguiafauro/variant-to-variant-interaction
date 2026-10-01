# variant-to-variant-interaction
In this project I describe and provide all the necessary code to execute an automated variant-to-variant interaction analysis in three steps: 
- 1) selection of variants of interest, that are independent (LD-prunned)
- 2) estimation of individual variants effect
- 3) estmiation of interactions effect

Note: this example code is developed to perform the analysis in an snakemake workflow, in the University of Lille - Zeus server via slurm jobs

# Original data status
the input dataset consist of TopMed bcf imputed sequencing data, GrCh38

# Setting
   conda activate epistasis
   GENES=TF,HFE
   OUT=results/tf_hfe
   QC='qc={"r2_min":0.8,"maf_min":0.01,"hwe_p_controls":1.0e-6,"snps_only":true,"biallelic_only":true}'
   ./run_epistasis.sh -g $GENES -o $OUT -t check -x "$QC"

# Rationale behind every step
# 1) Selection of variants of interest
The user will only provide gene names of the genes of interest which interactions the user wants to investigate. 

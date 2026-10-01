# variant-to-variant-interaction
In this project I describe and provide all the necessary code to execute an automated variant-to-variant interaction analysis in three steps: 
- 1) selection of variants of interest, that are independent (LD-prunned)
- 2) estimation of individual variants effect
- 3) estmiation of interactions effect

Note: this example code is developed to perform the analysis in an snakemake workflow, in the University of Lille - Zeus server via slurm jobs

# Original data status
the input dataset consist of TopMed bcf imputed sequencing data, GrCh38, 

# Rationale behind every step
# 1) Selection of variants of interest
The user will only provide gene names of the genes of interest which interactions the user wants to investigate. 

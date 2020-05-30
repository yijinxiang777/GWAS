# Genome-Wide Association Study (GWAS)

## What is GWAS?

## Things we need to learn before conducting GWAS  

1. Minor Allele Frequency (MAF)  
   * Definition: Frequency of the least often occurring allele at a specific location  
   > __Example__   
   10 individuals, freq(AA) = 6, freq(AB) = 3, freq(BB) = 1   
   freq(A) = 6*2+3/20 = 0.75 freq(B) = 5/20 = 0.25   
   MAF = freq(B) = 0.25  
   * In GWAS, we prefered to remove SNPs with low MAF
     1. Studies detecting the association with SNPs with a low MAP would be underpowered
     2. SNPs with low MAP are often more prine to genotyping errors  
   
2. Hardy-Weinberg Equilibrium (HWE)  
   * Definition: An Assumption states that the genotype and the allele frequencies are constant over generations and the population the population is with no selection, mutation, or migration.  
   > __Example__  
   In the population: 
   N=1000 freq(A) = 0.45 freq(B) = 0.55   
   freq(AA) = 0.18 freq(AB) = 0.54 freq(BB) = 0.28
   
   | Expected Genotype Freq |A                   | B                 |
   |:----------------------:|:------------------:| :----------------:|
   | A                      | 0.45*0.45 = 0.2025 | 0.55*0.45 = 0.2475|
   | B                      | 0.55*0.45 = 0.2475 | 0.55*0.55 = 0.3025|
   > What to test whether there is difference between the expected genotype frequency and the observed genotype frequency
   
   * In GWAS, we prefered to remove SNPs with low MAF

## Reference:  
> Mills, Melinda C., Nicola Barban, and Felix C. Tropf. An Introduction to Statistical Genetic Data Analysis. MIT Press, 2020.  
Marees, Andries T., et al. "A tutorial on conducting genome‐wide association studies: Quality control and statistical analysis." International journal of methods in psychiatric research 27.2 (2018): e1608.

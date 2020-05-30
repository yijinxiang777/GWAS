# Genome-Wide Association Study (GWAS)

## What is GWAS?

## Things we need to learn before conducting GWAS  

1. Minor Allele Frequency (MAF)    
   * Definition: Frequency of the least often occurring allele at a specific location   
   **Example**   
   10 individuals, freq(AA) = 6, freq(AB) = 3, freq(BB) = 1   
   freq(A) = 6*2+3/20 = 0.75 freq(B) = 5/20 = 0.25   
   MAF = freq(B) = 0.25  
   * In GWAS, we prefered to remove SNPs with low MAF
     1. Studies detecting the association with SNPs with a low MAP would be underpowered
     2. SNPs with low MAP are often more prine to genotyping errors  
   
2. Hardy-Weinberg Equilibrium (HWE)  
   * Definition: An Assumption states that the genotype and the allele frequencies are constant over generations and the population the population is with no selection, mutation, or migration.    
   **Example**  
   In the population: 
   N=1000 freq(A) = 0.45 freq(B) = 0.55 freq(AA) = 0.18 freq(AB) = 0.54 freq(BB) = 0.28  
   What to test whether there is difference between the expected genotype frequency and the observed genotype frequency (Chi-sqaure test with a p-value <0.05 can indicate the difference)  

   | Expected Genotype Freq |A                   | B                 |
   |:----------------------:|:------------------:| :----------------:|
   | A                      | 0.45*0.45 = 0.2025 | 0.55*0.45 = 0.2475|
   | B                      | 0.55*0.45 = 0.2475 | 0.55*0.55 = 0.3025|         

    <img src="https://latex.codecogs.com/gif.latex?\begin{align*}&space;X^{2}&space;=&space;\sum\frac{(O-E)^{2}}{E}&space;=&space;\frac{(180-202.5)^{2}}{202.5}&space;&plus;&space;\frac{(540-495)^{2}}{495}&plus;&space;\frac{(280-302.5)^{2}}{302.5}&space;=&space;8.25&space;\end{align*}" title="\begin{align*} X^{2} = \sum\frac{(O-E)^{2}}{E} = \frac{(180-202.5)^{2}}{202.5} + \frac{(540-495)^{2}}{495}+ \frac{(280-302.5)^{2}}{302.5} = 8.25 \end{align*}" />

    
   
   * In GWAS, we prefered to remove SNPs with low MAF  
     1. It is generally assumed that deviations from HWE are the result of genotyping errors.
3. 

## Reference:  
> Mills, Melinda C., Nicola Barban, and Felix C. Tropf. An Introduction to Statistical Genetic Data Analysis. MIT Press, 2020.  
Marees, Andries T., et al. "A tutorial on conducting genome‐wide association studies: Quality control and statistical analysis." International journal of methods in psychiatric research 27.2 (2018): e1608.
       

# Genome-Wide Association Study (GWAS)

## [What is GWAS?](https://www.genome.gov/genetics-glossary/Genome-Wide-Association-Studies)
A genome-wide association study (GWAS) is an approach used in genetics research to associate specific genetic variations with particular diseases. The method involves scanning the genomes from many different people and looking for genetic markers that can be used to predict the presence of a disease.  

## Things we need to learn before conducting GWAS  

1. Minor Allele Frequency (MAF)    
   * **Definition**: Frequency of the least often occurring allele at a specific location   
   * **Example**: 10 individuals, freq(AA) = 6, freq(AB) = 3, freq(BB) = 1   
     freq(A) = 6*2+3/20 = 0.75 freq(B) = 5/20 = 0.25   
     MAF = freq(B) = 0.25  
   * In GWAS, we prefered to remove SNPs with **low MAF**
     1. Studies detecting the association with SNPs with a low MAP would be underpowered
     2. SNPs with low MAP are often more prine to genotyping errors  
   
2. Hardy-Weinberg Equilibrium (HWE)  
   * **Definition**: An Assumption states that the genotype and the allele frequencies are constant over generations and the population the population is with no selection, mutation, or migration.    
   * **Example**    
   In the population: 
   N=1000 freq(A) = 0.45 freq(B) = 0.55 freq(AA) = 0.18 freq(AB) = 0.54 freq(BB) = 0.28  
   What to test whether there is difference between the expected genotype frequency and the observed genotype frequency (Chi-sqaure test with a p-value <0.05 can indicate the difference)  


    <img src="https://latex.codecogs.com/gif.latex?\begin{align*}&space;X^{2}&space;=&space;\sum\frac{(O-E)^{2}}{E}&space;=&space;\frac{(180-202.5)^{2}}{202.5}&space;&plus;&space;\frac{(540-495)^{2}}{495}&plus;&space;\frac{(280-302.5)^{2}}{302.5}&space;=&space;8.25&space;\end{align*}" title="\begin{align*} X^{2} = \sum\frac{(O-E)^{2}}{E} = \frac{(180-202.5)^{2}}{202.5} + \frac{(540-495)^{2}}{495}+ \frac{(280-302.5)^{2}}{302.5} = 8.25 \end{align*}" />    
    
   * In GWAS, we prefered to remove SNPs with **low HWE**  
     1. It is generally assumed that deviations from HWE are the result of genotyping errors.  
 
3. linkage Disequilibrium (LD)
    * **Definition**: This is a measure of non‐random association between alleles at different loci at the same chromosome in a given population.   
    * **[Example](https://pbgworks.org/sites/pbgworks.org/files/measuresoflinkagedisequilibrium-111119214123-phpapp01_0.pdf)**   
    ![basic](https://raw.githubusercontent.com/yijinxiang777/Images/master/data.png)    
    Observed:  
    ![OBSERVED](https://raw.githubusercontent.com/yijinxiang777/Images/master/observed.png)     
    ![EorD](https://raw.githubusercontent.com/yijinxiang777/Images/master/expcedt.png)  
    * **Standardization of D**: A common standardization method to gain a relative measure of D  
    <img src="https://latex.codecogs.com/gif.latex?{D}'=&space;D/D_{max}&space;\quad&space;D_{max}&space;=&space;\begin{cases}&space;min(p1q2,p2q1)&space;&&space;if&space;D>0&space;\\&space;min(p1q1,p2q2)&&space;if&space;D<0&space;\end{cases}" title="{D}'= D/D_{max} \quad D_{max} = \begin{cases} min(p1q2,p2q1) & if D>0 \\ min(p1q1,p2q2)& if D<0 \end{cases}" />  
    
    * **Correlation Coefficient**: Another measure of LD   
    <img src="https://latex.codecogs.com/gif.latex?r&space;=&space;\frac{D}{(p1p2q1q2)^{1/2}}" title="r = \frac{D}{(p1p2q1q2)^{1/2}}" />    
    
    * **Test Significance of LD**: Chi-sqaure Test    
    <img src="https://latex.codecogs.com/gif.latex?X^{2}&space;=&space;\sum&space;\frac{(Observed-Expected)^{2}}{Expected}" title="X^{2} = \sum \frac{(Observed-Expected)^{2}}{Expected}" />  
    
## [Quality Check Steps before GWAS](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6001694/table/mpr1608-tbl-0001/?report=objectonly)  
  * **Individual and SNP missingness**: Excludes SNPs that are missing in a large proportion of the subjects & Excludes individuals who have high rates of genotype missingness   
  * **Minor allele frequency (MAF)**: Includes only SNPs above the set MAF threshold  
  * **Deviations from Hardy–Weinberg equilibrium (HWE)**: Excludes markers which deviate from Hardy–Weinberg equilibrium   
  * **Inconsistencies in assigned and genetic sex of subjects**  
  * **Heterozygosity rate**  
  * **Relatedness**  
  * **Ethnic outliers (population stratification)**
  
## Modeling for GWAS   
  * **Coding Genetics Effect**  
  ![](https://raw.githubusercontent.com/yijinxiang777/Images/master/WX20200531-101551.png)  
  * **Association testing**
  Linear model: <img src="https://latex.codecogs.com/gif.latex?y_{i}&space;=&space;\alpha&space;&plus;&space;\beta&space;x_{i}&plus;&space;\epsilon_{i}" title="y_{i} = \alpha + \beta x_{i}+ \epsilon_{i}" />  
  - y represents the value of trait  
  - x numerical representation fo genotype  
  - ε error term representing unobservables and random noise in y  

## Result Interpretation  

## Reference   
> Mills, Melinda C., Nicola Barban, and Felix C. Tropf. An Introduction to Statistical Genetic Data Analysis. MIT Press, 2020.  
Marees, Andries T., et al. "A tutorial on conducting genome‐wide association studies: Quality control and statistical analysis." International journal of methods in psychiatric research 27.2 (2018): e1608.
       

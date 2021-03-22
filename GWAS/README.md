# Notes on GWAS
By Ha Vu

Today is March 20, 2021, a fine Spring day in IA. So, I thought, why not sit down and learn something new! Everything written in this document (as well as the codes, if there are any), are notes and practice exercises I picked up while reading about GWAS. I will make sure to cite any source of information that I learn from, although I can't promise to cite in the same style. Please also excuse any typos (espcially the future Ha, please excuse your own old self).

Some useful links that I learned from:
- [Genome-wide association studies in R](https://www.r-bloggers.com/2017/10/genome-wide-association-studies-in-r/), by Francisco Lima.
- [Glossary of Genetic Terms](https://www.genome.gov/genetics-glossary)
- [Marees AT, de Kluiver H, Stringer S, et al. A tutorial on conducting genome‐wide association studies: Quality control and statistical analysis. Int J Methods Psychiatr Res. 2018;27:e1608 10.1002/mpr.1608](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6001694/).
- [Genome-Wide Association Analysis Using R](https://pubmed.ncbi.nlm.nih.gov/28132152/), by Julio Isidro-Sánchez et al.
- Real data and data analysis were obtained from: 

First, let's start with some necessary introductory glossary. There might be new vocabulary later, but we will define them along the way.
| Glossary     | Definition | Source     |
| :---        |    :---   |          :--- |
| Genotype      | A genotype is an individual's collection of genes. The term also can refer to the two alleles inherited for a particular gene. The genotype is expressed when the information encoded in the genes' DNA is used to make protein and RNA molecules.      | [NIH](https://www.genome.gov/genetics-glossary/genotype)   |
| Phenotype   | The expression of the genotype contributes to the individual's observable traits, called the phenotype.        | [NIH](https://www.genome.gov/genetics-glossary/genotype)      |
| Locus | A locus is the specific physical location of a gene or other DNA sequence on a chromosome, like a genetic street address. The plural of locus is "loci". | [NIH](https://www.genome.gov/genetics-glossary/Locus)|
| Allele | An allele is one of two or more versions of a gene. An individual inherits two alleles for each gene, one from each parent. If the two alleles are the same, the individual is homozygous for that gene. If the alleles are different, the individual is heterozygous. | [NIH](https://www.genome.gov/genetics-glossary/Allele)|
| Haploid and diploid | Haploid is the quality of a cell or organism having a single set of chromosomes. Organisms that reproduce asexually are haploid. Sexually reproducing organisms are diploid (having two sets of chromosomes, one from each parent). In humans, only their egg and sperm cells are haploid. | [NIH](https://www.genome.gov/genetics-glossary/haploid)|
| Single nucleotide polymorphism (SNP) | Single nucleotide polymorphisms (SNPs) are a type of polymorphism involving variation of a single base pair. SNPs is pronouced as /snips/. | [NIH](https://www.genome.gov/genetics-glossary/Single-Nucleotide-Polymorphisms)|


## 1. Introduction to GWAS
- **GWAS** stands for **G**enone-**w**ide **A**ssociation **Studies**.
- Generally in GWAS, we scan the genomes from many individuals, identify SNPs that are present, and try to associate the SNPs with diseases/conditions/traits of the studies.
- GWAS can be useful in various scenarios. For example, we can predict novel biological markers that potentially cause diseases. These studies will facilitate precision medicine development and therapeutic methods.

### Some related (but maybe different) concepts

(I will learn about QTLs and share some notes soon!)
| Type     | Description | Source/Read more  |
| :---        |    :---   |          :--- |
| Quantitaive Trait Locus (QTL) | A quantitative trait is one that has measurable phenotypic variation because of genetic and/or environmental influences. A QTL is a genetic locus that affect this variation. QTLs can be SNPs, for example. | Members of the Complex Trait Consortium. The nature and identification of quantitative trait loci: a community's view. Nat Rev Genet 4, 911–916 (2003). [https://doi.org/10.1038/nrg1206](https://doi.org/10.1038/nrg1206) |
| QTL analysis | A statistical method to link phenotypic data with genotypic data. |[Miles, C. & Wayne, M. (2008) Quantitative trait locus (QTL) analysis. Nature Education 1(1):208](https://www.nature.com/scitable/topicpage/quantitative-trait-locus-qtl-analysis-53904/)|
| Linkage Disequilibrium (LD) mapping | Is a method to study the non-random associations/correlations between SNPs. These associations might be due to recombination, mutation, and selection in a region. ||
| Linkage mapping | Concerns about the correlations between genotypes and phenotypes. "Linkage mapping is **a highly controlled experiment**: individuals are crossed to generate a mapping population in which relatedness is known."| [Association Mapping: Critical Considerations Shift from Genotyping to Experimental Design](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2751942/) |
| Association mapping | Same as LD mapping. Unlike linkage mapping, "association mapping [...] is **not a controlled experiment**, but rather a natural experiment. Genotype and phenotype data are collected from a population in which relatedness is not controlled by the experimenter, and correlations between genetic markers and phenotypes are sought within this population."| [Linkage disequilibrium maps and association mapping](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1137007/), [Association Mapping: Critical Considerations Shift from Genotyping to Experimental Design](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2751942/) |
| Bulked Segregant Analysis (BSA) | Identifies genetic markers associated with a mutant phenotype. The experiemnt involves two populations with opposing phenotypes, and two bulked DNA samples are pooled from the members in each group. ||


## 2. General pipeline.
The pipeline listed here relied heavily on [Marees AT, de Kluiver H, Stringer S, et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6001694/) This publication is very well written, and I learned a lot from it.
1. Quality control: filtering out of SNPs and individuals based on:
- Individual and SNp missingness
- Sex discrepancy
- Minor allel frequency
- Derivations from hardy-weinberg equilibrium
- Heterozygority rate
- Relatedness
- Population stratification
2. Statistical tests of associations
- Correction for multiple testing is necessary.

Another pipeline can be found here: [Genome-Wide Association Analysis Using R](https://pubmed.ncbi.nlm.nih.gov/28132152/), by Julio Isidro-Sánchez et al.


## 3. Practice analyzing GWAS data.
In this section, I will be attempting to replicate the GWAS 

1. Data summary:

2. Data analysis:


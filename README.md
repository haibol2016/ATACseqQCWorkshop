# Best practices for ATAC-seq QC and data analysis

## Haibo Liu*, Rui Li*, Kai Hu* and Lihua Julie Zhu*

Haibo Liu, Department of Animal Science, Iowa State University, Ames, IA, 50010, USA. [haibol@iastate.edu](mailto:haibol@iastate.edu)  
Jianhong Ou, Department of Cell Biology, Duke University Medical Center, Durham, NC, 27710, USA. [Rui.Li@umassmed.edu](mailto:Rui.Li@umassmed.edu)  
Kai Hu, Department of Molecular, Cell and Cancer Biology, Worcester, MA01655, USA. [Kai.Hu@umassmed.edu](mailto:Kai.Hu@umassmed.edu)  
Corresponding author: Lihua Julie Zhu, Department of Molecular, Cell and Cancer Biology, Program in Molecular Medicine, Program in Bioinformatics and Integrative Biology, Worcester, MA01655, USA. [Julie.Zhu@umassmed.edu](mailto:Julie.Zhu@umassmed.edu)  
*Denotes workshop presenter

# Workshop Description
IIn this workshop, we will provide a valuable introduction to the current best practices for ATAC-seq assays, high quality data generation and computational analysis workflow. Then, we will walk the participants through the analysis of an ATAC-seq data set. single cell ATAC-seq data analysis will be briefly covered at the end by comparing to the bulk ATAC-seq data analysis. Detailed tutorials including R scripts will be provided for reproducibility and follow-up exploration.

**Expectation:** After this workshop, participants should be able to apply the learned skills to analyzing their own ATAC-seq data, provide constructive feedback to experimenters who expect to generate high-quality ATAC-seq data, and identify ATAC-seq data of reliable quality for further analysis.

# Pre-requisites
Participants are expected to have basic knowledge as follows:
-   Basic knowledge of R syntax
-   Basic knowledge of simple UNIX commands, such as grep, and awk
-   Some familiarity with the GenomicRanges, BSgenome, GenomicAlignments classes
-   Familiarity with the SAM file format ([https://samtools.github.io/hts-specs/SAMv1.pdf](https://samtools.github.io/hts-specs/SAMv1.pdf))

Basic understanding on how ATAC-seq data are generated is helpful but not required. Please refer to the following reference for detailed information about the ATAC-seq technology.

Jason Buenrostro, Beijing Wu, Howard Chang, William Greenleaf. ATAC-seq: A Method for Assaying Chromatin Accessibility Genome-Wide. Curr Protoc Mol Biol. 2015; 109: 21.29.1–21.29.9. doi:[10.1002/0471142727.mb2129s109](https://dx.doi.org/10.1002%2F0471142727.mb2129s109).

Please refer to the following resource to preprocess the ATAC-seq data prior to performing quality assessment using the ATACseqQC package.

The Additional File 1 from our publication (Ou et al., 2018; [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5831847/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5831847/))

# Workshop Participation
Participants are expected to have basic knowledge about R and several R packages as described above in advance. To follow along the hands-on session, we recommend participants bring your own laptop. We will post a Docker image with required packages and data pre-installed for you to download and run the analysis within a Docker container. If you will use the Docker image, please get Docker installed ([https://www.docker.com/get-started](https://www.docker.com/get-started)) in advance. For participants who wish to install all packages by themselves, you will also need to install the following computing tools.
 - R (version >3.5.0; [https://cran.r-project.org/](https://cran.r-project.org/)) 
 - RStudio (https://www.rstudio.com/products/rstudio/download/#download)
 - The ATACseqQC package along its dependencies
 - Integrated Genome Browser (IGV, http://software.broadinstitute.org/software/igv/download)

For participants who wish to install all packages by themselves and use a Windows with OS lower than Win 10, which lacks a UNIX terminal, we recommend one of the following alternatives.
 - Install Cygwin ([https://www.cygwin.com/](https://www.cygwin.com/))
 - Install git Bash ([https://gitforwindows.org/](https://gitforwindows.org/))
 - Install UnxUtils   ([https://sourceforge.net/projects/unxutils/](https://sourceforge.net/projects/unxutils/))
   
# R / Bioconductor packages used

The following R/_Bioconductor_ packages will be explicitly used:

 - library(ATACseqQC)
 - library(ChIPpeakAnno)
 - library(BSgenome.Hsapiens.UCSC.hg38)
 - library(TxDb.Hsapiens.UCSC.hg38.knownGene)
 - library(MotifDb)
 - library(motifStack)
 - library(GenomicAlignments)

# Time outline
|Activity|Time|
|--------|----|
|Introduction to ATAC-seq       | 5 m |
|Preprocessing of ATAC-seq data |5 m|
|ATAC-seq data QC workflow | 10 m |
|Hands on experience with ATACseqQC and live demo | 30 m |
|Best Practice | 5 m|
|Question & Answer | 5 m|

# Workshop goals and objectives

## Learning goals

 - Understand how ATAC-seq data are generated
 - Learn how to perform comprehensive quality control of ATAC-seq data
 - Identify high quality ATAC-seq data for downstream analysis
 - Identify most likely reasons for ATAC-seq data failing QC

## Learning objectives

 - Analyze a pre-aligned, excerpted ATAC-seq dataset from the original ATAC-seq publication (Buenrostro et al., 2015) to produce
   comprehensive insights into the quality of the data
 - Create a plot showing library fragment size distribution 
 - Create overview plots showing signal distribution around transcription start sites
 - Automatically generate IGV snapshots showing signal distribution along multiple housing keeping genes (positive control genes) 
 - Create a plot showing CTCF footprints
 - Evaluate the ATAC-seq data for mitochondrial DNA contamination, duplication rate, background noise level, library complexity and Tn5
   transposition optimality


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTMzOTM0NTI0MF19
-->

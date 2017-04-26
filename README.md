# Comprehensive mapping of HIV-1 escape from a broadly neutralizing antibody

## Authors
Adam Dingens, Hugh Haddox, Julie Overbaugh, Jesse Bloom
We are performing mutational antigenic profiling the bnAb PGT151 using the BF520 mutant Env library.
Adam performed the experiments and analyzed the data. 

## Goal
We are developing a deep mutational scanning approach to map anti-HIV Env antibodies, in an approach termed mutational antigenic profiling. 
These results define all single amino acid mutations that affect sensitivity to the mAb. 
In addition to providing a mutation-level view of the antibody epitope, completely defining all possible escape mutations could inform the development and evaluation of eptiope-focused immunogens and antibody-based immunotherpeutics. 
This work builds upon [Haddox et al (2016)](https://doi.org/10.1371/journal.ppat.1006114) and is conceptually similar to [Doud et al (2017)](https://doi.org/10.1371/journal.ppat.1006271).

This analysis downloads the deep sequencing data, aligns the reads and corrects sequencing errors using a barcoded subamplicon approach, and computes the differential selection that PGT151 exerts on BF520.C2 Env.
This analysis also compares the results to other known functional mapping information. The manuscript further validates these results with additional experiments not included in the computational pipeline. 

This analysis is included as a supplemental file to the manuscript to allow others to perform this analysis, as well as to assist others to analyze their own mutational antigenic profiling data. 

## Organization
The analysis is performed by the iPython notebook [`BF520-PGT151-FinalAnalysis_SupFile1.ipynb`](BF520-PGT151-FinalAnalysis_SupFile1.ipynb), which also summarizes the main results. 

Subdirectories:

   * `./FASTQ_files/` contains the input Illumina deep sequencing data.

   * `./diffsel/` s generated by [`BF520-PGT151-FinalAnalysis_SupFile1.ipynb`](BF520-PGT151-FinalAnalysis_SupFile1.ipynb), and contains the differential selection files.

   * `./counts/` is generated by [`BF520-PGT151-FinalAnalysis_SupFile1.ipynb`](BF520-PGT151-FinalAnalysis_SupFile1.ipynb), and contains codon counts from the aligned, error-corrected reads.

## Input data

### Illumina deepp sequencing data
The `./FASTQ_files/` subdirectory contains the Illumina deep sequencing data, downloaded directly from the NCBI SRA. 
They reads were submitted as SRA submission SUB2392015 on Feb 9, 2016, and they all have the BioSample Accession number SAMN06313000. 
The BioProject ID is PRJNA371844. The iPython notebook [`BF520-PGT151-FinalAnalysis_SupFile1.ipynb`](BF520-PGT151-FinalAnalysis_SupFile1.ipynb) details the sample that corresponds to each file.  

## Results and Conclusions
All of the results are detailed in the [`BF520-PGT151-FinalAnalysis_SupFile1.ipynb`](BF520-PGT151-FinalAnalysis_SupFile1.ipynb) notebook; click on that notebook to see the results.

Summary of findings (from this analysis, in addition to other analyses detailed in the manuscript):

   1. Mapped all HIV antibody-escape mutants in a single massively parallel experiment

   2. The high-throughput results correlated with individual neutralization assays 
   
   3. Identified new escape mutants not found by approaches such as alanine scanning
   
   4. The results provide insight into the biochemical basis of antibody escape

Mutational antigenic profiling is a powerful approach for mapping all possible antibody escape mutations to Env. 


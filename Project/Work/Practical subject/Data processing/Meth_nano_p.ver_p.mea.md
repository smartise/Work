---
Done: false
"date:":
tipe: dataanalysis
tags:
---
# Reference sequence 
Pocillopora verrucosa 
[Pocillopora verrucosa genome assembly CSIRO\_AGI\_Pver\_v1 - NCBI - NLM](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_030620025.1/)

Pocillopora meandrina 
[Pocillopora meandrina genome assembly PMEA\_v1 - NCBI - NLM](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_942486045.1/)

# Protocol 
protocol based on [[dimondDNAMethylationProfiling2021]].

1. **Mapping of Reads**: The reads were mapped using `minimap2 v. 2.14` and a reference genome.
    
2. **Analysis of DNA Methylation Patterns**: The DNA methylation patterns for the mapped reads were analyzed using `Nanopolish v. 0.10.1`.

    - **Nanopolish Functionality**: Nanopolish analyzes CpG motifs in short (11–34 bp) k-mer sequences. It distinguishes 5-methylcytosine from unmethylated cytosine based on signal disruptions in raw ONT FAST5 sequence data. The program calculates log-likelihood ratios for base modifications of each read, with positive values indicating support for modification.

1. **Summarization of Nanopolish Output**: The output from Nanopolish was summarized using the helper script `calculate_methylation_frequency.py`. This script summarizes methylation frequency by genomic coordinates.
    
4. **Filtering of Methylation Calls**: The methylation calls from Nanopolish were subjected to filtering. The criteria for filtering included:
    
    - A minimum read count of 10 reads per CpG motif.
    - Exclusion of transcriptome sequences with methylation called for fewer than 20% of CpGs in the sequence.
5. **Estimation of CpG Depletion**: To estimate CpG depletion, which is an indicator of evolutionary-scale methylation patterns, the number of CpGs observed vs. expected (CpG O/E) was calculated.

# nanopolish functionality 
1. **Polishing Genome Assemblies**: One of the main features of `Nanopolish` is to improve the accuracy of a genome assembly using the raw signal data from ONT sequencers. This process is often referred to as "polishing" the assembly. By comparing the raw signals to the assembled sequences, `Nanopolish` can correct small errors in the assembly.

2. **Detecting DNA Methylation**:
    
    - `Nanopolish` can detect DNA methylation by analyzing the raw electrical signals produced during sequencing. Methylation causes a distinct change in the electrical current when a modified base passes through the nanopore, and `Nanopolish` can recognize these signal disruptions.
    - Specifically, for CpG methylation, `Nanopolish` calculates log-likelihood ratios for base modifications of each read. Positive values indicate support for methylation.
3. **Variant Calling**: `Nanopolish` can also be used to call single nucleotide variants (SNVs) and indels directly from the raw ONT sequencing data.
    
4. **Haplotype Phasing**: It can phase variants into haplotypes, which is useful for understanding the combination of variants present on individual chromosomes.
    
5. **Signal-Level Analysis**: `Nanopolish` provides tools for more detailed analysis of the raw signal data, which can be useful for research and development purposes or for understanding specific sequencing artifacts.

# minimap 2 

1. **Alignment**: At its core, `minimap2` aligns sequences. Given a reference sequence and a set of query sequences, it finds the best-matching locations of the queries on the reference.
    
2. **Optimized for Long Reads**: While many traditional aligners were designed for short-read sequencing data (like that from Illumina platforms), `minimap2` is optimized for the longer reads produced by PacBio and ONT.
    
3. **Versatility**: Beyond just read mapping, `minimap2` can be used for:
    
    - Whole-genome alignment
    - Transcriptome read mapping (RNA-seq)
    - Overlap among long reads, which is useful for certain genome assembly strategies
4. **Speed and Efficiency**: `minimap2` is designed to be fast and memory-efficient, making it suitable for processing large datasets typical of long-read sequencing projects.
    
5. **Preset Parameters**: The tool comes with preset parameters tailored for various applications, making it user-friendly for those not wishing to delve deep into custom parameter settings.
    
6. **Output Format**: `minimap2` typically outputs alignments in the SAM (Sequence Alignment/Map) format, which is a standard format for storing large-scale nucleotide sequence alignments.
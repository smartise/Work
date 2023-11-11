---
Used: false
collections: "[[epigenetic coral]]"
tipe: article
---
tipe: journalArticle
Creators: [[Quentin Gouil]], [[Andrew Keniry]]
collections: [[epigenetic coral]]
Link to zotero:: [Gouil_Keniry_2019_Latest techniques to study DNA methylation.pdf](zotero://select/library/items/7IJFS4B4)
Journal: Essays in Biochemistry
DOI: 10.1042/EBC20190027
Tags: #Animals, #Epigenomics, #Nanopores, #5-Methylcytosine, #DNA Methylation, #🔍, #🎨, #epigenetics, #Adenine, #base modifications, #bisulfite, #DNA, #Humans, #Nanopore, #PacBio, #Sequence Analysis, DNA, #Sulfites

---
```ad-note
title: Abstract
color:: 

Bisulfite sequencing is a powerful technique to detect 5-methylcytosine in DNA that has immensely contributed to our understanding of epigenetic regulation in plants and animals. Meanwhile, research on other base modifications, including 6-methyladenine and 4-methylcytosine that are frequent in prokaryotes, has been impeded by the lack of a comparable technique. Bisulfite sequencing also suffers from a number of drawbacks that are difficult to surmount, among which DNA degradation, lack of specificity, or short reads with low sequence diversity. In this review, we explore the recent refinements to bisulfite sequencing protocols that enable targeting genomic regions of interest, detecting derivatives of 5-methylcytosine, and mapping single-cell methylomes. We then present the unique advantage of long-read sequencing in detecting base modifications in native DNA and highlight the respective strengths and weaknesses of PacBio and Nanopore sequencing for this application. Although analysing epigenetic data from long-read platforms remains challenging, the ability to detect various modified bases from a universal sample preparation, in addition to the mapping and phasing advantages of the longer read lengths, provide long-read sequencing with a decisive edge over short-read bisulfite sequencing for an expanding number of applications across kingdoms.

```

---
### Highlight

%% begin annotations %%



### Imported: 2023-10-11 5:00 pm

*gouilLatestTechniquesStudy2019*
	Long-read sequencing offers a solution to the mappability problem of short reads. Two long-read sequencing technologies are currently available: nanopore sequencing from Oxford Nanopore Technologies (ONT) and single molecule real-time (SMRT) sequencing from Pacific Biosciences (PacBio) (Figure 1). Both strategies can be applied to bisulfite-treated and amplified DNA to provide a readout similar to short-read bisulfite sequencing, but their main advantage lies in their ability to sequence native DNA and infer base modifications from their impact on the raw sequencing signal. 
	
[Page4](zotero://open-pdf/library/items/7IJFS4B4?page=4&a=P94DYWTU)
	
	
#introduction, #nanopore
	
	
	reference: ^f80574

*gouilLatestTechniquesStudy2019*
	More generally there is no longer a need for enzymatic or chemical treatments specific to each base modification of interest, opening up the range of assayable modifications and reducing experimental complexity. 
	
[Page4](zotero://open-pdf/library/items/7IJFS4B4?page=4&a=K6PGEPKU)
	
	
#introduction, #nanopore
	
	
	reference: ^98e736

*gouilLatestTechniquesStudy2019*
	The downside of this feature is that the DNA cannot be amplified; therefore, input amounts can be limiting (200 fmol for Nanopore, or about 1 μgof8kbfragments;5μg for a typical PacBio library, although 100 ng can be sufficient [63]). 
	
[Page4](zotero://open-pdf/library/items/7IJFS4B4?page=4&a=9TQKDD6F)
	
	
#introduction, #nanopore
	
	
	reference: ^79a6c4

*gouilLatestTechniquesStudy2019*
	In cases where only small DNA amounts are available because of experimental design (e.g. single small organism, microdissected tissue, single cells) or because of the preciousness of the original tissue (e.g. biopsies or paleogenomic samples), Nanopore and PacBio native DNA sequencing will not be feasible. 
	
[Page4](zotero://open-pdf/library/items/7IJFS4B4?page=4&a=4T9Q4IR9)
	
	
#introduction, #nanopore
	
	
	reference:

*gouilLatestTechniquesStudy2019*
	These approaches are therefore best suited to bulk samples, constraining the granularity of the analyses and making cell-to-cell variation difficult to evaluate. 
	
[Page4](zotero://open-pdf/library/items/7IJFS4B4?page=4&a=77IRYQVD)
	
	
#introduction, #nanopore
	
	
	reference: ^99bd64

*gouilLatestTechniquesStudy2019*
	ONT’s nanopore sequencing measures the variation in ionic current through a biological nanopore as a single-stranded nucleic acid is ratcheted through. Neural networks translate the current trace into nucleotides in a process named basecalling. Base modifications on the DNA introduce deviations in the raw signal, making them detectable (Figure 1). 
	
[Page5](zotero://open-pdf/library/items/7IJFS4B4?page=5&a=A9RMLJK6)
	
	
#introduction, #nanopore
	
	
	reference: ^18fe6e

*gouilLatestTechniquesStudy2019*
	Detection of base modifications in ONT data commonly involves three steps: (1) basecalling with canonical bases (e.g. with ONT’s Guppy basecaller [76]), (2) anchoring the raw signal to a genomic reference, and (3) weighing the evidence that a base is modified. 
	
[Page5](zotero://open-pdf/library/items/7IJFS4B4?page=5&a=J8SU3JTS)
	
	
#introduction, #methodology, #methylation, #nanopore
	
	
	reference: ^7e61c1

*gouilLatestTechniquesStudy2019*
	Nanopolish [77] is a popular software to detect 5mCG with a pre-trained algorithm, showing good correlation with bisulfite data on human and mouse genomes [62,77,78]. Because Nanopolish incorporates a model for 5mCG, there is no need to sequence a PCR-amplified, unmodified control in addition to the sample of interest. 
	
[Page5](zotero://open-pdf/library/items/7IJFS4B4?page=5&a=6C92KQMI)
	
	
#introduction, #methodology, #methylation, #nanopore
	
	
	reference: ^58f223

*gouilLatestTechniquesStudy2019*
	Nanopolish outputs the probability that a base is modified at a single-read, almost single-nucleotide (actually single k-mer) resolution. Other available tools differ in the underlying algorithms and the modifications they are trained to detect: signalAlign demonstrated detection of 6mA, 5mC and 5hmC [79], mCaller, DeepSignal, DeepMod and Megalodon detect 6mA and 5mCG [80–83], and D-Nascent and RepNano are tailored towards BrdU detection [84,85]. ONT-developed Tombo provides a model for 5mC and 6mA [86]. 
	
[Page5](zotero://open-pdf/library/items/7IJFS4B4?page=5&a=L3C8VK3I)
	
	
#introduction, #methodology, #methylation, #nanopore
	
	
	reference: ^c3569b

*gouilLatestTechniquesStudy2019*
	The price of whole-genome nanopore sequencing is comparable to that of whole-genome bisulfite sequencing. Detection of base modifications by nanopore sequencing is still an area of active development. 
	
[Page6](zotero://open-pdf/library/items/7IJFS4B4?page=6&a=5XE4H75M)
	
	
#introduction, #methylation, #nanopore, #price
	
	
	reference: ^b04ed7

*gouilLatestTechniquesStudy2019*
	Every time ONT upgradestheporechemistry,therawsignalchangesandthealgorithmshavetobetrainedagain.Fortunately,many tools offer the possibility for users to train the algorithms on their own data, both at the basecalling stage (e.g. Taiyaki [88], Chiron [89]) or post-alignment (Nanopolish, DeepSignal, mCaller, Tombo). Recent advances in basecalling hold the promise that genetic and epigenetic information will soon come directly out of the sequencer without the need for extra processing. 
	
[Page6](zotero://open-pdf/library/items/7IJFS4B4?page=6&a=AJPBCH6Y)
	
	
#introduction, #methodology, #methylation, #nanopore
	
	
	reference: ^d30d1d

*gouilLatestTechniquesStudy2019*
	Bisulfite sequencing provides a quantitative and sensitive assay for DNA methylation at base-resolution (Figure 1). The high-cost of deep coverage can be avoided by targeted sequencing techniques. However, standard bisulfite conversion cannot distinguish between 5mC and 5hmC and specialised protocols are required to specifically detect each of these marks. This is also true for 5caC and 5fmC and library preparation and sequencing have to be performed separately for each mark of interest. By contrast, SMRT and nanopore long-read sequencing have the capacity to detect a range of base modifications simultaneously, without additional sample preparation. 
	
[Page6](zotero://open-pdf/library/items/7IJFS4B4?page=6&a=TG4IDJBH)
	
	
#bisulfite, #introduction, #methodology, #methylation
	
	
	reference: ^296f93

*gouilLatestTechniquesStudy2019*
	In addition to the detection of base modifications not amenable to bisulfite sequencing, a major advantage of long-read sequencing is the ability to phase epigenetic and genetic information, providing allele-specific 5mC patterns that allow insight into the effect of mutations, structural variants, or parental origin on gene regulation [62,65,66,78]. 
	
[Page6](zotero://open-pdf/library/items/7IJFS4B4?page=6&a=VZMX89KK)
	
	
#introduction, #methylation, #nanopore
	
	
	reference:

*gouilLatestTechniquesStudy2019*
	Rapid iterations over ONT nanopore chemistry, protocols and software are both exciting and challenging. Contrary to bisulfite sequencing, there are few established analytical pipelines for long-read epigenetics. Benchmarking efforts are crucial to evaluate the performances of the available tools. While we are still a long way from reading out the 43 base modifications listed in DNAmod [4], long-read sequencing brings us closer to obtaining full-length, complete, and phased epigenomes. 
	
[Page7](zotero://open-pdf/library/items/7IJFS4B4?page=7&a=FHMU7JV5)
	
	
#introduction, #methylation, #nanopore
	
	
	reference: ^7dfd09




%% end annotations %%

## Bibliography

Gouil, Q., & Keniry, A. (2019). Latest techniques to study DNA methylation. _Essays in Biochemistry_, _63_(6), 639–648. [https://doi.org/10.1042/EBC20190027](https://doi.org/10.1042/EBC20190027)

%% Import Date: 2023-11-01T14:36:33.757+01:00 %%

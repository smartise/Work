---
Done: false
"date:":
tipe: Methodologysub
tags:
---
# introduction 
ONT sequencing measure the variation of an ionic current that go trough a biological nanopore as a single stranded nucleic acid is ratched through. neural network translate the current induced into nucleotides in a process named *basecalling* . DNA methylation also induce deviation in the signal making them detectable [[gouilLatestTechniquesStudy2019#^18fe6e]]. The price of this method is also similar to the the Bisulfate method [[gouilLatestTechniquesStudy2019#^b04ed7]].
ONT can detect efficiently 5mc, 5hmc and 6ma [[Accuracy#^a6acee5a]]


# methodo 
detection of base modification involve 3 steps [[gouilLatestTechniquesStudy2019#^7e61c1]]: 
- basecalling with canonical bases.
- anchoring the raw signal to a genomic reference.
- weighing the evidence that a base is modified. 


# Pros 
- nanopore offer long read sequencing that offer a solution to the mappability problem of short reads 
- can be applied to bisulfite-treated and amplified DNA to provide a similar readout than short read bisulfite sequencing 
- allow to sequance native DNA and infer base modification from their impact on the raw sequencing signal [[gouilLatestTechniquesStudy2019#^f80574]]
- no longer need for enzymatic or chemical treatments specific to each base modification of interes, reducing experimental complexity [[gouilLatestTechniquesStudy2019#^98e736]], [[Accuracy#^d993035d]].
- doesn't need any different specialised protocol to detect different mark such as 5cac, 5fmc or 5hmc wich are a variant of 5mc compare to bisulfite. nanopore has the hability to detect long range of base modification simultaneously without the need for additional sample preparation [[gouilLatestTechniquesStudy2019#^296f93]].
- has the abiliy to phase epigenetic and genetic information providing allele specific 5mc patterns, 
- alignement less complex as there is no mutation induced by sodium bisulfite 
# Cons 
- the DNA can not be amplified as PCR erase DNA methylation and thus need a significant amount of DNA (1-3 µg of DNA). it is only usable for bulk sample and not cell-to-cell analysis [[gouilLatestTechniquesStudy2019#^79a6c4]], [[gouilLatestTechniquesStudy2019#^99bd64]]

# software 
- Nanopolish : popular software to detect 5mCG with a pre trained algorithm, showing good correlation with bisulfite data [[gouilLatestTechniquesStudy2019#^58f223]].
for 6ma, 5mc and 5hmc detection 
- mCaller
- Deepsignal
- Deepmod
- Megalodon 

BrdU detection 
- D-Nascent
- RepNano 

6ma and 5mc (devlopped by ONT)
- Tombo 
[[gouilLatestTechniquesStudy2019#^c3569b]]

Allow to train the algorithme on the new data 
- Nanopolish 
- Deepsignal 
- mCaller 
- Tombo 
[[gouilLatestTechniquesStudy2019#^d30d1d]]

---
Done: false
"date:": 
tipe: subject
tags:
---
# introduction 

# How it works 
[How nanopore sequencing works](https://nanoporetech.com/support/how-it-works)

All Oxford Nanopore sequencing devices use flow cells which contain an array of tiny holes — nanopores — embedded in an electro-resistant membrane. Each nanopore corresponds to its own electrode connected to a channel and sensor chip, which measures the electric current that flows through the nanopore. When a molecule passes through a nanopore, the current is disrupted to produce a characteristic ‘squiggle’. The squiggle is then decoded using basecalling algorithms to determine the DNA or RNA sequence in real time.


# flow cells 

there is 3 tipes of flow cells: 
- The Flongle Flow Cell can generate up to 2.8 Gb of data enabling direct, real-time DNA & cDNA sequencing on smaller, single-use flow cells.
- The MinION Flow Cell can generate up to 50 Gb of data for sequencing DNA, cDNA or native RNA in real-time.
- The PromethION Flow Cell can generate up to 290 Gb for sequencing DNA, cDNA or native RNA in real-time.

cDNA is the complementary DNA of an ARN and is obtain through retrotranscriptase. 
## what's inside a flow cell
Oxford Nanopore devices are based around a core sensing unit — a nanopore set in an arrayed sensor chip  — used alongside a bespoke Application-Specific Integrated Circuit (ASIC), which controls and measures the experiments.

a flow cell is compose mostly of wells (something like 2048 wells) that each contain a nanopore

### The nanopore 
A protein nanopore is set in an electrically-resistant polymer membrane.

there is a protein called tether around the nanopore that will guide the DNA to the nanopore. 

the DNA then go through the nanopore and will disrupt the flow of ion. this diruption of flow change depending on the base that go through the nanopore 

### ASIC 
Each nanopore channel is controlled and measured individually by the bespoke ASIC. This allows for multiple nanopore experiments to be performed in parallel. More than one ASIC may be included in a device and Oxford Nanopore is building ASICs of different sizes for different purposes.



















![[0_Nanopore-metagenomic-sequencing-guide.pdf]]
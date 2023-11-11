---
Done: false
tipe: manipulation
---
protocol based on [[dimondDNAMethylationProfiling2021]]

# Protocol 
1. **DNA Quantity Assessment**: An assay was used to assess the DNA quantity.
    
2. **Confirmation of High Molecular Weight DNA**: 1% agarose gel electrophoresis was performed to confirm the presence of high molecular weight DNA (approximately 10 kb).

3. **Library Preparation**:
    
    - The first library was prepared using gDNA (genomic DNA) from a single aposymbiotic individual. The PCR-free, transposase-based ONT Rapid Sequencing Kit (SQK-RAD004) was used following the manufacturer's guidelines.
    
    - A second round of sequencing runs was performed later. For this, three libraries were prepared, each containing one aposymbiotic individual and one symbiotic individual. Both were individually barcoded. The PCR-free ONT Ligation Sequencing Kit with the Native Barcoding Expansion Kit (SQK-LSK109 and EXP-NBD103) was used, following the manufacturer's 1D native barcoding gDNA protocol.
4. **Sequencing**:
    
    - The MinION device from Oxford Nanopore Technologies (ONT) was used for sequencing. It was connected to an Apple iMac with specific hardware specifications.
    - The first library was sequenced on two FLO-MIN 106D R9.4 flow cells.
    - Each library from the second round of sequencing was run on a separate FLO-MIN 106D R9.4 flow cell.
5. **Basecalling and Demultiplexing**: This was performed using ONT Albacore Sequencing Pipeline Software v. 2.3.3.
    
6. **Adapter Removal**: Sequencing adapters were removed using Porechop v. 0.2.4[1](https://chat.openai.com/c/4b20584a-66d4-46ee-b5c8-2cce34825bd2#user-content-fn-pages:%202%5E).

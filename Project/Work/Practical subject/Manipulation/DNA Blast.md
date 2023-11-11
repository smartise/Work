---
tipe: manipulation
date: 2023-04-28T00:00:00.000-05:00
Done: true
---

# Etape 

- After having aligned and cleaned the sequence, export all sequence in TSV for that select all the sequences you want to export then go file-->export --> to multiple files --> choose TSV as file format --> OK --> choose sequence in the check box --> OK
- The next step is a bit sketchy and is open for easier modification. 
- ![[Pasted image 20230418124249.png]]
- on windows 10, there is an option where you can have a quick look of what is inside a tsv document (right window). To extract the sequence, you just double click on the sequence and then copy. 
- ![[Pasted image 20230418124720.png]]
- Next, copy the sequence on a word document as follow 
>the name of the sequence 
the sequence 

- do this step for every sequence you want to blast 

## Finding the sequence of reference using genebank
- go to this link [GenBank Overview](https://www.ncbi.nlm.nih.gov/genbank/)
- copy the gene bank code found in the article of interest (it should look like that "JX994072") in the research bar 
- when the genebank found the sequence, click on the FASTA link under the title and copy the sequence 
- Same as for the sample's sequence, copy this sequence in an other word as folow 
>the name of the sequence 
the sequence 

## doing the blast on NLM 
- go to this link  [Nucleotide BLAST: Search nucleotide databases using a nucleotide query](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome)
- click on the check box "allign two or more sequences"
- on the second text box "Enter query sequence" put all the sample's sequence one after an other 
- on the first text box "Enter subject seqence" put the reference sequence obtained with genebank 
- click on the button blast 
## what everythink mean 
![[Pasted image 20230418130916.png]]
- the tab shows diffent information, query cover percentage indicate de percentage of cover that the reference has on the sample. 100% means that the reference cover the all sample's sequence. 
- perc indentity give a percentage that express how similar are the two sequences, 100% mean an exact match. 
# Resultats en fonction des expérience 


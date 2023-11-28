# immune_receptor_genomics
Tools and human references for IG genomics. 

Notes on the reference.fasta
This reference file is a modified version of the reference.fasta downloaded from the IGenotyper github page (https://github.com/oscarlr/IGenotyper) November 2023.

Modifications to light chain loci:
1) chr22 was exchanged for T2T (CHM13v2.0) chr22. The IGL locus is on chromosome 22.
   28 kb of sequence (chr22:23,317,584-23,345,947) is from a HPRC haplotype from sample HG00621, which includes a 16093 bb insertion relative to the CHM13v2.0 reference, reflecting 3 additional copies of IGLJ-C3.
   To lift-over a chr22 coordinate from CHM13v2.0 to the chr22 in the reference.fasta in this repo, use the formula: "if start_coord > 23324706, then add 16093".

2) chr2, which includes the IGK locus, was modified to include a common insertion in the distal IGK region that includes the gene "IGKV1-NL1" - described in our preprint: https://www.biorxiv.org/content/10.1101/2023.10.23.563321v2.full

Modifications to heavy chain loci (igh, ighc):

No modifications to igh were made in this repo relative to the igh reference at https://github.com/oscarlr/IGenotyper. For a description of this igh reference, see our publications:
i) https://www.frontiersin.org/articles/10.3389/fimmu.2020.02136/full
ii) https://www.nature.com/articles/s41467-023-40070-x

which describe the igh franken reference.
The ighc reference sequence is from CHM13v2.0, without modification.

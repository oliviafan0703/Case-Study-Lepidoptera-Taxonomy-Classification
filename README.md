# Case Study: Lepidoptera Taxonomy Classification
Data science case study classifying DNA Barcodes

DNA barcoding is the practice of classifying DNA sequences sampled from an environment into a taxonomy, which is a nested sequence of tags spanned across 6 levels (phylum, class, order, family, genus and species). As seen in the picture above, the process is performed across various steps.
1. Collection of biologic material from the environment
2. DNA sequencing through PCR processing methods
3. Alignment of the obtained DNA. Alignment ensures that all the sequences are all of the same length, and the locations are meaningfully comparable.
Annotation. This means that we assign a taxonomic name to the sequence.

To show a concrete example, copy and paste the following DNA sequence into the Barcode of Life project (BOLD) identification engine:
```
---------------------------------------ACTTTATATTTTATTTTTGGAGTATGAGCAGGAATAATTGG
AACTTCTTTA---AGTTTAATAATTCGTACAGAATTAGGTAACCCTGGGTCACTAATTGGAGAT---GATCAAATTTATA
ATACTATTGTTACAGCTCATGCTTTTATTATAATTTTTTTTATAGTTATACCAATTATAATTGGAGGATTTGGTAATTGA
TTAATTCCCTTAATA---TTAGGAGCCCCTGATATAGCTTTCCCACGTATAAATAATATAAGATTTTGATTATTACCCCC
ATCATTAACTTTATTAATTTCTAGAAGTATTGTTGAAAATGGAGCAGGAACAGGATGAACAGTTTACCCCCCTCTTTCCT
CTAATATTGCCCATAGAGGATCTTCTGTTGATTTA---GCTATTTTTTCTCTACATCTTGCAGGAATTTCCTCCATCCTC
GGAGCAATTAACTTTATTACAACAATTATCAATATACGAATTAATAATATATCATTTGATCAAATACCTTTATTTGTATG
AGCAGTAGGAATTACTGCTTTATTATTATTATTATCATTACCGGTTTTAGCTGGT---GCAATTACTATATTATTAACTG
ATCGAAATTTAAATACCTCTTTTTTTGACCCTGCTGGCGGAGGAGACCCAATTCTTTACCAACATTTA------------
--------------------------------------------------------------------------------
--------------------------------------------------------------------------------
---------------------
```
The taxonomy of the DNA sequence should be returned (tap the Species page button). Which species is identified by the DNA sequence? With which level of confidence?

In this case study, a researcher from a Finnish lab has given you 7000 aligned DNA sequences collected by capturing butterflies (technically, all specimens belong to the order of Lepidoptera) in a nearby forest. Even though they he can confidently place the DNA sequences into the order of Lepidoptera, they would like to know more about the taxonomy of the specimen collected, since this was not possible to recognize through morphology. To fulfill this task, you are also given a historical dataset of 40000 annotated DNA sequences for which annotations have been confidently established. Your job is to build a classification model using this dataset and then to annotate the 7000 DNA sequence at the family and at the genus levels. In doing this, it is important that you introduce a measure of how uncertain your final annotation is.

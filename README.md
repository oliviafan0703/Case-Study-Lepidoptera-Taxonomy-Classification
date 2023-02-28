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

# Learning Objectives
- Learning about classification methods, such as logistic regression, multinomial regression, Naive Bayes and (if time allows) more complex ML methods.
- Learning how to evaluate a classification model (accuracy, ROC curves, MCC)
- Develop skills to handle categorical predictors
- Learning how to summarize and play with DNA-type data

# Case Study Goals
For each test DNA sequence, predict the Family and the Genus and provide a measure for the confidence in your prediction (e.g. best probability). When you build your model, make sure to first validate on a validation set (eg. 30%) of your training data.
Make sure you address the following questions (variable selection methods can be used):
- How accurate are your in-sample predictions at the family and at the genus levels?
- What about in the validation set(s)?
- Is the whole DNA sequence important for doing classification?
- Which loci along the sequences are particularly important for classification?

# Data
Data for this case study are available on the STA 440L container as well as on Sakai. There are two datasets:

Lepidoptera_library.csv: a dataset of 40000 DNA sequences and their annotations. You can ignore the species column, since we are interested in only family and genus

test_sequences.csv: 7000 test DNA sequences. No affiliation is reported, so your job is to predict both family and genus, and also to verify if some DNA sequences correspond to “new” species (if you want extra points).

The DNA sequence is constructed so that loci are comparable. However, alignnment comes with some problems. For example, some loci will not have the classic A, C, G and T letters, but might have alignemnt gaps - or other special characters. It is up to you how to deal with these terms, as long as you justify yorur choice.



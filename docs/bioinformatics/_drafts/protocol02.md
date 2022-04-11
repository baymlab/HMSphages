---
layout: default
title: 2. Working with sequencing reads
parent: Bioinformatics
nav_order: 2
---

# Working with sequencing reads

## Overview of sequencing technologies

## FASTQ format
What happens after we load our DNA in any of the machines listed above? How do we get the data out? Well, the exact details depend a bit on the machine we're using, but ultimately, they all have a way to export files containing the DNA sequences that the machine _read_. Therefore, the files contain a list of all of these sequencing <mark>reads</mark>, which are stored in text files using the <mark>FASTQ format</mark>.

Remember the [FAST**A** format](/bioinformatics/protocol01_intro.html#fasta-format)? Well, the FAST**Q** is an extension of the FASTA format, with the added feature that it can store the **Q**uality score associated with each nucleotide in a sequence. The score intends to be a measure of the confidence of a certain base being called correctly, and some programs take this information into account when using sequencing data.

A FASTQ entry, is comprised of the following 4 lines:
1. `@` character, followed by sequence name/description
2. Sequence
3. `+` character
4. Quality values (encoded in ASCII, you can read more about that [here](https://en.wikipedia.org/wiki/FASTQ_format))

For example:
```
@SEQ_ID
GATTTGGGGTTCAAAGCAGTATCGATCAAATAGTAAATCCATTTGTTCAACTCACAGTTT
+
!''*((((***+))%%%++)(%%%%).1***-+*''))**55CCF>>>>>>CCCCCCC65
```

And we could write the same sequence in FASTA format like this:

```
>SEQ_ID
GATTTGGGGTTCAAAGCAGTATCGATCAAATAGTAAATCCATTTGTTCAACTCACAGTTT
```

---
> 🧙‍♀️ We can always go from a `FASTQ` file to a `FASTA` file but not the other way around!

---

## Exploring reads (BLASTing reads)
An easy way 

## Quality checks and trimming with fastqc and trimmomatic
## Overview of aligning
## Aligning reads with minimap2
## Visualizing aligned reads with IGV
## Exercise: Explore a variant that confers antibiotic resistance in a bacterial genome
## Glossary:
short reads, long reads, paired reads, fastq, trimming, aligning, sam, bam
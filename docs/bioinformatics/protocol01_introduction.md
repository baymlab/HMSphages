---
layout: default
title: 1. Introduction
parent: Bioinformatics
nav_order: 1
---

# Introduction
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# Slides: The _flow_ of genetic information

<div class="responsive-wrap">

  <iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSttfgMom2F0OUXQbRmxcebQdzzSJGajI3kv6QJo6_l3f_Bj1rHaH0gA2XKi6phrYvh54blrbEGHM71/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

</div>

---

# Activity 1: From DNA to Protein

## Rationale
{: .no_toc }

We will start by manually _translating_ a DNA sequence into a protein sequence. 

## Activity 1
{: .no_toc }
{: .label .label-blue }

```
  1   CTATTATACCAATCGGCTTCATGTATCCGCACGCGGGCGAAATTAGCCCG    50
 51   CGCGAAACCACCTATTAACCTGACGAGGAGGCCCACACGCGAGGAAGATG   100
101   GCGGATAGCTGCATTGAAAACACCATTAGCACCTGGGCGCGCAACATTAA   150
151   CGGCTGATAGACTGTTGCACGTTGGGGGAGAACATCCAGATAGCGCTAGC   200
201   TATGATTTCCTCTGAACTGTTGATAGAATGGGCTTCCCATGAGCGCGAAT   250
251   AGTAAGCGAATAGAACAAAGACGCCTGCTACAACAGGAGTATCAACCCGT   300

```

1. Find all the possible start codons.
1. Using the DNA codon translation table, translate the DNA sequence into amino acid sequences from the start codon until you hit a stop codon.
1. Answer the following for each amino acid sequence:
  - What is the amino acid sequence?
  - How long is each amino acid sequence?
  - How long is the nucleotide sequence?
1. Write your own **DNA sequence** coding for a small mock protein with 10 amino acids of your choice. 


# Activity 2: Exploring phage genomes in NCBI

## Rationale
{: .no_toc }

NCBI is the **N**ational **C**enter for **B**iotechnology **I**nformation, and it's one of many online resources where biological data is stored. Their website, [https://www.ncbi.nlm.nih.gov/](https://www.ncbi.nlm.nih.gov/), hosts *many* different databases. We will explore how to use some of them to learn more about the biological sequences we find.


## Activity 2.1
{: .label .label-blue }
{: .no_toc }

- Follow along:

1. Go to the the [NCBI website](https://www.ncbi.nlm.nih.gov/) and look for the genome with the following accession `NC_002371.2`
    + ([Here's the direct link](https://www.ncbi.nlm.nih.gov/nuccore/NC_002371) but try to find it yourself first!)
1. Try to find the following information:
    + Where can you find the accession?
    + How big is the genome?
    + What other properties of the genome can you find in the `LOCUS` line?
    + What _type_ of phage is it? (Siphoviridae, Podoviridae, Myoviridae, other?) 
    + Can you find the bacterial host? 
1. Go back to the top and find the `FASTA` view. Click it. What do you see? Looks familiar?
1. Go into the `Graphics` view. Zoom in, move around, hover over the boxes. What do you see?
    + What does the boxes represent?
    + What are the arrows in the box?
    + Look for the **head protein** and zoom until you can see the nucleotide sequence. Can you find the `START` codon?
1. Go back to the `GenBank` view. (Make sure `Whole sequence` is selected in the top right corner!) Scroll down until you find the `FEATURES` section.
    + Can you find the sequence for the _head protein_?
    + Can you find a protein that says _hypothetical protein_? What does this mean?


## Activity 2.2
{: .label .label-blue }
{: .no_toc }

- Now, you'll each have an accession code for a phage genome. Follow the instructions bellow and take notes of what you find, so that you tell the rest of the class what you learned about your phage.

1. Select an accession code from the bag:
  - `XXXXXXX`
  - `XXXXXXX`
1. Go to [NCBI](https://www.ncbi.nlm.nih.gov/) and find the genome record.
1. Find the following information about your phage:
  - How big is the genome?
  - Is the genome DNA or RNA, linear or circular?
  - What _type_ of phage is it? (Siphoviridae, Podoviridae, Myoviridae, other?)
  - Can you find the bacterial host?
  - Can you find the _coat_ protein (or _capsid_ protein)? 

# Activity 3: Search DNA sequences with BLAST

## Rationale
{: .no_toc }

Here, we'll start with one of the most popular ways to search for sequences, a program called `BLAST`💥. It's so popular that it's become a verb among biologists: _"BLASTing"_. You can think about it as the _Google_ for biological sequences. We'll learn how to BLAST a phage genome, which will help us find other related phages.


## Activity 3
{: .label .label-blue }
{: .no_toc }

1. Open the [BLAST website](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
1. Click on *Nucleotide `BLAST`*
  - When would you use Protein `BLAST`?
1. Explore the `BLAST` window.
  - What is Query?
  - What databases are available?
1. In a new tab, open [NCBI](https://www.ncbi.nlm.nih.gov/) and find the genome record for the phage you selected in the Activity 2.2.
1. Go to the `FASTA` view, and copy the DNA sequence of your phage.
1. Return to the tab with `BLAST` and copy the sequence into the *Query* box.
1. Click on the button that says BLAST and wait for the results.
1. Take notes about some of the top results of your search.
  - Are there other phages that look a lot like your phage?
  - How similar or how different are they?
  - How do the *Query Cover* percentages look like?
  - How do the *Percent Identity* values look like?
  



---
layout: default
title: 1. Introduction
parent: Bioinformatics
nav_order: 1
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# 1. Introduction to Bioinformatics

## Why do we need bioinformatics?
_Bioinformatics_ may sound sophisticated, but its a generic term that roughly means using computers to study biology. 
**Using computers usually means less work!** (or I guess technically: _Less work for you, more work for the computer!_ ) 

The first step if you want to do _bioinformatics_ is learning how to talk to the computer in its "mother tounge". You already know some ways to talk to the computer: For example, when you double click to open a program, or when right click and select `Change file name` to rename an existing file. This is a very _human_ way to talk to a computer. Someone actually designed all of these buttons, icons and stuff (also called **G**raphical **U**ser **I**nterfaces or GUIs) so that it would be easy to interact with a computer without much previous knowledge, and it's great for many things! Like surfing the web, looking at pictures, etc.

But imagine you want to change the name of 10 files, it starts to get annoying, no? Now imagine 100, or 1 million. 😰

That's when being able to talk to the computer in it's "mother tounge" comes in handy. Computers are great at repeating tasks over and over, at chaining different instructions together, making decisions based on the information they have about each file, producing figures, etc. They are truly powerful! But to be able to use this power _fully_, we need to talk to them a bit differently. We need a _programmatic_ way to give it instructions, and we'll do this through the <mark>command-line</mark>. 

What does this have anything to do with biology? Well, biological data can be large and complex, and we need help interpreting what it means. If you open a file with the DNA sequence of a genome, you won't get much from just seeing a long list of letters, and if you were to use pen and paper to analyze it, it would take a long time. So, we'll start with the command-line, which at the beginning might look like a hacker-tool in which we just change file names in a fancy way, but we'll get to all the cool biology stuff soon enough.

So, in this section, we're going to learn the following:
- How is biological data stored and where to find it.
- How to give basic instructions to the computer through the <mark>command-line</mark>.


## Fantastic biological data and where to find it

### FASTA format

Genomes are made of DNA, they are long molecules made of a secuence of four different bases: **A**denine, **T**hymine, **C**ytosine, and **G**uanine, which we can represent with their initial letters: **A**, **C**, **G**, and **T**.

When we want to store this information in a computer, we can convieniently store the sequence of letters that _represents_ the real bases in the molecule, in a very similar way in which we can store any other text document. Easy enough, no? 

I guess before storing it, we can give the sequence a name too. We can do this by adding a `>`  in the first line, folowed by the name of the sequence. That way, we can even have multiple sequences per file. For example:


```
>sequence1
ATGATGGGAAAAGGTTTTGAAATGATGGTAGCCAGCGCAATCCGTGCCGCTGGTATTAATCCTGATGAAT
TGATGGAAAAGGCTAATACCCTTGTCCATAATTTGAATTACCAGCTTGACCGTTTCGGCCAGCGGCTGGA
TTCCATTGATTCGCGCCTTTCGGTAATTGAAAAGGCGCTTGATATTTCCCCGGCAGAAAAGCCGGACAAT
CAGCCCGAATTAACGGGTATTACTTTTGAAGGTGACAACAATGACCAATGA

>sequence2
ATCG
```


and _TA DA!_🎉 You have what we call the <mark>fasta format</mark>. This is the most popular, and one of the simplest ways to store DNA sequence information. These files are simple "text files", the sort that you can directly open in application like _Notepad_ or [_Sublime Text_](). By convention, we usually give them the file extension `.fasta` or `.fa`. 
Ok, let's go and explore some genomes!

---
> 🧙‍♀️ File extensions tell the computer what type of file something is, so that it can try to use the right program to open it, but they're not set in stone. You can change extensions as you wish or make up your own extensions, and the _file itself_ won't change! Give it a try!

---


### Exploring bacterial genomes in NCBI
NCBI is the **N**ational **C**enter for **B**iotechnology **I**nformation, and it's one of [many]() online resources where biological data is stored. Go ahead and visit their website:

[https://www.ncbi.nlm.nih.gov/](https://www.ncbi.nlm.nih.gov/)

As you can see, there are a lot of options there, and that's because NCBI hosts many different <mark>databases</mark>. To start, let's try to find a genome. You can click on **Genome** under **Popular Resources**, or go directly to: [https://www.ncbi.nlm.nih.gov/genome/](https://www.ncbi.nlm.nih.gov/genome/)


---

Activity 1
{: .label .label-green }

1. Find a reference genome for _Escherichia coli_.
    - ([Here's one](https://www.ncbi.nlm.nih.gov/nuccore/NC_000913.3) but try to find it yourself first!)
2. Try to find the following information: <mark>accession</mark>, size of the genome, year.
3. Find the `FASTA` view. What do you see? Can you figure out how to download that `FASTA` file?
4. Go into the `Graphics` view. Zoom in, move around. What do you see?
    - What does the red color represent? How about purple?
5. Download the `GenBank(full)` file.
    - Open the `GenBank(full)` file in your text editor. What do you see? What is the extension on that file?
    - Now open it with **SnapGene**. Explore!

---


### Searching with BLAST

One of the most powerful tools in biology, from plant biology to bioinformatics, is **comparing stuff** ✨. Sequence comparison is the basis for a lot of the things we'll learn for this course. There are many ways to do it, with different levels of sophistication depending on what you want to do.

Here, we'll start with one of the most popular ways to compare sequences, a program called `BLAST` 💥. It's so popular that it's become a verb among biologists: _"BLASTing"_. 

<mark>BLAST</mark> stands for **B**asic **L**ocal **A**lignment **S**earch **T**ool, so this name gives us a big hint of what it is usually used for: Searching. 


If you have a new DNA sequence, an obvious way to try to figure out what it, is by searching for similar stuff. For that you need two things: 1. The thing you are basing your search on (_Query_), 2. The collection of things you're going to search (_Database_), and 3. A way to search (_Search algorithm_).

- **Query**: 

- **Database**: is tremendously important. Searching/Comparing sequences is only possible if you have things to search in the first place! Additionally, you want to have an idea of what the things in the database are in the first place. If you have random pieces of DNA that you don't know what they are, or at least where they come from, it will be of little use to find a match. If the database has mostly DNA of bacteria but you're looking for a virus, it might not be very useful. This is called bias. If the database is large, you'll be more likely to find what you're looking for. But there's a problem! The bigger the database, the harder it is to find things. And that's why we need specialized _Search Algorithms_

- **Search Algorithm**: In this case, `BLAST`. The field of computational biology deals with this. BLAST is one of many. It also scores the hits.

- **Hit** is what the algorithm reports when it finds something. In blast, it will include a description, the name, query cover, e-value, percent identity,

---

Activity 2
{: .label .label-green }

1. Copy `sequence1` from the [FASTA format section](#fasta-format)
2. Go to NCBI's BLAST website: [https://blast.ncbi.nlm.nih.gov/Blast.cgi](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
3. Select **Nucleotide BLAST**
4. Copy your sequence into the box, select the `Nucleotide collection` database.
5. BLAST! 💥
6. How many resulst did you get?
7. Which organisms seem to have a similar sequence to your Query?
8. Look at Query Cover, E-value and per. identity.
9. Check the **Graphic Summary**
10. Click on the first hit.
11. Click on Graphic 
12. Explore: What do you think your sequence is? How similar is it? Is it the full length of the reference?
13. Repeat with `sequence2` and `sequence3`
14. Try a protein you get from your SnapGene file.

---


## Command-line basics
OK, so now we've seen how we can store, view and search some biological data. Going back to BLAST, it has a nice GUI in a website, which is all good, but again, imagine I give you 10 000 sequences. That would be horrible. So first we'll learn some basics. Ok, how to start the command line?



### File management, browsing
The first thing is to open the <mark>command-line</mark>. (Shell, terminal). Imagine this was one of the first computers. This is just how they look. Let's get it in full screen to get the real experience. You would start the computer and see that: Welcome, you're now in the computer. One of the first things you'll notice is that there are no pictures. No cool background image, no icons, apps or nothing.  So the first thing is to figure out where we are. 

---

Activity 3
{: .label .label-green }


- Type:
```
pwd
```

What you see there is your _location_, or we could think of it as the _adress_ of where you are in the computer. That's our first command:

> `pwd`: **p**rint **w**orking **d**irectory

Why <mark>print</mark>? Well, in computer science it means show the text, <mark>directory</mark> is a computer-sciency way of saying folder. So _working directory_ it's just refering to where you're working. So it's like asking "tell me where I am". 

Now that we know *where* we are, let's try to see what's there.

- Type:
```
ls
```

> `ls`: **l**ist **d**irectory contents

This shows us all the contents of that directory. If we want more information, we can ask for the "long format" and writing `ls -l`, (`l` for long) and that way we get the size of the files, and a bunch of other data.

---


- `.`: means "in this directory"
- `..`: means "in the parent directory"
- `cd \<directory\>`: **c**hange **d**irectory
- `mkdir`: **m**ake **d**irectory
- `touch`: make a file
- `mv`:
- `rm`:
    - `rm -r`:
- `less`:
- `nano/vim`






---



### Downloads
### Installing software
### Running software
### Local vs. server - ssh

## Glossary
<mark>accession</mark>
: Some sort of ID that uniquely identifies a record in a database. Sometimes called _accession number_, although it is rarely a number.
: (For example, for _E.coli_ MG1655, the NCBI's RefSeq database accession is: `NC_000913.3`)

<mark>BLAST</mark>
: Is a program/algorithm to compare DNA (RNA, or protein) sequences. It can be used to *search* similar sequences in databases. Nucleotide BLAST is also called `BLASTn`, Protein BLAST is also called `BLASTp`.

<mark>directory</mark>
: It's a folder in the computer!

<mark>fasta format</mark>
: Text-based file format used to store DNA (RNA, or protein) sequences. It is usually stored with the extensions: `.fasta`, `.fa`, `.fna` (to specify it'a a nucleotide file), or `.faa` (to specify it's a protein file). You can find an example [here](#fasta-format).

<mark>genbank format</mark>
: Text-based file format that stores DNA sequences, as well as many additional information, like author, references, anotations, etc. It is usually stored with the extensions: `.gb` or `.gbk`.

<mark>NCBI</mark>
: The National Center for Biotechnology Information. They host many important databases (like _RefSeq_ and _GenBank_) and bioinformatics services (like _BLAST_), which can be accessed through their [website](https://www.ncbi.nlm.nih.gov/).

<mark>path</mark>
: Is the location of a file, directory, or program in a computer. You can see it with the command `pwd`. The separaction character: `/`, is used to represent the directory organization. For example:
: The path for a directory could look like this: `/Users/nquinones/folder1/`
: The path for a file inside that directory could look like this: `/Users/nquinones/folder1/file1.txt`

<mark>print</mark>
: In computer science, printing means

<mark>ssh</mark>
: `ssh` is a fancy thing called Secure Shell Protocol. For our purposes, it's what allows us to remotely connect to a computer (to a _server_) through the command-line.
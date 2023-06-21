---
layout: default
title: 2. Assembling whole phage genomes
parent: Bioinformatics
nav_order: 2
---

# Assembling whole phage genomes
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# Slides: Assembling genomes

<div class="responsive-wrap">

  <iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTS3E2vXEi5mWIczMjpSBaaOqAC5ue-FKuJBoT3bvlGIJz36hXHoFYps3xZS_kyFcUUfbbt6YMzG3Vs/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="460" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

</div>


# Activity 1: Command line basics

## Rationale
{: .no_toc }

We will learn the basics of how to use the terminal to give direct instructions to the computer.

## Activity 1
{: .no_toc }
{: .label .label-blue }

- Follow along and **take notes in your printed cheat sheet**:

1. Open the **Terminal Preview** app
    - (Make the window half of the size of the screen so that you can see the Desktop)
1. Write:
```
bash
```
1. Write
```
ls
```
    - What shows up in the Terminal?
    - Take notes on your *cheat sheet*.
1. Write:
```
mkdir myfolder
```
    - What showed up in the Desktop?
    - Open `myfolder/` by clicking on it on the Desktop.
    - Take notes on your *cheat sheet*
1. Write:
```
cd myfolder
```
    - What changed in the terminal?

1. Write:
```
ls
```
    - Why happened? Why?
1. Write
```
mkdir myfolder2
```
1. Write
```
ls
```
1. Write
```
touch hello.txt
```
1. Open `hello.txt` on the **Sublime Text** app.
1. Inside **Sublime Text**, write: "Hello world!"
1. Save the file by going to File > Save. You can close Sublime Text now.
1. Go back to the **Terminal Preview**
1. Write
```
less hello.txt
```
1. Exit the `less` view by typing the letter:
```
q
```
1. Write
```
rm text_file.txt
```
1. Write:
```
ls
```
    - What happened to `hello.txt`?
1. Write:
```
cd ..
```
    - Where did we go?
1. Write:
```
ls
```
1. You can close the **Terminal Preview** app now.

# Activity 2: Exploring your read files from the command line

## Rationale
{: .no_toc }

We will download your read files and learn how to look at your reads in the terminal.

## Activity 2
{: .no_toc }
{: .label .label-blue }

1. Download your read files from Google Drive
    - Visit the [Google Drive](https://drive.google.com/drive/folders/14AFbHZkzES69j9jdyqCtLmkQAYv2cwao?usp=share_link) and open the folder with your name
    - Click on the little arrow in the top right of the page
    - Click download. This will get saved in your `Downloads/` folder
    - Move the folder from your `Downloads/` to your `Desktop/`
    - If the folder is "zipped", open it and move the folder inside into the `Desktop/`.
1. Open the **Terminal Preview** app.
1. Write
```
ls
```
1. Write
```
cd <name of your folder>
```
    - **Here, replace `<name of your folder>` with the name of the folder you downloaded!!**
    - Instructions between angle brackets  **`< like this >`** mean that you have to write the name of the files YOU have.
1. Write
```
ls
```
    - Do you see your read files?
    - There should be two, one that ends with `_R1.sub.fastq.gz` and another that ends with `_R2.sub.fastq.gz`

1. To make it human readable, write
```
gunzip -c <name_of_your_reads>_R1.sub.fastq.gz > reads_R1.fastq
```
    - *(You don't need to remember this one.)*
1. To see it, write:
```
less reads_R1.fastq
```
    - What do you see?
    - How long is the first read?
    - You can exit this view by writing `q`
1. To know how many reads are in the file, write:
```
echo $(cat reads_R1.fastq|wc -l)/4|bc
```
    - This is another "special command" to count the number of reads in our file. (You don't need to remember this one.)
    - How many reads are in one of your read files?



# Activity 3: Assembling your genome with `Unicycler`

## Rationale
{: .no_toc }

We will use a software called `Unicycler` to assemble our reads into whole genomes.

## Activity 3
{: .no_toc }
{: .label .label-blue }
1. Go to the class computer
1. Write
```
ls
```
1. Locate your folder, and enter the folder that contains your reads
```
cd <name of your folder>
```
1. Then write:
```
unicycler -h
```
    - This is the software's "help". It tells us how to use it.
    - Scroll up and down to see the options.
1. Now we will run the assembly. Write in a single line:
```
unicycler
-1 <name_of_your_reads>_R1.sub.fastq.gz
-2 <name_of_your_reads>_R2.sub.fastq.gz
-o assembly
```
    - What are the options `-1` and `-2`?
    - What is the `-o` option?
1. Let your assembly run.


# Activity 4: Looking at your assembled genome

## Rationale
{: .no_toc }

Once the assembler has run, you should have larger pieces of DNA sequence, which hopefully corresponds to a whole genome sequence.

## Activity 4
{: .no_toc }
{: .label .label-blue }
1. Download your assembly from [Google Docs](). Put it inside the folder with your reads.
1. Open the **Terminal Preview** app
1. Write
```
bash
```
1. Go to the folder in the Desktop that contains your reads
```
cd <name of your folder>
```
1. Go to the folder that contains the results from the assembly:
```
cd assembly
```
1. Write:
```
ls
```
    - There, you will find many files, but the one we care about is `assembly.fasta`
1. The assembly might contain more than one large piece of DNA. Let's check how many it has:
```
grep -c "^>" assembly.fasta
```
    - How many pieces of DNA does your assembly contain?
    - (This is another special command you don't need to remember.)
1. To extract only the first piece. Write
```
cat assembly.fasta | awk "/^>/ {n++} n>1{exit} 1" > contig1.fasta
```
    - (This is another special command you don't need to remember.)
1. Write:
```
less contig1.fasta
```
    - How long is the assembly you got?
1. Exit this by typing
```
q
```
1. Open the `contig1.fasta` file in the **Sublime Text** app.
1. Open the [BLAST website]()
1. Copy the sequence inside `contig1.fasta` and paste it into the **Query box** of the `BLAST` website.
1. Search by clicking "BLAST" and wait for the results.
1. Look at the 5 best hits and make note about:
    - Description
    - Query Cover
    - Percentage ID
    - In your opinion, how similar is your phage to the previously known phages?
1. Select one of the hits, and go to its genome record. Just like yesterday, try to find:
    - How big is the genome?
    - Is the genome DNA or RNA, linear or circular?
    - What type of phage is it? (Siphoviridae, Podoviridae, Myoviridae, other?)
    - What is the bacterial host?

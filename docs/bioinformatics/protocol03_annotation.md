---
layout: default
title: 3. Annotating genomes
parent: Bioinformatics
nav_order: 3
---


# Annotating genomes
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# Slides: Annotating genomes

<div class="responsive-wrap">

  <iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRcNpEYO1NcpxzBS_VUMBdvO6dKM8K4wKiGxwazOzyS2A-OkZro3oaqs78z66s5-4ks1qA03rAWUqhd/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="460" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

</div>



# Activity 1: Review of command-line

## Activity 1
{: .no_toc }
{: .label .label-green }


> See [Command line basics](./protocol02_assembly.html#activity-1-command-line-basics) from yesterday.


# Activity 2: Annotating your phage genome

## Rationale
{: .no_toc }
Now that we have whole genome assemblies, we can find coding sequences in our phage's genome, and _annotate_ what we know about the proteins we find. 


## Activity 2.1
{: .no_toc }
{: .label .label-green }

- Generating the annotation

1. Open the **Terminal Preview** app
1. Write:
```
bash
```
1. Go to the folder that has your assembly:
```
cd <name_of_your_folder>
cd assembly
```
1. Write:
``
ls
``
    - You should see the file `assembly.fasta`.
1. To enable `prokka`, write:
```
conda activate prokka
```
1. To look at the options, write:
```
prokka -h
```
    - What do the following options do:
        - `--prefix`
        - `--hmms`
1. Finally, to run the annotation you should write:
```
prokka --prefix <name_of_your_sample> --hmms phrogs/all_phrogs.hmm --compliant assembly.fasta
```
1. Wait for the software to finish annotating
1. Once it's done, a new folder should appear in your `assembly` folder.
1. Open the folder in the file browser and look for a file ending in `.gbk`
    - It will be `<name_of_your_sample>.gbk`
1. Right-click on that file and open it with **Sublime Text**
    - Does it look familiar?
    - Why is the organism data wrong?

## Activity 2.2
{: .no_toc }
{: .label .label-green }
- Visualizing your genome

1. Now, open the program **UGENE**
1. Click on **Open File(s)**, and select your `<name_of_your_sample>.gbk` file.
    - What do you see? Let's review the main sections of this program.
1. Go to the bottom panel of the window, click on the arrow `>` next to **gene**
1. Right-click on the first gene and click **Disable gene highlighting**
1. Click on the arrow `>` next to **CDS**
    - Remember what CDS means?
    - What is the number in parenthesis next to **CDS**? (Take notes!)
1. Click on the **Show circular view** button (top of the window)
1. Click on the **Annotations Highlighting** button (right side of the window)
    -   In the text box under **Show value of qualifier** erase the contents and write: **product**
1. Click on the **Circular View Settings** button (right side of the window)
1. Make the font bigger for the Title and Annotations
1. Explore your annotation
    - How many proteins does your whole genome assembly have in total?
    - How many are "hypothetical protein"?
    - How many are not?
1. Save the genome map by clicking on the Camera icon (left side of the window)
    - Disable the two check boxes
    - Select format PNG
    - Make it at least 3000px x 3000px
    - Save it in the folder that you created in the Desktop
1. Click on the **Statistics** button (right side of the window)
    - Record length, GC content

> Keep UGENE open, we will need it for Activity 3.


# Activity 3: Building a phylogenetic tree

## Rationale
{: .no_toc }
To learn more about how our phage relates to other phages, we are going to build a small phylogenetic tree. These trees represent relationships between organisms, and we are going to use a single protein of our phage, look for related proteins with `BLAST`, and build a tree using the program `seaview`


## Activity 3.1
{: .no_toc }
{: .label .label-green }

To get a sense of how trees are built, we will have an activity with candy!

## Activity 3.2
{: .no_toc }
{: .label .label-green }
1. Go back to UGENE and with the help of the map, look for the **capsid protein**. (It might also be called **major head protein**, **coat protein**)
1. Click on the arrow representing the protein in the map. It should get highlighted.
1. Then, right-click on the protein, and select `Copy/Paste`>`Copy annotation amino acids`
1. Open **Sublime Text** and write:
```
> myphage
```
1. Press enter to make a new line, and paste the protein sequence you had copied.
1. Save this file in your folder in the `Desktop` and call it `capsid_proteins.fasta`
1. Open the [BLAST website](https://blast.ncbi.nlm.nih.gov/Blast.cgi) and click on **Protein BLAST**
1. In the query box, paste the protein sequence you have in **Sublime Text**. Click BLAST.
1. Look at your results.
1. Uncheck the **select all** box
1. Select 5-10 interesting results by clicking on the selection boxes to the left.
1. Click on the **Alignments** tab, and click the `Download`>`FASTA (aligned sequences)` option.
1. This will download a file called `seqdump.txt` into your `Downloads` folder. Open this file.
1. Copy the contents of `seqdump.txt` and paste them into your `capsid_proteins.fasta` file.
1. Save the file again.
1. Open the software **seaview**
1. Open the `capsid_proteins.fasta` file, by selecting `File`>`Open` and select your file.
1. Align your sequences by clicking on `Align`>`Align all`. When it's done, click **OK**.
    - What happened to your sequences?
1. Build a tree by clicking on `Trees`>`PhyML` and then clicking `Run`. When it's done, click **OK**
    - Where did your protein (`myphage`) land?
1. Save your tree by clickin on `File`>`Save as PDF`. Save it in your folder in the `Desktop`

# (PART\*) Testing Ideas {-}

# RNA-seq Analysis

## Pre-lab: Intro to RNA-seq

### Purpose

In this pre-lab, students learn about RNA-sequencing so that we can take a closer look at some RNA-seq data in class.

### Learning Objectives

1. Compare and contrast the genome and the transcriptome
1. Describe the steps involved in RNA-seq
1. Define bioinformatics and its role in biology

### Introduction

Next-generation DNA sequencing has revolutionized biological research. This tutorial will explain the basic process of next-gen sequencing and will discuss some of the ways it is used in research.

### Activity 1 - Biotechnology: Next-Gen Sequencing

*Estimated time: 20  min*

#### Instructions

1. Log into SciServer, click on compute and open your C-MOOR LearnR” container.
1. Start the “Biotechnology: Next-Gen Sequencing” tutorial. Visit [SciServer Guides and FAQs](https://help.c-moor.org/t/sciserver-guides-and-faqs/22). if you need to jog your memory on how to do this.
1. To move through the activities click "Continue" at the bottom of the screen. When you are done with a topic, click "Next Topic" to move on.

#### Questions

| What is Bioinformatics? |
|:-|
| <br> |

<br>

| Briefly describe each of the following steps of next-gen sequencing: | |
|:-|:-|
| in vivo | |
| in vitro | |
| in silico | |

### Activity 2 - Biotechnology: RNA-Seq

*Estimated time: 10 min*

#### Instructions

1. Start the “Biotechnology:RNA-Seq” tutorial.
1. To move through the activities click "Continue" at the bottom of the screen. When you are done with a topic, click "Next Topic" to move on.

#### Questions

| What is Differential Gene Expression? |
|:-|
| <br> |

<br>

| What feature  of mRNA allows scientists to specifically isolate mRNA for RNA-seq? |
|:-|
| <br> |

<br>

| Describe the steps in making cDNA from an mRNA. |
|:-|
| <br> |

<br>

| Explain how the number of reads related to gene expression. |
|:-|
| <br> |

### Footnotes

#### Resources

- [Google Doc](https://docs.google.com/document/d/1zqTb5HacEqEVhFv4nmRsCB8FSCEMDkP_)

#### Contributions and Affiliations

- Stephanie R. Coffman, Ph.D. Clovis Community College
- Katie Cox, Ph.D. Carnegie Institute at John Hopkins University

Last Revised: March 2022

## Lab Slides and Demo {#lab-slides-rna-seq-analysis}

### Lab Slides

<img src="rna-seq-analysis_files/figure-html//1-bQsuEIWO6e0ekb98byMAHR8_l45pp_fsl7NxJIXkbM_g35f391192_00.png" width="480" />

[[slides](https://docs.google.com/presentation/d/1-bQsuEIWO6e0ekb98byMAHR8_l45pp_fsl7NxJIXkbM)]

### Sort Gene Expression Data Using Spreadsheets

<img src="rna-seq-analysis_files/figure-html//1oNO9JFmC8itk3eq6amT95MWvOsr3zQb6LNwZsQ7-i-g_gdf3f6e5285_0_0.png" width="480" />

[[slides](https://docs.google.com/presentation/d/1oNO9JFmC8itk3eq6amT95MWvOsr3zQb6LNwZsQ7-i-g)][[test-driveR.tsv](https://drive.google.com/file/d/1kMWQReRTg0FDZDA5abxmkgKxp-7o5IeM)]

## Lab Activity: RNA-seq Analysis

### Purpose

In this lab, students will complete a tutorial on RNA-seq data and learn how to analyze, graph and interpret the data. In the following lab, we will use these skills to compare two RNA-seq data sets to investigate gene expression patterns.

### Learning Objectives

1. Use R to analyze HTSeq files
1. Create and analyze histograms from HTSeq files

### Introduction

Today’s lab will investigate how scientists use computer science to analyze RNA-seq data. In general, the sequences are first aligned to a reference genome. For RNA-seq, the sequences will align to exons of the expressed genes. The data you will look at today has already been processed using a program called HTSeq. This program aligns the sequences to the reference genome and counts how many sequences align to each gene, producing files known as HTSeq files. The more sequences that align to the gene, the higher the expression level of the gene. The following tutorial will walk you through how to analyze an HTSeq file using the programming language R.

The RNA-seq libraries from today’s lab are from: [eLife 2013;2:e00886 DOI: 10.7554/eLife.00886](https://elifesciences.org/articles/00886).  The paper analyzes genes expression in the drosophila midgut.

### Activity 1 - Introduction to RNA-seq Data Tutorial

*Estimated time: 20 min*

#### Instructions

1. Log into SciServer, click on compute and open your C-MOOR LearnR” container.
1. Start the “Introduction to RNA-seq Data” tutorial. Visit [SciServer Guides and FAQs](https://help.c-moor.org/t/sciserver-guides-and-faqs/22). if you need to jog your memory on how to do this.
1. To move through the activities click "Continue" at the bottom of the screen. When you are done with a topic, click "Next Topic" to move on.
1. This tutorial has small boxes in which you can enter and run short lines of code to analyze the data.
1. As you work through the tutorial, answer the questions below. When you get to “Try it Out!” move on to Activity 2.

#### Questions

| What are the two columns (V1 and V2) in an HT-seq file? What data is stored in each column? |
|:-|
| <br> |

<br>

| Explain what is readCount and what is GeneID |
|:-|
| <br> |

<br>

| Share a screenshot of the row showing the readCount of the lab gene in the “Reproduce Results for a Single Gene” section and explain in your own words what the code in your screenshot is doing. |
|:-|
| <br> |

### Activity 2 - Analyze an HT-seq file

*Estimated time: 15-20 min*

#### Instructions

1. In groups of two, analyze the HTSeq samples assigned to you.

| | Assigned Sample |
|:-|:-|
| Name | |
| Name | |

2. Use the code blocks on the "Try it out!" page to analyze the data.
    a. The codeblocks on the "Try it out!" page, has this code typed out for you:
        i. `readCounts <- read.table( "data/FILENAMEHERE.htseq")`
    a. Change `FILENAMEHERE` to the filename for your file. Once you have done this, **readCounts** will have the new HTSeq file loaded into it
        i. Example: `readCounts <- read.table( "data/SRR891602.htseq")`
1. The code above loads the data set into `readCounts`. If you run this code alone, nothing will happen. Try requesting some analysis to get a look at the data and answer the questions below.
1. Answer the questions below as you analyze the data. Consult the “Cheat Sheet” to figure out which code to use.

#### Questions

Determine the total reads across all genes, and the mean, median and max read counts for a single sample. Each student reports on one of the samples analyzed.

| Assigned Sample | |
|:-|:-|
| Total Reads | |
| Mean Read Count  | |
| Median Read Count  | |
| Max Read Count  | |

<br>

Look up the GeneID of the gene you presented on from the Biological Databases Lab. Use the filter command to find the readCount in both samples assigned to your group.

| How many reads does the gene have in your assigned dataset? |
|:-|
| Share a screenshot. |

<br>

| How many reads does the gene have in your partner's dataset? |
|:-|
| Share a screenshot. |

<br>

| Compare this number to the mean; is it average, high or low? |
|:-|
| <br> |

### Footnotes

#### Resources

- [Google Doc](https://docs.google.com/document/d/1ABmBmDwDtxipxmlfWuVypjIVt2AmTZtY)

#### Contributions and Affiliations

- Stephanie R. Coffman, Ph.D. Clovis Community College
- Rosa Alcazar, PH.D. Clovis Community College
- Katie Cox, Ph.D. Carnegie Institute at John Hopkins University

Last Revised:
March 2022

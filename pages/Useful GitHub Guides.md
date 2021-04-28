---
title: Useful GitHub Guides
---

## https://rstudio.com/wp-content/uploads/2016/10/how-big-is-your-graph.pdf

## Markdown cheatsheet: https://gist.github.com/jonschlinkert/5854601

## [[Skicka Github Package]]

## Page on into to command line/bash: https://astrobiomike.github.io/unix/getting-started

## How to circularize analyses/plots in R: https://ourednik.info/maps/2020/01/22/draw-anything-you-want-with-r-on-the-cartesian-grid/

## tanghaibao/jcvi

## Determining copy number in R: https://osf.io/zq879/wiki/home/

## Flow charts in R: https://krlmlr.github.io/dm/

## https://biomedicalhub.github.io/genomics/04-part4-denovo-assembly.html

## https://jmonlong.github.io/Hippocamplus/2017/09/19/mummerplots-with-ggplot2/

## **Useful code**
### check for contamination
#### `sendsketch.sh in= ../4_8.fastq`

### remove contamination
#### `bbduk.sh in1=Z001_illumina_1.pe.qc.fastq in2=Z001_illumina_2.pe.qc.fastq out1=clean_Z001_illumina_1.fastq out2=clean_Z001_illumina_2.fastq mingc=0.45`

### For determining read coverage:
#### The best way to calculate coverage is by mapping, not by looking at the assembler's logs.  For example, with BBMap:

#### `bbmap.sh in=reads.fq ref=contigs.fa covstats=covstats.txt`

#### That will print a message like this:
##### Average coverage:                       278.50
Percent scaffolds with any coverage:    100.00
Percent of reference bases covered:     99.98

#### ...in addition to creating "covstats.txt" which will list the coverage statistics for each individual scaffold.  The reads you use for mapping should be the ones you fed into Spades.

## Bam/Sam files: https://seqan.readthedocs.io/en/seqan-v1.4.2/Tutorial/BasicSamBamIO.html

## In depth comparison of assemblers: https://github.com/rrwick/Long-read-assembler-comparison

## http://combo.dbe.unifi.it/contiguator/

## ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FQualifying_Exam%2FUh6Uj0w87m.png?alt=media&token=86f36b8b-f695-445c-8efc-7b4f9746f2a4)

## 

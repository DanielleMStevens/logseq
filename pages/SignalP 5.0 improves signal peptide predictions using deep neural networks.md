---
title: SignalP 5.0 improves signal peptide predictions using deep neural networks
---

## **Authors**: [[José Juan Almagro Armenteros]], [[Konstantinos D. Tsirigos]], [[Casper Kaae Sønderby]], [[Thomas Nordahl Petersen]], [[Ole Winther]], [[Søren Brunak]], [[Gunnar von Heijne]] and [[Henrik Nielsen]]

## **Journal**: [[Natural biotechnology]]

## **Readcube**: https://www.readcube.com/library/95fd6ff6-fca1-4a81-9ddb-c57079c1e1f2:a3e69fd1-6a64-4a74-a5ef-e19ae739e4f5

## **Tags**: #genomics 

## **Abstract**:
### a deep neural network-based approach that improves SP prediction across 
all domains of life and distinguishes between three types of prokaryotic SPs

## **Introduction**:
### The general secretory pathway (Sec) directs protein translocation across
 the plasma membrane in prokaryotes and the endoplasmic reticulum 
membrane in eukaryotes

### Bacteria, Archaea, chloroplasts and some mitochondria also have a Tat 
(twin-arginine translocation) pathway that recognizes generally longer 
and less hydrophobic SPs containing two consecutive arginines (R-R) in 
the amino-terminal region

### Unlike the Sec pathway, which transports proteins in an unfolded state, 
the Tat pathway can translocate folded proteins across the lipid 
membrane bilayer.

### Most SPs are removed by signal peptidase (SPase) I (LepB in Bacteria), which has orthologs in Archaea and Eukarya.

### Bacterial lipoproteins are cleaved by a second signal peptidase, signal peptidase II (or Lsp), which cleaves SPs that contain a conserved 
carboxy-terminal ‘lipobox’

### Sec substrates can be processed by SPase I, SPase II or SPase III, but Tat substrates are only processed by SPase I or SPase II.

### SignalP versions 1 through 4 can only predict Sec-translocated SPs cleaved by SPase I

### Specialized methods are available to predict Tat translocation or SPase 
II cleavage, some of which only apply to one type of SP and cannot  differentiate between all three classe

## **Results**:
### SignalP 5.0 distinguishes three types of signal peptides in prokaryotes: Sec substrates cleaved by SPase I (Sec/SPI), Sec substrates cleaved by SPase II (Sec/SPII), and Tat substrates cleaved by SPase I (Tat/SPI).

### it cannot identify Tat substrates cleaved by SPase II, although these are known to exist

### therefore our algorithm cannot identify Sec substrates processed by SPase III.

### SignalP 5.0 achieved an overall MCC of 0.938, 0.907, 0.890 and 0.966 for
 predicting Sec/SPI SPs for Archaea, [[Gram-negative bacteria]], Gram-positive bacteria and Eukarya, respectively

### A common problem in CS prediction is that experimental data used to 
train prediction algorithms can have erroneous or uncertain annotations.

### To account for this uncertainty, we considered a window of one, two and 
three AAs around the annotated CS position, assuming that, if the annotation was incorrect, the correct position should be nearby. We reported a correct prediction if the predicted CS was within that window.

### SignalP 5.0 is the only method capable of simultaneously predicting all types of SPs, each benchmark was run twice: first with only the respective SP type as the ‘positive’ data set and TM and globular proteins as the ‘negative’ data set and then adding the two remaining SP types to the ‘negative’ data set

### SignalP 5.0 has the best SP discrimination across all organisms in the Sec/SPI benchmark, with the exception of Gram-positive bacteria, for which it ranks second after SignalP 4.1

## **Discussion**:
### Finally, the performance of TOPCONS2 (ref. 24), which is the only consensus method tested in our benchmark, is high in Bacteria, but not in Archaea or Eukarya, for which it ranks below average

### although PRED-TAT has better prediction performance in Gram-positive bacteria.

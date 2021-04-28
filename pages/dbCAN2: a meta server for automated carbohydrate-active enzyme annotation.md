---
title: dbCAN2: a meta server for automated carbohydrate-active enzyme annotation
---

## **Authors**: [[Han Zhang]], [[Tanner Yohe]], [[Le Huang]], [[Sarah Entwistle]],[[Peizhi Wu]], [[Zhenglu Yang]], [[Peter K. Busk]], [[Ying Xu]], and [[Yanbin Yin]]

## **Journal**:

## **Readcube**: https://www.readcube.com/library/95fd6ff6-fca1-4a81-9ddb-c57079c1e1f2:8d7e6ee1-0388-43a9-8b41-6b296878f84c

## **Tags**: #genomics #CAZymes

## **Abstract**:
### all [[CAZymes]] of a genome annotation: (i) HMMER search against the dbCAN HMM (hidden Markov model) database; (ii) DIAMOND search against the CAZy pre-annotated CAZyme sequence database and (iii) Hotpep search against the conserved CAZyme short peptide database.

### Combining the three outputs and removing CAZymes found by only one tool can significantly improve the CAZome annotation accuracy.

## **Introduction**:
### Hybrid biopolymers with carbohydrates covalently linked to other biopolymers, such as glycoproteins and glycolipids, are called glycoconjugates

### are synthesized, degraded, and modified by carbohydrate active enzymes (CAZymes) in all organisms

### genomes of animal gut bacteria encode hundreds of carbohydrate-degrading
 GH (glycoside hydrolase) genes, in contrast to only 17 digestive GH genes encoded in the human genome 

## **Results**:
### **CAZy database**:
#### Since 1990s over 360 CAZyme families have been defined and classified by the CAZy database, forming six major classes: glycosyltransferases [GTs], glycoside hydrolases [GHs], polysaccharide lyases [PLs], carbohydrate esterases [CEs], carbohydrate-binding module [CBM] and enzymes for the auxiliary activities [AAs]

#### Two approaches of CAZome annotation exist in the literature:
##### (A) Users contact the CAZy database for collaboration, who will perform semi-automatic CAZome annotation for the users (11); as expert manual curations are involved, CAZy annotation is regarded as the gold standard method.

##### (B) sers run automatic tools such as HMMER (12) or BLAST (13) by themselves for CAZome annotation

#### each CAZyme family we retrieved its signature domains from CAZy pre-annotated members, by searching against the CDD (conserved domain database of NCBI) database and manual literature curation; we then built our own HMMs for most CAZyme families instead of using Pfam HMMs.

#### We update dbCAN almost once a year, by creating HMMs for CAZyme families and subfamilies newly created in the CAZy database

#### n 2017, a new tool named Hotpep (15) annotates CAZymes by searching 
against PPR (peptide pattern recognition) library for conserved short 
peptide motifs

### **New functions and updates**:
#### HMMER search against dbCAN HMM database, and also DIAMOND (23) search against CAZy pre-annotated CAZyme sequence database

#### In dbCAN2, we have added the third tool: Hotpep search against the PPR short peptide library.

#### The accuracy is calculated as an F-score = 2 × (Recall × Precision)/(Recall + Precision) for the three tools on each examined genome, following the method presented in our previous papers

#### Table 1 shows that ^^DIAMOND+CAZy has the highest F-score (0.89) for bacteria but the lowest F-score for eukaryotes (0.84)^^; in contrast, Hotpep + PPR has the highest F-score (0.94) for eukaryotes but the lowest F-score for bacteria (0.80). HMMER + dbCAN performs very well for both eukaryotes (0.86) and bacteria (0.88) and a slightly higher overall F-score than the other two tools

#### In terms of running time, DIAMOND runs the fastest, followed by Hotpep and HMMER.

#### It should be mentioned that DIAMOND + CAZy has a much higher risk than 
the other two tools to give wrong CAZyme family annotation.

#### ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FQualifying_Exam%2FB25QQfVO1Z.png?alt=media&token=d6981540-b41e-438b-8af9-be70036dbdce)

#### **CAZyme gene clusters (CGCs)**:
##### CGCs are also known as polysaccharide utilization loci (PULs), which are defined as physically linked genes specializing in the degradation of various complex carbohydrates

## **Discussion**:
### dbCAN2 is a web server for automated carbohydrate-active enzyme 
annotation. It is an updated version of the original dbCAN web server, 
and has the following new features: 
#### (1) dbCAN2 allows submission of nucleotide sequences: genomic sequences of prokaryotic draft genomes and metagenomes; 

#### (2) dbCAN2 integrates three state-of-the-art tools/databases for automated CAZyme annotation: 
##### (i) HMMER for annotated CAZyme domain boundaries determination according to the dbCAN CAZyme domain HMM database; 
(ii) DIAMOND for fast Blast hits in the CAZy database; 
(iii) Hotpep for short conserved motifs in the PPR library; 

#### (3) dbCAN2 can also identify transcription factors (TFs), transporters (TCs), and further CAZyme gene clusters (CGCs) using CGC-Finder if users submit protein sequences plus gene location files or genomic DNA sequence file;

#### (4) dbCAN2 combines the results from the three tools and allows visualization of the overlaps as Venn diagram and the detailed results as graphs.

#### 

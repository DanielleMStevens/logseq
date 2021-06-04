---
title: How to apply de Bruijn graphs to genome assembly
---

- **Authors**: [[Philip E.C. Compeau]], [[Pavel A. Pevzner]], and [[Glenn Tesler]]
-
- **Journal**: [[Natural biotechnology]]
- **Readcube**: https://www.readcube.com/library/95fd6ff6-fca1-4a81-9ddb-c57079c1e1f2:ec399605-4936-4ae1-955c-6a4c959b5e2f
- **Tags**: #genomics
-
- **Scalable assembly with de Bruijn graphs**:
	- finding a cycle that visits all nodes of a graph exactly once (called the Hamiltonian cycle problem) is a difficult computational problem
	- ^^finding a cycle that visits all edges of a graph exactly once is much easier^^
	- we will now assign each such [[k-mer]] to an edge
	- **Eulerian cycle:**
		- 1. Form a node for every distinct prefix or suffix of a [[k-mer]], meaning that a given sequence of length k –1 can appear only once as a node of the graph.
		  2. connect node x to node y with a directed edge if some [[k-mer]] (e.g., ATG) has prefix x (e.g., AT) and suffix y (e.g., TG), and label the edge with this [[k-mer]]
	- As it visits all edges of the de Bruijn graph, which represent all possible [[k-mer]]s, this new ant also spells out a candidate genome
	- He proved that a connected graph with undirected edges contains an Eulerian cycle exactly when every node in the graph has an even number of edges touching it
		- Königsberg Bridge graph (Fig. 1b), this is not the case because each of the four nodes has an odd number of edges touching it and so the desired stroll through the city does not exist
	- de Bruijn graph contains an Eulerian cycle as long as we have located all [[k-mer]]s present in the genome
-
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FQualifying_Exam%2Fb2BbPkUIom.png?alt=media&token=c59577b3-fd44-409d-bca4-aceeeb2daa19)
  **Figure 3: Two strategies for genome assembly: from Hamiltonian cycles to Eulerian cycles.** (a) An example small circular genome. (b) In traditional Sanger sequencing algorithms, reads were represented as nodes in a graph, and edges represented alignments between reads. Walking along a Hamiltonian cycle by following the edges in numerical order allows one to reconstruct the circular genome by combining alignments between successive reads. At the end of the cycle, the sequence wraps around to the start of the genome. The repeated part of the sequence is grayed out in the alignment diagram. (c) An alternative assembly technique first splits reads into all possible k-mers: with k = 3, ATGGCGT comprises ATG, TGG, GGC, GCG and CGT. Following a Hamiltonian cycle (indicated by red edges) allows one to reconstruct the genome by forming an alignment in which each successive k-mer (from successive nodes) is shifted by one position. This procedure recovers the genome but does not scale well to large graphs. (d) Modern short-read assembly algorithms construct a de Bruijn graph by representing all k-mer prefixes and suffixes as nodes and then drawing edges that represent k-mers having a particular prefix and suffix. For example, the k-mer edge ATG has prefix AT and suffix TG. Finding an Eulerian cycle allows one to reconstruct the genome by forming an alignment in which each successive k-mer (from successive edges) is shifted by one position. This generates the same cyclic genome sequence without performing the computationally expensive task of 
  finding a Hamiltonian cycle.
-
- The time required to run a ^^computer implementation of Euler’s algorithm is roughly proportional to the number of edges^^ in the de Bruijn graph
- The factors that influence the choice of algorithms include the quantity of data (measured by read length and coverage); quality of data (including error rates); and genome structure (e.g., ^^GC content and the number and size of repeated regions^^)
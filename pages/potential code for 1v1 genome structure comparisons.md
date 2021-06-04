---
title: potential code for 1v1 genome structure comparisons
---

- ```r
											-
											  #install.packages(devtools)
											  devtools::install_github("dwinter/pafr")
											  library(pafr, quietly=TRUE)
											  test_alignment <- pafr::read_paf(file_name = file.choose())
											  test_alignment2 <- subset(test_alignment, test_alignment$qlen > 1000)
											  #adjust order before plotting
											  ref_order <- list(c("NODE_1_length_3089142_cov_12.251788"), c("MDHC01000001.1"))
											  
											  pafr::dotplot(test_alignment2, order_by = "provided", ordering = ref_order, alignment_colour="blue") + theme_bw()
											  pafr::plot_synteny(test_alignment2, q_chrom="DMS092", t_chrom="CASJ002", centre=F, rc=T )
											  plot_coverage(test_alignment2, fill = 'qname')
											  ```
											  
											  ## ```r
											  #######
											  # Purpose: Visualize fastANI core-genome comparison
											  # Usage: Rscript <this_script>  <query sequence in fasta format> <subject sequence> <fastANI visualization output>
											  # Output: <fastANI visualization output filename>.pdf
											  # Uses genoPlotR package: http://genoplotr.r-forge.r-project.org
											  
											  # make sure to set path to the same place where the figure 
											  setwd(dirname(rstudioapi::getActiveDocumentContext()$path))
											  
											  
											  
											  #Parse command line arguments
											  #query_fasta=commandArgs(TRUE)[1]
											  #subject_fasta=commandArgs(TRUE)[2]
											  #fastANI_visual_file=commandArgs(TRUE)[3]
											  
											  install.packages('genoPlotR', dependencies = T)
											  #library(devtools)
											  #install_github("sdray/ade4")
											  
											  library(genoPlotR)
											  #library(ade4)
											  
											  #choose file to visualize .out.visualize from fastANI
											  #Read fastANI output
											  comparison_analyse <- genoPlotR::read_comparison_from_blast(file = file.choose())
											  
											  #Read sequences into genoPlotR objects
											  Query <- genoPlotR::read_dna_seg_from_file(file = file.choose()) #query fasta file
											  Ref <- genoPlotR::read_dna_seg_from_file(file = file.choose()) #reference fasta file
											  
											  # update name (query vs. reference)
											  plotTitle = paste("CASJ002_original", "CASJ002", sep=" v/s ")
											  
											  pdf(paste("CASJ002_originalvs_CASJ002",".pdf",sep=""))
											  
											  genoPlotR::plot_gene_map(dna_segs=list(Query, Ref), 
											                           comparisons=list(comparison), main=plotTitle, scale=FALSE, scale_cex=1, n_scale_ticks=4)
											  
											  dev.off()
											  
											  ```
- 
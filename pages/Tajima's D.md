---
title: Tajima's D
---

- **Tajima's D** is a population genetic test [statistic](https://en.wikipedia.org/wiki/Statistic) created by and named after the Japanese researcher [Fumio Tajima](https://en.wikipedia.org/wiki/Fumio_Tajima).
-
- is a statistic that compares the average number of pairwise differences with the number of segregating sites.
	- is computed as the difference between two measures of genetic diversity: ^^the mean number of pairwise differences (π)^^ and ^^the number of segregating sites (θ)^^, each scaled so that they are expected to be the same in a neutrally evolving population of constant size.
- However, it must be carefully analyzed because population demography changes how Tajima’s D can be interpreted
- ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FQualifying_Exam%2F66h1jEfVId.png?alt=media&token=cc0ee1a1-707f-4a26-8809-1cfb2a6d8054)
- *Figure 1.** A population bottleneck with a new rare allele (orange) arising after the bottleneck.
- The purpose of Tajima's D test is to distinguish between a [DNA sequence](https://en.wikipedia.org/wiki/DNA_sequence) evolving randomly ("neutrally") and one evolving under a non-random process, including [directional selection](https://en.wikipedia.org/wiki/Directional_selection) or [balancing selection](https://en.wikipedia.org/wiki/Balancing_selection), demographic expansion or contraction, [genetic hitchhiking](https://en.wikipedia.org/wiki/Genetic_hitchhiking), or [introgression](https://en.wikipedia.org/wiki/Introgression).
- The strength of genetic drift depends on population size. If a population is at a constant size with constant mutation rate, the population will reach an equilibrium of gene frequencies.
- to identify sequences which do not fit the neutral theory model at equilibrium between [mutation](https://en.wikipedia.org/wiki/Mutation) and [genetic drift](https://en.wikipedia.org/wiki/Genetic_drift).
-
- Interpreting Tajima's D
	- A negative Tajima's D signifies an excess of low frequency polymorphisms relative to expectation, indicating population size expansion (e.g., after a bottleneck or a selective sweep) and/or purifying selection. A positive Tajima's D signifies low levels of both low and high frequency polymorphisms, indicating a decrease in population size and/or balancing selection. However, calculating a conventional "p-value" associated with any Tajima's D value that is obtained from a sample is impossible. Briefly, this is because there is no way to describe the distribution of the statistic that is independent of the true, and unknown, theta parameter (no pivot quantity exists). To circumvent this issue, several options have been proposed.
-
-
  |Value of Tajima's D| Tajima's D=0|Tajima's D<0|Tajima's D>0|
  |:---| :---: | :---: |---:|
  |Mathematical reason|θ-π equivalent to Theta-k (Observed=Expected). Average Heterozygosity= # of Segregating sites.|θ-π less than Theta-k (Observed<Expected). Fewer haplotypes (lower average heterozygosity) than # of segregating sites.|
  |Biological interpretation 1|Observed variation similar to expected variation|Rare alleles abundant (excess of rare alleles)|
  |Biological interpretation 2|Population evolving as per mutation-drift equilibrium. No evidence of selection.|Recent selective sweep, population expansion after a recent bottleneck, linkage to a swept gene|
-
-
- {{[[table]]}}
	- Value of Tajima's D
		- Mathematical reason
			- Biological interpretation 1
				- Biological interpretation 2
	- Tajima's D=0
		- θ-π equivalent to Theta-k (Observed=Expected). Average Heterozygosity= # of Segregating sites.
			- Observed variation similar to expected variation
				- Population evolving as per mutation-drift equilibrium. No evidence of selection.
	- Tajima's D<0
		- θ-π less than Theta-k (Observed<Expected). Fewer haplotypes (lower average heterozygosity) than # of segregating sites.
			- Rare alleles abundant (excess of rare alleles)
				- Recent selective sweep, population expansion after a recent bottleneck, linkage to a swept gene
	- Tajima's D>0
		- θ-π greater than Theta-k (Observed>Expected). More haplotypes (more average heterozygosity) than # of segregating sites.
			- Rare alleles scarce (lack of rare alleles)
				- Balancing selection, sudden population contraction
-
- **Rare variants contribute little to π**
	- In the examples below, sequences are represented as dashes and asterisks. The sequences are aligned and a dash is a site that is the same between sequences and the asterisks represents a mutation.
- Given some sequences, what are the values for π and θ?
- **Example 1**
- ---*---*------
  -------*---*--
  -------*------
  -----------*--
	-
	- ![\hat{\theta}_T=\frac{2+1+3+1+1+2}{6}=1.67](https://s0.wp.com/latex.php?latex=%5Chat%7B%5Ctheta%7D_T%3D%5Cfrac%7B2%2B1%2B3%2B1%2B1%2B2%7D%7B6%7D%3D1.67&bg=ffffff&fg=111111&s=3)
	- ![\hat{\theta}_W=\frac{3}{1+\frac{1}{2}+\frac{1}{3}}=1.63](https://s0.wp.com/latex.php?latex=%5Chat%7B%5Ctheta%7D_W%3D%5Cfrac%7B3%7D%7B1%2B%5Cfrac%7B1%7D%7B2%7D%2B%5Cfrac%7B1%7D%7B3%7D%7D%3D1.63&bg=ffffff&fg=111111&s=3)
- So in this case, π gives us a similar estimate compared to θ. However, this will change once we introduce more rare mutations. The numerator in π  is the number of differences between each sequence. For example, if you compare the first 2 sequences, there are 2 differences. The first and third have 1 difference, etc.
-
- **Example 2**
- -*------------
  ----*---------
  -------*------
  -----------*--
- ![\hat{\theta}_T=\frac{2+2+2+2+2+2}{6}=2](https://s0.wp.com/latex.php?latex=%5Chat%7B%5Ctheta%7D_T%3D%5Cfrac%7B2%2B2%2B2%2B2%2B2%2B2%7D%7B6%7D%3D2&bg=ffffff&fg=111111&s=3) and ![\hat{\theta}_W=\frac{4}{1+\frac{1}{2}+\frac{1}{3}}=2.2](https://s0.wp.com/latex.php?latex=%5Chat%7B%5Ctheta%7D_W%3D%5Cfrac%7B4%7D%7B1%2B%5Cfrac%7B1%7D%7B2%7D%2B%5Cfrac%7B1%7D%7B3%7D%7D%3D2.2&bg=ffffff&fg=111111&s=3)
- Here, because each mutation is a rare variant, the estimate of ![\theta](https://s0.wp.com/latex.php?latex=%5Ctheta&bg=ffffff&fg=111111&s=3) is lower in ![\hat{\theta}_T](https://s0.wp.com/latex.php?latex=%5Chat%7B%5Ctheta%7D_T&bg=ffffff&fg=111111&s=3) than in θ.
   This effect is not very pronounced in this example because n is so small, but if we increase n to 100 and make every mutation a rare one (i.e. at a frequency of 0.01), we can see the effect more clearly.
-
- Tajima’s D
- Tajima’s D is the ^^comparison between the average number of pairwise differences and the number of segregating sites in a sample^^. We expect positive selection (or selective sweeps) to give us a negative Tajima’s D in a population that doesn’t have any demographic changes going on (population expansion/contraction, migration, etc). This is because θ will be greater than π.
	- **Why?** Because after a selective sweep, most of the haplotypes in a population will be the same. Therefore, when mutations occur they will be rare. When you have a lot of rare mutations, π underestimates θ compared to θw and you get a negative Tajima’s D.
- In the case of balancing selection, alleles are kept at intermediate frequencies. This produces a positive Tajima’s D because there will be more pairwise differences than segregating sites.
-
- The effect of bottlenecks
- ![](https://arundurvasula.files.wordpress.com/2015/02/unnamed-chunk-6-1.png?w=493)
- Under demographic scenarios, Tajima’s D can exhibit signals that look like selection even under neutral simulations. Above, you can see how Tajima’s D changes before, during, and after a bottleneck. The effect of population expansion (recovery) on Tajima’s D is staggering. As soon as the population expands, Tajima’s D drops to about -0.45. It continues to drop and begins to recover, but stays negative. This effect is common even when the bottleneck size changes. Below, you can see what happens to Tajima’s D after a bottleneck when the recovery from the bottleneck event varies (10% of the population survives in the bottleneck):
- ![Tajima's D is negative after a bottleneck](https://i2.wp.com/i.imgur.com/3hMooRp.png)
- Why does this happen? On average, a bottleneck event will remove rare alleles due to sampling and intermediate alleles will be rare. On average, there will be more rare variants than intermediate variants and Tajima’s D will be negative. This makes it hard to distinguish signals of selection from Tajima’s D when a population has gone through a bottleneck. A neutral population with no selection will look the same as a population that has recently undergone a selective sweep. Below is a stronger bottleneck (1% of population survives):
- ![1% bottleneck](https://i0.wp.com/i.imgur.com/DosYZrm.png)
- and here is a weaker bottleneck (20% of population survives):
- ![20% bottleneck](https://i1.wp.com/i.imgur.com/Cr1zQTM.png)
- In all cases, Tajima’s D drops to negative values after a bottleneck. The 1% bottleneck has a much different shape than either of the other bottlenecks. This is because when such an extreme bottleneck occurs, every allele will be rare and Tajima’s D will start out negative. It 
  recovers from the bottleneck in a similar way towards 0. However, in all of these simulations, Tajima’s D never converges to 0 (note that these are neutral simulations). This is because when we have a finite number of samples, the resting point of Tajima’s D is not 0, but a small 
  negative number close to 0.
- As we can see from these simulations, Tajima’s D is a complicated statistic and care must be taken when using it to analyze populations. For more on the effect of bottlenecks on populations, check out this presentation: http://www.slideshare.net/jrossibarra/bottlenecks-some-ramblings-and-a-bit-of-data-from-maize
-
- Good papers and posts:
	- [This is a good blog post.](https://arundurvasula.wordpress.com/2015/02/18/interpreting-tajimas-d/)
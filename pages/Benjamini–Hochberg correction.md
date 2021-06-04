---
title: Benjamini–Hochberg correction
---

- What is the Benjamini-Hochberg Procedure?
- The Benjamini-Hochberg Procedure is a powerful tool that decreases the [false discovery rate](https://www.statisticshowto.com/false-discovery-rate/).
- Adjusting the rate helps to control for the fact that sometimes small[ p-values ](https://www.statisticshowto.com/p-value/)(less than 5%) happen by chance, which could lead you to incorrectly [reject the true null hypotheses](https://www.statisticshowto.com/support-or-reject-null-hypothesis/). In other words, the B-H Procedure helps you to avoid [Type I errors ](https://www.statisticshowto.com/probability-and-statistics/statistics-definitions/type-i-error-type-ii-error-decision/)(false positives).
- A p-value of 5% means that there’s only a 5% chance that you would get your observed result __if__ the null hypothesis were true. In other words, if you get a p-value of 5%, it’s highly unlikely that your null hypothesis is not true and should be thrown out. But it’s only a probability–many times, true null hypotheses are thrown out just because of the randomness of results.
- **A concrete example: **Let’s say you have a group of 100 patients who you know are free of a certain disease. Your null hypothesis is that the patients are free of disease and your alternate is that they __do__ have the disease. If you ran 100 statistical tests at the 5% alpha level, **roughly 5% of results would report as false positives.**
- There’s not a lot you can do to avoid this: **when you run statistical tests, a fraction will always be false positives.** However, running the B-H procedure will decrease the number of false positives.
-
- See this website: [**Benjamini-Hochberg procedure**](https://www.statisticshowto.com/benjamini-hochberg-procedure/)
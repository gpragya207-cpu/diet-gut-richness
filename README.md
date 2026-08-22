# Diet and Gut Microbiome Richness

## Table of Contents
- [Overview](#overview)
- [Research Question](#research-question)
- [Data Source](#data-source)
- [Approach](#approach)
- [Findings](#findings)
- [Limitations](#limitations)
- [Conclusion](#conclusion)
- [Tools](#tools)

## Overview

This project tests whether diet, specifically fat and calorie intake, relates to gut microbiome richness, using the COMBO dataset (96 individuals). Raw bacteria abundance and diet data were merged, a richness metric was computed per person, and permutation-based hypothesis testing was used to check whether richness differs meaningfully between above- and below-average intake groups. Neither fat nor calorie intake showed a statistically significant relationship with richness in this sample.

## Research Question

Does diet, specifically fat and calorie intake, relate to gut microbiome richness?

## Data Source

Processed data from the COMBO study, originally published in:
> Wu, G. D. et al. (2011). Linking Long-Term Dietary Patterns with Gut Microbial Enterotypes. *Science*, 334(6052), 105-108.

Data files provided via Shi, Zhang & Li (2016), *Ann. Appl. Stat.*, 10(2), 1019-1040, hosted at [github.com/muellsen/c-lasso](https://github.com/muellsen/c-lasso).

## Approach

1. Load and merge raw data files (bacteria abundances, fat and calorie intake) for 96 individuals.
2. Compute microbiome richness (the count of distinct bacterial genera present) for each person.
3. Split individuals into above- and below-average intake groups, separately for fat and calorie intake.
4. Run permutation tests comparing median richness between these groups, to check whether any observed difference is larger than would be expected by chance.

## Findings

Neither fat intake (p = 1.0) nor calorie intake (p = 0.26) showed a statistically significant relationship with microbiome richness in this dataset. The observed differences in richness between above- and below-average intake groups were well within the range expected under random chance.

## Limitations

The small sample size (n = 96) limits statistical power, meaning a real but modest relationship could exist without being detected here. Fat and calorie values are mean-centered rather than absolute, so group comparisons reflect relative standing within this sample rather than true intake amounts.

## Conclusion

This analysis did not find evidence that fat or calorie intake relates to gut microbiome richness in this sample. That is a genuine, honestly reported null result rather than an inconclusive one: both permutation tests returned p-values well above conventional significance thresholds. Given the limited sample size, this should be read as "no detectable relationship in this dataset" rather than proof that no relationship exists at all.

## Tools

Python, pandas, NumPy, Jupyter Notebook

# Diet and Gut Microbiome Richness

Analysis of whether diet (fat and calorie intake) relates to gut microbiome richness, using the COMBO dataset.

## Data Source

Processed data from the COMBO study, originally published in:
> Wu, G. D. et al. (2011). Linking Long-Term Dietary Patterns with Gut Microbial Enterotypes. *Science*, 334(6052), 105–108.

Data files provided via Shi, Zhang & Li (2016), *Ann. Appl. Stat.*, 10(2), 1019-1040, hosted at [github.com/muellsen/c-lasso](https://github.com/muellsen/c-lasso).

## Approach

1. Load and merge raw data files (bacteria abundances, fat/calorie intake) for 96 individuals
2. Compute microbiome richness (count of distinct bacterial genera present) per person
3. Run permutation tests comparing richness between above- and below-average fat/calorie intake groups

## Findings

Neither fat intake (p = 1.0) nor calorie intake (p = 0.26) showed a statistically significant relationship with microbiome richness in this dataset.

## Limitations

Small sample size (n=96) limits statistical power, and fat/calorie values are mean-centered, so comparisons reflect relative standing rather than absolute intake.

## Tools

Python, pandas, NumPy, Jupyter Notebook

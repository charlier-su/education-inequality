# Education Inequality Data Investigation

This investigation aims to explore the relationship between socioeconomic factors and school performance, as measured by average student scores on the ACT exam, in order to understand the impact of educational opportunity inequality in U.S. high schools.

## Data Source

- **EdGap**: Socioeconomic characteristics and average ACT scores of schools from [EdGap.org](https://edgap.org). Available in this repository as `EdGap_data.xlsx`.
- **NCES**: Basic identifying information about schools, provided by the [National Center for Education Statistics](https://nces.ed.gov/ccd/pubschuniv.asp). Available via Dropbox at [https://www.dropbox.com/s/lkl5nvcdmwyoban/ccd_sch_029_1617_w_1a_11212017.csv?dl=0](https://www.dropbox.com/s/lkl5nvcdmwyoban/ccd_sch_029_1617_w_1a_11212017.csv?dl=0).

## Data Processing

### Preparation

Several steps were taken to prepare the data:
- Unhelpful columns were removed from the NCES data set.
- The EdGap and NCES data sets were merged based on their NCES ID number.
- The columns were renamed to follow best practices and improve clarity.
- Schools with missing or impossibly low average ACT scores were removed.
- Schools that were not regular high schools were removed.
- Impossible values for `percent_lunch` and missing values were imputed using an `IterativeImputer` from `scikit-learn`.

The prepared data as well as the notebook used for data preparation are available in this repository as `clean_school_info.csv` and `data_preparation.ipynb`.

### Analysis

The data analysis was done in the `data_analysis.ipynb` notebook, which is available in this repository. Several questions were explored:
* What factors contribute most to ACT score?
  * More specifically, what quantitative predictors are most effective for estimating ACT score?
* If certain socioeconomic factors are unhelpful for predicting ACT score, why might that be?
* Does region (i.e. area within the US) affect ACT score?

## Authors

- Charlie Robinson ([LinkedIn](https://www.linkedin.com/in/-charlierobinson/))

## License

This project is licensed under the terms of the MIT License.

# DS650-Project

## Data Dictionary

### Key Columns
- `year`: Year from 2012-2015
- `INSTNM`: Institution name
- `coltype`: Describes the type of data represented in that row for the feature columns
  - `raw`: Represents raw value (preexisiting or engineered); multiplied by -1 if inversely correlated with diversity
  - `scaled`: Raw values min-maxed scaled (min is 0, max is 1)
  - `weight`: Weight for that feature (based on overall variance for the feature)
  - `score`: Final value used for diversity index (`scaled * weight`)

### Existing Ranking/Score Columns
- `world_rank_THE`: Ranking from Times Higher Education (THE)
- `world_rank_RUR`: Ranking from Round University Ranking (RUR)
- `world_rank_CWUR`: Ranking from Center for World University Ranking (RUR)
- `score_THE`: Score used to create THE ranking
- `score_RUR`: Score used to create RUR ranking
- `score_CWUR`: Score used to create CWUR ranking

### Feature Columns for Diversity Index
- `UGDS_race_score`: Variance of race distribution (inverse)
- `UGDS_gender_score`: Variance of gender distribution (inverse)
- `first_gen_score`: Variance of first generation distribution (inverse)
- `income_score`: Variance of income distribution (inverse)

### Diversity Columns
- `diversity_index`: Weighted average of scores from feature columns
- `diversity_rank`: Rank based on score from diversity index
- `diversity_year_rank`: Rank based on score from diversity index (partitioned by year)

### Feature Engineering Columns

#### UGDS (Undergraduate Degree Seeking) Score
- `UGDS_WHITE`: Percentage enrolled who are White
- `UGDS_BLACK`: Percentage enrolled who are Black
- `UGDS_HISP`: Percentage enrolled who are Hispanic
- `UGDS_ASIAN`: Percentage enrolled who are Asian
- `UGDS_AIAN`: Percentage enrolled who are American Indian/Alaska Native
- `UGDS_NHPI`: Percentage enrolled who are Native Hawaiian/Pacific Islander
- `UGDS_2MOR`: Percentage enrolled who are two or more races
- `UGDS_NRA`: Percentage enrolled who are non-resident aliens
- `UGDS_UNKN`: Percentage enrolled who have unknown race

#### UGDS Gender Score
- `UGDS_MEN`: Percentage who are male
- `UGDS_WOMEN`: Percentage who are female

#### First Gen Score
- `PAR_ED_PCT_1STGEN`: Percentage who are first generation
- `PAR_ED_PCT_NOT_1STGEN`: Percentage who are not first generation

#### Income Score (Aided Students)
- `INC_PCT_LO`: Percentage whose family income is $0-$30,000
- `INC_PCT_M1`: Percentage whose family income is $30,001-$48,000
- `INC_PCT_M2`: Percentage whose family income is $48,001-$75,000
- `INC_PCT_H1`: Percentage whose family income is $75,001-$110,000
- `INC_PCT_H2`: Percentage whose family income is $110,001+

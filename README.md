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
- `world_rank_CWUR`: Ranking from Center for Worled University Ranking (RUR)
- `score_THE`: Score used to create THE ranking
- `score_RUR`: Score used to create RUR ranking
- `score_CWUR`: Score used to create CWUR ranking

### Feature Columns for Diversity Index
- `international_students_THE`: 
- `UGDS_score`
- `female_male_score`

### Diversity Columns
- `diversity_index`
- `diversity_rank`
- `diversity_year_rank`

### UGDS Score Feature Engineering Columns
- `UGDS_WHITE`
- `UGDS_BLACK`
- `UGDS_HISP`
- `UGDS_ASIAN`
- `UGDS_AIAN`
- `UGDS_NHPI`
- `UGDS_2MOR`
- `UGDS_NRA`
- `UGDS_UNKN`

### Female Male Score Feature Engineering Columns
- `male_proportion`
- `female_proportion`

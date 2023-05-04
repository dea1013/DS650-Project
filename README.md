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
- 

### Feature Columns for Diversity Index
- 

### Diversity Columns
-

### UGDS Score Feature Engineering Columns
- 

### Female Male Score Feature Engineering Columns
- 

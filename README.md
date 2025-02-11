# NBA Player Statistics Analysis

A comprehensive data science project analyzing NBA player statistics spanning over three decades. This analysis explores player performance dynamics, geographical trends, and key success factors in professional basketball.

## Project Overview

This project combines two primary datasets:
- Player personal and draft information (positions, draft year, draft team)
- Year-by-year player statistics (salary, season, team)

## Key Findings

### Geographical Impact
- Larger cities are significantly more likely to produce NBA talent
- Cities like Los Angeles, Chicago, and Philadelphia produce disproportionately more NBA players
- Population size shows strong correlation with NBA talent production

### Physical Attributes Impact
- Height and weight influence NBA success, but less than traditionally assumed
- Career duration shows moderate correlation with player build
- Salary distribution varies across different height/weight ranges

### Performance Indicators
- Moderate correlation between win shares and salary
- Player Efficiency Rating (PER) shows positive correlation with compensation
- Draft position has notable impact on career earnings
- Position flexibility (especially positions 2-4) correlates with career success

### Position Analysis
- Centers show highest contribution to team success (measured by win shares)
- Players with multi-position capabilities (especially positions 2-4) demonstrated highest career success rates
- Salary distribution varies significantly across positions

## Technologies Used

- R Programming
- Key Packages:
  - ggplot2
  - tidyverse
  - dplyr
  - scales

## Data Processing

```R
# Example of data cleaning process
nba_stats <- nba_stats %>%
  mutate(
    height = as.numeric(sub("([0-9]+)-([0-9]+)", "\\1", height)) * 12 +
      as.numeric(sub("([0-9]+)-([0-9]+)", "\\2", height)),
    # Additional cleaning steps...
  )
```

## Getting Started

1. Clone the repository
2. Install required R packages:
```R
install.packages(c("tidyverse", "ggplot2", "dplyr", "scales"))
```
3. Open the R project file
4. Run the analysis scripts in the provided RMD file

## Project Structure

```
├── .gitignore              # Git ignore file
├── DS202-Final-Project.Rproj  # R project file
├── README.md              # Project documentation
└── analysis.Rmd          # Main analysis file
```

## Analysis Components

- Data cleaning and preprocessing
- Geographical analysis of player origins
- Physical attribute correlation studies
- Performance metric analysis
- Position-based success evaluation

## Authors

- Blake Nelson
- Nick Olech

## License

MIT License

---
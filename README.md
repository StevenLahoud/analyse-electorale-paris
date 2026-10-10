# Paris Elections 2007–2024 — A Multivariate Analysis

Statistical analysis of election results in Paris at the **polling-station level**, across 11 elections (presidential, European, legislative and municipal) from 2007 to 2024.

**Goal:** identify the structure of the Parisian political landscape and how it changed over time — in particular the east/west divide and the shift in electoral competitiveness between 2017 and 2024.

## Methods

| Method | Used for |
|---|---|
| **PCA** (Principal Component Analysis) | Main axes of opposition between candidates for each presidential and European election |
| **CCA** (Canonical Correlation Analysis) | Stability of political blocs between the 2008 and 2020 municipal elections |
| **K-means clustering** | Grouping polling stations by competitiveness (gap between the top two candidates) and blank/null vote rate |
| **Linear regression** | Explaining the 2024 legislative results from previous elections (2017–2024) |
| **Choropleth maps** | Mapping each result onto Paris polling-station boundaries |

## Key findings

- The **first principal axis** captures a clear west-right / east-left divide (16th–17th vs 19th–20th arrondissements).
- In 2022, the traditional right and the far right appear almost superimposed in Paris, with Macron shifting toward the right compared with 2017.
- **Clustering:** in 2017, central Paris was dominated by landslide wins; by 2024 the same area became the most competitive part of the city.
- **Regression:** the 2024 European election is the best predictor for most 2024 legislative winners (highest adjusted R²).

## Tech stack

**R** · tidyverse · FactoMineR · factoextra · CCA · sf · broom · gt · patchwork · **Quarto**

## Data

Official open data from the City of Paris: [opendata.paris.fr](https://opendata.paris.fr) (election results by polling station, polling-station boundaries).

## How to run

Install the required R packages:

```r
install.packages(c("tidyverse", "FactoMineR", "factoextra", "CCA", "sf",
                   "broom", "gt", "patchwork", "generics"))
```

Then render the report:

```bash
quarto render report.qmd
```

## Authors

Group project — Master in Mathematics & Computer Science for Data Science, Université Paris Cité.

Steven Lahoud, Fernandes Anthony

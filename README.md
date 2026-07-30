# Rscript_comparative_foraging
Rscript to accompany PhD research paper on harbour porpoise foraging behaviour 

code was made in R studio and R version 4.3.1. 

# Workflow

This script (`Rscript`) covers the foraging detection, comparison, and analysis pipeline (sections 5–9 below). It assumes a cleaned input dataset which can be found at Calonge, A.; Aoufi, S.; Conings, B.; Deneudt, K.; Debusschere, E.; Flanders Marine Institute (VLIZ); (2026): LifeWatch observatory data: Inter-click intervals of harbour porpoises recorded from two F-POD stations of the Belgian cetacean passive acoustic network in 2023. Marine Data Archive. https://doi.org/10.14284/786 

## Data and preprocessing

sections 1-4 contain cleaning of the dataset to obtain the final ICI file by combining all different deployments in 2023 for both locations into one datafile. 

## Analysis workflow

| Section | Description | Input | Output |
|---|---|---|---|
| **5. Foraging** | Calculation of foraging events, compared across four detection methods | raw ICI data | foraging event datasets per method |
| 5.1 Foraging according to Pirotta | Foraging events calculated using the Pirotta method | | |
| 5.1.1 General patterns in Pirotta | Summary/exploration of patterns from the Pirotta method output | | |
| 5.2 Foraging according to Nuuttila | Foraging events calculated using the Nuuttila method | | |
| 5.2.1 General patterns in Nuuttila | Summary/exploration of patterns from the Nuuttila method output | | |
| 5.3 Foraging according to DeRuiter | Foraging events calculated using the DeRuiter method | | |
| 5.3.1 General patterns in DeRuiter | Summary/exploration of patterns from the DeRuiter method output | | |
| 5.4 Foraging according to Schaffeld | Foraging events calculated using the Schaffeld method | | |
| 5.4.1 General patterns in Schaffeld | Summary/exploration of patterns from the Schaffeld method output | | |
| 5.5 Foraging SBFI | Foraging events calculated using the SBFI method | | |
| 5.5.1 General patterns in SBFI | Summary/exploration of patterns from the SBFI method output | | |
| **6. Combined data foraging** | Combining foraging results across all methods | foraging event datasets (5.1–5.5) | combined dataset |
| 6.1 Graphs and patterns | Visualisation of combined foraging patterns | combined dataset | plots |
| 6.2 Transformation to wide format | Reshaping combined data to wide format | combined dataset | wide-format dataset |
| 6.2.1 Division faulbaums belwind | Splitting wide-format data by site (Faulbaums / Belwind) | wide-format dataset | site-specific datasets |
| **7. Correlation Analysis** | Correlation analysis between foraging methods | site-specific datasets | correlation results |
| 7.1 Total | Correlation analysis, combined sites | | correlation results (combined) |
| 7.2 Belwind | Correlation analysis, Belwind site only | | correlation results (Belwind) |
| 7.3 Faulbaums | Correlation analysis, Faulbaums site only | | correlation results (Faulbaums) |
| **8. Distance and trend / slope analysis** | Trend/slope analysis of foraging vs. distance | site-specific datasets | trend/slope results |
| 8.1 Total | Combined sites | | results (combined) |
| 8.2 Belwind | Belwind site only | | results (Belwind) |
| 8.3 Faulbaums | Faulbaums site only | | results (Faulbaums) |
| **9. Combined plots for paper** | Generates final figures used in the manuscript | results from sections 5–8 | manuscript figures |

## Notes
- Section numbers/subtitles above correspond directly to the section headers (`#`) in `Rscript`, so you can jump to the relevant code using Ctrl+F / Cmd+F with the section title. Numbering starts at 5 because earlier steps (1–4) were part of separate preprocessing not included in this script — see "Data and preprocessing" above.
- Each foraging detection method (Pirotta, Nuuttila, DeRuiter, Schaffeld, SBFI) should be referenced to its original publication in the Data/Methods section below.

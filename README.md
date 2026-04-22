# Drug Offences in London: Spatial Data Analysis

This repository contains the coursework project for **7CUSMSDA Spatial Data Analysis**. It brings together the analysis notebook, processed spatial dataset, and the key figures used in the final write-up.

## What is included

- `notebooks/drug_offences_london.ipynb`: main analysis notebook
- `data/processed/london_drug_gdf.gpkg`: processed GeoPackage used for the analysis workflow
- `figures/`: exported maps and model output figures
- `data/raw/LSOA_london_2021/`: LSOA boundary copied into this project so the notebook is self-contained
- small raw inputs used directly by the notebook, such as IMD, Nomis tables, and gang shapefiles

## What is intentionally not uploaded by default

To keep the GitHub repository readable and lightweight, some large or non-essential raw files are excluded by `.gitignore`:

- monthly crime CSV files under `data/raw/crime/`
- unused local boundary shapefiles under `data/raw/LB_shp/`
- archived ZIP files and duplicate IMD folders

If full raw-data reproducibility is required, these files can be added later or linked from an external storage location.

## Recommended repository structure

```text
CourseWork/
├── README.md
├── .gitignore
├── notebooks/
│   └── drug_offences_london.ipynb
├── data/
│   ├── processed/
│   │   └── london_drug_gdf.gpkg
│   └── raw/
│       ├── 1590321589052220.csv
│       ├── IMD/
│       ├── London_Gangs/
│       ├── LSOA_london_2021/
│       ├── nomis_2026_04_22_011527.xlsx
│       └── nomis_2026_04_22_014758.xlsx
└── figures/
```

## How to use this repository

### Quick review

If the goal is to inspect the analysis, open the notebook and start from the section that reloads:

- `data/processed/london_drug_gdf.gpkg`

This is the best option for a marker or reader because it avoids downloading very large raw datasets.

### Full preprocessing

The notebook also contains a one-time preprocessing section that builds the GeoPackage from raw inputs. Some very large raw crime files are not committed by default, so that section may require local data that is not present in the GitHub version.

## Useful links for the report

The written report can link to:

- the repository homepage
- the notebook file
- the processed dataset, if you want to reference the reproducible analysis input

## Data notes

Main sources used in this project include:

- Metropolitan Police street crime data
- IMD spatial data
- Nomis Census tables
- London gang territory shapefiles
- LSOA 2021 boundary data

## Suggested report wording

You can cite the repository in the report with a short sentence such as:

> The full notebook, processed data, and exported figures are available in the accompanying GitHub repository.

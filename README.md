
# COCONUT Natural Products Property Analysis

A cheminformatics project using Python and RDKit to analyze a 2,000-compound subset of the COCONUT natural products database and profile molecular properties relevant to early-stage drug discovery.

## Project Relevance

Natural products remain an important source of biologically active scaffolds and lead compounds in drug discovery. This project was designed to explore how computational chemistry methods can be used to characterize natural product chemical space through descriptors linked to medicinal chemistry decision-making, including molecular size, polarity, lipophilicity, hydrogen-bonding capacity, and molecular flexibility.

## Objective

The objective of this project was to build a reproducible workflow for:

- loading and organizing natural product data,
- parsing molecular structures from SMILES strings,
- calculating medicinal chemistry-relevant descriptors with RDKit,
- generating clean datasets for downstream analysis,
- and visualizing trends across a natural product subset.

## Dataset

- **Source:** COCONUT (Collection of Open Natural Products)
- **Input file:** `coconut_csv_lite-05-2026.csv`
- **Working subset:** 2,000 randomly sampled compounds
- **Structure field used:** `canonical_smiles`

## Methods

The analysis was performed in Python using pandas, RDKit, matplotlib, and seaborn.

### Workflow

1. Loaded the COCONUT lite CSV into a pandas DataFrame.
2. Randomly sampled 2,000 compounds from the full dataset.
3. Parsed the `canonical_smiles` column into RDKit molecule objects.
4. Calculated the following descriptors for each valid molecule:
   - Molecular weight
   - LogP
   - Topological polar surface area (TPSA)
   - Hydrogen-bond donors
   - Hydrogen-bond acceptors
   - Rotatable bonds
5. Combined RDKit descriptors with selected COCONUT property fields.
6. Saved cleaned output tables and figure files for reuse and downstream interpretation.

## Key Results

- Successfully parsed **2,000 / 2,000** sampled SMILES strings.
- Built a descriptor-ready dataset for property-based profiling of natural products.
- Generated visualizations showing molecular weight and LogP distributions across the subset.
- Explored descriptor relationships using a correlation heatmap and MW vs LogP scatterplot.

## Drug Discovery Context

This workflow demonstrates a foundational step in compound prioritization: translating chemical structure into interpretable physicochemical descriptors. Descriptor-based profiling can help identify compounds with properties that may influence permeability, solubility, flexibility, and overall drug-likeness during early-stage screening.

## Repository Structure

```text
natural-products-db/
├── coconut_natural_products_analysis.ipynb
├── README.md
└── data/
    ├── processed/
    │   ├── coconut_subset_cleaned.csv
    │   └── descriptor_table.csv
    └── results/
        ├── molwt_hist.png
        ├── logp_hist.png
        ├── mw_vs_logp.png
        └── descriptor_heatmap.png
```

## Visualizations

### Molecular Weight Distribution
![Molecular weight distribution](data/results/molwt_hist.png)

### LogP Distribution
![LogP distribution](data/results/logp_hist.png)

### MW vs LogP Scatterplot
![MW vs LogP scatterplot](data/results/mw_vs_logp.png)

### Descriptor Correlation Heatmap
![Descriptor correlation heatmap](data/results/descriptor_heatmap.png)

## Technical Skills Demonstrated

- Cheminformatics data processing
- SMILES parsing and molecule validation
- Molecular descriptor calculation with RDKit
- Scientific plotting and exploratory data analysis
- Reproducible project organization
- Interpretation of physicochemical properties in a medicinal chemistry context

## Tools Used

- Python
- pandas
- RDKit
- matplotlib
- seaborn
- Jupyter Notebook

## Future Directions

Potential extensions of this project include:

- applying simple drug-likeness or lead-likeness filters,
- comparing descriptor profiles across natural product classes,
- analyzing scaffold diversity,
- and integrating similarity search or clustering methods.

## Portfolio Summary

This project demonstrates an interest in natural product-based drug discovery and the use of computational chemistry tools to evaluate molecular properties relevant to medicinal chemistry.

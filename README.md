

\# COCONUT Natural Products Property Analysis



This project builds a small local database of natural products from the COCONUT collection and profiles their molecular properties using RDKit descriptors. \[web:36]\[web:38]\[web:40]



\## Data



\- Source: COCONUT lite CSV (May 2026 release). \[web:34]\[web:36]  

\- Sample: 2,000 randomly selected compounds from the full COCONUT dataset. \[cite:23]  

\- Structure field used: `canonical\_smiles`.



\## Methods



\- Loaded the COCONUT lite CSV and sampled 2,000 rows into a working subset. \[cite:23]\[web:36]  

\- Parsed the `canonical\_smiles` column into RDKit molecule objects; all 2,000 SMILES parsed successfully. \[cite:23]\[web:40]  

\- Computed RDKit descriptors for each molecule:

&#x20; - Molecular weight (MolWt\_rdkit)

&#x20; - LogP (LogP\_rdkit)

&#x20; - Topological polar surface area (TPSA\_rdkit)

&#x20; - Hydrogen-bond donors (HDonors\_rdkit)

&#x20; - Hydrogen-bond acceptors (HAcceptors\_rdkit)

&#x20; - Rotatable bonds (RotBonds\_rdkit) \[web:40]  

\- Combined RDKit descriptors with COCONUT’s existing property fields (e.g., `molecular\_weight`, `alogp`, `topological\_polar\_surface\_area`) into a cleaned descriptor table. \[web:36]\[web:38]\[web:40]  

\- Generated:

&#x20; - Histograms of molecular weight and LogP

&#x20; - An MW vs LogP scatterplot

&#x20; - A descriptor correlation heatmap \[web:40]



Key files:



\- `data/processed/coconut\_subset\_cleaned.csv` – full 2,000-compound subset with RDKit descriptors. \[cite:23]  

\- `data/processed/descriptor\_table.csv` – compact descriptor table for analysis. \[web:36]\[web:38]\[web:40]  

\- `data/results/molwt\_hist.png`, `logp\_hist.png`, `mw\_vs\_logp.png`, `descriptor\_heatmap.png` – saved figures. \[cite:23]\[web:40]



\## Results



\- \*\*Parsing:\*\* 2,000/2,000 sampled SMILES converted to RDKit molecules with no failures. \[cite:23]\[web:40]  

\- \*\*Property distributions:\*\* The subset spans a broad range of molecular weights and LogP values, with many molecules extending beyond classical “rule-of-five” space, consistent with known natural-product physicochemical properties. \[web:36]\[web:39]  

\- \*\*Descriptor relationships:\*\* Correlations show expected trends, such as higher molecular weight associating with more hydrogen-bond acceptors/donors and rotatable bonds, and an inverse relationship between TPSA and LogP for more polar scaffolds. \[web:40]



\## Tools



\- Python (pandas, matplotlib, seaborn)  

\- RDKit (installed via `conda-forge`) for SMILES parsing and descriptor calculation \[web:40]


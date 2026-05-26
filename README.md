
<p align="center">
  <img src="https://img.shields.io/badge/Python-Data%20Analysis-blue?style=for-the-badge&logo=python" alt="Python badge">
  <img src="https://img.shields.io/badge/RDKit-Cheminformatics-green?style=for-the-badge" alt="RDKit badge">
  <img src="https://img.shields.io/badge/Data%20Source-COCONUT-orange?style=for-the-badge" alt="COCONUT badge">
</p>

# Natural Products Database Analysis

A cheminformatics and data-analysis project using a curated subset of natural products from the COCONUT database. This workflow uses RDKit to parse molecular structures, compute medicinal-chemistry–relevant descriptors, and visualize chemical property distributions across a 2,000-compound natural-products dataset. 

---

## Problem

Natural products occupy a large, structurally diverse region of chemical space, but the raw structural data in large databases can be difficult to interpret without systematic profiling. 
For early-stage drug discovery, teams need to know whether a natural-products collection is enriched in compounds that are too large, too polar, too lipophilic, or too flexible before committing resources to screening or optimization.   

Without a reproducible way to compute and summarize key physicochemical descriptors (molecular weight, lipophilicity, polarity, hydrogen-bonding capacity, flexibility), it is hard to:
- assess how “drug-like” a library is  
- compare natural-product space to typical small-molecule libraries  
- prioritize subsets for follow-up design or screening campaigns 

---

## Why This Project Is Important

By turning a raw list of natural-product structures into quantitative descriptor distributions and visual summaries, this project helps answer a central question: *what kind of chemical space does this natural-products collection actually cover?  
This type of profiling supports better decisions about library design, lead selection, and whether additional filtering or augmentation is needed to align with drug-discovery guidelines (for example, balancing molecular weight, LogP, and polar surface area).   

The resulting workflow is useful as:
- an exploratory analysis for natural-product libraries  
- a starting point for building lead-like or fragment-like subsets  
- a template for integrating descriptor profiling into larger computational pipelines 

---

## Executive Summary

This project was designed to profile the physicochemical space of natural products using a reproducible Python workflow. A subset of 2,000 compounds was sampled from the COCONUT collection, successfully parsed with RDKit, and analyzed using descriptors relevant to molecular property profiling and early-stage drug discovery. 

The project demonstrates practical skills in molecular data handling, cheminformatics, descriptor generation, and scientific visualization. It also provides a foundation for downstream workflows such as compound prioritization, clustering, similarity analysis, or lead-like subset selection. 

---

## Key Outcomes

- Built a reproducible RDKit workflow for natural-product descriptor analysis.  
- Parsed and analyzed 2,000 natural-product structures with no failed molecules.  
- Computed molecular weight, LogP, TPSA, hydrogen-bond donor/acceptor counts, and rotatable bond counts.  
- Generated publication-style visual summaries of descriptor distributions and relationships.  
- Organized outputs into a clean GitHub-ready project structure.

---

## Scientific Context

Natural products are a rich source of structurally diverse bioactive molecules and remain highly relevant to drug discovery and chemical-biology research.   
Compared with many synthetic libraries, natural products often occupy different regions of chemical space (for example, higher complexity, different heteroatom patterns), which can translate into novel biological activities but also distinct ADME and developability profiles. 

Understanding how a natural-products set is distributed across key physicochemical properties—such as molecular weight, lipophilicity (LogP), polarity (TPSA), and hydrogen-bonding capacity—helps researchers judge whether the collection is suitable for particular screening strategies and where additional design or filtering might be needed. 

This project focuses on property profiling rather than bioactivity prediction. By characterizing the descriptor space of a natural-products subset, the workflow supports later decisions about filtering, prioritization, and medicinal-chemistry relevance. 

---

## Data Source

The dataset used in this project was derived from the **COCONUT** database (Collection of Open Natural Products), an open resource for natural-product structures that aggregates and curates data from multiple sources.   
A 2,000-compound subset was sampled and used for descriptor analysis and visualization.

---

## Descriptors Calculated

The workflow computed the following RDKit-derived properties:

- Molecular weight  
- LogP  
- Topological polar surface area (TPSA)  
- Hydrogen bond donors  
- Hydrogen bond acceptors  
- Rotatable bonds  

These descriptors were selected because they are commonly used to characterize physicochemical behavior, permeability, solubility, and molecular flexibility, all of which strongly influence drug-likeness and developability. 

---

## Results

### Project Summary

| Metric                         | Value |
|-------------------------------|------:|
| Natural products analyzed     |  2000 |
| Valid molecules parsed by RDKit | 2000 |
| Descriptor categories computed |     6 |
| Output figures generated      |     4 |

The complete parsing success across all 2,000 sampled compounds supports the reliability of the workflow and produced a clean dataset for downstream visualization and analysis.

---

## Repository Structure

```text
natural-products-db/
├── README.md
├── coconut_natural_products_analysis.ipynb
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

---

## Visual Outputs

### Molecular weight distribution

![Molecular weight histogram](data/results/molwt_hist.png)

### LogP distribution

![LogP histogram](data/results/logp_hist.png)

### Molecular weight vs LogP

![MW vs LogP scatter plot](data/results/mw_vs_logp.png)

### Descriptor correlation heatmap

![Descriptor heatmap](data/results/descriptor_heatmap.png)

---

## Technical Skills Demonstrated

- Python data analysis with pandas  
- Molecular structure parsing with RDKit  
- Descriptor-based property profiling  
- Scientific visualization with matplotlib and seaborn  
- Reproducible workflow organization for computational chemistry projects

---

## Limitations

This project focuses on descriptor profiling and does not include biological activity data, experimental validation, or predictive modeling.  
While descriptor analysis is useful for understanding chemical space, it should be interpreted as a first-step profiling approach rather than a direct measure of pharmacological potential. 

---

## Future Extensions

Potential next steps include:

- Identifying lead-like or drug-like subsets using common medicinal-chemistry filters  
- Clustering compounds by descriptor similarity  
- Integrating structural fingerprints for scaffold or similarity analysis  
- Adding similarity search functionality  
- Combining descriptor profiling with downstream ADME or virtual screening workflows 

---

## Author

**Ava Richards**  
Biomedical Science graduate interested in medicinal chemistry, natural-product drug discovery, and computational analysis.

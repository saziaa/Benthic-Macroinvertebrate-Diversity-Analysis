## **Benthic-Macroinvertebrate-Diversity Analysis**

📌  **Project Overview**

This project investigates benthic macroinvertebrate communities across U.S. ecoregions using EPA biological monitoring data. Macroinvertebrates are widely used bioindicators because they integrate ecological conditions over time and respond to multiple stressors, such as nutrient enrichment, sedimentation, and habitat alteration.

By combining traditional biodiversity metrics, trait-based approaches, and multivariate statistics, this analysis provides insights into biodiversity patterns, water quality gradients, functional ecosystem processes, and indicator species at regional scales.

🎯 **Objectives**

1. Quantify biodiversity and compare diversity across ecoregions and states.

2. Assess pollution sensitivity using community-weighted tolerance values (CWM-PTV) and EPT (Ephemeroptera, Plecoptera, Trichoptera) indicators.

3. Explore functional feeding groups (FFGs) and habitat traits (HABIT) to infer ecosystem processes.

4. Identify indicator taxa and test whether community composition differs significantly among ecoregions.

📊 **Data**

- Source: [EPA National Rivers and Streams Assessment (NRSA)](https://www.epa.gov/national-aquatic-resource-surveys/nrsa).

- Columns include:

    * Metadata: SITE_ID, STATE, AG_ECO9, SAMPLE_TYPE, DATE_COL

    * Taxonomy: PHYLUM, CLASS, ORDER, FAMILY, GENUS

    * Abundance: TOTAL, TOTAL300

    * Traits: FFG (Functional Feeding Group), HABIT, PTV (Pollution Tolerance Value)

⚙️ **Methodology**

- Alpha diversity: Richness, EPT richness, EPT proportion.

- Pollution tolerance: Community-Weighted Mean PTV (CWM-PTV).

- Functional traits: Site-level proportions of FFGs and HABITs.

- Community analysis:

   * Hellinger transformation

   * NMDS ordination

   * PERMANOVA for group differences

- Indicator species: IndVal analysis with permutation tests.

🔑 **Key Findings**





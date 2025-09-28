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
### Biodiversity & Regional Variation

- **Shannon Diversity**: Highest in Northern Appalachians, (NAP ~3.1), lowest in Southern Plains, (SPL ~2.5).
- 
- **Richness by State**:  
  - High: Virginia, Vermont, Pennsylvania (~62–65 taxa) → diverse and complex communities.  
  - Low: Mississippi, South Dakota, Texas (~25 taxa) → less diverse, possibly reflecting environmental stressors or habitat simplification.
    
- **EPT Proportion**: Highest in Western Mountains,(WMT ~0.42), lowest in Coastal Plains, (CPL ~0.18)
 
- **Interpretation**: WMT and NAP support more structurally complex, less disturbed communities, while CPL and SPL indicate degraded or stressed conditions.

### Pollution Sensitivity & Water Quality

- **ANOVA Results**: Significant differences in pollution tolerance across ecoregions (F = 55.67, p < 2e-16).
- **EPT Proportion**:
      - High: WMT, Western Mountains (~0.42) → better water quality.
      - Low: CPL, Coastal Plains (~0.18) → degraded water quality.
- **Community-Weighted Pollution Tolerance (CWM-PTV)**:
      - High: TPL, Temperate Plains & CPL, Coastal Plains → dominance of tolerant taxa.
      - Low: WMT, Western Mountains & SAP, Southeastern Plains → dominance of sensitive taxa.
- **Interpretation**: WMT shows healthier, less polluted conditions; TPL and CPL indicate degraded systems; SAP reflects mixed ecological conditions.



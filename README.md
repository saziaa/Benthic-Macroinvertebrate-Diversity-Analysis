## **Benthic Macroinvertebrate Diversity Analysis**

📌  **Project Overview**

This project investigates benthic macroinvertebrate communities across U.S. ecoregions using EPA biological monitoring data. Macroinvertebrates are widely used bioindicators because they integrate ecological conditions over time and respond to multiple stressors, such as nutrient enrichment, sedimentation, and habitat alteration.

By combining traditional biodiversity metrics, trait-based approaches, and multivariate statistics, this analysis provides insights into biodiversity patterns, water quality gradients, functional ecosystem processes, and indicator species at regional scales.

🎯 **Objectives**

1. Quantify biodiversity and compare diversity across ecoregions and states.

2. Assess pollution sensitivity using community-weighted tolerance values (CWM-PTV) and EPT (Ephemeroptera, Plecoptera, Trichoptera) indicators.

3. Explore functional feeding groups (FFGs) and habitat traits (HABIT) to infer ecosystem processes.

4. Identify indicator taxa and test whether community composition differs significantly among ecoregions.

🛢️ **Data**

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
This analysis evaluates how richness and diversity vary among states and ecoregions to establish baseline patterns of community structure. It helps identify regions with complex, healthy assemblages versus those with simplified, stressed communities.

- **Shannon Diversity**: Highest in Northern Appalachians, (NAP ~3.1), lowest in Southern Plains, (SPL ~2.5).

- **Richness by State**:
   - High: Virginia, Vermont, Pennsylvania (~62–65 taxa) → diverse and complex communities.  
  - Low: Mississippi, South Dakota, Texas (~25 taxa) → less diverse, possibly reflecting environmental stressors or habitat simplification.
    
- **EPT Proportion**: Highest in Western Mountains,(WMT ~0.42), lowest in Coastal Plains, (CPL ~0.18)
 
- **Interpretation**: WMT and NAP support more structurally complex, less disturbed communities, while CPL and SPL indicate degraded or stressed conditions.

### Pollution Sensitivity & Water Quality
This analysis assesses the balance between pollution-sensitive and tolerant taxa across ecoregions. It provides direct insight into ecological condition and water quality, highlighting areas under greater anthropogenic pressure.

- **ANOVA Results**: Significant differences in pollution tolerance across ecoregions (F = 55.67, p < 2e-16).

- **Community-Weighted Pollution Tolerance (CWM-PTV)**:

   - High: **Temperate Plains (TPL) & Coastal Plains (CPL)** → dominance of tolerant taxa.

   - Low: **Western Mountains (WMT) & Southeastern Plains (SAP)** → dominance of sensitive taxa.

- **EPT Cross-Validation**: Regions with higher EPT richness (e.g., **WMT**) also show lower PTV, reinforcing their better ecological condition.

- **Interpretation**: **WMT** shows healthier, less polluted conditions; **TPL and CPL** indicate degraded systems; **SAP** reflects mixed ecological conditions.

### Functional Traits & Ecosystem Health

- **Functional Feeding Groups (FFG):**

  * Collectors (CG + CF): Dominate across all regions (>60%), showing widespread reliance on fine and suspended organic matter.
  * Scrapers (SC) & Shredders (SH): More prominent in **WMT** and **NAP** (mountainous/forested regions), indicating dependence on algae and coarse organic inputs from intact riparian zones.
  * Predators (PR): Consistently low (~5–10%), lowest in **XER** (arid regions).
  * Regional Note: **XER** shows particularly high collectors, reflecting simplified food webs driven by fine detritus.

* **Habitat Traits (HABIT):**

  * Clingers (CN): Highest in **WMT** and **NAP** (~35–40%), linked to fast-flowing, oxygen-rich habitats.
  * Burrowers (BU): Dominate in **CPL** and **SPL** (~25–30%), consistent with sedimented, low-flow environments.
  * Sprawlers (SP) & Swimmers (CB): Moderate presence across regions; Sprawlers higher in plains.
  * Divers (DV): Nearly absent everywhere.

* **Interpretation:**

  * Mountain ecoregions (WMT, NAP) host more sensitive, habitat-specialist traits → cleaner, structurally complex systems.
  * Plains/coastal ecoregions (CPL, SPL) are dominated by tolerant, generalist traits (burrowers, collectors) → more degraded, sediment-rich systems.
  * Overall, trait distributions capture ecosystem processes (e.g., detritus processing, algae grazing) and reinforce regional water-quality patterns.


### Community Composition & Indicator Taxa

The analysis of macroinvertebrate community composition across U.S. ecoregions is to identify distinct assemblages and indicator taxa that reflect regional environmental conditions and water quality.

- **Community Composition**:

   - NMDS ordination shows clear separation of sites by ecoregion, with some overlap due to shared taxa.

   - PERMANOVA confirms significant differences among ecoregions (p < 0.001), explaining ~10–20% of community variation.

- **Indicator Taxa**:

   - Western Mountains (WMT): Sensitive taxa (mayflies, stoneflies, caddisflies, clingers) → high-quality streams.

   - Coastal Plains (CPL) & Southern Plains (SPL): Tolerant taxa (midges, worms, burrowers) → nutrient-rich, sedimented habitats.

   - Other regions: Intermediate assemblages with mixed indicator taxa.

- **Interpretation**:
   - Communities differ significantly across ecoregions.
   - Sensitive taxa in WMT reflect clean, fast-flowing habitats.
   - Tolerant taxa in CPL/SPL indicate degraded or enriched conditions.
   - Indicator species provide useful bioindicators of water quality and ecosystem health.

⚙️ **Tools & Libraries**

- Language: R

- Key Packages:

   - vegan (diversity, ordination, PERMANOVA)

   - indicspecies (Indicator Species Analysis)

   - ggplot2 (visualization)

   - dplyr, tidyr (data wrangling)

# NextGen Omics Day 1



## Keynote - Computational Pathology - The Next Revolution in Cancer Diagnostics

**Mark Gustavson, AstraZeneca**

Computational pathology - next transformative technology to enable better patient selection and clinical outcomes
- First digital scanner authorized by FDA in 2017, so recent

Traditional IHC path scoring is semi-quantitative, subjective, and limited to the resolution of low-level staining
- Traditionally done by eye
- Heterogeneity is measured by a single cutoff (estimate of cells positive for X marker)
- Scores are categorical (i.e., 1-4)

Computational path scoring allows for quantitative, continuous scoring, more reliable
- Resolution is lower, can quantify spatial heterogeneity better
- Gustavson: "You get the same result every time - not subjective" - not sure this is true given ML

Brief mention of antibody-conjugated drugs (ADCs)
- 11 approved as of now, targeting various solid and hematological malignancies
- Need IHC/spatial to better understand targeting/effectiveness of ADCs

T-DXd is an AZ ADC
- Humanized anti-HER2 IgG1 mAb linked to topo 1 inhibitor and cleavable linker

T-DXd has robust effecacy against HER-2 low late model of BC
- Demonstrated in RCT that T-DXd improved response in patients compared to standard of care

Use validated IHC assay to categorize patients into IHC 1+, 2+, or 3+ which describes staining of HER2 on tumor cells in path sample
- HER2 low cancer means 1+ or 2+ designated patients
- Significant heterogeneity in IHC slides between patients within groupings

Developed "Quantitative Continuous Score" - QCS for ML-driven pathology scoring
- IHC slides are digitized and used as training data with manual path annotations
- Used neural net (almost certainlty a CNN) to train model - unclear what response/output here is
- Gustavson: "Won't go into detail on how we validated it" - no ROC or anything
- Transform staining intensity into "optical density"
- Two method developments as part of this technology:
  - ART -  automatically segment tumor from IHC image
  - SSTC - subcellular segmentation of tumor cell (identifying cellular membrane)

QCS scores as compared to path scoring into IHC +1, +2, +3 categories reveals that there is significant variation between groups (as based on optical density scores for single cells)
- Particularly, IHC +3 group has very broad QCS optical density scores

Retrospectively analyzed data from T-DXd trial and categorized HER2-low patients using QCS scoring
- Created QCS+ and QCS- groups and identified better/worse responding patients

Can analyze spatial heterogeneity in different ways - spatial proximity score
- % of HER2+ tumor cells in a local neighborhood
- Once again, retrospective analysis provides better cohort segmentation

Final note - can try to link computational pathology to mass spec for better target priortization and identifying protein signatures (potential biomarkers)


## Talk 1 - Quality-Control Methods In NGS Diagnostic Test Development

**James Willey, Univeristy of Toledo**



## Talk 2 - Discovering Next-Generation Biomarkers Through Integrating Single-Cell ‘Omics And Artificial Intelligence

**Sarah Carl, Scailyte**

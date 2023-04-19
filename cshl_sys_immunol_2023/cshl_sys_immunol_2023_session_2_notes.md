# CSHL Systems Immunology 2023 - Session 2

**Human Systems Immunology I**
*Wednesday, 19 April*

## Systems immunology of human immune set points

**John Tsang, Yale**

The human immune response is very variable - i.e., responses to vaccination or cancer immunotherapy
- Age explains some, but not all variation

Why? Due to extensive genetic variation in population, intrinsic factors like age/sex (includes cumulative exposure to enviroment) as well as pre-existing immunity
- Based on twin studies, heritability of immune vaccine response is fairly high but drops with increased age

Group has tried to identify individual "set points" signatures that predict response beyond age, sex, and pre-existing immunity
- Consider homeostatic setpoints like the regulatory state that maintains homeostasis for an individual's immune system
- Conceptual system: sensor (detects outside of range), controller (coordinates response), effector (causes return to normal range)

Vaccination is a timed pertubation that can be used to probe individual immune set points
- Can identify inter-subject and within-subject variation pre/post vaccination

Used CITE-seq to profile blood signatures and measure cell frequency shifts/cell state differences
- Study of 10 low and 10 high responders to vaccine
- Found that high responders tended to have more activated pDCs (leading to more activated B cells), which are making interferon in healthy individuals which primes for a stronger vaccine response (in terms of B cells)

How are antigen-agnostic setpoints established?

Study of childhood development - cohorts included children 1-6, 2-7, 5-9, and 9-14
- Annual sampling of whole blood
- Individuals tracked for at least five years longitudinally

Produced average time trajectory from all measurements, and identified signatures of human peripheral immune development
- Interestingly, individual variation explained significantly more variation than sex or age
- Some genes show stable expression temporally _within_ an individual but can be at very different levels _between_ individuals
- Other genes show fairly steady expression over time regardless of individuality
  - Many of these genes are linked to NK cell development (?)

Showed data suggesting gene individuality is linked to heritability (from largescale gene expression heritability study)
- Also examined eQTLs and showed same broad pattern - more individually variable genes had more variance explained by eQTLs

Performed regression to identify genes that show increasing or decreasing individuality over time
- Created age windows, did jackknife resampling and ran least squares model

Genes that increase in variability over time (i.e., exposure-driven) are enriched for inflammatory and monocyte gene signatures

Went on to examine influence of acute immune/inflammatory exposures on immune setpoints
- i.e. can certain events cause a return to a "new" set point

Performed study on patients with either prior mild COVID or no covid, and examined response to seasonal influenza vaccination (D0)
- Assays: flow cytometry, whole blood RNA, some CITE-seq to profile immune response
- Found that flu-specific plasmablast levels were significantly higher in males - but not females - in patients who recovered from COVID as opposed to healthy controls
  - Data is not super strong
- Deeper examination revealed that covid-recovered males had higher levels of IFNg and more single cells with IFNg response signature (?)

Identified subset of CD8 Tem that express GPR56+ and were significantly higher in covid-recovered males than HCs
- Showed some data indicating GPR56+ T cells showed some overlap with "bystander" gene signature
- Resemble virtual memory CD8 T cells (?)
- covid-recovered males had slightly higher production of IL-15 from monocytes (?)
- Overall takeaway: setpoints are related to poised monocytes and virtual memory CD8+ T cells

Went back and attempted to quantify virtual memory CD8 T cells in pediatric cohort
- Used gene signature to define subset then tested how individually variable signature was -> found that it was very highly variable -> thus, set points can be affected by exposure.

Overall: very cool talk and study, not sure GPR56+ CD8+ T cells are much of anything as data was relatively week and no attempts to validate in other contexts shown.

Question: What could underly observed sex differences? Answer: Has been shown that males mount a more inflammatory reponse to COVID infection and that leads to more virtual memory CD8 T cells; unclear on why monocytes appeared more poised in recovered males vs females

Question: Is a setpoint cell frequency or cell states? It's both, with CD8 vm T cells, it's frequency differences observed, but also capability to respond to IL-15 stimulation. So it's both numbers (frequency) and capacity (state)

Question: Do standard blood metrics (total WBC) predict immune responses? No - most standard metrics dont show association and effects are small

## Testosterone-induced changes in transcriptional responses to stimulation during female-to-male sex-reassignment

**Rikard Forlin, Karolinska**




## A spatial thymus human cell atlas mapped to a continuous tissue axis

**Veronika Kedlian, Wellcome Sanger**

## Medicine as a continuum—Monitoring immune-age and disease progression

**Shai Shen-Orr, Technion-Israel Institute of Technology**

## Systematic discovery of autoimmune disease-causal regulatory variants and their effects on T cell function

**John Ray, Broad**

## Identification of CD4+ T cell antigens in Sjögren's disease using TScan-II

**Mohammad Dezfulian, HMS**

## Microglial-specific miR-155 deletion enhances interferon- dependent response to neurodegeneration and mitigates cognitive impairment in a mouse model of Alzheimer’s disease

**Kilian Kleemann, BWH**

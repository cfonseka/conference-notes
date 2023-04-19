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

Sex differences are significant in response to infectious disease
- Male sex had increased risk of death due to COVID
- Potential reason? Delayed type 1 IFN response is more frequent in males than females and leads to more severe disease
- Cytokine release syndrome is also more associated with males
- Conversely, females are overrepresented in most autoimmune disorders (SLE, RA)
  - SLE is thought to be related to type 1 IFN dysregulation

Studied longitudinally 20 female sex individuals who were undergoing F->M sex horomone treatment
- Able to study effects of T in vivo
- Took samples at baseline, then 3 months and 12 months post
- All individuals showed increase of T to male ranges and no changes in estradiol

Testosterone treatment led to increased signaling in TNFa via NFkB

Examined pDC population in particular - decreased frequency in response to T
- pDCs that remained upregulated CD81, and CD81+ pDCs have been shown to have reduced type 1 IFN reponses and are thought to modulate Tregs
- Measured response of pDCs in response to stimulation - showed reduction in IFNa responding genes after 3 mo T
  - Most patients showed bimodal IFNa response - moderated by expression of IRF7
 in pDCs
- Plasma levels of IFN didn't vary with testosterone treatment, but response did

 pDCs express more of the androgen receptor than other immune cells, and thus may act as sensors for blood antigens

Monocytes also showed changes in response to testosterone
- Upregulation in TNFa family proteins
- Performed similar stimulation experiment (challenged with LPS)
- Found that increased expression of hallmark TNFa pathway genes after treatment
- Peformed "NicheNet" analysis on data (single cell ? - unclear) and identified receptor-ligand pairs that suggested an autocrine loop in monocytes

Testosterone upregulates TNFa responses in monocytes and downregulates Type 1 IFN responses in pDCs
- Potentially aligned with observed sex differences in vaccine response/infection

## A spatial thymus human cell atlas mapped to a continuous tissue axis

**Veronika Kedlian, Wellcome Sanger**

T cells develop in the thymus - thymic architecture is critical for these processes
- Cortex, medulla, and cortico-medullary junction
- T cells enter through junction area, acquire TCRs in cortex, move to medulla where positive selection takes place
- Resident thymic cells play a significant role in this process, such as epithelial and dendritic cells

Performed spatial transcriptiomic analysis of thymus to build better single cell atlas (had previous work published in 2020, all single cell + TCRs)
- Collected fetal thymus (11-21 wks) and pediatric thymus (0-3 y)
- 1M cells, better T cell developmental resolution

Used 10x visium to visualize foetal or pediatric thymic slices, get 50 um spot resolution for whole trancsriptome (so not quite single cell)
- Combined data with 50-plex multicolor imaging with IBEX to get protein Data
- Developed automated image pipeline called ImageSpot to perform thymic-level segmentation (cortex/medula/etc)

Used spatial data to better define cortico-medullary axis using something called OrganAxis with distances of spots from medulla (?)
- This was not explained well and the slides said KNN on them, so would need to examine paper
- Appears that this was used to bin spatial data into layers

Combined Visium data with protein data, then binned all cells in a layer into psuedobulk measurements
- Showed that T cells in different stages of development (presumambly annotated by expression or protein) show abundance levels across binned tissue layers that are concordant with T cell development model (movement from junction to top of cortex to medulla)
  - Very unclear how much the definition of T cell development (and thus annotations) is driven by the model anyway
- Few differences between fetal and pediatric, other than potential evidence for entry of double negative T cells into cortex for fetal
- Also annotated various types of thymic epithelial cells, which they then mapped to different tissue layers from spatial info
  - mcTEC cells localize to capsular/subcapsular cortex in fetus but also appear in the junction area in pediatric samples

Overall: It's a Teichmann lab joint so the single cell atlas aspect is well done, but its not clear how relevant any of this would be to us and the talk was less than illuminating

## Medicine as a continuum — Monitoring immune-age and disease progression

**Shai Shen-Orr, Technion-Israel Institute of Technology**

Immune system responses vary by age!
- Nothing in medicine makes sense except in the lite of time - i.e., we often ignore/underestimate the effect of time on biology
- Incredibly important to understand immune system in a longitudinal manner

Immune system aging (immune-age) is the first PC of human immune variation
- Tracks with earler talk from John Tsang

Cohort is 135 young and older adults measured annually for 9 years
- Performed high-dimensional cytometry using flow then CyTOF
- Allows them to assay 72 cell types
- Can create matrix of cell type frequency by individual over time by stiching together samples
- Interestingly, they cluster without age information and build diffusion map based on celltype frequencies
  - Find that younger individuals cluster on one edge, but age-based variation decreased across other diffusion component
  - Cytokine response scores decrease with increase along pesudotime axis

What is the pesudotime axis? Made up of cell type frequency variation data
- Weirdly, they show that things align across this axis (because it is literally created from it)

Using this data, they create an "IMM-AGE" score that is a gene expression score derived from their psuedotime axis (how?) and applied to Framingham Heart cohort
- Found survival differences correlated by IMM-AGE score by kaplan-meier
  - Didn't show cutoff for high/low IMM-AGE score dichotomy
- strong claim: predicts all-cause mortality better than other epigenetic scores (??)

Hypothesis: Immune-aging is a conserved process that people undego at different rates
- Small Mark Davis study in Front. Immunol. shows that bangladeshi children (1-3 y) had IMM-AGE scores more comparable to US 30 year olds than US 1-3 y
  - Again, unclear how this score is being measured by CyTOF (cell frequencies presumambly)
- Examined 27 health care workers who were COVID-naive and measured their "IMM-AGE" score during response to Pfizer vaccine
  - Chronological age and IMM-AGE show moderate correlation (r = 0.49
  - There are significant differences in immune cell population frequencies in response to vaccine - they go onto stratify cell types by whether they change in frequency across the IMM-AGE axis
  - Claim: IMM-AGE better predicts immune response than chronological age

Have reduced 40 marker CyTOF panel to 8-color flow
- Signatures show high correlation between panels
- Based on 17 different cell types or 57 gene marker panel

Conclusion: we have a young immune system, reach an inflection point, switch to "old" immune system (??)
Also included information about TimeAx - a pesudotime-based approach of modeling disease (based on what input data?) by placing patients onto a modeled continuous trajectory

Overall: This is a very Mark Davis type talk - get a ton of measurements -> use a overly simple modeling approach -> make grand conclusions. The conceptual idea that a composite score based on immune cell type frequencies in an individual might better predict immune response than chronological age on its own is sound, but the data shown here are not particularly convincing and the IMM-AGE score itself is not well defined (is it based on 72 cell type frequencies? expression scores? how do the two correspond?)

## Systematic discovery of autoimmune disease-causal regulatory variants and their effects on T cell function

**John Ray, Broad**

Autoimmune disorders are highly heritable but the genetic mechanisms underpinning this remain unknown

GWAS studies can help pinpoint risk loci associated with disease status
- Fine mapping is required to differentiate the causal variant with other linked variants
- 90% of disease-associated variants are in non-coding regions, particularly immune cell enhancers

Can use DNA accessibility assays to identify putative regulatory elements in a cell-type specific manner, then looks for enrichment of disease-associated variants in open areas by cell type (LD score regression)
- ENCODE project has done this for many cell lines

Performed luciferase reporter assays to test putative casual varaints to determine effects on expression
- Did this for 20k variants linked to autoimmune disorders in Jurkats
- Identified pCRE (putative cis-regulatory elements) and emVAR (expression modulating variants)
- Performed risk ratio analysis + fine mapping to find that accessible chromatin variants
 are significantly more likely to be disease-linked (or literally, have higher hazard ratios)

Identified 60 variants in accessible chromatin (Jurkats) that modulate reporter activity
- Focus on rs72928038 which is 30 kb downstream of BACH2
- Used base editing to confirm that risk allele downregulates BACH2
- BACH2 maintains T naive state by repressing T cell activation, decreasing expression in effector state; phospho-BACH2 allows for AP-1 ehancer binding and T cell activation

Performed 18bp deletion around BACH2 allele in mice, did co-mingling experiment, and identified decrease in freq of memory CD8 t cells and more CD8 effector cells
- Also showed that there are less naive CD8 t cells
- Chimeras also showed decrease in natural Treg formation in thymus (but not total Treg numbers)
- Finally, BACH2del18 mice also have more severe EAE

Want to scale this approach as making a mouse for each variant is incredibly time-consuming - made CRISPRi screen in primary human T cells
- Transduce cells with lenti with dCas9 + KRAB
- Showed data of screen on variants that affect T cell proliferation

Showed that positive controls (IL2RB, VAV1, TBX21) are all down in proliferation, alongside other new positive regulators; also discovered negative regulators
- Showed example of variants that targeted MYC using promoter-HiC data to link variants to regulated genes

Overall: Very good talk, reminded me of the SR lab immune GWAS studies back in the day.

## Identification of CD4+ T cell antigens in Sjögren's disease using TScan-II

**Mohammad Dezfulian, HMS**

Difficult to link specific TCR sequences to cognate antigen due to high levels of diversity at the TCR and HLA

Developed TScan, which helps identify targets of TCRs at scale
Next, developed TScan-II to understand what antigen CD4 T cells recognize
- Platform is sensitive enough to perform genome-wide scale screens
- Wanted to capture endogenous antigen processing and T cell signaling; i.e., want to find antigens that can be processed and do activate T cells
- Uses reverse-engineered 293 cells to behave more like APCs (need to check paper for details)
- Use engineered CD8 cells that have been modified to take up CD4 TCRs and express GzmB; also introduced CD4 coreceptor and had to stabilize TCRs (?)

Developed reporter linked to GzmB activity, you have GFP linked to inactivated RFP by a GzmB cleaveage site. When GZMB cleaves the site, the RFP folds properly and expresses
- Relies on the fact that activated CD4 T cells will secrete GzmB into presenting cell

Used human peptidome library (covers 22K protens)
- Built by tiling 90 AA windows across every ORF in genome to get 259K fragments
- These fragments are then synthesized, cloned in-frame with the signaling peptie so that they will be properly processed and presented on class II

Can load presenting cell with multiple different HLAs or a single HLA allele
- if T cell recognizes antigen, will turn on reporter which can then be flow sorted and sequenced to resolve antigen
- Data shown is fold change enrichment presumambly over negative control (vehicle?)

Sjogren's disease is an autoimmune disorder mainly affecting exocrine (salivary and tear) glands
- High levels of T cell infiltration into these glands, predominately clonally expanded memory like CD4 T cells
- Ductal cells in salivary glands in these patients express class II and co-stim proteins
- What antigens do thse CD4 cells recognize?

Extracted CD4+ CD45RA- T cells from salivary gland biopsies from patients, then performed TCR seq to identify TCRs that had clonal expansion and were shared across patients
- Then took 20 top TCRs and performed TScan-II assay and screened against peptidome with multiple HLA alleles that were in patients
- Showed nice data that highlighted MAP3K4 as a recognized self-peptide, could use screen to identify specific HLA molecule that could load it
- Self-antigens were *not* shared across patients  
- Went on to show that ductal cells expressed both MAP3K4 and HLA class II

Overall: TScan and TScan-II seem like powerful methods for doing large-scale TCR screening in a multiplexed fashion. Unclear how engineering changes to APCs/T cells affect applicability of results

## Microglial-specific miR-155 deletion enhances interferon- dependent response to neurodegeneration and mitigates cognitive impairment in a mouse model of Alzheimer’s disease

**Kilian Kleemann, BWH**

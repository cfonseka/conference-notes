# CSHL Systems Immunology 2023 - Session 3

**Modeling of Immune Signaling and Gene Regulatory Networks**
*Wednesday, 19 April*

## Macrophage states defined by the dynamic responses to stimuli

**Alexander Hoffmann, UCLA**

Single cell RNAseq has revealed that there are many distinct macrophage states (demonstrated by scRNA on COVID patient lung samples showing 12 different macrophage clusters)
- However, single cell measurements are not necessarily an accurate measurment of these states due to various issues (dropout, etc)
- Cell states are both a function of molecular abundances (gene expression) but also molecular flux (how molecules turn over)
- scRNA cannot reveal changes in expression without perturbation

Question: Can we measure these fluxes to better define cell states?

Experimental design: single analyte dynamic response measurement - very different from scRNAseq data
 - Macrophages are the model system for this approach

Macrophages are context dependent, have memory of prior exposure, and perform stimulus-specific responses

Use mouse line with knock-in reporter that allows for tracking NFxB by automated image analysis (produced by Macs)

Polarized macrophages into six different states using different polarizing agents (IFN, IL-10, IL-4, IL-13, etc), then stimulated with different stimuli (LPS, P3CSK, etc) to generate NFkB trajectories
- Two day polarization regime
- Timepoints appear to be hours or potentially sub hours, 0-8h
- Timing and strength of responses (actually measured six QC metrics for pattern) is fairly reproducible across replicates
- takeaway: polarized states have distinct stimulus responses, so you have both stimulus-specific and polarization-specific responses

Trained LSTM ML model on timeseries data to predict...something? This was not clear
 - Showed F1 scores for differently polarized macrophages, suggesting naive macrophages (M0) have less identifiable stimuli
- This part did not make much sense but something about confusion matricies and how similar/different NFkB dynamic patterns are

Performed decomposition of timesries and used "XGBoost Classifier" to identify features that predict "classification"
- The machine learning approaches are difficult to follow but appear to be around identifying informative signaling features
  - Features here are things like "Deerivative at 10 min, or integral between 0.5h and 1 h" - seems very much like p-hacking or slicing the data endlessly
  - The data here about stimulus confusion is not very strong at all (no p-values on comparisons, unclear why anyone would care about predicting the integral of NFkB reporter between 0.5-1 hrs)

Then went on to perform LDA on their 9 pattern metrics and found different polarization states leads to different stimulus responses

Performed "Functional PCA" to dimensionally reduce timeseries data, allows them to determine how differentiated polarized macrophage states are in response to different stimuli
- Analysis here was looking at a bunch of UMAPs and saying things were more or less on top of each other

Overall: There is very little connection between the NFkB response dynamics and anything to do with macrophage biology. Difficult to understand how we could use this.

## Flexible control of T cell memory and self renewal by a reversible epigenetic switch

**Kathleen Abadie, UW**

Maintaining the stem-cell like nature of T cells (ability of naive T cells to differentiate into effector and memory states) is crucial for immunity

Two different theories for how memory cells are formed from naive progenitors
1. Decision to bicurfacte between effector and memory states is made very early
2. Decision is made later - all naive cells take on effector-like propoerties, then de-differentiate back into a more memory-like stem state

Use minimal system with naive CD8+ T cells isolated from mice, then grown in plate and stimulated and assayed by live imaging
- Can differentiate cells into effector and memory states - TCF1 is known to be critical for memory cell generation and self-renewal.
- TCF1 is on in naive and memory cells, turned off in effectors

Live imaged activated T cells with reporter for TCF7, allowing for live imaging of TCF7 expression for multiple clonal lineages
- Data suggests that certain branches of cells silence TCF7 and can measure those dynamics
- TCF7 silencing goes on heterogeneously, despite clonal nature of cells and controlled experimental system

Are sister cells related in their decision to silence TCF7? No - silencing is independent and stochastic - mediated by epigentic control that responds to inflammatory signaling (?)

While data does support early decision model, silencing could also support late decision modeling
- Showed cool video showing TCF7 turning back on stochastically after 50+ hrs and standard cell division

To address if this holds up in vivo, used congenic mouse model of LCMV infection and identified heterogeneity in TCF1 protein - indicating early decision
- Can cells that silence TCF1 _in vivo_ turn it back on? After sorting out TCF1 high and low cells and transplanting to secondary recipient, reactivation occurred post 2 days
- TCF7 high cells and reactiving cells could both display memory markers

Since both early and late decision models are supported by this epigenetic variability, built mathematical model for "flexible decision"
- Naive cells are activated and transition to "memory-competent" state that can stochastically and reversibly transition to an effecto state, mediated by pathogen load
- This model appears to recapitulate the standard immune response to viral infection

Maintenance of the TCF1+ stem-like state is important for mounting response against chronic infections and cancer
- Can cells reactivate TCF7 after exhaustion?
- Used ex-vivo exhaustion assay (6 days) and sorted functional intermediate and exhausted T cells to see if TCF7 could reactiavte after rest
  - 4 days of rest showed that some cells could reactivate TCF7, but this potential was degraded in exhausted cells

Overall: A cool talk with a lot of implications for T cell therapeutics particularly in the context of chronic inflammation.

## Systematic prediction of STAT-cooperating pathways that support cytokine-specific gene expression

**Rachel Gottschalk, University of Pittsburgh**

Interest of lab: how do macrophages interpret stimuli to produce diverse functions?
- specifically: cytokine signaling and specificity/diversity of gene expression

Cytokines primarily signal through limited number of STAT TFs that then lead to specific and diverse gene programs - how is this achieved?
- phospho of specific tyrosine residue on STAT TFs is thought to allow them to act

Model system: bone-marrow derived Macs are stimulated with either IL-6 or IL-10 (both activate STAT1 and STAT3 but lead to very different gene expression programs)
- Used proteomic data of STAT Tyr phospho to select timepoints to study by scRNA
- Identified both common and IL-6/IL-10 specific phosphosites

Want to link changes in phosphodynamics of STAT Tyr singlaing to downstream gene expression
- Used lasso regression to rank phosphosites by ability to predict gene expression
  - data shown here was without statistics or even legends

Used more complex mathematical modeling (sparse N-way partial least squares) to incorporate time information
- Claimed this model is still being built and showed uninterpretable graph of model weights

Overall: This talk was about using mathematical models to understand JAK-STAT driven gene regulation without any real explanation of the math or validation of the models

## Building models of CAR-T signal integration, using automatized/dynamic high-dimensional experimental profiling

**Grégoire Altan-Bonne, NCI**

Self/non-self discrimination by TCR signaling is a complex decision
- TCR activation leads to multiple outputs, not just IFN
- Choice of readout (IFNg vs IL-2 vs IL-3) can map different signaling dynamics

Can think of this as TCRs reading an encoding (antigen presentation) which is then "projected" onto a signaling cascade, which is then projected into T cell outputs (primarily cytokines in this study)
- Like neural network, you have input layer, encoding layer, and output layer

Built custom robotics platform for scaling T cell activation studies
- Standard murine system, take OT1 T cells and mix with B6 APCs
- Measure cytokines by flow over multiple timepoints
- generates a lot of data not amenable to simple clustering

To model the dynamics of this system, turned to simple neural network
- Input is timeseries readouts of marker (cytokine) expression
- Want to learn if cytokine dynamics effectively encode antigen quality (type of antigen used)
- Compresses data into latent space yielding a single parameter to quantify antigenicity (?)

Claim: Model defines over six different classes of antigens
- Latent space variable 2 has a non-linear relationship to antigen quality (as measured by EC50 from elispot)

Next, went on to understand bi-valent agonism; that is, different peptides can lead to very different activation dynamics when used in combination

Made mouse with degraded downstream TCR phosphorylation capability, and result is abrogation of non-monotonicity of latent space axis 2
- Leads to a more bimodal response to different antigens - i.e., antigens lose dynamic range and either produce a strong response or don't'
- Takeaway: signaling machinery allows for multiple levels of T cell response and more distinction between different agonists

Went on to extend study to CAR-T cells, which use a combined scFV segment with CD28 intracellular domain linked to the CD3 intercellular tail for signaling
- Claim: weak antigenic signals received through the endogenous TCR can lead to weak CAR-T activation

Developed AEBS CAR-T cell, which uses self-antigen as break to prevent strong CAR-T activation,
- Skipped through most of the data supporting this
- Allows for using tumor neoantigens as effectors while self-antigens will reduce off-target activity

Overall: The CAR-T development stuff is the most scientifically interesting but the underlying data wasn't presented; the neural network model does seem powerful. The implications of being able to decrease CAR-T off-target activity is intriguing but it's not clear how you would define these weak self-antigens (and what happens in autoimmune disorders?)

## Organism-wide analysis of sepsis reveals mechanisms of systemic inflammation

**Nicolas Chevrier, UChicago**

Study inter-organ pathways and immune responses
- Approach: perturb organ -> perform systemic phenotyping (whole genome expression) -> validate with functional tests (KO, blockade, etc)

Sepsis is a systemic immune response to infection with life-threatening consequences
- Understanding of organ-specific effects is difficult in humans, typically limited to assaying blood (difficult to biopsy septic patients)
- No targeted therapies exist

Induced sepsis through LPS and measured expression in many different tissues
- measured timepoints 6h up to 5d post LPS injection
- Used topic modeling to reduce dimensionality and identify gene modules of interest
  - how is k-selection done for topic modeling?
- Use pathway enrichment to link topics to things like LPS signaling and IFNg response
- Also identify tissue-specific topics

Asked - can cytokines explain the tissue specificity of response?
Injected cytokines either singly or as pairs and then measured RNA expression in various tissues
- Found that TNF + Il-18 or TNF + IFNg or TNF + IL1B recapitulate the expression changes induced by sepsis organism-wide

Used single cell data to identify cell type specific gene signatures, then used that to estimate cell type abundances from tissue RNA data
- Deconvolved 195 (!) cell types
- Showed that certain antigen combinations recapitulated known cell type effects from infection

For validation, performed sectioning of whole mice and then spatial transcriptomics on sections
- Because Visium is only 5 mm x 5mm, had to come up with a way to grid sections
- Somehow repurposed SNP-chip to perform section assay
- Identified 161 cell types across 17 organs

Can then ask what whole tissue changes occur after LPS injection
- Validated that TNF + IL1B/IL18/IFNg depletes epithelial and neuronal cell types
- Also see dysregulation of neutrophils

Pairwise profiling of cytokines reveals that different tissue types have different responses, allowing for better dissection of sepsis response

Identified that _Pla2g5_ is induced in gut during sepsis, apparently produced by goblet cells
- Data showed that expression peaks in gut initially, then increases much later in kidneys/heart
- _Pla2g5_ blockage is able to rescue septic mice
- _Pla2g5_ KO also rescued tissue injury, even though cytokine levels were not different between KO and controls
- _Pla2g5_ blocking led to upregulation of markers of red pulp macrophages
  - Potentially linked to iron metabolism and RBC homeostasis
  - Stained spleen sections for ferrous iron and found iron metabolism appears impaired in KO
- Followup work suggests _Pla2g5_ is upregulated in human sepsis and related to increased mortality
  -  _Pla2g5_ is released from the gut during sepsis and causes intervascular damage

Overall: impressive work, especially whole organism sections.  _Pla2g5_ story appears to validate well in humans

## Executable models of pathways built using single-cell RNA seq data reveal immune signaling dysregulations in people living with HIV and atherosclerosis

**Juilee Thakar, University of Rochester**

Interested in identifying innate/early immune signatures that drive immune/Ab response to vaccination or infection

Cohort of HIV-positive patients - how does long-term infection affect people as they age?
- Over 50% of HIV+ population is 50+

HIV infection is known to increase risk of cardiovascular disease (particularly artheosclerosis)
- HIV infection enhances the inflammatory environment - monocytes are particularly of interest as they can cross the endothelial barrier and differentiate into something plaque-like inside the vessels
- Molecules that drive monocyte migration )PSGL-1, SELPLG, CD162) are known

Performed single cell RNA on HIV cohort PBMCs to better understand signaling networks that drive molecular states
- Cohort was 8 subjects, half with cardiovascular disease and half w/o; all males, mostly age-matched (healthier patients were younger)

Developed method called scBONITA which uses single cell expression data to infer Boolean rules and perform pathway analysis
  - Initially developed for bulk RNA seq, adapted for single cell
  - Inputs: expression data and network topology (?)
  - Benefit of model: can simulate effects of network (?) by "deleting" or "increasing" the importance of a node
  - State of each node is defined by 1/0 (on/off) expression of genes, in which steady-state node represents "sink" attractor
  - Idea: distinct cell types exhibit characteristic signaling or transcriptional patterns - just like these nodes

Identified pathways related to monocytes that are dysregulated in AS HIV+ patients
- Leukocyte transendothelial migration pathway came up, as well as cAMP signaling

Next, performed "attractor" analysis on leukocyte transendothelial migration and identified dominant attractors: F11R and PECAM1
- These genes are required for platelet adhesion to vascular endothelial cells

Finally, developed tool called "WikiNetworks" for powering this tool - check Thakar-Lab github
- Also have "multiomics" version of BONITA (mBONITA)

Overall: scBONITA might be worth exploring (although not clear how applicable predefined networks will be for us); in a larger sense, these network approaches with "attractors" seem popular but people do not seem to explain them well.

## Non-coding fragility within interleukin-2 feedback circuitry shapes autoimmune disease risk

**Harikesh Wong, MIT**

APCs like DCs present both self and non-self antigens to conventional T cells, and this system can activate T cells to self
- Tregs can constrain autoimmune Tconv responses selectively while allowing for non-self response

Tconv that get a weak self input signal from DCs release IL-2, which led neighboring Tregs to expand and constrain the input signals required for the Tconv to mount the response, leading to transient burst of proliferation followed by massive dieoff

Do Tregs discriminate between self and non-self using this local feedback network?
- Showd data suggesting weak foreign agonists caused a Treg-constrained response, while a powerful foreign agonist escaped the Treg feedback

Hypothesis: it's not about self/non-self, it's about strength of signal and whether you exceed level of "feedback control" that tamps down on weak signals
- Can imagine diseases move this threshold around and lead to different T cell responses

Can genetic variation reshape the feedback boundary between self and non-self?

Most common autoimmune linked variants map to non-coding immune enhancers (often cell-type selective in effect)
- Studied IL2RA (CD25) as they had a good set of associated variants that mapped to this locus
- KO CaRE4 enhancer and did not see differences in expression of CD25 in Tregs, but the CD4 and CD8 Tconv showed significant reduction of CD25 expression at 6h post-stim
  - This effect disappears after 24h
- KO CaRE3 enhancer and found that CD25 expression is reduced in Tregs (not Tconv) but effects disappear upon stimulation
- Overall, genetic pertubations led to minor changes in expression

Used multiscale model (not described) to simulate effects of IL2RA expression kinetics and found that effects of enhancer deletion become non-linear and dramatic
- Suggests small effects in regulation can have non-linear effects in vivo

Summarized in vivo data as showing that these enhancer deletions do affect the density of Tregs in pancreas of animals prone to developing T1D
- Deletion of CaRE4 actually prevents animals from autoimmune diabetes; conversely, CaRE3 deletion (that weakens Tregs) leads to significant acceleration in the development of T1D

Takeaway: small changes in parameters in feedback circuits can cause large, non-linear effects

Overall: Threshold idea is interesting and relevant for autoimmunity; perhaps potentially useful for our rejection purposes as well?

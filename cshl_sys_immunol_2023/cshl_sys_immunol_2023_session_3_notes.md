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


## Organism-wide analysis of sepsis reveals mechanisms of systemic inflammation

**Nicolas Chevrier, UChicago**

## Executable models of pathways built using single-cell RNA seq data reveal immune signaling dysregulations in people living with HIV and atherosclerosis

**Juilee Thakar, University of Rochester**

## Non-coding fragility within interleukin-2 feedback circuitry shapes autoimmune disease risk

**Harikesh Wong, MIT**

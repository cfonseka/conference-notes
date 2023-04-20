responsecombinatorialrecommendsactivityunderstanding# CSHL Systems Immunology 2023 - Session 4

**Cellular Dynamics, Interactions, and Communication**
*Thursday, 20 April*

## Tipping points in biology: Quantitative and temporal control of responses from the cell level to organismal survival upon infection

**Ron Germain, NIAID**

Started talk with disclosure: no UMAPs, no scRNA, no topic modeling

Feedback circuitry is a common part of biology, and small changes can have non-linear effects through feedback loops
- Same extends to immune cell dynamics

Showed older data from experiments on THP monocytes in which TLR protein had been truncated (and placed under doxy control) to cause constant activation
- Used NOD1 as a control and found expression changes even without induction
- Takeaway: small concentration shift can cause a feed-forward effect which drives process to completion
- NOD1 regulation is controlled by miRNAs to prevent the concentration within a 1-1.4x threshold of wt (?)
  - People with variants that increase NOD1 expression to 1.5 get gastric cancer - small expression change -> very different results

Showed video of neutrophil recruitment accelerating at a wound and destroying both dead cells and collagen

Showed interesting failed experiment in which implication is what genes that are DE immediately after infection may just represent group shift to new tipping point and survival prediction may require more in-depth investigations
- Found that using genes for activated T cells allowed for prediction of survival to 1 LD50 viral challenge (mice) but only on measurements taken day 5-6 (they die on day 7-9)
- Found that presence of CD8+ T cells at day 5-6 was best predictor, assumption is that small differences in repertoire cause differences in CD8 T response

IBEX - iterative staining and bleaching that allows for 10-14 colors per cycle, allowing for capture of 80-plex by flow cyt (typically do 25-35 plex)
- Works with fresh and FFPE samples
- Pointed out that flow staining of tissues allows you to look at nuclear vs cytoplasmic localization of markers and make better guesses at cell state than spatial transcriptomics gets you
  - They measure by voxel, ot single cell but appear to get good enough resolution
- RAPID is neural net segmentation algorithm that is better than other segmentation and helps resolve 42 parameter IBEX experiments into cell types
- Also have combined with 3CD to get 3D-imaging
 - Images were very impressive

Showed data from covid/flu experiments in murine models that imply that immunopathology from Type I IFN blocks aveolar repair and causes death
- Counter-intuitive, but can't treat with anti-innate drugs early, must wait until later to tamp down on immunopathology response without affecting disease response

Fundamental issue: Immune function occurs in a complex tissue context - can't just isolate and look at single molecules or cell types
- Really pushed for more tisuse imaging/staining and less single cell

Overall: Great talk

## The spread of interferon-γ in melanomas is highly spatially confined, driving non-genetic variability in tumor cells

**Alon Oyler-Yaniv, HMS**

IFNg is a broadly acting cytokine, mainly produced by activated T cells and NKs
- upregulates antigen presentation
- directs cytotoxic effects
- prevents angiogenesis

IFNg is thus necessary for anti-tumor immunity
- Need to understand under what conditions IFNg can spread throughout tumor

Factors that determine exposure to IFNg
- Depends on how far IFNg can spread from producing cells + number of producing cells

From literature, IFNg spread is described as anywhere from just a synapse to 80 cell lengths away (800 um)
- Used diffusion consumption equation to model this process -> suggested spread would be in the range of 10s of um
- Confirmed this experimentally by staining OVA-pulsed OT-1 T cells and using layering to measure spread of IFNg on slide
  - Staining suggest localized spread is about 30 um

Two components to distribution of sourccs (IFNg producers)
- Source density and source organization (spatially)
- Showed mathematically how increasing density of producers narrows range of cytokine exposure for neighboring cells, while less density leads to a winder distribution of responses

Used patient data (melenoma multiomics dataset) to confirm that IFNg signaling spreads roughly 30-40 um in vivo
- Find that density of producing cells is deeply variable around tumors - some are 1:1 TIL to tumor cell, while other regions are devoid of T cells
- Recent study showed that the proximity or local density of T cells to tumor is more predictive of outcome than the overall number of T cells

Overall: Interesting talk and it's cool to see experimental data line up so well with the modeling. Wonder if we should think about trying to quantify some of our IHC data in similar ways, although we'd likely need more colors

## Multiplex imaging of localized prostate tumors reveals changes in mast cell type composition and spatial organization of AR- positive cells in the tumor microenvironment

**Ece Eski, OSHU**

Need to be able to distinguish indolent vs aggressive prostate cancers
- Want to avoid unnecessary biopsies and treatments
- Need better understanding of early tumor biology

Current approach: use H&E staining to grade tumor from 1-5
- This is insufficent, as many important markers are missed by H&E staining

Study heterogeneity of cell types and interactions between cancer and stromal cells in prostate cancer
- Can use single cell ATAC, but you get low number of cells and little to no spatial information
- Conversely, protein-based imaging (Cyclic IF) tools can recover more cells and spatial information
 - Allows for capturing >30 proteins on single-tissue FFPE sections on a subcellular level
 - Using AI segmentation, can get ~700,000 cells per slide

Study of prostate cancer samples from grade 3 and grade 4, alongside tumor adjacent normal tissues
- Found that Mast cells are present in high fractions in localized prostate tumors
  - 2 Mast cell clusters -> differentiated by expression of CD44, CD90, AR, and GZMB

Generated Voronoi tessellations to understand spatial interactions between the two Mast cell pops and tumor cells
- Found that GZMB+ Mast cells spatially interact with M2 macrophages in the tumor
- Found that AR+ mast cells interacted with Tregs in prostate tumors

Using 32 marker imaging, create neighborhoods (20 neighbors) and count cell type frequencies in each local neighborhood
- Identified significant differences in AR receptor expression between neighborhoods in stromal cells
- Then went back to scATAC -> topic clustering -> Identified that DAR (differentially accessible regions) were enriched for genes that enrich for NFkB signaling by GO
- AR+ stromal cells showed increased expression of HIF1a

Overall: Nice talk, but not particularly relevant for us.

## Exploring the regulation of macrophage heterogeneity across tissue contexts

**Kathryn Miller-Jensen, Yale**

Lab studies cell-to-cell heterogeneity in macrophages responses to different environments
- Talk today is about role of macrophages in the tumor microenvironment (and potential targeting)

Real talk title: Uncovering mechanisms of myeloid-targeted CD40 immunotherapy in treating melanoma
- Melanomas have been responsive to checkpoint inhibitor therapies (50%) - for those who don't respond, macrophages are promising target (since there aren't as many TILs in melanoma)
- Goal: reprogram tumor-associated macrophages
  - Inhibt T-cell repression caused by macrophages, or activate for antitumor effects

Approach: target CD40 with agonists to have activating effect on macrophages in tumors
- Currently in trial as combination therapy with anti-PD1 and anti-CTLA4

Used YR 1.7 mouse model (melenoma model with human oncodriver mutations)
- Found that triple combination therapy (anti-PD1, anti CSF1R, and CD40 agonist) lead to 80% survival

Use scRNA data to understand cell-cell communication
- Current methods require clustering, calcualte average receptor and ligand expression, then use previous knowledge to link cells in logical ways
- Developed NN cell type annotation method (Waskin, Bridges, _Dev Cell_ 2022)
- For cell-cell communication, used method called NicheNet to infer interactions

Used single cell secretion method to test waht DCs and Macrophages responding to CD40 combo therapy produce - found that DCs did indeed make IL-12 (as predicted by GO enrichment + interaction analysis), while macs secreted Chi313 and TNF
- Data shown had almost no difference in secretion between controls and triple therapy (?)

Hypothesis: CD40 agonism establishes an IL-12 and IFNg positive feedback loop between DCs and tumor-associated macrophages to promote anti-tumor activity

Showed more data on new trials for melanomas that tested with CD40 agonism improved response to double anti-PD1 and anti-CTLA4 therapy (checkpoint inhibtor)
- checkpoint inhibtor works so well (100% survival) so had to use lower dose so experiment was properly sensitized to detect CD40 induced effects
- IL-12 blockade suggested it was dispensable for CD40 effects (?)

scRNA on dissociated tumors (enriched for myeloid cells by FACS) and had difficulty clustering macrophage subtypes
- Difficult to use cell-communication approaches without pre-clustering, methods often returned too many putative R-L interactions

NICHES - method for inferring cell-cell communication without clustering by examining all potential pairs of cells (developed by colleagues at Yale) -  Raredon and Yang, _Bioinformatics_ 2023.
- You get some kind of low-dimensional pair embedding which can then be projected
- Used second tool called MILO (Teichmann/Marioni) which looks for enrichment in neighborhoods to determine differently abundant changes in neighborhoods of cell-cell pairs

Overall: This was very relevant in terms of understanding cell-cell communication, approach they used to R-L interactions seemed powerful for hypothesis generation.

## Knowledge-based machine learning to extract molecular mechanisms from single-cell and spatial multi-omics

**Julio Saez-Rodriguez, Heidelberg**

Lab works on single cell methods - tools presented are available on lab github (saezlab.github.org)

Developed knowledge database called Omnipath (omnipathdb.org)
- Comparable to knowledge graph for machine learning approaches
- >1K TFs, and >45K TF-gene interactions listed

Typically analyze gene regulatory networks by analyzing TF-target interactions using transcriptomic approaches
- Learn relationships between different genes
- Some methods also include TF motif info (SCENIC)

What can you do with this information?
- Can estimate activity of TFs from activity of regulated targets

**decoupleR** - performs many types of TF enrichment algorithms at once

Takeaway: Look (and cluster) data based on inferred TF activity and not expression of TFs alone

Then, scATAC data came along and algorithms adapted to use open chromatin regions to refine inferred activity

How do we evaluate whether a GRN is correct?
- Does it have tissue specificity, cooperation and predit gene expression
- GRNs should be able to recover active TF markers of cell types and tissues
- GRNs should be able to recover known TF-TF cooperativity events

Have set up framework to analyze different GRN-inference methods called GRETA

Also interested in cell-cell communication
- many assumptions behind inferring from gene expression (assumes if cell type A express high levels of ligand and B expresses high levels of receptor then they are communication, but this process is dependent on proximity, diffusion of signal, etc)
- We don't have a lot of detailed knowledge on these processes

**LIANA** - allows you to run many cell-cell interation methods (CellChat, CellPhoneDB, NATMI, Connectome, others)
- To evaluate, looked at how well predicted cell-cell communication happens between colocalized cells (spatially) - found generally positive results but lack ground truth proof of communication
- Recommendation: use multiple methods and take consensus set
- Most cell-cell communication methods don't handle aggregating data across multiple samples well
  - recommends Tensor Cell2CEll, which projects data into latent space to reduce number of interactions (?)

**MISTy** - allows you to predict cell-cell communication by incorporating spatial data with transcriptiomics
- other methods: SpatialDM, scHOT

Ended with looking at host-microbiome interactions using Visium data adapted to align from multiple species (looked at mouse gut slides)
- Tried to identify host-microbiome interactions but it was very challenging

Overall: Good talk, pointed out that there's a huge glut of new sc methods, but without good ground truths it's really difficult to truly benchmark how well they work

##  Microscale combinatorial stimulation of human myeloid cells reveals inflammatory priming by viral ligands

**Miguel Reyes, Broad**

Many of the advancements in systems immunology have been driven by advances in throughput and resolution from single cell methods
- Started to define disease-associated transcriptional states in humans
- How do we follow up on these findings experimentally?

Two typical approaches: go to relevant animal model and try to find analogue of human state OR take precursor cell and provide factors to try and push it into transcriptional state found in disease
- Second method helps identify drivers that push cells into disease-associated state

Want to try to find the sets of factors that can push cells towards these disease-states, but there are a significant amount of factors and combinatorial space to screen
- scRNA has reached high enough throughput to do these types of screens (caveats, 50-1000 cells/condition, roughly 40-80 perturbations, either single or double combinations)

Developed technology called StimDrop = cell hashing + droplet arrays
- Take set of pre-stimulated cells and label with barcode A, then take second set of cells with activation stimuli labeled with barcode B, then plate on microwell array with room for two droplets
- Thus cells are activated and labeled by barcodes A and B
- Reduces operational complexity

Used this to profile monocytes primed with one set of ligands and then challenged with a second ligand
- Primed monocytes with 21 ligands in 3 concentrations
- Challenged with 7 ligands at 1 concentration
- Cells end up labeled by both priming condition and challenge condition
- Use NMF to identify gene programs, found an inflammatory program driven by NFkB
- Found that anti-viral priming led to persistent expression of anti-viral program 7 days later
- Priming monocytes with viral DNA (poly dA:dT) leads to more production of TNF in response to later LPS challenge
- Identified set of genes that are uniquely unregulated in viral-primed monocytes
  - Some of these genes were elevated in patients with severe COVID

Overall: SimDrop seems like a good approach for reducing combinatorial issues in performing these types of screens

## Dissecting the cellular events that control swarming dynamics of neutrophil populations

**Katharina Glaser, Max Planck**

Neutrophils are sentinel cells of the innate immune system, circulate through blood and can enter tissue to detect tissue damage, cell death, and pathogens
- Undergo distinct migration behavior called swarming
- Swarms can be persistent (like around a wound) or tmeporary

Swarming behavior is controlled by LTB4, which amplifies swarming response
- LTB4- neutrophils lack swarming behavior

Neutrophil swarming depends on a cell self-amplification loop - yet somehow swarming does stop at point (as it causes collateral tissue damage)
- Is this also internally controlled?

Examined GPCR-Kinases (GRKs) in neutrophils
- Showed that GRK2- neutrophils will migrate linearly without stopping, while WT swarms stop after some time
- GRK2- neutrophils also fail to form tight clusters
- GRK2- neutrophils result in to impared bacterial containment

Suggests swarming and swarming inhibition are both self-organized controls from neutrophils

Created experimental system that allowed for swarming behavior to be assayed on a chip, allowing for high-throughput screening and alternative imaging approaches

Neutrophils are though to be highly glycolysis-dependent for metabolism
- Showed images of neutrophils taking up glucose; however, glucose uptake is dispensible to swarming
- Neutrophils can use glycogen for energy storage as well, which can be fed into the glycolysis pathway
  - Abolition of glycogen prevents swarming behavior even in presence of glucose

Conclusions: neutrophil swarming is a self-organizing response with specific metabolic requirements (glycogenolysis)

Overall: Nice description of neutrophil migration behavior

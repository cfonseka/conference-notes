understanding# CSHL Systems Immunology 2023 - Session 4

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



## Knowledge-based machine learning to extract molecular mechanisms from single-cell and spatial multi-omics

**Julio Saez-Rodriguez, Heidelberg**

##  Microscale combinatorial stimulation of human myeloid cells reveals inflammatory priming by viral ligands

**Miguel Reyes, Broad**

## Dissecting the cellular events that control swarming dynamics of neutrophil populations

**Katharina Glaser, Max Planck**

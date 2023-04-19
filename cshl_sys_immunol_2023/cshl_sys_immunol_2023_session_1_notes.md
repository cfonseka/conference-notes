# CSHL Systems Immunology 2023 - Session 1

**Single Cell Multi-Ome Analysis**
*Tuesday, 18 April*

## Decoding immune cell states in single cell and spatial data

**Christina Leslie, MSK**

story 1: cell states synovial fibroblasts in RA (collaboration w Laura + Sasha R.)
story 2: cellspace = sequence informed method for scATAC

RA synovium is characterized by infiltrating innate + adaptive immune cells
Asked how tissue resident cells (fibroblast-like synoviocytes) change in response to this environment?

Study design:
- 5 RA patients + 1 HC
- Sorted fibroblasts from synovium (CD45- CD31 - PDPN+) assayed by 10x multiome (scRNA + ATAC), also have cytokine stim response data, and then spatial data on synovial tissue slices

Identified THY1+ sublining fibroblasts (always nice to see your grad school work recapitulated) as well as lining fibroblasts
- Claim CD34+ and PI16+ identify a set of progenitor-like sublining fibroblasts
- Some sublining fibroblasts appear to be more "resting" while others are expressing inflammatory cytokines
- lining fibroblasts also divide into resting and HLA-DR+ "activated" clusters

Increasing fractions of inflamed sublining fibroblasts are found in patients with more severe leukocyte infiltration

Used scATAC to identify differences between lining/sublining acivated/resting synovial fibroblasts
- used tool called chromVAR to identify TF binding motifs that are most accessible by clusters
- Identified potential TF binding that implies either IFNg/TNFA (STAT/NFkB signaling) or AP-1 motifs that are downstream of IL-1B signaling

Found that inflamed lining fibroblasts do indeed express STAT1 phospho downstream of IFNg signaling

Wanted to use spatial data but ran into issue - Visium is not quite single cell (~10-30 cells/spot)
- Presence of T cells and B cells can be confirmed by IF, but difficult to map spatial to immune references
- Used "topic modeling" to deconvolve spatial data

Topic modeling approach: documents = spots, words = genes, topics = gene expression programs (hopefully represent cell types)
- Advantage: atlas-free deconvolution
- Requires manual annotation of each "topic"; however, can model topic posterior probabilities onto spatial map for better understanding
- Use this approach to identify macrophage "topic" that colocalizes with activated lining
- Initially ran deconvolve using LDA, have since switched to a variational autoencoder

Overall interesting, but I wonder how much of this is anchored by good IF staining of the fairly structured system of the synovium.

Learning meaningful embeddings from scATAC
- Typically end up with sparse cells x peaks matrix (similar to scRNAseq) and then perform dim red + clustering
  - R tool for this: ArchR
- Other approach is to aggregate to pseudobulk to get ATAC-like profiles

Proposal: map DNA-kmers (8-mers + reverse complements) from peaks and cells into same latent space
- Captures TF motif in sequence information, claim that it reduces batch
- In latent space, push kmers from sequence under peaks towards cells in which that sequence was open (i.e., had peak)
- Show data resolving batch effects and recapitulating hematopoesis
  - Used method called Palantir to identify pseudotime and backup their UMAP
- I would try it to batch-correct/cluster scATAC data if we had any, but unclear how good method actually is
  - Evidence was mainly visual and not statistical
  - Showed scalability to 720K cells without any runtime information so who knows

## Single cell molecular readouts coupled with migration assays to test unifying core tissue resident memory CD8+ T cell identity

**Milcah Scott, University of Minnesota**

Memory resident CD8+ T cells are found pervasively throughout most tissues
- Patrol for previously encountered pathogens and expand rapidly to secondary challenges
- Recruit B cells, DCs, etc
- Mouse studies have shown that Trms do not recirculate

Trm cells take on tissue-specific adaptations to reside there - what are these changes?

Use migration assays to study Trms, but difficult to do in human. CD69/CD103 are used as surrogate cell surface markers to identify Trms
- However, these markers may not identify Trms faithfully in different tissue types

Used CITE-Seq to analyze Trms from mice
- Also analyzed infectivity and migration capacity

Claim: tissue environment is primary driver of transcriptional heterogeneity

Performed DGE either grouping Trms across tissue or for each tissue independently
- Aggregate DGE did not work well, and they claim its because of tissue-specific adaptations
- Instead, they suggest comparing intra-tissue (so circulating lung to lung Trm, etc)
- They go onto to suggest there are two broad subtypes of Trms based on ICOS expression (??)
  - Subsets are not tissue specific; both are in the salivary gland for example

Talk ends with description of how to go from marker lists to flow sorting markers - this is not very novel
- Points out protein info from CITE-seq is also helpful (seems underutilized imho)
- Went on to map genes to markers with good Abs, significantly reduces list
- Finally, tested markers in cohoused mice and propose the following marker definitions

CD69+ CXCR6+ KLRG1(lo) CD62L(lo) = core Trm set, with ICOS and something else to differentiate.

Overall: light on conclusions, surprisingly descriptive (felt like a 2016ish paper)

## Quantifying how TCR sequence variation affects T cell fate at single-cell resolution

**Kaitlyn Lagattuta, HMS**

Used 5' 10x sequencing to get TCRs and transcriptome for single cells
- 123 individuals with COVID
- Got ~350K T cells (both TCRA/B, met other single cell QC events)

Identified 116 cases in which the exact same TCR sequence was observed in different individuals
- Asked how often they ended up in the same clusters (i.e. similar transcriptional phenotypes)

Used CCA to identify axes of covaraition between TCR scores and cell states
- Uae batch-corrected PC scores as input for "cell states"

Used Symphony to integrate initial dataset with additional 200K cells

Identified four separate CVs that were statistically significant over null permutation
- Good gut check, first CV pulls out NKTs and MAITs (restricted sequence, restricted expression pattern)
- Used orthogonal data to evaluate T cell state scores and got middling results

Hyopthesis: TCR memory score is capturing ability of TCR to detect general pHMC structure
- Thus, recapitulates (to some extent) thymic selection and they show that TCR score does distinguish single positive vs double positive selected T cells

10x BEAM queries dextamer staninng for individual T cells - might be useful for us/Mike C?

Overall: TCRs of memory T cells are systematically different; filtering of TCRs suggests some circulating T cells are more likely to reach the memory state

## Single-cell and spatial transcriptomics reveal aberrant lymphoid developmental programs driving granuloma formation

**Thomas Krausgruber, CeMM Research Center (Vienna)**

Focus of lab is on structural cells (particularly epithelial, endothelial, and fibroblasts) and how they participate in the immune response

Granulomas are aggregates of immune + structural cells in the skin - good place for studying

Sarcoidosis is a chronic, non-infectious disease in which granulomas form in the skin and lung, although can affect other organs
- No treatment options available
- What is the role of immune cells in this disease? Do altered cell-cell interactions affect granuloma propagation?

Performed skin biopsies on netural skin + lesional skin (with granulomas) on 12 patients with sarcoidosis and performed IF + scRNAseq

Identified lesional-specific CD4 Th cells, fibroblasts, and macrophages
- Validated presence of these cell types via staining; recapitulated granuloma structure with fibroblasts ringing immune cells
- Identified gene signatures for these cell types and then projected signatures onto spatial transcriptomics data

Goes on to talk about characterizing fibroblasts specifically, find both immune-interacting and tissue-remodeling fibroblasts
- FAP is highly expressed in the tissue-remodling subset
- Found that tissue-remodeling fibroblasts are found mostly within the granuloma (based on projecting signatures onto Visium data)
  - Validated with staining FAP
- Found that tissue-remodeling fibroblasts had expression of innate-like related TFs (?)

Used scRNA-seq to build cell-cell interaction network (ligand-receptor pairs), then evaluated colocalization in Visium data
- Used this to reduce number of ligand-receptor pairs
- Identified sets of pairs that were higher up in granulomas than other tissue

Overall: Interesting talk and convincing single-cell deconstruction of granuloma structure - unclear if this is relevant to us.

## Assembly and modeling of a dynamic gene regulatory network that regulates human B cell fate dynamics

**Harinder Singh, University of Pittsburgh**

Activated B cells either generate Ab-secreting plasmablasts that result in a fast, low-affinity response or differentiate into pre-GC B cells which then undertake SHM, perform affinity maturation and can eventually lead to the development of long-lasting plasma cells

Developed system for culturing primary human B cells and generating either trajectory
- Relies on series of activation markers (first anti-IgM/CpG/CD40L/IL-2; then CD40L/IL-2/IL-4/IL-10)
- Performed scRNA-seq on timepoints D0, D2, D4, D6
  - 2 days required for first cell division, later timepoints can have up to 5 divisions per 2 day period
  - Proliferation at D2, differentiation at D4 and D6 into plasmablasts/GC precursors
  - Identified bifurcation state at between day 4 and day 6
Functional annotation of cell states using known B cell signatures also revealed differentation into a memory B cell like phenotype

Identify BCL6 and PRMD1 as master regulators of GC precursors/plasmablasts respectively; interestingly, this fate appears to be predicted by ratio of IRF4 and IRF8 (?)
- Flow followup using those two markers and showed that naive B cells express more IRF8 than IRF4; go to double positive by Day 4, then resolve to either IRF4+ or IRF8+ populations by day 6 (although expression of the other molecule remains elevated, so more like IRF4++ IRF8+ and IRF4+ IRF8++)

scVelo analysis suggests bifurcation event may be arising as early as D2 - in terms of generating intermdediates that then go down the PB or GC trajectory

Attempted to assemble gene regulatory network that underlies these states, using bulk RNA-seq analyses of purified PB, GC, and naive/memory/activated B cell states alongside single cell (scRNA+BCR and scRNA+ATAC)
- Got samples every day from D0 to D6
- Used recently published method MIRA (topic modeling approach) - might be worth looking into for scRNA-seq work
  - ref: Lynch et al. Nat Methods (2022)

Used MIRA to perform "regulatory potential modeling" to infer which transcription factors are regulating a set of genes specific to PBs (or their binding regions are in open areas that are associated with the PB state by topic modeling)
- Top hit was MYC so has some potential issues this is but conceptually sound
- Didn't work as well for the GC-specific state

Finally, tested hypothesis by using CRISPR to KO PRMD1 and determine how differentiation is impacted
- Used RNPs with PRMD1 gRNAs, confirm deletion on D4 and then differentiate
- IRF4 expression is diminished in PRMD1 KO, IRF8 expression is increased
- PRDM1 KO reduces PB frequency and potentially increases GC frequency

Questions: if you follow a single B cell clone, does it undergo this bifurcation?
- using BCR-seq, tracked clones and showed that certain clones can be found in both PB and GC pops, indicating that they arose from the same precursor clone
- Also saw many GC or PB specific clones, suggestive of expansion after bifurcation

Overall: we should look more into topic modeling?

## Simultaneous snRNA & ATACseq characterizes specific innate immune memory

**Khodor Abou-Daya, University of Pittsburgh**



## Epigenetic states of germinal center B cells determined by single cell multiomics analysis can predict B cell fate

**Christopher Chin, Weill Cornell**

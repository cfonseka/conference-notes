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

Proposal: map DNA-kmers from peaks and cells into same latent space
- Captures TF motif in sequence information, claim that it reduces batch
- In latent space, push kmers from sequence under peaks towards cells in which that sequence was open (i.e., had peak)
- Show data resolving batch effects and recapitulating hematopoesis
  - Used method called Palantir to identify pseudotime and backup their UMAP
- I would try it to batch-correct/cluster scATAC data if we had any, but unclear how good method actually is
  - Evidence was mainly visual and not statistical
  - Showed scalability to 720K cells without any runtime information so who knows

## Single cell molecular readouts coupled with migration assays to test unifying core tissue resident memory CD8+ T cell identity

**Milcah Scott, University of Minnesota**



## Quantifying how TCR sequence variation affects T cell fate at single-cell resolution

**Kaitlyn Lagattuta, HMS**

## Single-cell and spatial transcriptomics reveal aberrant lymphoid developmental programs driving granuloma formation

**Thomas Krausgruber, CeMM Research Center (Vienna)**

## Assembly and modeling of a dynamic gene regulatory network that regulates human B cell fate dynamics

**Harinder Singh, University of Pittsburgh**

## Simultaneous snRNA&ATACseq characterizes specific innate immune memory

**Khodor Abou-Daya, University of Pittsburgh**

## Epigenetic states of germinal center B cells determined by single cell multiomics analysis can predict B cell fate

**Christopher Chin, Weill Cornell**

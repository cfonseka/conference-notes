# CSHL Systems Immunology 2023 - Session 6

**Tissue Systems Immunology**
*Friday, 21 April*

## Spatiotemporal regulation of T cell activation niches—Integrating intravital multiphoton imaging with spatial and temporal scRNAseq

**Deborah Fowell, Cornell**

Lab is interested in spatiotemporal control of CD4 T cells and their function in response to infection

Think about how the activation event for CD4 T cells is optimized
- Need system to be both extremely sensitive and reversible, as well as precise and quick
- Many times, immune cells have to respond to weak signals in a noise environment
- Solution: generate inducible self-organizing structures

The organization of the lymph node and germinal centers is well established, but the structure of CD4 T cells in peripheral tissues is less well understood
- Have described peri-vascular activation niches

These types of peripheral peri-vascular activation niches occur both in inflammation in response to vaccine challenge as well as in cancers

Focus on Th1s - main producers of IFNg and TNFa in anti-microbial response
- Th1s express CXCR3, which binds CXCL9/CXCL10/CXCL11 on APCs

Peri-vascular niches are created by a chemokine hub, APC clustering, and defined by a T cell point of entry into tissue
- In the niche, T cells make prolonged contact with APCs
- Clustering of T cells in peri-vascular region prevents need for T cells to search for NPCs
- These type of niches may be important for cancer immunotherapy by providing an area sequestered away from the generally immunosuppresive region of the tumor

Study peri-vascular niches by integrating imaging with optagenetics and spatial transcriptomics
- Niches are identified using intravital multiphoton, then regions in and out of the niche are biopsied and assayed by scRNA-seq
- Murine model system of inflammation used to develop niches in accessible tissue (skin)

Niches have expanded population of neutrophils compared to non-niche and total tissue
- Also monocytes and monocyte-derived macrophages along side T cells
- DGE reveals that niche-specific genes consist of chemokines (CXCL3, CXCL2, CCL4, CCL3)
  - Most expression derives from myeloid lineages
- CXCL10 is upregulated in the monocytes and monocyte-derived macrophages, consistent with previous work
  - These cells also express Class II, so can both recruit and present to T cells

Performed CellChat analysis and identified most chemokine signaling (CCL) coming from myeloid cells, signaling to themselves and each other
- Looking at CXCL signaling, got weak results for T cells

T cells are enriched for genes related to T cell proliferation and cytokine activity
- Some markers of Th1 function for niche T cells, but not dramatically different from non-niche cells
- Conversely, signaling molecules are highly expressed (caveat: only selected genes shown, no scale bar so unable to tell if its simple z-scaling artifacts)
- T cells themselves produced many recruitment factors (CXCL2, CXCL3, CXCL10, so on)

Went on to show that recruitment of CXCL10+ myeloid cells was independent of T cells (you get recruitment in a Rag-/- mouse)
- However, lack of T cells leads to loss of peri-vascular organization

CD4 T cells were able to enter into peri-vascular structures in the absence of CCR2 (main attractant from monocytes) but did not activate or produce IFNg - suggesting T cells need monocytes to form activation niche

Takeaway: T cell driven, monocyte-dependent niche assembly leads to highly organized peri-vascular immune structures to produce localized IFNg responses

Overall: Interesting talk and I wonder if we could identify these types of structures in the transplant setting (unlikely). Mouse perturbations are so strong (no T cells, no monocytes) that its hard to understand how these findings would apply to a human/NHP system.

## The immune checkpoint molecule Tim-3 regulates microglial function and Alzheimer’s disease pathology

**Ayshwarya Subramanian, BWH**

Alzheimer's disease affects many people, two major types: familial or sporadic
- Familial involves genetic mutations that lead to amyloid buildup
- Sporadic is the dominant form (95%) mediated by genetic risk factors

GWAS revealed a Alzheimer's linked variant that controls the expression of TIM-3 (_Havcr2_) in myeloid cells
- Expression of TIM-3 and other immune checkpoint molecules are high in microglia

TIM-3 has been studied on T cells, but role in microglia is less well understood

Microglia can be described as being in two states: homeostatic and activated
- homeostatic: Clec7a+
- activated: Clec7a-

Microglia play in important role in the development of the brain (neuronal pruning) and thus activate very early on (prenatal)
- TIM-3 expression tracks with TGF-b expression in public microarray data

Showed that TGF-b can induce the expression TIM-3 in microglia; TGF-b KO abolishes TIM-3 expression

TIM-3 KO microglia have less of a homeostatic phenotype and are marked by acticated/phagocytotic signatures
- phagocytotic activity assay data is weak in TIM-3 KO vs WT (barely any difference)

TIM-3 binds Smad2 (important for TGFb signaling) and TGFbRII
- phosphorylated Smad2 is reduced in TIM-3 KO

Overall: Clearly early research where followup characterization work is in progress - there was not any hypotheses made about what TIM-3 is doing in microglia (other than it can be considered part of TGF-b signaling)

## Lymphatic migration of unconventional T cells promotes site- specific immunity in distinct lymph nodes

**Paulina Cruz de Casas, Würzburg Institute of Systems Immunology**

## The good, the bad and the beautiful side of Kupffer cell activation in infection

**Charlotte Scott, VIB-UGent**

## Temporal profiling of human lymphoid tissues reveals coordinated defence to viral challenge

**Menna Clatworthy, Cambridge**

## Uncovering the spatiotemporal dynamics of placental IgG transfer toward precision prenatal vaccination

**Sepideh Dolatshahi, UVA**

## A comprehensive thyroid cellular atlas reveals thyrocyte-stromal-immune interactions that drive tissue infiltrative autoimmunity

**Michelle Rengarajan, MGH**

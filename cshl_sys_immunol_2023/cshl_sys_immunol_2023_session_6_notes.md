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

Lymph nodes are the central starting point for the adaptive immune response
- Allows for close contact between APCs, B cells, T cells, etc
- LNs are attached to tissue by afferent lymphatics, allowing them to surveil for pathogens

Dendritic cells drive tissue-specific immune responses - can mature in tissue, migrate to draining lymph nodes, then present to T cells, before homing back to tissue

Studied differences in tissue-specific draining lymph (skin, lung, small intestine)
- isolated LN, activated, and assayed cytokine expression by flow
- Observed different patterns of cytokine expression based on tissue (IL-17A/IL-4/GM-CSF)
- Identified _unconventional_ T cell population that expressed IL-17A (CD3+ CD4- CD8-)

Unconventional T cells do not recognize antigen presentation from APCs but instead have restricted reactivity, primarily to endogenous lipids or microbial metabolites

Performed scRNA on unconventional T cell population from three LN sites
- Could not annotate these cells as MAIT or gdT based on typical marker expression
- CD62L divided the unconventional T cells into two major groups: non-recirculating (CD62L-) and recirculating (CD62L)
  - Non-recirculating population differed (in % of cells) across LN types

Performed lymph node transplant experiment to show that unconventional T cells do not show tissue-resident expression patterns and instead resemble their transplanted location.

Used Dendra mouse model (engineered to express GFP -> RFP under UV) to determine if unconventional T cells are draining from tissue to lymph
- Found that unconventional T cells continuously migrate from tissue to draining LNs

Showed very weak data suggesting unconventional T cells from LNs have expression patterns similar to Th17s
- Almost certainly driven by IL-17A expression alone

Overall: We do observe unconventional T cells in our data as well, although its unclear how much of that is due to poor CD4 detection in mRNA. This talk did not distinguish gdTs from MAITs from NKs from whatever these cells are, but could follow up with paper to see if definitions are availble
- Marco Ataide et al., _Immunity_, 2022

## The good, the bad and the beautiful side of Kupffer cell activation in infection

**Charlotte Scott, VIB-UGent**

Kupffer cells = hepatic tissue-resident macrophages

Dysregulation of macrophages (and meyloid cells in general) is thought to play significant role in liver disease

Lab previously published liver cell atlas using spatial/scRNA (livercellatlas.org)

Identified heomeostatic and inflammation-recruited hepatic macrophage states
- Resident Kupffer cells (KCs) marked by VSIG4+ FOLR2+ CD5L+ TIMD4+

KCs do not become activated in murine model of non-alcoholic fatty liver disease
- Other data shown suggests same in humans
- This contravened conventional wisdom about KCs in disease

Looked to see if KCs could become activated in other disease models
- Applied paracetamol overdose to starved mice to induce liver damage - get massive liver damage after 24h that regenerates by 96h
- Initial damage causes massive recruitment of KCs - scRNA divides these into 3 populations
  - Specicially interested in "LAM-like" KCs, which show expression patterns similar to earlier described lipid-associated macrophages
- Chimera data shows that its resident KCs that become activated, not migratory

Looked to see what is inducing activated KCs by staining + confocal
- KCs in zone of injury (following paracetamol overdose) have altered morphology and drop expression of CLEC4F

Using Visium, showed that LAM-like KCs specifically reside in zones of injury next to LAMs

Showed experiments demonstrating that LAM-like KCs can be generated in absense of TLR signaling (and thus NF-kB signaling)
- conversely, lipid antigens do appear able to induce LAM-like KCs - makes sense for fatty liver disease but not so much overdose
- However, phagocytosis of damaged/dead cells could lead to lipid production as cell walls are broken down (?)

Moved to using salmonella infection murine model, and found that removing A20 from KCs (A20 negatively regulates NF-kB signaling) leads to exarcerbated immune response -> get better bacterial clearing but also death

Overall: This might be an interesting cell type to look into for our liver txp, especially once we have RNA profiles.

## Temporal profiling of human lymphoid tissues reveals coordinated defence to viral challenge

**Menna Clatworthy, Cambridge**

In order to understand human tissue immunity, we need an entirely human systems that are amenable to experimental manipulation

Lymph nodes contain both adaptive cells (B, Tfh, fDCs) but also innate lymphoid cells (myeloid)
- The details and timing of these processes have been established in mice, not humans
- Most human studies are from sampling peripheral blood following vaccine response

SARS-COV2 provided unique opportunity for natural experiment: everyone has gotten a novel challenge
- Sampled adenoid tissue biopsies (mucosal associated lymphoid tissue) from HCs and COVID-infected patients
  - Either active (3-5 days post infection) or recovered
- Assayed with scRNA, IBEX, spatial

Integrated dataset with airway scrapings with scANVI and identified cell types specific to tissue (and not blood)
  - Germinal center B cells, etc

Biggest (percentage) shift between blood and MALT tissues is monocyte populations
- Get layer of activated monocytes + neutrophils that are forming a defensive shield (undergoing netosis)

In recovered COVID patients, FOLR2+ macrophages expanded significantly
- Also change transcriptionally and take on a more anti-inflammatory/M2 signature

So in active infection: monocytes infiltrate and produce self- and neutrophil-recruiting chemokines -> form shield at peiphery -> macrophages come in to repair

scBCR-seq revealed the expansion of specific clones (~5% SARS-COV2 specific)

Plasma cells form niche in MALT tissue samples, IgD + IgA producing cells together
- Used CellphoneDB to identify cells that are producing chemokine ligands to recruit plasma cells - turns out to be myeloid and stromal cells according to sc analysis

Showed that polyclonal Ig receptor (PIGR) allows for IgA to cross epithelial barrier

Memory B cells expand first in acute infection, then plasmablasts - similar to mouse

Second talk: kidney tissues

Kidney is made up of outer cortex + medulla
- principal immunological challenge comes from bacteria in urine from bladder, while others come from blood stream in glomeruli

Created kidney cell atlas using pre-natal and post-natal samples
- Found many resident immune cells (including adaptive immune cells)

Pelvic epithelial cells are expressing molecules for neutrophil recruitment (CXCL8) as well as AMPs (anti-microbial peptides)

Used kidney atlas to see what changes occur in lupus nephritis
- Used perfusion system to test human kidneys (from same individual) allowing for internal controls
- Did stimulation and then performed scRNA (with some enrichment)
- Identified that NK cells, inflammatory monocytes, and endothelial cells were enriched post IC stimulation

Overall: Good talk, kidney cell atlas has obvious relevance for our work. Interested in endothelial cell changes observed in response to Immunochallenge given txp experiences.

## Uncovering the spatiotemporal dynamics of placental IgG transfer toward precision prenatal vaccination

**Sepideh Dolatshahi, UVA**

Lab studies systems biology of neonatal-maternal immunity and cancer systems immunology
- Todays talk is about placental transfer

Newborns are born immunocomprimised, have tranisnet and low levels of IgG for the first year of life
There is also some passively transferred maternal IgG as well - transported by way of Fc receptor mediated transcytosis across placental barrier before it is galactosylated for transport across the fetal endothelium
- IgG1 is preferentially transferred

Previously examined cord and maternal levels of Abs at birth to measure transfer efficiency, but "that is not fair because it is a dynamic process"

Decided to build a kinetic-dynamic model of IgG-subclass specific placental transfer
- Model parameters are built off old experimental data (1996 studies of cordocentesis)

Used simulations to determine which factors in model are most important for transfer efficiency
- Identified expression of FCgRIIb as key player

Endothelial cell-bound FCgRIIb is a key driver of subclass-specific IgG transfer
- Expression of FCgRIIb increases over time in prenatal human

Different subclasses will compete with each other for access to FCgRIIb - showed evidence that transfer efficiency dropped when mixed with other IgGs

Used model to simulate effects of prenatal vaccination at different times and found that ~20 weeks produced a stronger IgG response than earlier or later
- Caveat: just considering IgG titer and not other protective effects

## A comprehensive thyroid cellular atlas reveals thyrocyte-stromal-immune interactions that drive tissue infiltrative autoimmunity

**Michelle Rengarajan, MGH**

Hormone-producing cells are specifically targeted by the immune system in some forms of autoimmune syndromes (specifically thyroid)
- T1D, drug induced autoimmunity, or genetic autoimmunity (AIRE/FoxP3 muts)

Thought to be due to self-reactive T cells attacking hormone producing cells

However, there are checkpoints that can reduce this process

Thyroid is infiltrated in many patients, but only 30% require hormone replacement
- 15% of american women have antibodies to thyroid (!)
- Thyroid infiltration can clearly be held in check without drugs in some people, and typically immunotherapy is not used to treat

Studied surgical samples of thyroid + paired blood spanning spectrum of thyroid diseases
- Control, Graves (early infiltration) and Hashimotos (chronic infiltration)

scRNA captured many different cell types, primarily thyrocytes (epithelial)
- Even in patients with significant infiltration, only amounts for 20-30% at most
- Within-disease states shows significant heterogeneity of infiltration

Measured TSH levels in patients (higher TSH levels means low function)
- Found weak correlation between degree of infiltration and TSH levels
- Provides support for idea that there are tolerating checkpoints in system

Performed DGE on thyrocytes in Hashimotos vs Control - identified upregulation of MHC I and MHC II, as well as interferon-responsive genes
- Subcluster thyrocytes into five clusters: classical thyrocytes and then four less well-described ones (E1-E4)
  - E5 cluster showed upregulation of HLA genes

Also identified subset of CD8+ T cells that produce thyroid IFNg and cluster into Trm-like and GZMK+ clusters
- These populations are elevated in frequency in Hashimotos vs control

Showed unconvincing data that E5 thyrocytes are responding to IFNg production from CD8 Trm-like cells

Next, looked at reverse signaling (E5 send to T cells)
- Identified that E5 thyrocytes in Hashimotos or Graves express inhibitory molecules but not costimulatory molecules

Finally, showed weak data of correlation between TSH levels and fraction of E5 cells/total immune cells in patients
- Caveats: weak correlation, small sample size, low fractions

Takeaway: Trm-like CD8+ cells produce IFNg that induce classical -> E5 transition for thyrocytes that can then go onto inhibit immune response (?)

Overall: Interesting talk although not clear thyroid activity is a major concern for us.

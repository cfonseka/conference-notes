# CSHL Systems Immunology 2023 - Session 7

**Immunoreceptors: Specificity and Signaling**
*Friday, 21 April*

## High-throughput and high-dimensional single-cell profiling of T cells

**Jenny Jiang, Penn**

The diversity of T cell repertoire forms the safety net of our immune systems
- Theoretical limit 2x10^19, humans have roughly 10?^11 T cells per individual
- Potential antigen space is larger than available T cells (1e14 > 1e11)
  - Thus, you have crossreactive T cells

Molecular interactions between the TCR and antigens shape the T cell repertoire

Developed DNA-barcoded tertamers to be able to profile 300+ epitopes in a single experiment (as opposed to flow based methods)
- UV exchange process allows for fast load of peptides onto MHCs
- Used in vitro transcription translation to create DNA-barcoded pHMC tetramers
- called TetTCR-seq

Most cancer neoantigens are a point mutation change from the wildtype antigen
- Evaluated multiple neoantigen-WT antigen pairs with different mutation positions and measured amount of crossreactivity by TetTCR-seq

TetTCR-seq can be combined with DNA-labeled pAbs to allow for flow sorting
- Can get 20,000 cells per experiment with >300 tetramers

Examined cohort of healthy and T1D individuals and studied foreign and T1D antigens
- Identify TCRs cross-reactive to self-peptides (insulin) and microbial peptides

Trying to understand how SARS-COV2 Omicron is able to avoid humoral immunity
- Decrease of neutralization Abs is observed in Omicron, but T cell responses are stable across variants
- Curated 80 or so peptides to test on cohort of 22 vacinnated patients
- Use Bhattacharyya index to determine how similar T cell repertoires are and identified specific sub cluster of T cells
  - This cluster upregulates activated markers like GZMB
- Identified conserved epitope that nearly all patients reeact to

Hypothesis: Generate multiple TCRs to a common antigen to provide backup in case virus mutates and antigen changes
- If immune response is too clonally dominant, you will generate a single clone and be susceptible to second round of infection

Conducted study to determine if a diverse TCR repertoire can resist antigeneic drift
- Found that position 5 is relatively invariant but other positions can tolerate variation
  - 5 position appears important for interaction with CDR3 alpha chain

## Decoding and rewiring immune recognition at the single-cell level

**Bingfei Yu, USC**

ENTER system - model of viral display and delivery
- Can display user-defined ligands on lentiviruses (like Ab scFv, or pMHcs)
  - Lenti can be loaded with other cargo or fusogens

Engineered viruses to display version of pMHC along with VSVG fusogen, allowing for entry into antigen-specific T cells
- Use GFP labeled viral proteins and place 10x-compatible seq-tags to barcode specific pMHC used

Applied this technique on primary T cells from CMV seropositive patients
- First, induce expansion of primary T cell pool with CMV peptide, then use pooled MHC displaying viruses with CiteSeq and Hashtag Abs (?)
- Compared phenotype of CMV-specific T cells to bystander T cells
  - CMV-specific T cells are mostly effector memory T cells and have high expression of IFNg and TNFa, alongside specific CCL3 expression
- Saw that T cells that bound to different CMV antigens clustered separately, suggesting they underwent antigen specific gene signatures
  - Interestingly, one antigen seemed to push T cells towards a CD8+ Treg like state
- T effector gene set enrichment correlates weakly with size of T cell clonal expansion

Used modified version of virus to deliver specific payload to antigen-specified payloads
- Generated viruses containing CMV epitope and inducible "suicide" gene as payload
- Observe that they are then able to specifically deplete antigen-specific T cells using drug
- Did reverse experiment where they use lenti to deliver shRNA against FAS, then add anti-FAS - see about 2x-fold enrichment in antigen-specific T cells
- They go on to do similar experiments with B cells by expressing BCRs

Overall: System seems very cool (and similar to Sana and others cell therapy modalities) - seems like it would be useful for screening (but throughput is apparently quite low at the moment)

## Germline-encoded amino acid-binding motifs drive public antibody responses

**Ellen Shrock, HMS**

Using Tomasz's VirScan, can use phage display library to tile across all potential viral peptides (meant to be full representation of human virome)
- Can use this to determine which peptides are recognized by using patient blood and sequencing phage

Public epitopes are recognized by individuals
- Over 70% of people make Abs to one specific SARS-COV2 epitope
- Showed another example where people from across the globe all react strongly to a small section of the RSV Glycoprotein G or Adenovirus C penton peptides, suggesting that these are public epitopes

Are the Abs that recognize these public epitopes the same between diverse individuals?
- points out that antigen specificity is defined by both the CDR3 but also the CDR1 and CDR2 regions (which are mostly germline encoded)

Identified nine Abs across 7 donors that recognized a specific public flu epitope
- CDR3s were completely different, but shared specific IgH V and IgL/K V genes
- Claim: This pattern is observed time and time again for different public epitopes

Do public epitopes themselves have skewed AA composition (compared to human virome)
- found that lambda V recognized epitope had overrepresentation of lysines - does this mean labmda V genes have germline-encoded affinity for lysines?
- Identified positions within V genes that contain lysine-specific binding domains (dubbed GRAB domains)
  - Example shown is IgLV6-57 - points out all critical residues are germkine encoded
  - Other lambda V genes have highly similarly structured GRAB domains

More broadly searched V genes for GRAB motifs that were specific for certain residues
- Identified additional 18 V genes with GRAB motifs
- Also experimentally showed that mutating critical residues destroys residue-specificity of domain

## Quantitative modeling and analysis of TCR cross-reactivity

**Amitava Banerjee, CSHL**



## An integrated analysis of the antigen-specific T cell landscape in autoimmunity

**Alok Joglekar, University of Pittsburgh**


## Engineering next-generation T Cells for cancer immunotherapy

**Yvonne Chen, UCLA**

## Mapping the T cell repertoire to a complex defined gut bacterial community

**Kazuki Nagashima, Stanford**

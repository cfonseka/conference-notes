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

## Quantitative modeling and analysis of TCR cross-reactivity

**Amitava Banerjee, CSHL**



## An integrated analysis of the antigen-specific T cell landscape in autoimmunity

**Alok Joglekar, University of Pittsburgh**

## Decoding and rewiring immune recognition at the single-cell level

**Bingfei Yu, USC**

## Engineering next-generation T Cells for cancer immunotherapy

**Yvonne Chen, UCLA**

## Germline-encoded amino acid-binding motifs drive public antibody responses

**Ellen Shrock, HMS**

## Mapping the T cell repertoire to a complex defined gut bacterial community

**Kazuki Nagashima, Stanford**

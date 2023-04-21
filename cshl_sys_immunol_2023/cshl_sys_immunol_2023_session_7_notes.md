successful# CSHL Systems Immunology 2023 - Session 7

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

## An integrated analysis of the antigen-specific T cell landscape in autoimmunity

**Alok Joglekar, University of Pittsburgh**

Focus of this talk: identifying epitope specificity of T cell response
- Use cell-based epitope technology (TScan/SABR) allowing for profiling 10^4 - 10^5 epitopes against library of T cells/TCRs of interest

SABRs - Signaling and Antigen-presenting Bifunctional Receptors
- Contains pMHC linked to signaling molecule (CD28/CD3) so you get transduction upon congnate TCR-pMHC interactions - lights up GFP in cells
- Express SABRs in Jurkats that are expressing TCRs of interest
- Takeaway: SABRs read successful TCR-pMHC interactions
- In screen setup, calculate enrichhment score for epitope (expected value of enrichment if there was no TCR)

Used NOD mice (murine T1D model) - get progressive heterogeneous infiltration of T cells into pancreas
- Autoantigens are already known and broadly shared between mice and humans
- Class of autoantigens thought to be specific to T1D are hybrid insulin peptides
  - Hybrid epitope with left part made up of insulin and right part made up of different protein - often created post-translationally
- Isolated T cells from pancreas at 6, 8, 10 weeks and performed scRNA + TCR
  - Identified both clonally expanded and unique T cells
  - Expanded T cells fall into clusters with activated/proliferating expression phenotype
  - Unexpanded T cells are mostly naive like

Created tissue-specific B cell epitope library for screening
- Had database of all autoimmune peptides isolated from pancreatic islets
- Validated using known TCR and epitopes

Took top 40 clonally expanded TCRs (most likely to have seen antigen within islets)
- Reconstructed TCRs and expressed in jurkats, then screened against epitope library
- Identified TCRs that recognize both native insulin and hybrid insulin peptides
- Out of 40 clones, 10 TCRs validated -> 6/10 were reactive to hybrid peptides

Designed _in silico_ hybrid insulin peptide library using insulin and proteins found in beta cells then performed screen against TCRs
- TCRs tended to react to peptides that had left side from insulin and right side from various proteins
- Went back to single cell and observed that different TCRs did not cluster, suggesting they did not have large differences phenotypically despite recognizing different epitopes

Overall: This was a very cool talk on how to do large scale TCR-epitope screens and SABR seems like a really effective method for doing this

## Engineering next-generation T Cells for cancer immunotherapy

**Yvonne Chen, UCLA**

Focused on engineering CAR-T cells
- Adoptive T cell therapy involves isolating T cells from patient blood, engineering in tumor-specific TCRs, expanding _ex vivo_, and then re-infusing into patient
- Currently autologous all though many people are working on allogeneic

Antigen escape significantly limits the durability of response to CAR-T
- Showed data from diffuse B-cell lymphoma indicating that 50% of patients relapse in 6 months and progression-free survival is only 3-6 mos
  - Substantial fraction of relapsiing patients end up with tumors that have lost targeted antigen (in this case, CD19)

Works on developing bi-specific CARs that can recgonize multiple tumor antigens (in this case, CD20 alongside CD19)
- Set up binding domains in tandem (called tandem CARs) - they call them "OR gate" CARs since they can recognize one or the other
- In clinical trial, 10/11 responded to tandem CAR therapy, while 8/11 saw complete response
 - One complete non-responder was found to have CD19- CD20- tumor
- Claim: very little toxicity even though trial patients have very high tumor burden - maximum cytokine release syndrome stage was stage 1 for any patient

For some reason, CD19 CAR T cells outcompete CD20 CAR T cells (which is why they worked to build bispecific CAR instead of dosing with two different CARs)

Tested a series of CD20-targeting CARs using different monoclonal Abs and tested in murine model
- Rituximab based CAR outperformed others initially but eventually burned out and there were no differences in long-term survival rates
- Some CARs (including the Rituximab CAR) suffer from tonic signaling (proliferation in absence of antigen)

Hypothesis: Some tonic signaling is good but too much drives the cells towards premature exhaustion

Developed modified Rituximab CAR by inserting alanines to base of CAR transmembrane domain to induce conformational changes in TCR
- Observed significant reduction of tonic signaling with 1, 2, or 4 alanines
- Saw that 1, 2, and 4 alanine mods also lead to bettter survival while 3 alanines did not
  - 3 alanines leads to a 320 degree twist which is fairly close to 360 degrees (i.e., no induced conformational change)

Generated hybrid CARs using Rituximab and Leu16 CARs
- Appear to generate moderate levels of cytokines (between Rituximab and Leu16 single CARs)
- Showed data indicating hybrid CAR significantly outperforms CD19 CAR and can handle second tumor challenge

Used bulk RNA to analyze gene expression changes in hybrid CAR cells upon antigen stim
- Observed enrichment for memory cell phenotypes as well as IFNg response and T cell activation

Overall: Pretty amazing evidence - hybrid and bispecific CARs seem like the next generation of the therapies, given all the current caveats with CAR T therapy overall

## Quantitative modeling and analysis of TCR cross-reactivity

**Amitava Banerjee, CSHL**

Focus of talk is T cell crossreactivity - ability of a TCR to bind multiple pMHC complexes
- How do we predict whether a given epitope binds to a TCR?

Describes methods for testing a single pMHC against many TCRs (clain: these methods are well established) while testing multiple pMHCs vs a single TCR (claim: not well understood)
- Want to cluster epitopes that can bind (or not bind) to a given TCR and identify similarities

Can describe epitopes mathematically by similarity using methods like Hamming distance or more complex ones that take in biochemical data

Performed screen of peptides by identifying most strongly binding "index peptide" and then mutating each position to new residues and measure binding
- Identify "strong binders" and "non-binders"

Showed data indicating that using Hamming distance metric fails as it cannot discriminate between strong binders and non-binders (since they can both be 1 AA change away)
- BLOSUM100 metric outperforms random classification (AUC 0.7)

Claim: Positional information needs to be included for better result (changes at end of epitope instead of center might have different effects)

Adding in positional data using a Bayseian framework improves AUCs to 0.8 for Hamming (from 0.5) and to 0.9 for BLOSUM100

Across different TCRs and different distance functions, position weights learned appear fairly similar - weights are lowest on the first and last positions and highest in the middle

Going to crystal structures showed that middle positions of epitope has most contact with CDR3 arm of TCRs - thus weights learned by algorithm correspond to structural knowledge

Overall: Interesting that even a very naive approach like Hamming distance improves so much with positional weighting. Unclear to me how prior distributions on weights are set, or how applicable this is outside of the two epitopes tested

## Mapping the T cell repertoire to a complex defined gut bacterial community

**Kazuki Nagashima, Stanford**

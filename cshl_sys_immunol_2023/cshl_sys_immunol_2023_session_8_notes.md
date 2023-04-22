lymphoid# CSHL Systems Immunology 2023 - Session 8

**Human Systems Immunology II**
*Saturday, 22 April*

## Multi-Omic analysis identifies metabolic enhancement of immune memory by lysine deacetylase inhibition during immunisation and infection

**Eoin McKinney, Cambridge**

History of immunomodulation - "vaccine boosting"
- In 1926, Al2(SO4)3 - Aluminum sulfate was found to boost vaccine response by serendipity

Now - want to systematically evaluate immunomodulation to identify boosting adjuvants

Signature of experimental setup is T cell phenotype - does it develop a robust memory response or progressively proliferate and exhaust
- These two states are mutually polarized and transcriptionally distinct
- Use these profiles are template to identify compounds that can modulate between exhaustion and memory
- Previous work has shown that T cell exhaustion leads to better outcomes in autoimmune disorders; in other disorders it leads to worse outcomes

Compare gene signatures of immune cells to gene signatures from drug response libraries or disease studies
- Predict which drugs match best onto signature and are predicted to produce either a memory or exhausted phenotype
- Perform phenotypic screening on primary human CD8+ T cells and stimulate with polyclonal Ab, measure phenotype by PD1 (exhausted) vs IL7R (memory)
  - Allows for validation of _in silco_ predicted compounds
- Identified KDACi (lysince deacetylase inhibitor) compounds pushed CD8+ T cells towards memory state in reproducible manner
  - Only some KDACi had a strong effect, so studied differences between compounds to identify specific differences

KDACi induced glutaminolysis promote Tmem differentiation _in vivo_

Performed RNA-seq and ATAC-seq to understand changes being induced in T cells
- Identified DEGs and saw strong enrichment of entire memory signature
- ATAC analysis indicates multiple changes in memory-associated pathways especially Wnt

Tested KDACi in multiple _in vivo_ murine models and saw markedly increased memory T cell responses in each setting.

## Multi-dimensional integration of protein interactomes with genomic and molecular data discovers distinct RA endotypes

**Jishnu Das, University of Pittsburgh**

Lab focuses on using machine learning to integrate multiomics data in the context of immunological disorders
- Focus: defining disease subtypes in RA

RACER cohort - 1,000 RA patients with clinical metadata and individual genotypes
- Sequenced on SNP chip
- Most subjects are either CCP+ RF+ or CCP- RF+
  - There have been differences in disease progression outcomes between the two subtypes
  - Current clinical practice uses the same treatment regimen (MTX/aTNF)

First looked if there are differences in heritability between the two subtypes
- Used RML framework (restricted maximum likelihood) to estimate heritability for each group
- Found significant differences in heritability (~30%) with double positive subtype being more heritable
- Performed GWAS and the only locus over sig was HLA - but only ~10% of heritability can be explained by HLA locus variants
  - Study cohort is likely underpowered

Tried to use additional genetic data to identify other potentially responsible loci
- Approach: map interaction networks to perform GWAS using network propagation
- Feed in LD-adjusted scores, and then use random-walk to determine significance
  - Used entire human interactome network (17,000 nodes and 250,000 edges)
- Identified 13 modules of interest

Use tool called PrediXcan that predicts individual level gene expression data from genotypes (how?)

Than used stratified-LD score regression to evaluate modules identified by network analysis and validated 7/13 as heritable

## Human infant and adult T cells exhibit distinct programs of residency, activation, and effector function across tissues

**Peter Szabo, Columbia**

Have lots of single cell data on tissues from RDH adults and infants - data is unpublished but may eventually be useful for pediatric heart program

Papers are Conners et al. (in revision) and Szabo et al. (in prep) from Farber lab at Columbia

Single cell hierarchial poisson factorization is an NMF-like approach for single cell developed by Peter Sims at Columbia
- yields non-orthogonal latent factors, models dropout

## Dynamic immune landscapes during melanoma progression reveal a role for endogenous opioids in driving T cell dysfunction

**Linglin Huang, HMS**

## Development of adaptive immunity in human tissues

**Donna Farber, Columbia**

Immune cells are distributed throughout tissues and circulation
- TRM - tissue resident memory T cells
- BRM - tissue resident memory B cells

TRMs coordinate _in situ_ immune responses
- Showed data from murine influenza model showing that lung TRMs were able to keep mice alive while spleen TRMs had similar survival rates to WT
- Also associated with autoimmune skin disorders (psoriasis, vitiligo)

Coordinated with OPOs to get tissues from RDHs (adult and child)
- Many tissues from one person (tonsil, thymus, lung, spleen, pancreas, LN, kidneys, skin, bone marrow, intestines)
- 614 donors collected over 12 years, majority non-pediatric

Susceptibility to infectious disease (as measured by pre-pandemic infectious disease hospitalization rates) is highest at birth and old age (>70)

COVID was a sweep through entire population of new challenge with no memory
- Age was strongest predictor of COVID mortality

Studied immune tissues in 90 pediatric organ donors from 0-10 ys

First, measured accumulation of T cells in mucosal sites over time
- Nearly none at 8 days of age, but get to 50% of later total by 1.3-1.4 ys
- Most mucosal sites quickly accumulate memory cells (almost sigmoid) while rate of naive-memory shift is much slower and linear in lymphoid tissues

Described Trm phenotype in early and late childhood by bulk RNAseq
- Identified more "vulnerable" stage for Trms before 3 ys of age

Found that pediatric lungs contain BALT (bronchus-associated lymphoid tissues) - secondary lymphoid tissue with follicles + B cells
- Appears in first 6 mos of life and matures at 3 ys of age, then begins to recess by 6-0 ys
- Similarly, B cell numbers in lung peak at 3 and then decrease
- BALTs only appear in adults in disease
- Stained for CD10 and identified germinal centers in BALT follicles
  - Flow cytometry revealed that lung tissue contained major B cell differentiation subsets
  - Then performed scRNA and compared lung B cells to lymph node B cells, finding that lung B cells exhibit markers of GC formation (Bcl6/Ly9) and activation (NR4A1/2, CD83)

Performed CITE-seq profiling of 24 adult (20-75 yrs) donors, assayed 1.3M cells
  - MMOCHI - cell type classifier for CITE-Seq

Overall: Good work and tissue-relevant data will become more relevant for us in the future. Hopefully these datasets will be released soon, but clearly worth keeping track of the Farber lab

## Discovery of novel Treg modulators by integrating gene expression profiling with computational modeling and functional assays

**Ali Zarrin, TRexBio**

## Single cell profiling of blood immune cell substate kinetics in early sepsis reveals progressive decrease in monocytic myeloid-derived suppressor cells

**Pierre Ankomah, Broad**

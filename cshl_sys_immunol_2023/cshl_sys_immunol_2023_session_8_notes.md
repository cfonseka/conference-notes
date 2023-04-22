# CSHL Systems Immunology 2023 - Session 8

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

## Dynamic immune landscapes during melanoma progression reveal a role for endogenous opioids in driving T cell dysfunction

**Linglin Huang, HMS**

## Development of adaptive immunity in human tissues

**Donna Farber, Columbia**

## Discovery of novel Treg modulators by integrating gene expression profiling with computational modeling and functional assays

**Ali Zarrin, TRexBio**

## Single cell profiling of blood immune cell substate kinetics in early sepsis reveals progressive decrease in monocytic myeloid-derived suppressor cells

**Pierre Ankomah, Broad**

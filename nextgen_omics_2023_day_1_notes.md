# NextGen Omics Day 1



## Keynote - Computational Pathology - The Next Revolution in Cancer Diagnostics

**Mark Gustavson, AstraZeneca**

Computational pathology - next transformative technology to enable better patient selection and clinical outcomes
- First digital scanner authorized by FDA in 2017, so recent

Traditional IHC path scoring is semi-quantitative, subjective, and limited to the resolution of low-level staining
- Traditionally done by eye
- Heterogeneity is measured by a single cutoff (estimate of cells positive for X marker)
- Scores are categorical (i.e., 1-4)

Computational path scoring allows for quantitative, continuous scoring, more reliable
- Resolution is lower, can quantify spatial heterogeneity better
- Gustavson: "You get the same result every time - not subjective" - not sure this is true given ML

Brief mention of antibody-conjugated drugs (ADCs)
- 11 approved as of now, targeting various solid and hematological malignancies
- Need IHC/spatial to better understand targeting/effectiveness of ADCs

T-DXd is an AZ ADC
- Humanized anti-HER2 IgG1 mAb linked to topo 1 inhibitor and cleavable linker

T-DXd has robust effecacy against HER-2 low late model of BC
- Demonstrated in RCT that T-DXd improved response in patients compared to standard of care

Use validated IHC assay to categorize patients into IHC 1+, 2+, or 3+ which describes staining of HER2 on tumor cells in path sample
- HER2 low cancer means 1+ or 2+ designated patients
- Significant heterogeneity in IHC slides between patients within groupings

Developed "Quantitative Continuous Score" - QCS for ML-driven pathology scoring
- IHC slides are digitized and used as training data with manual path annotations
- Used neural net (almost certainlty a CNN) to train model - unclear what response/output here is
- Gustavson: "Won't go into detail on how we validated it" - no ROC or anything
- Transform staining intensity into "optical density"
- Two method developments as part of this technology:
  - ART -  automatically segment tumor from IHC image
  - SSTC - subcellular segmentation of tumor cell (identifying cellular membrane)

QCS scores as compared to path scoring into IHC +1, +2, +3 categories reveals that there is significant variation between groups (as based on optical density scores for single cells)
- Particularly, IHC +3 group has very broad QCS optical density scores

Retrospectively analyzed data from T-DXd trial and categorized HER2-low patients using QCS scoring
- Created QCS+ and QCS- groups and identified better/worse responding patients

Can analyze spatial heterogeneity in different ways - spatial proximity score
- % of HER2+ tumor cells in a local neighborhood
- Once again, retrospective analysis provides better cohort segmentation

Final note - can try to link computational pathology to mass spec for better target priortization and identifying protein signatures (potential biomarkers)



## Talk 1 - Quality-Control Methods In NGS Diagnostic Test Development

**Dr. James Willey, Univeristy of Toledo**

Co-founder of Accugenomics, Inc

Data from FDA-sponsered study of circulating tumor DNA (ctDNA)
- Why study? Can discover actionable (druggable) mutations specific to patients tumor
- Help track disease activity, potentially predict reoccurence

Spike in controls are used to improve QC in NGS analysis of ctDNA
- Called SNAQ-SEQ IS controls
- Full exon with actionable mutation +500 bp flank, dinucleotide changes made every 50 bp for bioinformatic separation
- idea is to mix controls in with ctDNA samples

ctDNA analyses are challenged by false negative results due to low levels, technical error, and flucuations in ratio of ctDNA to normal ctDNA

Can use standards to identify rate of sequencing errors, since sequences are standard to ref
- All differences from reference are errors

Study objective: identify guidelines for liquid biopsy (LBx) ctDNA testing:
- Reference materials include mix of DNA from 10 cell lines + normal control
- Determined ground truth set of 42K known positve and 10M known negative sites
- Generated test samples by mixing tumor-normal at 1:1, 1:5, and 1:25

Results:
- High precision + reliablity of VAF > 0.5%, becomes unreliable below that
- Performance degrades with limited starting material (< 25 ng)
- False negatives (missed mutations) more common than false positives
- Fragment depth is critical variable, deep coverage needed for detection of rare variants

Used SNAQ-SEQ internal standards in conjugation with Illumina TST170 ctDNA method:
- Align IS and test reads to different references, then call variants in both and use IS variant calls to normalize calls for test samples
- Methodology is unclear
- Allowed them to recover 13% of true positive mutations that were missed by Illumina due to low support
- SNAQ-SEQ only increases sensitivity for variants with VAF < 0.3%

Showed evidence that IS controls help control variation in ctDNA measurements
- Reduced CV to less than 25%

Methylation of ctDNA may be useful for diagnosis/monitoring of malignancies
- Performed study on GM24385 cell line to study improvements from adding IS
- Used bisulfite sequencing to detect methylation over samples with known % methlation at site (SOXA)
- Found that SNAQ-SEQ improved reliablity of methylation detection in ctDNA analysis (data lacking)

## Talk 2 - Discovering Next-Generation Biomarkers Through Integrating Single-Cell ‘Omics And Artificial Intelligence

**Sarah Carl, Scailyte**

Scailyte is a Swiss startup, ~6 years old

Biomarkers can help improve R&D productivity by helping improve clinical trial failure rates
- 90% of clinical trials fail, 50% of those to lack of effecacy

Use single cell data to power biomarker Discovery
- Advantages:
  - highly granular and sensitive, doesn't average across bulk tissues
  - Directly assess state of biologically-relevant primary patient samples
  - Get 1000s-10,000s of cells per sample (doesn't seem compelling)
- Disadvantages:
  - Data are noisy and vulnerable to batch effects
  - Patterns can be too complex to analyze manually

Use supervised representation learning model
- Patient-level annotations are used as input to model (i.e., responders/non-responders)
- Representation learning attempts to find a better representation of the original feature space
- So for scRNA-seq, idea is to find features other than the measured features (genes) to better separate patient labels

Claim that supervised RL is better than standard scRNA-seq analysis of unsupervised clustering -> manual cluster annotation -> compare clusters across outcomes
- Standard method is bad because:
  - Very dependent on inital clustering
  - Requires pre-existing knowledge to perform annotations
  - Reduces sensitivty to cell signatures that are shared across clusters
  - Dilutes single cell data to bulk (cluster-level)

For some reason - computational cost (?) - they train the NN on many subsamples of patient data
- Claim improves generalizability - probably true
- NN representation is fairly shallow, allowing for better explainability
  - this is a key feature - allows them to claim biomarker discovery by examining model weights

ScaiVision can be used in cell therapy development
- Donor selection for allogenic cell therapy
- Patient stratification for autologous cell therapy

Analyzed scRNA-seq data generated from CAR-T infusion products prior to dosing (external study)
- 24 patient cohort, labeled as high-grade or low-grade neurotoxicity
- Trained model on 70% split to identify biomarker profile that predicted groups
- Identified genes changing in CD8 and CD4 T cells that yields interesting looking GO enrichment
- Standard clustering approach used by external study authors claimed no difference between CD4s and CD8s and instead stratified patients based on presence or absence of rare cell type
  - Overall percentages of "signature-associated" cell pop found by ScaiVision was quite low (< 0.2%)

Used ScaiVision to perform biomarker discovery in a study of CTCL
- CTCL - cutaneous t cell lymphoma
- Used CyTOF data to get 3.5M cells with 36 protein markers
- Identified set of CD4 t cells specific to CTCL patients
- Reduced 36 marker description of pop to 9 marker panel that maintained sensitivty for diagnosing CTCL patients

Overall: Interesting technology and supervised RL could be useful for our single cell analyses
  - Unclear how much this would improve results from our current NMF-based approaches



## Talk 3 - PRCISR™: Vivlion’s CRISPR-Enabled Discovery Platform

**Martin Wegner, Vivlion GmbH**

CRISPR-based library screening platform

CRISPR consists of endonuclease (cutter) and small gRNA (sequence-specific guide) that introduces DSBs in known locations
- NHEJ-mediated repair of these DSBs creates indels, which shift the reading frame and break the gene, affecting functionality
- Can easily perform genome-wide screens by applying a set of guides to a collection of cells (1 guide/cell), then look for differences in treatment response based on gene KO
- Can perform synthetic lethality screens using WT and single-gene KO cell lines, identify potential genes that are synthetically lethal with existing KO
  - Use combinatorial CRISPR library where two KOs occur in each cell; avoids cell line effects from establishing KO line

Combinatorial CRISPR screening has many challenges
- Library setup can be complicated (size of guide, dsitribution, genes, controls)
- Cell line, assay, analysis plan all can vary

Talk will cover three main points:
- Library design
- Uniform sgRNA generation
- Scaling

Library design
- Offer both single and dual-target libraries
- Dual-target libraries can be set up to be all vs all, all vs many, or fixed combinations as requested by customer

Uniform representation of guide RNAs
- Some guides are generated more easily than others
- Measure uniform library dsitribution using ratio of 90th percentile to 10th percentile (so closer ratio is to 1 = more uniform)
- Important because distribution determines coverage available during screen
  - The more skewed a library is (less uniform), the more coverage is required to overcome bias
- Vivlion avoids this issue by avoiding PCR cloning (or restriction/ligation based cloning)
  - Instead, use template site-directed mutagenesis to bacterially amplify the final CRISPR library with gRNA sequences
- Showed data suggesting that single- or dual-target libraries from Vivlion increase KO rates for essential genes by > 10-fold

Scaling/Parallelization
- Typically large-scale screens require many rounds of PCR cloning
- Vivlion says their libraries allow for reducing size of screens by 10fold

_Question: How do you define guide RNAs for each gene?_
Wegner: We use guides from published work (so emperically validated) but also use synthetic design tools if needed (i.e., if they don't have a guide for that target in their database)

_Question: How many guides to use for each gene?_
Wegner: Use between 3-4 guides per gene or you can't guarantee KO



## Talk 4 - Panel Discussion: Novel Genome Editing Techniques & Their Applications

**Laralynne Przybyla, UCSF**

**Mara Pavel-Dinu, Stanford**

**Tirtha Chakraborty, Vor Biopharma**



_Question: How can we design screens for identifying new theraputic targets_

Przybyla: When we're trying to discover new targets, have to spend a lot of time setting up model system and assay correctly. Need to pay attention to what kind of readouts are being used and if they're relevant to the disease of interest.

_Question: What has been your experience in array screening (vs pool screening) for CRISPR?_

Przybyla: Scale is smaller for array-based screening.

_Question: How do you validate hits from initial screen?_

Przybyla: Again, follow the biology. For example, use large-scale pooled survival screen, then take hits and evaluate in array-based or single-cell-based assay in more targeted/relevant symbol.

_Question: Have you seen variation based on the source of iPSCs (batch effects)?_

Przybyla: Run multple cells from multple donors, do followups in multiple donors to avoid cell line specific biases

_Question: In your experience, do you use screening to find new targets?_

Pavel-Dinu: We want to develop broadly-applicable therapies, meaning we need to use much larger payloads (?). Too large payloads (>4.7 kb) reduces transduction efficiency as well as causing lethality in target cells.

_Question: What are the pros/cons of using DSBs vs nicks for CRISPR?_

Pavel-Dinu: Nick system is still new and has room for improvement; DSBs are more mature technology. Need DSBs to deliver large payloads, although some nick-based CRISPR systems exist for payload delivery. Have to balance risk/reward of therapy to determine which method is better - endpoint effectiveness?

_Question: What downstream work needs to be done to evalute screening targets?_

Chakraborty: We're focused on developing transplants using stem cell biology. We don't use CRISPR engineering for target discovery; we harness its strengths to build a theraputic. Most important part of target discovery comes from biological knowledge of targets - look for KOs that yield no biological phenotype (or otherwise KO data is contaminated by biology)

_Question: What approach works best for engineering cell lines for high-efficiency screening?_

Przybyla: We mostly use lenti insertation at safe harbor sites to ensure we generate productive cell lines with the correct mutations.

Chakraborty: We use electroporation to perform single gene mutations. We do ex-vivo insertions mostly so off-target is not an issue. Must be cautious making changes in primary sequence. Brought up imporatnce of considering heterogeneity when considering on/off-target interactions (i.e., is on-target liver? hepatocyte specifically?)

_Question: What is your system for controlling for off-target effects?_

Pavel-Dinu: When we develop therapies (for monogenic immune disorders), we must be very careful to not have off-target effects. High-fidelity Cas9 helps a lot, rarely find worrying off-target edits that would lead us to changing guide design. Need to watch out for translocation events with high homology targets (CCR5 vs CCR2 for example). Rarely use two guides to prevent generating two DSBs and subsequent translocations.



## Talk 5 - An Introduction to Automated Genomic Workflow Solutions

**Dr. Han Wei, Beckman-Coulter**

Agenda:
- Introduction to Beckman Coulter
- Collaboration & Grant Program
- Case study of FFPE vs cfDNA sample
- Upcominb automated workflow solution

Beckman Coulter makes many products that support life sciences research - specifically liquid handling (?)

Have matched FFPE and cell free DNA samples from patients
- circulating tumor DNA has been used for diagnostic purposes for liquid tumors (liquid biopsy)
  - Emergent product to complement standard biopsy assay
- FFPE slides are screened by pathologists for cancer biomarkers, often compared to matched control sample

Majority of source of cfDNA is from necrotic or apoptotic cells
- Generates wide variety of fragment sizes, but peak at 175 bp
- Can be detected in PBMCs, allowing for easy patient monitoring

DNA and RNA extracted from FFPE samples are degraded and often low quality
- Want method that provides complete digestion with gentle lysis step
- Beckman Coulter kit provides better RNA quality (higher >200 bp score)
- Takeaway: chemistry is key determinant of how much nucleic acid that can be later assayed.

For cfDNA, one of the largest challenges is starting materials
- Typically 1-15 ng is most you get
- Comparied BC kit to QIAGEN qiaamp circulating nucleic acid kit, showed better yields

Wanted to measure concordance between FFPE and cfDNA samples
- 8 pairs of matched samples, covering four cancer types
- Used 100 ng of DNA and used IDT Library Prep Kit + Pan Cancer Hyb Panel -> NextSeq
  - Got good coverage (>90% @ 50x)
- Identify common set of variants from both sample types
  - For SNVs, >95% are shared
  - For indels, variatns are more sample-type specific, particularly for breast cancer samples
- Used ClinVar to identify two variants in samples that were potentially pathogenic; most identified variants were not in ClinVar

Showed some data suggesting that BC's new automated cell-free extraction system is significantly faster than manual extraction.
- Upcoming end-to-end cell-free assay method claims "conversion" is better - leading to more library complexity
  - Unclear what "conversion" means in this context
- Uses IDT xGen cfDNA kit



## Talk 6 - Next-Generation CRISPR Screening Platforms For Insights Into Human Disease Biology

**Laralynne Przybyla, UCSF**



## Talk 7 - Nano Scale Multiomics Solution With Highly Accurate Single Cell Sorting And Isolation

**Dr. Andrea Ockhardt, Cellenion**



## Talk 8 - Enhancing Immune Profiling Through SingleCell Multiomics

**Devan Phillips, Genentech**

## Talk 9 - Single Cell Biology Made Simple

**Dr. Robert Meltzer, Fluent Biosciences**



## Talk 10 - SIMBA - Building Interpretable Regulatory Maps Using Graph-Embedding On Single-Cell Multiomics Data

**Luca Pinello, MGH**



## Talk 11 - Panel Discussion: Utilising Multiple Large Scale Single Cell Datasets

**Daniel Lu, Amgen**

**Luca Pinello, MGH**

**Dr. Lihua Julie Zhu, UMass Medical**

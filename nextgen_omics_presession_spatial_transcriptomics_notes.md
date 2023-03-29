# Spatial Transcriptomics Session

## Talk 1 - Advancing Bioimaging With DNA Probes
**Dr. Peng Yin, HMS**

_DNA paints_ - superres imaging similar to B. B. DNA painting.
Difference between STORM/PALM is that blinking of fluorophores is not externally driven, but autonomous
  No photobleaching
  Blinking behaviour is programmable, allows for 5 nm resolution and 10 color multiplexing
    With artificial grids, can achieve resolition of ~ 1 nm

Because intial fluorophores use docking strand and secondary amplification, can use orthogonal labeling to multiplex and assay multiple markers in superres

_DNA nanoscope_ - nanoimaging by sequencing
Uses nanopore sequencing to reconstruct single molecule spatial transcriptomics (scope-free)
  unlike DNA paints, no superres setup required

_DNA-Exchange_ - Uses DNA barcodes to label primary antibodies, then use fluorophores conjugated to barcodes and exchange rapidly (~ 5 min) to perform high throughput multiplexing
  Can be used in conjuction with confocal or superres
  There is no secondary antibody which helps with background issues, but decreases sensitivity

_SABER_ - Similar to DNA-exchnage, except you hit barcoded primary antiobody with long concatemer, allowing many many fluorophores to bind to the primary Ab, increasing sensitivity
  Incremental improvements in scaffolding synthesis methodology allows for signal amplifcation up to 20-30x
  Avoids multiple rounds of primary Ab staining
  Demonstrated multiplexed imaging of 29 proteins and 3 mRNA markers in brain tissue claiming 32-plex amplifcation
  Belibro tech!

_Light-Seq_ - Whole transcriptome spatial sequencing via light-directed DNA barcoding in tissue
  Allows for single-cell acquisition of transcriptome using light-sensitive cross-linking to introduce spatially-linked barcodes to RNA, which provides localization information
  Unclear how sequencing is performed as talk went to videos
  Further talk on this tech by Jocelyn Kishi (9 am, room 3, friday mar 31)

## Talk 2  - Panel Discussion: Moving Towards The Utilisation Of Spatial Technologies In The Clinic
**Dr. Peng Yin, HMS**

**Dr. Rana Chakraborty, Mayo Clinic**

**Espy Anguiano, Nanostring**

  Nanostring categorizes platforms into imagers and profilers:
  - Imagers - single cell
  - Profiler - multicellular

  Yin - DNA-based probes are both imaging and profiling based
    High-value applications of their technology - identifiying tissue-specific biomarkers in a clinical context
      All examples during Dr. Yin's talk were academic, research studies and no human data shown

  Chakraborty - exciting period for field, historically didnt have opportunity to analyze tissue in multidimensional space
    Allows us to answer questions regarding immune crosstalk
    Using Nanostring tech a lot in clinical profiling of tissues
    Moving into personalized medicine is dependent on personalized genomics
      Need spatial platforms to integrate proteomics/metabolomics
    "From single cell to single patient"


  Anguiano - Nanostring says most common application of their tech is immune profiling of patients to discover biomarkers
    Didn't specify tissue vs peripheral blood

### Q&A

  - _Question: What are limitations of the tech and what needs to be prioritized for development?_
    - Yin
      - Need scalable high-throughput assays to profile tissues in a deep fashion (100+ marker multiplex)
      - Cost of sequencing has plummeted - need similar changes for spatial tech
    - Chakraborty
      - Innovations drive up tech cost, especially for non-western healthcare systems
      - How does rest of world keep up? Need breakthroughs that drive cost downwards

  - _Question: How do you envision moving spatial txp into the clinical setting?_
    - Yin
      - Need to bring technology to both clinicians and pharma researchers, perhaps preclinical stage
      - Eventually compelling diagnostic use cases may emerge
      - Immunooncology space is major opportunity for spatial txp
    - Chakraborty
      - Science is a global space, so hopefully world-wide innovations will help bring down costs
      - Can't lose sight of bigger picture - patient care
      - Need forums to explain tech to clinicians and requires constant communication
      - Encourages groups to look past image analysis when extolling virtues of spatial transcriptomics (docs may not know what transcriptome is)

  - _Question: Can we use formalin-fixed tissue + does DNA paint work with all Ab?_

    - Yin - technology is modular and should be compatible with any Ab and any tissue, in practice have been able to use commercially-available Abs

  - _Question: Using tissue imaging for gene therapy - challenges and concerns_

    - Anguiano - Nanostring could be used to detect successful expression of a transgene as it is sequence-agnostic; for cell therapy, would need specific biomarkers. Emphasizes flexibility of Nanostrings tech for assaying localization + expression for both dosage and on/off-target simultaneously

  - _Question: How sensitive are spatial txp to low-expressed transcripts_

    - Yin - Depends on sequencing depth (for his tech), comparable to scRNA-seq Technologies

    - Anguiano - Nanostring whole transcriptome amplification has large dynamic range; sensitivty can be adjusted by including more cells (i.e., if you knowq specific populations express gene of interest, enrich for that pop)

  - _Question: How to we categorize unbiased (discovery) approaches vs targeted approaches for spatial txp_

    - Chakraborty - If you identify biomarkers/new pathways using orthogonal method, could then use spatial txp to identify that biomarker in patient samples. Can evaluate expression in given cell types of biomarker, which can subsequently guide targeting decisions (siRNA vs mAbs vs small molecule). Overall, can help with targeting decisions

    - Anguiano - One of the benefits of spatial whole txp allows to understand both molecular and celluar programs that may be distinct to patient subpopulations and thus guide theraputic hypothesis generation (i.e., spatial txp -> better market segmentation). Also very successful in demonstrating/validating expression of markers of response to theraputic treatment, can be easily validated (DNAscope)

## Talk 3 - Characterizing CytoMegalo Virus In Placental Tissue
**Dr. Rana Chakraborty, Mayo Clinic**

Topic: Characterizing the placental proteome during congenital CMV infection

Chakraborty: "Want to give real-world perspective on using this tech in the clinic"

### Background

Epidemiology of CMV - ubiquitious virus, affects 90%+ of women in developing countries, ~50% in western world
Most infections are sublinical, prevelance estimated between 83%-100%
Similar to HSV, CMV establishes lifelong latency following primary infections, trophic for stem cells
In utero infection can occur in both naive women and those who acquire an unfamilar strain during pregancy (also, can get reactivation of latent virus during pregancy)

Congenital CMV infection is most common worldwide, 0.4-2.3% of newborns affected

Spectrum of severity for congenital infections
  Children can be born asymptomatic
  Associated with hearing loss (responsible for ~25% of all congenital hearing loss)
  10-20% have severe manifestations
    - microencephaly
    - chorioretinitis
    - developmental delay

### Placenta

Placental-fetal interface remains poorly characterized - very understudied. Lab specifically looks at effects of maternal infection on fetus.
Constant contact between maternal decidua (cell type) and invading fetal chorionic villi.
  Allows for maternal to fetal blood supply to be established
  Fetal-placental mixing occurs in intervillous space
  Barrier contains trophoblasts and maternal macrophages, no B and T cells

CMV infection of placenta - can infect wide variety of cells (endothelial, epithelial, myeloid, hofbauer cells/placental macrophages).
Infection can lead to distinct innate response, IFNg + IP-10 production
Chronic villitis and trophoblast damage are noted in CMV infection of placenta

Initial CMV infection is thought to be mediated by FcRN-mediated transcytosis of villous cytotrophoblasts

CMV infection upregulates activation markers on placental macrophages; also increases CCR5 expression on macs + bystander cells
  These cells also secrete inflammatory markers (IL-10)
CMV infection causes downregulation of STAT2 and disruption of Type 1 IFN response in infected cells

### Study and Prelim Results

Main hypothesis: CMV-induced activation + apoptosis is associated with trophoblast damage

Cohort: 5 CMV-affected and 4 CMV-unaffected pregnancies

Used Nanostring GeoMx DSP to perform spatial transcriptomic profiling on placental tissue samples
  Stain FFPE-slides with oligo-conjugated Abs, select region of interest (in spatial space) -> cleave barcodes and quantify digitally
  Allows for (small region) spatially resolved transcriptomics

Identified CD45+ cells (and cytotrophoblasts via CK7) and profiled using GeoMx
 Studied four specific ROIs based on interface betwen CD45+ and CK7+ cells

Unsupervised clustering showed that CMV-infected immune cells have distinct proteomic signature:
    HLA-DR, GZMB, other markers of T cell activation

Differential protein expression analysis identified genes like immune cell markers (CD8, KI67, CD3) and markers of cell death (BIM, BCLXL, PARP, Neurofibromin) associated with CMV-positive tissue immune cells

Didn't identify as obvious + broad changes in cytotrophoblasts vs immune cells

Tentative conclusions:
  - CMV-infected plancetal tissues show proteomic changes associated with cell death + immune activation
  - Want to use this data to screen newborns for biomarkers/pathways associated with these data.
  - Specific to distal villi compartment so unclear how broadly applicable results are
  - Next steps would be to determine if CTBs are coming from maternal or fetal side
  - Long-term, identify infants with congential CMV and apply antiviral drugs early

### Q&A

- _Question: Is CMV infection associated with development of autoimmunity?_

  - Audience member noted that many of the markers associated with activation of T cells are similar to what is seen in autoimmunity. Chakraborty said that based on ZA collaboration on patients with congential HIV infection suggests infants demonstrate signs of having exhausted T cells. Belives that inflammatory effects could easily have deleterious effects on post-natal newborns but data is preliminary

- _Question: How similar were the placentas in terms of gestational age?_

  - Chakraborty: CMV-infected placentas were 36-38 weeks (as infection is associated with pre-term delivery) while control samples were a little later (40+ weeks).


## Talk 4 - Nanostring Spatial Platforms
**Eric Miller, Nanostring**

**Espy Anguiano, Nanostring**

### Let's Get Spatial Q&A Session

Nanostring has been around since 2003, 2008 when nCounter came online.

Now offer three platforms:
  - nCounter (bulk targeted gene expression analysis)
  - GeoMx Digital Spatial Profiler (tissue spatial proteomics)
    - Uses photocleavable linkers to sequence Ab-linked barcodes with localization
  - CosMx Spatial Molecular Imager (tissue spatial transcriptomics)

GeoMx can only obtain whole transcriptome data for very small spatial areas; CosMx provides _less-than_ whole transcriptomic evidence for larger areas (?)

CosMx - 6000 transcripts/50-60 proteins; 2-20 samples/wk

GeoMx - 20,000 transcripts/150+ proteins; 60 samples/wk

#### GeoMx

  GeoMx use case - you have an idea of the physical region of interest, want to acquire gene expression/protein expression data on cells _in that small area_
    Works with ffpe, fresh frozen, whole mount, tma samples
  Protein panels available: immune cell, neural cell
  Gene panels: 18,000 human genes, 22,000 mouse genes
  Custom assays available (including spike-in controls)

  Differs Nanostring GeoMx from "array-based" technologies for use case where you are certain a given interface/margin is more important than other areas.
    Avoids dropout/averaging issues from capturing entire slide (?)
    Miller: "Similar to localized IHC"

  Can define different "regions of interest" for spatial profiling
    Geometric filters, grids, and actual cell segmentation options
    ROIs can be drawn by hand as well, although they claim automation based on markers is "very possible"

  Claims that although ROIs are not single cell, resolution is 1 um, allowing you to get close to single cell

  In example, you can identify melanocytes in slide by segmentation based on marker expression, then quantify whole transcriptome from that _bulk_ population (i.e., wash off Abs and count transcripts with that localization-affected barcode)

  Example, used GeoMx to profile pancreas cells and identified a and B islets, then quantified txp from those pops and showed that Insulin and Glucagon expression is associated correctly

  Cool example of using scRNA-seq data of clustered cell types to power GeoMx to subcluster whole trancriptome profiles (but its still bulk profiles)

  Over 200 peer-reviewed pubs with GeoMx

#### CosMx

  Claim: unbiased single cell spatial analysis of whole tissue sections
  Showed from on 1.4m single cells with localization information from lymph node FFPE sections

  Library size is limited to 1000 genes (they say 1000-plex?)
  Can use FFPE, fresh frozen, TMA and organoids
  Multiomic profiles possible - i.e., protein/mRNA co-profiling
    Mentioned protein expression is highly helpful for segmentation
  Localizes with 50 nm resolution

  System just launched so panels are limited:
  - 1000 gene panels for Human universal, neuroscience and immunoncology:
    - 250 genes for cell typing (full expression profiles are used for cell type annotation)
    - 500 for cell state/function
    - 200 genes for cell-cell interaction (receptor/ligand pairs)
    - 50 genes for hormone activities

  - Claim their 1000 gene panel is 4x what is available from competitors
      - Can customize with 50 additional targets

  - 64 marker protein panel available for human

  Cell segmentation is ML-based, uses Z-stacks and nuclear + cytoplasmic markers to perform. Backbone is called CellPose, but changed in proprietary ways:
  - Not geometry based
  - Segmentation performs well across different cell types

  First publication using CosMx is in Nat Biotech, 2020
  - ~750K cells, ~250 transcript/cell
  - Can handle low quality RNA, all samples shown had RIN < 3

  Claim automation is straightforward for high-throughput applications

  More recent liver cancer dataset achieves ~ 450K cells at ~1150 transcript/cell -> 218 genes detected/cell
  - Capture ~676 genes above LOD (so ~ 67.6% of panel is recoverable)

  New 6000 transcript panel is coming soon (estimated Q1 2024)
  - Claim ~5500 unqiue genes detected
  - Claim 119 proteins - potentially powers better segmentation (?)

  Interesting use case: performing co-expression analysis of signaling molecules + ligands to identify _spatially_ organized clusters of cell-cell interactions

  - Can then associate cell type interface abundance with clinical outcomes

## Talk 5 - Nanostring Customer Presentations


### Spatial Transcriptomics Profiling Of COVID-19 Lungs And Pancreatic Ductal Adenocarcinoma
**Dr. Martin Hemberg, BWH**

Topic: Identifiying molecular drivers of alveolar damage in COVID-19 patients and identifying novel theraputic targets for pancreatic ductal adenomas with spatial Transcriptomics

Two different projects that Nanostring asked him to talk about (COVID-19/pancreatic cancer)

**Profiling molecular drivers of alveolar damage in COVID-19**

COVID-19 is a multisystemic virus, but mainly respiratory disease that affects lungs.
Better understanding of disease progression could help prediction and guide treatment.

SARS CoV2 binds to ACE2 receptor on alvelor cells - subsequent progression is less well understood
Previous spatial analysis work idetnified changes in mesenchymal cells and fibroblasts in lung for COVID patients
  Tracks with fibrosis and inflammtory respiratory symptoms in disease

Used GeoMx platform - labels small tissue region/"cell types" with whole transcriptome

Cohort: 30 COVID-19 autopsy lung tissue and donor lung tissue from non-healthy controls (n=?), samples were FFPE. All from UK and processed uniformly.
  - Each spatial sample was manually annotated by pathologist for damage state based on alveolar morphology (four states with increasing damage)

Used sc/snRNA-seq data separately alongside Nanostring profiling
  - single cell data used to drive cell type annotation from GeoMx
  - Many public scRNA-seq datasets on COVID-19 vs healthy were available, but integration was problematic
  - Ended up with 600K cell reference with fairly balanced contributions from studies without too much batch variability (by UMAP)

Annotated lung cell types + broad immune cell types, then used sc references to yield final set of ~70 fine-grained cell types

Differential abundance (in scRNA-seq or Nanostring? unclear) analysis identified enrichment of immune cells in COVID-19

Also performed cell-cell interaction analysis on both dissociated scRNA-seq and spatially organized transcriptomes from Nanostring
  - Identify condition-specific pathway enrichment

Asked if spatial data would be able to resolve damage states as assesed by histopathology
  - Used random forest classification to identify gene sets associated with outcome
  - Prediction accuracy (dont know what number this is) was 0.73 using top 1000 HVGs, drops to 0.67 using only surface markers and 0.69 using secreted markers
  - From looking at data, markers are more associated with a single stage vs others as opposed to defined sets for all four stages

Followup analyses focus on EDAD vs ODAD (different alveolar damage categories) - identify many pathways that are potentially interesting -> investigated dysregulation of coagulation
  - Downregulation of SERPINE1 leads to fibrinolysis and coagulation - from previous COVID work
  - Confirm same change in COVID samples  

Interesting - abundance estimates from scRNA-seq deconvolution vs Nanostring tissue are consistent but differ significantly
  - Based on regions of interest sampled, cell type abundance differences between damage categories are very minimal compared to COVID vs control

Extend this type of analysis to identify a set of "cell states" - i.e., gene expression profiles that are associated with earlier stages of COVID disease

Went on to use NMF to associate Nanostring Region of Interests with cell types via NMF factorization
  - They call factors "niches" and attempt to identify which subcomponents of the _SPP1_ pathway (identified as COVID relevant orthogonally) are associated with which cell types

Concusions:
  - Profiled 33 donors using Nanostring GeoMx
  - Histopathology allowed for investigation of cell type abundance during disease progression
  - Identified dysregulated coagulation pathway
  - Identified _SPP1_ macrophages as potentially key driving population in early COVID-19 damage

**Talk 2: pancreatic ductal adenomas**

Overview:

Cohort:

Conclusions:




### Utility Of High-Plex Spatial Biology Approaches To Drug Development
**Dr. Edgardo Parrilla Castellar, Q2 Solutions**

Q2 solutions is CRO based out of North Carolina


### AtoMtx Presentation

  Cloud platform for spatial transcriptomics, similar to Tercen and other "walled garden" all-in-one analysis suites.

  Seems useful for companies without computational biology analysts, but not sure of utility for us.

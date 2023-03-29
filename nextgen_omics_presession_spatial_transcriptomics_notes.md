# Spatial Transcriptomics Session

## Talk 1 - Advancing Bioimaging With DNA Probes
**Dr. Peng Yin, HMS**

- _DNA paints_ - superres imaging similar to B. B. DNA painting.
Difference between STORM/PALM is that blinking of fluorophores is not external, but autonomous
  No photobleaching
  Blinking behaviour is programmable, allows for 5 nm resolution and 10 color multiplexing
    With artificial grids, can achieve resolition of ~ 1 nm

Because intial fluorophores use docking strand and secondary amplification, can use orthogonal labeling to multiplex and assay multiple markers in superres

- _DNA nanoscope_ - nanoimaging by sequencing
Uses nanopore sequencing to reconstruct single molecule spatial transcriptomics (scope-free)
  unlike DNA paints, no superres setup required

- _DNA-Exchange_ - Uses DNA barcodes to label primary antibodies, then use fluorophores conjugated to barcodes and exchange rapidly (~ 5 min) to perform high throughput multiplexing
  Can be used in conjuction with confocal or superres
  There is no secondary antibody which helps with background issues, but decreases sensitivity

- _SABER_ - Similar to DNA-exchnage, except you hit barcoded primary antiobody with long concatemer, allowing many many fluorophores to bind to the primary Ab, increasing sensitivity
  Incremental improvements in scaffolding synthesis methodology allows for signal amplifcation up to 20-30x
  Avoids multiple rounds of primary Ab staining
  Demonstrated multiplexed imaging of 29 proteins and 3 mRNA markers in brain tissue claiming 32-plex amplifcation

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

Used Nanostring GeoMix DSP to perform spatial transcriptomic profiling on placental tissue samples
  Stain FFPE-slides with oligo-conjugated Abs, select region of interest (in spatial space) -> cleave barcodes and quantify digitally
  Allows for (small region) spatially resolved transcriptomics

Identified CD45+ cells (and cytotrophoblasts via CK7) and profiled using GeoMix
 Studied four specific ROIs based on interface betwen CD45+ and CK7+ cells

Unsupervised clustering showed that CMV-infected immune cells have distinct proteomic signature:
    HLA-DR, GZMB, other markers of T cell activation

Differential protein expression analysis identified genes like immune cell markers (CD8, KI67, CD3) and markers of cell death (BIM, BCLXL, PARP, Neurofibromin) associated with CMV-positive tissue immune cells

Didn't identify as obvious + broad changes in cytotrophoblasts vs immune cells

Tentative conclusions:
  - CMV-infected plancetal tissues show proteomic changes associated with cell death + immune activation
  - Want to use this data to screen newborns for biomarkers/pathways associated with these data.
  - Specific to distal villi compartment so unclear how broadly applicable results are

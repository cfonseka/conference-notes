# Spatial Transcriptomics Session

## Talk 1 - Advancing Bioimaging With DNA Probes
**Dr. Peng Yin, HMS**

_DNA paints_ - superres imaging similar to B. B. DNA painting.
Difference between STORM/PALM is that blinking of fluorophores is not external, but autonomous
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

_Light-Seq_ - Whole transcriptome spatial sequencing via light-directed DNA barcoding in tissue
  Allows for single-cell acquisition of transcriptome using light-sensitive cross-linking to introduce spatially-linked barcodes to RNA, which provides localization information
  Unclear how sequencing is performed as talk went to videos
  Further talk on this tech by Jocelyn Kishi (9 am, room 3, friday mar 31)

## Talk 2  - Panel Discussion: Moving Towards The Utilisation Of Spatial Technologies In The Clinic
**Dr. Peng Yin, HMS**
**Dr. Rana Chakraborty, Mayo Clinic**
**Espy Anguiano, Nanostring**

  Nanostring categorizes platforms into imagers and profilers
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

  _What are limitations of the tech and what needs to be prioritized for development?_
    Yin
      - Need scalable high-throughput assays to profile tissues in a deep fashion (100+ marker multiplex)
      - Cost of sequencing has plummeted - need similar changes for spatial tech
    Chakraborty
      - Innovations drive up tech cost, especially for non-western healthcare systems
      - How does rest of world keep up? Need breakthroughs that drive cost downwards

  _How do you envision moving spatial txp into the clinical setting?_
    Yin
      - Need to bring technology to both clinicians and pharma researchers, perhaps preclinical stage
      - Eventually compelling diagnostic use cases may emerge
      - Immunooncology space is major opportunity for spatial txp
    Chakraborty
      - Science is a global space, so hopefully world-wide innovations will help bring down costs
      - Can't lose sight of bigger picture - patient care
      - Need forums to explain tech to clinicians and requires constant communication
      - Encourages groups to look past image analysis when extolling virtues of spatial transcriptomics (docs may not know what transcriptome is)

  _Question: Can we use formalin-fixed tissue + does DNA paint work with all Ab?_
      Yin - technology is modular and should be compatible with any Ab and any tissue, in practice have been able to use commercially-available Abs

  _Question: Using tissue imaging for gene therapy - challenges and concerns_
      Anguiano - Nanostring could be used to detect successful expression of a transgene as it is sequence-agnostic; for cell therapy, would need specific biomarkers. Emphasizes flexibility of Nanostrings tech for assaying localization + expression for both dosage and on/off-target simultaneously

  _Question: How sensitive are spatial txp to low-expressed transcripts_
    Yin - Depends on sequencing depth (for his tech), comparable to scRNA-seq Technologies

    Anguiano - Nanostring whole transcriptome amplification has large dynamic range; sensitivty can be adjusted by including more cells (i.e., if you knowq specific populations express gene of interest, enrich for that pop)

  _Question: How to we categorize unbiased (discovery) approaches vs targeted approaches for spatial txp_
    Chakraborty - If you identify biomarkers/new pathways using orthogonal method, could then use spatial txp to identify that biomarker in patient samples. Can evaluate expression in given cell types of biomarker, which can subsequently guide targeting decisions (siRNA vs mAbs vs small molecule). Overall, can help with targeting decisions

    Anguiano - One of the benefits of spatial whole txp allows to understand both molecular and celluar programs that may be distinct to patient subpopulations and thus guide theraputic hypothesis generation (i.e., spatial txp -> better market segmentation). Also very successful in demonstrating/validating expression of markers of response to theraputic treatment, can be easily validated (DNAscope)

  ## Talk 3 - Characterizing CytoMegalo Virus In Placental Tissue
  **Dr. Rana Chakraborty, Mayo Clinic**

  

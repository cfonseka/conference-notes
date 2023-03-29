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
    Imagers - single cell
    Profiler - multicellular

  Yin - DNA-based probes are both imaging and profiling based
    High-value applications of their technology - identifiying tissue-specific biomarkers in a clinical context
      All examples during Dr. Yin's talk were academic, research studies and no human data shown

  Chakrborty - exciting period for field, historically didnt have opportunity to analyze tissue in multidimensional space
    Allows us to answer questions regarding immune crosstalk
    Using Nanostring tech a lot in clinical profiling of tissues
    Moving into personalized medicine is dependent on personalized genomics
      Need spatial platforms to integrate proteomics/metabolomics
    "From single cell to single patient"


  Anguiano - Nanostring says most common application of their tech is immune profiling of patients to discover biomarkers
    Didn't specify tissue vs peripheral blood

  What are limitations of the tech and what needs to be prioritized for development?
    Yin - Need scalable high-throughput assays to profile tissues in a deep fashion (100+ marker multiplex)
    Cost of sequencing has plummeted - need similar changes for spatial tech

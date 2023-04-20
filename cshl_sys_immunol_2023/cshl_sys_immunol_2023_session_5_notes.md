# CSHL Systems Immunology 2023 - Session 5

**Engineered Cells and Systems**
*Thursday, 20 April*

## Modeling adaptive immunity using lymph nodes and microfluidics

**Rebecca Pompano, UVA**

Consider immune system from perspective of spatial organization
- Specifically, dyanmics - how do cells and molecules move and flow

Trying to predict immune function in complex settings (like post-vaccination)
- For example, vaccine challenge involves arm injection -> drains to lymph node -> APC to T cell interaction

Trying to use organiods and 3D cultures to give both experimental control while replicating complexity of _in vivo_ models
- Trying to both build organs (lymph node) on chip but also section tissue and keep alive _ex vivo_ allowing for better experimental control

Two experimental designs for exploring adaptive immunity
- Top down: lymph node explants
- Bottom up: microphysiological models
- Also developing assays that allow for spatially resolved readouts

Eventual goal: couple model of lymph nodes to models of other organs to eventually be able to predict multi-organ immune responses

Have created live ex-vivo lymph node slices
- Can label known cell types, can add drugs, allows for cell migration (T cells tend to reside in lymph node only for a day)
- Drawback - can't stain with markers that might activate lymph (so CD3...)
- Lymph node slices are capable of responding to ex vivo antigen challenges

Developing new version of assay to measure oxygen consumption (involves detector layer lying underneath slide)
- Showed data of T cell zones in lymph node slices taking ip O2 faster than B cell zones

Used microfluidic chips to assay local drug delivery to lymph node slices
- Use port to distribute drug to center of slice and observe changes if drug is directed at T cell zone vs B cell follicles
- Can also measure diffusion effects and model by using visual information (spread of stain after delivery)

Want to study responses to vaccination, built system to co-culture lymph node slices with cultures of other tissues (on chip) with shared media, allowing for crosstalk
- Cocultured lymph node slice with either healthy tissue or tumor (murine) for 24 hours, then remove lymph node from chip and stimulated with aCD3
  - Found that tumor co-culture suppressed secretion of IFNg in response to stimulus
- System can be used to mimic draining of immune cells in other tissue to lymph

Overall: Interesting work, but unclear how much results would translate out of this experimental system. Also mentioned lymph slices can be highly heterogenous depending on what gets included in slice

## Synthetic cytokine circuits drive targeted infiltration and proliferation of T cells in immune-excluded tumors

**Greg Allen, UCSF**

Lab focus: synthetic immunology can allow us to understand biological systems
- Engineer cells, place them in a tumor microenvironment, and see what happens

Want to move CAR-T cell therapy away from using CARs to using synthetic notch receptors, in which the extracelullar side has an scFv to the target and the intracellular side that has an engineered TF that can turn on any output

CAR-T cells have worked well against liquid biopsy, but fail 90% of the time against solid tumors
- Solid tumors have evolved to escape the adaptive immune system

Goal: engineer cells to make their own cytokines (IL-2)
- IL-2 is strong promoter of T-cell activation/proliferation/differentiation
- Instead of giving IL-2 systemically, engineer T cells to recognize tumor antigen (targeted CD19 in exp) which will then use notch receptor to turn on synthetic IL-2 production
  - Idea is that cells producing IL-2 will then take it up and proliferate, causing a positive feedback loop that is spatially controlled by the tumor antigen

In murine model, tested CAR-T and CAR-T + synthetic IL-2 edit for ability to clear orthotopic pancreatic cancers
- Found that tumor volume dropped dramatically and survival went to 100%
- Claim: unlike systemic dosage of IL-2, much safer and unlikely to cause systemic effects

Microscopy revealed that IL-2 circuit helps tumors to infiltrate solid tumor (which just CAR T cells are unable to do)
- Claim: Only affecting T cell function based on CyTOF data (not shown)
- Both CAR and native T cells expanded, but naive cells don't appear to be activated and instead appear to take on a naive phenotype
  - Hypothesis: are these antigen inert cells playing a "sink" role to take up IL-2 and tamp down on feedback without secreting IFNg

Claim: because IL-2 is under synthetic control, avoids suppressive effects from normal regulation

Able to differentiate between paracrine or autocrine dependence for IL-2 production by either testing CAR + syn in a single cell vs in different cells
- Found that paracrine setup led to T cell recruitment but no T cell cytotoxcity in immune-healthy mice; conversely, it worked in immune-compromised mice which backs up idea that native cells serve as sink

Takeaways: IL-2 production must be inducible/tumor-triggered, orthogonal to native pathways, occur in an autocrine fashion, and selectively self-signal

Overall: Really cool idea to use synthetic receptors to control gene expression and particularly interested that IL-2 of all molecules has such a strong effect; just not clear how to translate these findings to our work

## Engineering RNA export for measurement and control of living cells

**Felix Horns, CIT**

Focus: engineering cells to export RNA to help measure the dynamic states of immune cells
- Current methods tend to provide "snapshots"

RNA allows us to read and write cell states - however, current RNA analysis methods -destroy cells
- Similarly, RNA has theraputic potential, but difficult to target properly

RNA export systems initially reverse-engineered RNA virus by expressing capsid to produce virus-like particles and developing Gag-MCP system that has binding sites for cognate signaling molecule (tag that allows for selective export of cargo)
- Showed data that this system is sufficient for exporting the cargo RNA into the supernatant - imporantly, only cargo and not untagged mRNAs

Revised system moved away from viral-like particles and to engineered protein nanocages
- Nanocages are made up of engineered proteins that self-assemble
- Nanocages can be tagged for export and will be exported via extracellular vesciles
- Nanocage design is large enough for RNa export

Interestingly, both VLP or nanocage system are protected from degradation by RNase (unless detergent is used to disrupt vesicles)

Proof of concept experiment: Cell labeling by exporting and sequencing RNA barcodes
- Had to do some engineering but as able to insert exportable barcode into cells
- Thus, can monitor growth and death of different clones in non-destructive fashion (by sequencing what ends up in the supernatant)
- Did this experiment on selective media and monitored population dynamics

Takeaway: non-destructive monitoring of cell population dynamics

Showed data where they added a fusogen (viral method of entry) to vesicle by co-expressing it with other delivery components
- System had CRE as cargo, allowing for visualization of RFP in reportor cells if CRE is properly exported and imported
  - Saw efficiency rates of 50%

Overall: Highly-engineered system that has potential research use (and the fusogen angle is obviously a therapeutic modality of interest for many groups) but it's too far from biology for our purposes

## Regulatory T cell subsets in autoimmunity, immune organoids, and analyzing T cell responses at scale

**Mark Davis, Stanford**

## Antibody-lectin chimeras for glyco-immune checkpoint blockade

**Jessica Stark, Stanford**

## A lymph node slice culture model to characterize T cell activation dynamics and anti-viral responses in human tissue

**Alex George, Columbia**

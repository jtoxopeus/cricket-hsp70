# cricket-hsp70

These data files and code are associated with the scientific article 
"HSP70 is upregulated after heat but not freezing stress in the freeze-tolerant cricket Gryllus veletis."<br>
This material is under the same copyright protections as the article itself.

# RCode file
The code can be run in R v4.4.1, and was used to conduct statistical analysis and generate the manuscript figures from the data files below. (Recommendation: use RStudio for easier visualization of figures.)


# Data files
These are used for statistical analysis and figure generation in the RCode file.

## Hsp70 heat shock survival.csv

We exposed groups of 12 crickets to the indicated high temperatures for 2 h and measured survival post-heat shock.
Each row pertains to a different group of crickets, with information provided for each variable (column heading), as described below.

VARIABLE:                  DESCRIPTION <br>
#Temperature:              Temperature (in °C) of the 2 h heat shock<br>
#Alive:                    Number of crickets that were alive 48 h post-heat shock<br>
#Dead:                     Number of crickets that were dead 48 h post-heat shock<br>
#Palive:                   Proportion of crickets that were alive 48 h post-heat shock<br>
#SEP:                      Standard error of proportion of living crickets<br>

## qPCRdata_forR.csv

Relative abundance of HSP70 mRNA was determined via RT-qPCR in tissues from crickets exposed to heat shock, fall-like acclimation, or freezing stress and compared to unstressed controls. See Figure 1 in the manuscript for full experimental design.
Each row pertains to one biological replicate (pool of tissue from 3 crickets exposed to the same conditions), with information provided for each variable (column heading), as described below.

VARIABLE:                  DESCRIPTION <br>
#Tissue:                   Type of tissue (FB, fat body; MT, Malpighian tubules; MG, midgut; M, muscle; NT, nervous tissue)<br>
#Expt:                     Whether crickets were part of the Heat, Acclimation, or Freezing experiment<br>
#Treatment:                Treatment the crickets experienced within the experiment. For the Heat experiment, these included never stressed controls (HSCtrl), and crickets that were heat shocked for 2 h at 40°C and allowed to recover for 2 h (HSR2) or 24 h (HSR24). For the Acclimation experiment, crickets were exposed to 0 (WK0), 3 (WK3), or 6 (WK6) weeks of fall-like acclimation, with the WKO serving as controls. For the Freezing experiment, acclimated crickets were either never stressed controls (FSCtrl), or frozen at -8°C for 1.5 h and allowed to recover for 2 h (FSR2) or 24 h (FSR24).<br>
#Sample ID:                Unique identifier for each sample (biological replicate)<br>
#rpl18 Cq:                 Cq (also know as Ct) value for the reference gene, rpl18<br>
#hsp70 Cq:                 Cq (also know as Ct) value for the target gene, hsp70<br>
#DeltaCq:                  Difference in Cq values between target and reference gene (hsp70 - rpl18)<br>
#meanCtrlDeltaCq:          Mean (average) DeltaCq value for control samples of each tissue within an experiment (i.e., the HSCtrl, WK0, or FSCtrl)<br>
#DeltaDeltaCq:             Difference in DeltaCq values between each sample and the relevant mean Delta Cq value for control samples (DeltaCq - meanCtrlDeltaCq)<br>
#FoldChange:               Abundance of HSP70 mRNA in each sample relative to the control for that tissue and experiment (2^-DeltaDeltaCq)<br>

## Western_data_forR.csv

Relative abundance of HSP70 protein was determined via semi-quantitative Western blotting in tissues from crickets exposed to heat shock, fall-like acclimation, or freezing stress and compared to unstressed controls. See Figure 1 in the manuscript for full experimental design.
Each row pertains to one biological replicate (pool of tissue from 3 crickets exposed to the same conditions), with information provided for each variable (column heading), as described below.

VARIABLE:                  DESCRIPTION <br>
#Tissue:                   Type of tissue (FB, fat body; MT, Malpighian tubules; Mg, midgut; M, muscle; NS, nervous tissue)<br>
#Expt:                     Whether crickets were part of the Heat, Acclimation, or Freezing experiment<br>
#Treatment:                Treatment the crickets experienced within the experiment. For the Heat experiment, these included never stressed controls (HSC), and crickets that were heat shocked for 2 h at 40°C and allowed to recover for 2 h (HS2) or 24 h (HS24). For the Acclimation experiment, crickets were exposed to 0 (0Wk) or 6 (6Wk) weeks of fall-like acclimation, with the 0Wk serving as controls. For the Freezing experiment, acclimated crickets were either never stressed controls (CSC), or frozen at -8°C for 1.5 h and allowed to recover for 2 h (CS2) or 24 h (CS24).<br>
#Sample ID:                Unique identifier for each sample (biological replicate)<br>
#Blot ID:                  Identification number assigned to the blot (and gel) from which protein abundance was quantified for each sample. Relative protein abundance of each sample was calculated compared to control samples from the same gel/blot.<br>
#Lane:                     Lane number for that sample on the gel (lane 1 was always a molecular weight marker)<br>
#[Protein] (ug):           Mass of protein in micrograms loaded into the SDS-PAGE well<br>
#Ponceau IntegratedDensity: A measure of total protein abundance in each lane based on Ponceau staining of blots<br>
#HSP-RelativeDensity:      A measure of HSP70 protein abundance in each lane based on immunostaining of blots<br>
#HSP Ratio:                Ratio of HSP-Relative Density to Ponceau IntegratedDensity, correcting for any changes in HSP protein abundance that may be due to overall increases or decreases in total protein abundance<br>
#ControlAverage:           Mean (average) HSP70 Ratio for control samples of each tissue within a blot<br>
#foldChange:               Abundance of HSP70 protein in each sample relative to the control for that tissue and experiment (HSP Ratio/ControlAverage)<br>

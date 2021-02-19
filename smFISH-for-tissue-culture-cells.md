---
layout: protocols
title: smFISH for tissue culture cells
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2021-02-19
---


### 1. Sample fixation and permeabilization

- Culture cells in 8-well ibidi chamber ([ibidi #80826](https://ibidi.com/chambered-coverslips/13--slide-8-well-ibitreat.html) or [#80827](https://ibidi.com/glass-bottom/183--slide-8-well-glass-bottom.html)) at ~30,000 cells per well density if aiming for sub-confluency.

  - It is convenient to use an 8-well chamber for parallel processing multiple conditions. However, the protocol can be easily adapted to other culture formats as well.
  - Each well has ~1 cm<sup>2</sup> growth area and typically 100% confluence is equivalent to ~130,000 cells.


- Before sample processing, make fixative (4% PFA in 1× PBS):

  | Stock | for 1 mL | for 10 mL |
  |:---|---:|---:|
  | Water	| 650 µL | 6.5 mL |
  | [16% PFA](https://www.emsdiasum.com/microscopy/products/chemicals/paraformaldehyde.aspx) (EMS, 15170) | 250 µL | 2.5 mL |
  | [10× PBS](https://www.fishersci.com/shop/products/lonza-accugene-pbs-10x-pbs-1l/bma51226) (e.g., Lonza, 51226) | 100 µL | 1 mL |

- Aspirate growth medium. Rinse each well with 250 µL PBS.

- Add 250 µL of fixative and incubate at room temperature for 15 minutes with gentle rocking.

- During fixation, make enough 70% (vol./vol.) ethanol (250 µL per well). Cool it in the fridge or on ice.

- Rinse each well twice with 250 µL PBS.

- To permeabilize, add 250 µL of 70% ethanol for at least 1 hour in the fridge (~4°C).

  - Cells can be stored at 4°C in 70% ethanol for up to a week before hybridization.


### 2. Autofluorescence Quenching (optional; cell type dependent)

Due to the intrinsically low signal of smFISH, the autofluorescence signal of some cells can significantly obscure the signals. When working with a cell line for the first time, always include a no-probe control to get a sense of whether the cell is rather clean or has strong autofluorescence background.

In my experience, 3T3 cells are very clean without any significant autofluorescence, but another cell line, SIMS, has very dirty autofluorescence background that has to be quenched.

One common type of autofluorescence come from lipofuscin, which can be quenched quite well by the TrueBlack reagent ([Biotium, Cat# 23007](https://biotium.com/product/trueblack-lipofuscin-autofluorescence-quencher/)). Using TrueBlack will definitely still hurt the real signal a little as well, but it does help to reduce or remove the autofluorescence. The efficacy varies depends on the nature of autofluorescence.

To quench autofluorescence with TrueBlack:

- Dilute dilute 20× stock to 1× in 70% ethanol.
- Treat each well with 250 uL of 1X TrueBlack for 30 seconds.
- Rinse with PBS.


### 3. Probe design, preparation and storage

- smFISH probes for your RNAs of interest can be designed using the [Stellaris probe designer](https://www.biosearchtech.com/support/tools/design-software/stellaris-probe-designer) (free with registration). You can order the probes from LGC Biosearch Technologies after the design. They have a helpful article that discusses [important considerations for smFISH probe design](http://blog.biosearchtech.com/considerations-for-optimizing-stellaris-rna-fish-probe-design).

- In general, using more probes for the same target RNA generates better signal-to-noise ratio. At least 25 probes that are 18–22 nucleotides in length should be used to ensure robust detection. There should be a gap of at least 2 nucleotides between the sequences of adjacent probes to avoid interference during hybridization.

- There are many choices of fluorescent dyes ranging from green to far-red wavelengths, but I have found orange/red dyes such as tetramethylrhodamine (TMR) and Quasar 570 are the brightest and most resistant to photo bleaching among currently available choices. The far-red dye Quasar 670 can be used for multiplexing with TMR or Quasar 570, but it is dimmer and more prone to photo bleaching.

- The custom-designed probe sets from LGC Biosearch Technologies come as a dry pellet typically at a scale of 5 nmol. Dissolve the pellet in 200 μL of Nuclease-free water to obtain a probe stock solution at 25 μM. Divide into 20 μL aliquots and store them frozen at −20°C or −80°C. The probes can be thawed at least 5 times without affecting performance.


### 4. Hybridization, washing and imaging

- Prepare solutions:

  - Prepare smFISH Wash Solution (2× SSC and 10% formamide in DEPC-treated water). Make fresh on the day of usage, store at RT and use it within a few days.

    | Stock | for 10 mL | for 50 mL |
    |:---|---:|---:|
    | DEPC-treated or any RNase-free water	| 8 mL | 40 mL |
    | [20× SSC](https://kdmedical.com/Product.dmx?wid=702a2e7f-6ee0-466a-9ce4-2525f0bea1bd) (e.g., K D Medical, RGF-3240) | 1 mL | 5 mL |
    | [Formamide](https://www.sigmaaldrich.com/catalog/product/sigma/f9037?lang=en&region=US) (Sigma-Aldrich, F9037) | 1 mL | 5 mL |


  - Prepare smFISH Hybridization Solution (2× SSC, 10% formamide, 10% dextran sulfate and 50 μg/mL of yeast tRNAs in DECP-treated water). Store frozen at -20°C. There is no need to aliquot, since this solution can be frozen and thawed more than 10 times without any negative effects on the hybridization results.

    | Stock | for 10 mL |
    |:---|---:|
    | DEPC-treated or any RNase-free water	| 6 mL |
    | [20× SSC](https://kdmedical.com/Product.dmx?wid=702a2e7f-6ee0-466a-9ce4-2525f0bea1bd) (e.g., K D Medical, RGF-3240) | 1 mL |
    | [Formamide](https://www.sigmaaldrich.com/catalog/product/sigma/f9037?lang=en&region=US) (Sigma-Aldrich, F9037) | 1 mL |
    | [10 mg/mL Yeast tRNAs](https://www.sigmaaldrich.com/catalog/product/sigma/r5636?lang=en&region=US) (Sigma-Aldrich, R5636) | 50 µL |
    | [50% Dextran Sulfate](https://www.emdmillipore.com/US/en/product/Dextran-Sulfate-500-0-Solution,MM_NF-S4030) (MilliporeSigma, S4030) | 2 mL |

    The 50% dextran sulfate stock solution is very sticky, so it is highly recommended to use a positive displacement pipette (e.g., Gilson, M-1000R) with specialty pipette tips (e.g., Gilson, CP1000ST). A 50 mL tube is used for the 10 mL volume to make the solution easier to vortex.


  - Prepare Imaging Solution, which is 700 mM [N-Acetyl-Cysteine](https://www.sigmaaldrich.com/catalog/product/sial/a7250?lang=en&region=US) (NAC) in water. Adjust to pH 7.4. This is from [Gut et al., 2018](https://science.sciencemag.org/content/361/6401/eaar7042). NAC acts as both a radical scavenger and an acceptor for free radical-induced photocrosslinking.


- Hybridization, washing and imaging procecures:

  1. Aspirate off the 70% ethanol. Wash once with 250 µL PBS for 5 min at room temperature with gentle rocking.
  1. If incubated with TrueBlack, wash 3× with 250 µL PBS for 5 min at room temperature with gentle rocking.
  1. Add 250 µL smFISH Wash Solution to each well. Incubate at room temperature with gentle rocking for 5 min.
  1. During the incubation, dilute probes in Hybridization Buffer for a final 50 nM total concentration (1:500 from 25 µM stock).
  1. Add 250 µL probe solution to each well.
  1. Incubate in dark at 37 °C for at least 4 hours (can be up to 16 hours; rocking is optional).
    - To avoid cross-contamination between wells especially when different probe sets are used for neighboring wells, DO NOT close the lid during the incubation. Instead, place the slide in a humidified chamber for the incubation.
  1. Wash 2× with 250 µL smFISH Wash Solution for 5 min at room temperature with gentle rocking.
  1. During the wash, dilute DAPI in the smFISH Wash Solution (50 ng/mL). This low amount of DAPI is to avoid bright nuclear staining that bleed into other channels as higher-than-usual laser power and/or longer-than-usual exposure time is needed to image the intrinsically dim smFISH signal. It may be worth trying 50 ng/mL and 500 ng/mL DAPI in parallel (I have used 500 ng/mL DAPI for smFISH of whole-mount embryonic organs and they are fine).
  1. Wash once with 250 µL PBS for 5 min at room temperature with gentle rocking.
  1. Aspirate off the PBS and add 250 µL Imaging Solution (700 mM NAC, pH 7.4) to each well. It is now ready for imaging.
    - Alternatively, you can use PBS with traditional oxygen scavenger (e.g. GLOX buffer) or overflow the wells with some mounting medium (can be quite wasteful) for imaging.


### 5. Imaging

- There has been some conventional wisdom claiming you have to image smFISH samples using wide-filed epifluorescence microscopy instead of confocal microscopy. However, the key is rather to gain enough optical resolution and contrast. In my experience, confocal microscopy does work for imaging smFISH samples and it is the only viable way to image thick tissue samples such as whole-mount embryonic organs. For detailed guidelines of imaging smFISH samples with confocal microscopy, refer to the "Fluorescence Confocal Microscopy Imaging of smFISH Samples" section of [this paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6500779/).


### 6. Quantification

- Please refer to the "Semi-Automated smFISH Image Analysis Using ImageJ Macros" section of [this paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6500779/).

- For 2D cultured cells, it is easier and probably more appropriate to count dots on maximum intensity projections of the images.

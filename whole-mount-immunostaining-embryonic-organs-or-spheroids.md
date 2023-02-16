---
layout: protocols
title: Whole-mount immunostaining for mouse embryonic organs or 3D spheroid cultures
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-12-03
---

### 1. Sample fixation

The choice of fixatives depends on what you want to stain. In most cases, 4% PFA (paraformaldehyde) works well. However, certain antigens are known to NOT work with PFA fixation, noticeably keratins. If you want to stain keratins, fix samples in cold 1:1 mixture of acetone and methanol instead.

* To make 4% PFA in 1× PBS:

  | Stock | for 1 mL | for 10 mL |
  |:---|---:|---:|
  | Water | 650 µL | 6.5 mL |
  | [16% PFA](https://www.emsdiasum.com/microscopy/products/chemicals/paraformaldehyde.aspx) (EMS, 15170) | 250 µL | 2.5 mL |
  | [10× PBS](https://www.fishersci.com/shop/products/lonza-accugene-pbs-10x-pbs-1l/bma51226) (e.g., Lonza, 51226) | 100 µL | 1 mL |

* To fix mouse embryonic organs such as salivary glands cultured on polycarbonate filters:

  1. With PFA fixation:

     * Replace culture media under the filter with 200 µL 4% PFA in 1× PBS. This volume assumes the filter was cultured in a [50-mm MatTek dish with 14-mm glass-bottom opening](https://www.mattek.com/store/p50g-1-5-14-f-case/). Adjust accordingly.
     * Incubate at RT (room temperature) for 30 min to 1 hour, or overnight at 4°C, with gentle rocking.
     * If not staining immediately, store PFA fixed samples in 1× PBS at 4°C.
     * Samples can be stored for at least a month. Seal the containers to minimize liquid evaporation.

  2. With acetone and methanol:

     * Pre-fill and pre-chill a 1.5 mL tube with 1 mL 1:1 mixture of acetone and methanol at -20°C.
     * Use a pair of forceps to grab the filter and quickly immerse it into the acetone-methanol fixative in the 1.5 mL tube.
     * Incubate at -20°C for 30 min to 1 hour.
     * Replace the fixative with 100% methanol for long-term storage at -20°C.
     * It might be OK to store samples in the acetone-methanol mixture, but I haven't tried it.

* To fix 3D spheroid cultures cultured in sticky solutions with extracellular matrix such as Matrigel, first rinse spheroids several times in 1× PBS or [HBSS](https://www.thermofisher.com/order/catalog/product/14170161#/14170161) in clean 35 mm dishes to get rid of the gel chunks often found to attach to the spheroids. After that:

  1. With PFA fixation:

     * Transfer spheroids into sample baskets (e.g. Intavis, 12.440) using low-retention pipette tips (the tips may need to be cut for larger opening; Rainin, 30389187 or 30389190). Use one basket for each staining group.
     * Pre-fill a well in a 24-well plate (e.g. Corning, 3524) with 1 mL 4% PFA in 1× PBS.
     * Immerse the sample basket in 1 mL fixative in the 24-well plate.
     * Incubate at RT (room temperature) for 30 min to 1 hour, or overnight at 4°C, with gentle rocking.
     * If not staining immediately, store PFA fixed samples in 1× PBS at 4°C.
     * Samples can be stored for at least a month. Seal the containers to minimize liquid evaporation.

  2. With acetone and methanol:
  
     * Pre-fill and pre-chill a 1.5 mL tube with 1 mL 1:1 mixture of acetone and methanol at -20°C.
     * Using low-retention pipette tips (the tips may need to be cut for larger opening; Rainin, 30389187 or 30389190) to transfer spheroids into the acetone-methanol fixative in the 1.5 mL tube.
     * Incubate at -20°C for 30 min to 1 hour.
     * Replace the fixative with 100% methanol for long-term storage at -20°C. Be careful not to accidentally discard the sample when pipetting.
     * It might be OK to store samples in the acetone-methanol mixture, but I haven't tried it.

### 2. Re-hydration (only for acetone-methanol fixed samples)

1. Prepare methanol series for re-hydration by mixing 1.2 mL, 2 mL and 2.8 mL methanol with 2.8 mL, 2 mL and 1.2 mL PBSTx (PBS + 0.2% Triton-X-100) in 15 mL tubes (enough for 4 staining groups) to obtain 4 mL 30%, 50% and 70% methanol in PBSTx. Place the methanol series on ice.

2. Re-hydrate samples stored in 100% methanol by incubating them sequentially in 70%, 50%, 30% and 0% methanol in PBSTx on ice, 10 min each step.

   * Re-hydration can be done in 1.5 mL tubes, glass scintillation vials or in sample baskets (Intavis, 12.440) in a 24-well plate.
   * It might be OK to directly go from 100% methanol to PBSTx, but I do the re-hydration series based on my successful experience with single-molecule RNA FISH staining that involves de-hydration and re-hydration.

### 3. Permeabilization, Blocking, Staining and Washing

1. Wash and permeabilize samples in PBSTx (PBS + 0.2% Triton-X-100) for 15-30 min at RT with gentle rocking.

   * If samples are still attached to filters at this step, detach them in a 35-mm dish filled with PBSTx.
   * Split samples into sample baskets (e.g., Intavis, 12.440) immersed in 1 mL PBSTx in the wells of a 24-well plate. Use 1 sample basket per staining condition.

2. Block in 5% [normal donkey serum](https://www.jacksonimmuno.com/catalog/products/017-000-121) diluted in PBSTx for at least 1 hour at RT with gentle rocking. Use 500 µL per well of a 24-well plate.

   * This is assuming secondary antibodies from donkey -- change accordingly.
   * If using mouse primary antibodies, consider adding [M.O.M](https://vectorlabs.com/mouse-on-mouse-m-o-m-blocking-reagent.html) (mouse on mouse) reagent to block mouse IgGs that may be present in the tissue.

3. Incubate in primary antibodies diluted in PBSTx (optionally also include 5% normal donkey serum) for 48 hours at 4 C with gentle rocking. Use 500 µL per well of a 24-well plate.

   * It is critical to incubate in sufficient volume of antibody solutions for an extended period of time. 48 hours incubation is sufficient for most proteins that have a moderate expression level. One example antigen that works well with 48 hours incubation but not 24 hours incubation is E-cadherin.
   * It is critical to include detergent (Triton-X-100 here) to aid antibody penetration towards the tissue center.
   * Longer incubation may be needed if staining highly abundant proteins. One example is anti-PDI as a marker of the endoplasmic reticulum (ER), where 48 hours incubation was not sufficient and resulted in dimmer signal towards the center of the tissue.

4. Wash 4x 15-30 min in PBSTx at RT with rocking. Use 1 mL per well of a 24-well plate.

5. Incubate in labeled secondary antibodies and other fluorescence labels (such as DAPI for nuclear staining and phalloidin for F-actin staining) diluted in PBSTx for 48 hours at 4 C with gentle rocking. Use 500 µL solution per well.

   * We unusually use secondary antibodies from Jackson ImmunoResearch, which come as lyophilized powders. After reconstitution as instructed, we add an equal volume of glycerol for storage at -20°C. All these secondary antibodies were diluted in PBSTx at 1:200 (final 1.5-3 μg/mL) for staining.
   * For [DAPI](https://www.thermofisher.com/order/catalog/product/D1306#/D1306) (e.g., Thermo Fisher, D1306), use 0.5 µg/mL for staining.
   * Make 5 mg/mL DAPI stock in water, aliquot and store at -20°C. For convenience, make 50 µg/mL intermediate stock in water and store at -20°C.
   * __DO NOT__ store DAPI in PBS. It deteriorates pretty badly.

6. Wash 4x 15-30 min in PBSTx at RT with rocking. Use 1 mL per well of a 24-well plate.

   * During these washes, prepare for mounting (see the mounting section below), if you intend to mount these samples for longer storage.

### 4. Quick and easy imaging

1. Prepare 700 mM [N-Acetyl-Cysteine](https://www.sigmaaldrich.com/catalog/product/sial/a7250?lang=en&region=US) (NAC) in water. Adjust to pH 7.4. This will be used as the imaging solution.

   * This is from [Gut et al., 2018](https://science.sciencemag.org/content/361/6401/eaar7042). NAC acts as both a radical scavenger and an acceptor for free radical-induced photocrosslinking.

2. Add 250 µL 700 mM NAC per well in a [glass-bottom 8-well ibidi chamber](https://ibidi.com/glass-bottom/183--slide-8-well-glass-bottom.html).

3. Transfer samples into the ibidi chamber for imaging.

   * The solution is quite high concentration and relatively dense, so the samples can be reasonably immobile at the bottom, especially when it is flat (as the salivary gland cultured on filters).
   * Nevertheless, samples are not completely immobilized, so they could move while imaging.

### 5. Mounting samples for optimal imaging and longer-term storage

1. During the final washes, prepare the following for mounting samples for microscopy imaging.

   * Bring a dropper bottle of ProLong Gold or Diamond Antifade Mountant to room temperature. Put the dropper bottle upside down on a tube rack to help the sticky mountant reach the opening.
   * Pipet 3 mL of PBSTx into a clean 35 mm dish.
   * Cut the imaging spacers into small pieces (~8 pieces from each imaging spacer; Grace Bio-labs, 654004).
   * The imaging spacers are double-sided tape with a paper protector on one side and a plastic protector on the other side. Remove the paper protector to expose one sticky side, and then attach two imaging spacer pieces on a 75 × 25 mm glass slide, so that they occupy two corners across a diagonal line of a 22 × 22 mm area. Peel off the plastic protector of the imaging spacer pieces to expose the other sticky side for the coverslip. Prepare one slide per sample group, and mark the sample information and date on the frosted annotation area of the slide.
   * This geometry of imaging spacers is important for curing mounting media such as the ProLong Gold or Diamond Antifade Mountant used here. It provides enough support to avoid crushing of the samples by the coverslip, and at the same time allows the mounting media to make contact with air for successful curing.

2. After the washes, follow instructions below to mount the samples one group at a time.

   * Under a dissection microscope, transfer one sample basket from the 24-well plate to the 35 mm dish containing 3 mL of PBSTx, and tilt the basket sideways to release all samples into the solution.
   * Occasionally some samples may stick to the side of the basket, and you will need to use forceps to detach them. Remove the empty basket from the dish.
   * The sample baskets can be reused after being cleaned. Discard the sample basket when its bottom mesh is damaged or detached.
   * From the dropper bottle, squeeze out a generous drop of ProLong Gold or Diamond Antifade Mountant inside the imaging spacer supported area on the glass slide. The exact amount does not matter, but should be enough to cover the whole coverslip area (~50 μL). Try to avoid bubbles.
   * Alternatively, squeeze some mounting media into a 1.5 mL tube and pipette the desired amount.
   * If bubbles do appear, use a 20 μL pipet to suck them up. Add more mounting media if you remove too much when sucking up bubbles.
   * Sometimes an unusually large amount of bubbles come out from the dropper bottle, and that is often a sign that the bottle is nearly empty.
   * For organ samples, use a pair of bent-tip forceps to transfer them one by one into the mounting media by holding the sample from below using (“scooping”) to avoid damaging the sample.
   * Use low-retention tips to transfer spheroids by pipetting them into the mounting media one by one.
   * After all samples in the same group are transferred into the mounting media, use the bent-tip forceps to gently push them down to touch the slide, and separate them to avoid touching each other.
   * Place a 22 × 22 mm \#1.5 thickness coverslip on top.
   * Use forceps to hold one side of the coverslip.
   * First, lay one side of the coverslip on the sticky surface of one piece of the imaging spacer, and then gently lower the coverslip down until the held side touches the other piece of the imaging spacer.
   * Use the handle of forceps to press on and brush above the imaging spacers to firmly attach the coverslip.
   * When using ProLong Gold or Diamond Antifade or other mounts for oil objective microscopy, the \#1.5 thickness of the coverslip does not matter. However, when using Fluoro-Gel or equivalent mounting for using a water immersion objective, the thickness of the coverslip should match what the objective is corrected for (most likely for \#1.5 coverslips).
   * Place the slide in a cardboard folder (or any dark container) to protect from light.

3. After all samples are mounted, leave the cardboard folder containing all slides at RT for at least 24 hours to allow the mounting media to cure.

   * After curing, the slides can be stored at -20°C (using proLong Diamond) or RT (using proLong Gold) for at least several months.

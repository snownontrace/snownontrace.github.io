---
layout: protocols
title: Whole-mount immunostaining for mouse embryonic organs or 3D spheroid cultures
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-12-03
---

### 1. Sample fixation

The choices of fixative depends on what you want to stain. In most cases, 4% PFA (paraformaldehyde) works well. However, certain antigens are known to NOT work with PFA fixation, noticeably keratins. If you want to stain for keratins, fix samples in cold 1:1 mixture of acetone and methanol instead.

* To make 4% PFA in 1× PBS:

  | Stock | for 1 mL | for 10 mL |
  |:---|---:|---:|
  | Water	| 650 µL | 6.5 mL |
  | [16% PFA](https://www.emsdiasum.com/microscopy/products/chemicals/paraformaldehyde.aspx) (Electron Microscopy Sciences, 15170) | 250 µL | 2.5 mL |
  | [10× PBS](https://www.fishersci.com/shop/products/lonza-accugene-pbs-10x-pbs-1l/bma51226) (e.g., Lonza, 51226) | 100 µL | 1 mL |

* To fix mouse embryonic organs such as salivary glands, lungs and kidneys cultured on polycarbonate filters:

  1. With PFA fixation:
    - Replace culture media under the filter with 200 µL 4% PFA in 1× PBS. This volume is assuming the filter was cultured in a 50-mm MatTek dish with 14-mm glass-bottom opening (MatTek, P50G-1.5-14-F).
    - Incubate at RT (room temperature) for 30 min to 1 hour, or overnight at 4°C, with gentle rocking.

  1. With acetone and methanol:
    - Pre-fill and pre-chill a 1.5 mL tube with 1 mL 1:1 mixture of acetone and methanol at -20°C.
    - Use a pair of forceps to grab the filter and quickly immerse it into the acetone-methanol fixative in the 1.5 mL tube.
    - Incubate at -20°C for 30 min to 1 hour.
    - Replace the fixative with 100% methanol for long-term storage at -20°C. It might be OK to leave in the acetone-methanol mixture.

* To fix 3D spheroid cultures cultured in sticky solutions with extracellular matrix such as Matrigel, first rinse spheroids several times in 1× PBS or HBSS in clean 35 mm dishes to get rid of the gel chunks often found to attach to the spheroids. After that:

  1. With PFA fixation:
    - Transfer spheroids into sample baskets (one basket per staining group; Intavis, 12.440) using low-retention pipette tips (the tips may need to be cut for larger opening; Rainin, 30389187 or 30389190).
    - Pre-fill a well in a 24-well plate (e.g. Corning, 3524) with 1 mL 4% PFA in 1× PBS.
    - Immerse the sample basket in 1 mL fixative in the 24-well plate.
    - Incubate at RT (room temperature) for 30 min to 1 hour, or overnight at 4°C, with gentle rocking.

  1. With acetone and methanol:
    - Pre-fill and pre-chill a 1.5 mL tube with 1 mL 1:1 mixture of acetone and methanol at -20°C.
    - Using low-retention pipette tips (the tips may need to be cut for larger opening; Rainin, 30389187 or 30389190) to transfer spheroids into the acetone-methanol fixative in the 1.5 mL tube.
    - Incubate at -20°C for 30 min to 1 hour.
    - Replace the fixative with 100% methanol for long-term storage at -20°C. Be careful not to discard the sample accidentally. It might be OK to leave in the acetone-methanol mixture.


### 2. (Only for acetone-methanol fixed samples) Re-hydration

* Before staining acetone-methanol fixed tissues, I usually do a re-hydration step by incubating the samples in a series of 70%, 50%, 30% and 0% methanol in PBSTx on ice, 10 min each step.


Note: this step may not be necessary, but I do it out based on my experience with single-molecule RNA FISH staining that involves de-hydration and re-hydration.


### 3. Permeabilization, Blocking, Staining and Washing

2. Wash in PBSTx for 15 min at RT with gentle rocking. At this stage, split samples into sample baskets immersed in 1 mL PBSTx in the wells of a 24-well plate according to experimental and staining conditions.
3. Block in 5% normal donkey serum diluted in PBSTx for at least 1 hour at RT with gentle rocking.
- This is assuming secondary antibodies from donkey -- change accordingly.
- If using mouse primary antibodies, consider adding some M.O.M reagent to block mouse IgGs that may present in the tissue.
4. Incubate in primary antibodies diluted in PBSTx (optionally also include 5% normal donkey serum) for 48 hours at 4 C with gentle rocking. Use 500 µL solution per well.
- It is critical to incubate in sufficient volume of antibody solutions for an extended period of time. 48 hours incubation is sufficient for most proteins that have a moderate expression level. An example antigen that works well with 48 hours incubation but not 24 hours incubation is E-cadherin.
- It is critical to include detergent (Triton-X-100 here) to aid the antibody penetration towards the tissue center.
- Longer incubation may be needed if staining highly abundant proteins. One example is anti-PDI as a marker of the endoplasmic reticulum (ER), where 48 hours incubation was not sufficient and resulted in dimmer signal towards the center of the tissue.
5. Wash 4x 15-30 min in PBSTx at RT with rocking.
6. Incubate in labeled secondary antibodies and other fluorescence labels (such as DAPI for nuclear staining and phalloidin for F-actin staining) diluted in PBSTx for 48 hours at 4 C with gentle rocking. Use 500 µL solution per well.
7. Wash 4x 15-30 min in PBSTx at RT with rocking.

### 5. Mounting

8. During the final washes, prepare the following for mounting samples for microscopy imaging.
- Bring a dropper bottle of ProLong Gold or Diamond Antifade Mountant to room temperature.  Put the dropper bottle upside down on a tube rack to help the sticky mountant reach the opening.
- Pipet 3 mL of 2× SSC into a clean 35 mm dish.
- Cut the imaging spacers into small pieces (~8 pieces from each of the imaging spacer from Grace Bio-labs, Item \# 654004).  The imaging spacers are double-sided tape with a paper protector on one side and a plastic protector on the other side.  Remove the paper protector to expose one sticky side, and then attach two imaging spacer pieces on a 75 × 25 mm glass slide, so that they occupy two corners across a diagonal line of a 22 × 22 mm area.  Peel off the plastic protector of the imaging spacer pieces to expose the other sticky side for the coverslip.  Prepare one slide per sample group, and mark the sample information and date on the frosted annotation area of the slide.
- This geometry of imaging spacers is important for curing mounting media such as the ProLong Gold or Diamond Antifade Mountant used here.  It provides enough support to avoid crushing of the samples by the coverslip, and at the same time allows the mounting media to make contact with air for successful curing.
- Alternatively, the sample can be mounted in the enclosed space of a circular imaging spacer when using non-curing mounting media such as Fluoro-Gel (Electron Microscopy Sciences, Catalog Number 17985-31).  However, samples mounted in Fluoro-Gel should be imaged as soon as possible after mounting (ideally within 1~2 days).  Store Fluoro-Gel mounted samples at 4°C, and avoid freezing.
9. After the washes, follow instructions below to mount the samples one group at a time.
-  Under a dissection microscope, transfer one sample basket from the 24-well plate to the 35 mm dish containing 3 mL of 2× SSC, and tilt the basket sideways to release all samples into the solution.  Occasionally some samples may stick to the side of the basket, and you will need to use forceps to detach them.  Remove the empty basket from the dish.
- The sample baskets can be reused after being cleaned as described in step 3.  Discard the sample basket when its bottom mesh is damaged or detached.
- From the dropper bottle, squeeze out a generous drop of ProLong Gold or Diamond Antifade Mountant inside the imaging spacer supported area on the glass slide.  The exact amount does not matter, but should be enough to cover the whole coverslip area (~50 μL).  Try to avoid bubbles.
- If bubbles do appear, use a regular 20 μL pipet to suck them up.  Add more mounting media if you remove too much when sucking up bubbles.  Sometimes an unusually large amount of bubbles come out from the dropper bottle, and that is often a sign that the bottle is nearly empty.
- Use the bent-tip forceps to transfer samples of the same group one-by-one into the mounting media.  When transferring, hold the sample from below using the bent-tip forceps (“scooping”) to avoid damaging the sample.
- After all samples in the same group are transferred into the mounting media, use the bent-tip forceps to push them down to touch the slide, and separate them using the forceps to avoid touching another sample.
- Place a 22 × 22 mm \#1.5 thickness coverslip on top.  Use forceps to hold one side of the coverslip.  First, lay one side of the coverslip on the sticky surface of one piece of the imaging spacer, and then gently lower the coverslip down until the held side touches the other piece of the imaging spacer.  Use the handle of forceps to press on and brush above the imaging spacers to firmly attach the coverslip.
- When using ProLong Gold or Diamond Antifade or other mounts for oil objective microscopy, the \#1.5 thickness of the coverslip does not matter.  However, when using Fluoro-Gel or equivalent mounting for using a water immersion objective, the thickness of the coverslip should match what the objective is corrected for (most likely for \#1.5 coverslips).
- Place the slide in a cardboard folder (or any dark container) to protect from light.
10. After all samples are mounted, leave the cardboard folder containing all slides at RT for at least 24 hours to allow the mounting media to cure.  After curing, the slides can be stored at -20°C for at least several months.  Refer to Basic Protocol 2 for instructions of using fluorescence confocal microscopy to image the samples.

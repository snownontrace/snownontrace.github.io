---
layout: protocols
title: Miniprep (regular)
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-10-25
---

Sometimes we still fall back to the good old regular Miniprep, when RNA contamination gets out of control using [Miraprep](./miraprep.html). Although the yield is lower, the quality from regular Miniprep is robust.

### 1. Reagents

We usually use the [Qiagen miniprep kit](https://www.qiagen.com/us/products/top-sellers/qiaprep-spin-miniprep-kit/#orderinginformation) (Qiagen, 27104) that contains all required solutions and columns. However, you can also make all solutions according to [the OpenWetWare recipe](https://openwetware.org/wiki/Qiagen_Buffers) and use [cheaper columns](http://www.epochlifescience.com/Product/SpinColumn/minispin.aspx).

### 2. Procedure

1. Inoculate each bacterial colony into 2.5 mL [terrific broth](https://www.thermofisher.com/order/catalog/product/A1374301#/A1374301) with appropriate antibiotics in a [14 mL round bottom Falcon tube](https://www.fishersci.com/shop/products/falcon-round-bottom-polypropylene-tubes-7/1495911b). Culture in a 37°C shaker incubator at 250 rpm overnight.

    - We usually use 2 mL for miniprep and the remaining 0.5 mL for cryopreservation by making a glycerol stock (see [Freezing and streaking bacteria](./freezing-and-streaking-bacteria.html)).

1. Pour bacterial suspension into pre-labeled [2 mL tubes](https://online-shop.eppendorf.us/US-en/Laboratory-Consumables-44512/Tubes-44515/Eppendorf-Safe-Lock-Tubes-PF-8863.html) (Eppendorf, catalog # 022363352). Centrifuge at 9,000 rpm for 1 min to pellet bacterial cells. Discard the supernatant by pouring into a liquid waste container.

    - For intermediate tubes, simply label them with 1, 2, 3 ... can save labeling time, especially when processing many samples. Just make sure plasmids are ordered in a natural way to avoid trouble of decoding at the last step.

1. Add 250 µL P1 resuspension buffer (with 100 µg/mL RNase A) into each tube.

    - When processing multiple tubes, open all tubes on a rack and use a [repeater pipette](https://online-shop.eppendorf.us/US-en/Manual-Liquid-Handling-44563/Manual-Pipetting--Dispensing-44564/Repeater-M4-PF-44619.html) can be a time-saver.

1. Resuspend the pellet by vortexing or scratching each tube against a tube rack for a few times. Although scratching can be noisy, it is much faster.

1. Add 250 µL P2 lysis buffer into each tube. Invert the tubes 4-6 times or more until the solution becomes viscous and somewhat clear (it will never become very clear if too much bacteria were used -- avoid using too much bacteria for each prep).

    - If LyseBlue was included in P1, the solution should turn blue.
    - Again, use a [repeater pipette](https://online-shop.eppendorf.us/US-en/Manual-Liquid-Handling-44563/Manual-Pipetting--Dispensing-44564/Repeater-M4-PF-44619.html) if processing multiple tubes.
    - When the amount of bacteria is on the higher end, you often need to wait for a couple minutes for the lysis to complete. However, do not go over 5 min for lysis as it may affect the recovery of plasmids.

1. Add 350 µL N3 neutralization buffer into each tube. Immediately invert the tube 4-6 times (or more) to make sure the solution was thoroughly mixed.

    - If LyseBlue was included in P1, the blue color should disappear.
    - I usually do not use the repeater pipette at this step to avoid localized precipitation in the solution (not sure how much it matters though).

1. Centrifuge at ≥ 13,000 rpm for 10 min to pellet cell debris.

1. During centrifugation, a set of spin columns on the columns themselves (instead of on the waste collection tubes).

    - If processing multiple tubes, use a [vacuum manifold](https://www.qiagen.com/us/products/discovery-and-translational-research/lab-essentials/vacuum-manifolds-and-accessories/qiavac-24-plus/#orderinginformation) can be a time-saver. Place labeled columns on the vacuum manifold.

1. After spinning, pour the supernatant into label-matched columns.

1. Centrifuge at ≥ 13,000 rpm for 1 min or use vacuum to drive it through the column.

1. Wash each column using 750 µL PE buffer.

    - Since the volume here does not need to be precise, I often use a 10 mL or 25 mL pipette to fill up the columns with PE buffer when using a vacuum manifold.

1. Centrifuge emptied columns and collection tubes at ≥ 13,000 rpm for 1.5 min to get rid of residual PE buffer.

1. During the centrifugation, arrange a new set of 1.5 mL tubes on a tube rack. Do not close the tubes or label them yet.

1. After the centrifugation, place the columns onto the new set of 1.5 mL tubes. Add 50-75 µL EB buffer to each column. Let sit for ≥ 1 min.

1. Place the tubes in the centrifuge with the open lids towards the center. Put on the centrifuge lid and tighten it. Centrifuge at 9,000 rpm for 1 min in to elute the DNA.

1. Remove the columns and label the tubes one by one. This is when you can elaborate the labeling to your like.

1. Measure DNA concentrations on a nanodrop spectrometer. Perform diagnostic digestion test and send for Sanger sequencing if this is a newly constructed plasmid.

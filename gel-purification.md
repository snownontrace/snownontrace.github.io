---
layout: protocols
title: Gel Purification of DNA
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-10-25
---

### 1. Reagents

We usually use the [Qiagen Gel Extraction kit](https://www.qiagen.com/us/products/discovery-and-translational-research/dna-rna-purification/dna-purification/dna-clean-up/qiaquick-gel-extraction-kit/#orderinginformation) (Qiagen, 28704) that contains all required solutions and columns. However, you can also make all solutions according to [the OpenWetWare recipe](https://openwetware.org/wiki/Qiagen_Buffers) and use [cheaper columns](http://www.epochlifescience.com/Product/SpinColumn/minispin.aspx).

### 2. Procedure

1. Make 1% [agarose](https://www.sigmaaldrich.com/catalog/product/sigma/a9539?lang=en&region=US) (Sigma-Aldrich, A9539) in [TAE](https://qualitybiological.com/product/tae-buffer-10x/) buffer. Heat in a microwave to dissolve the agarose.

1. Cool down the agarose solution for a little, add 0.0001% crystal violet (e.g. Sigma-Aldrich, C6158).

    - Prepare crystal violet stock solution at 0.2% in water in a 50 mL tube. Wrap with foil and store at room temperature. Use at 2000× (50 µL in 100 mL).
    - We don't use ethidium bromide or SYBR dyes for gel extraction. Using crystal violet has the unique advantage to visualize gel bands under ambient light. It indeed is less sensitive. However, if your gel band cannot be seen using crystal violet, you probably need to get more DNA by cutting more plasmids or optimize PCR conditions.

1. Load the DNA samples with the orange loading dye (or any other preferred loading dye). Run the gel in TAE buffer. Usually we run the gel at 100 V for 20-30 min. Gel bands should be visible under ambient light after a few minutes.

    - Orange loading dye: (1) Dissolve 20g of sucrose in 40ml water in a 50 mL tube; (2) Add ~100mg of [Orange G](https://www.sigmaaldrich.com/catalog/product/sigma/o3756?lang=en&region=US); (3) Add water to the 50 mL mark.

1. Cut each desired gel band with a new razor blade. Put it in a 2 mL tube.

1. Add 500 µL buffer QG into each tube to dissolve the gel. Incubate at 50°C for 5 min.

1. During the incubation, label a set of spin columns on the columns themselves (instead of labeling on the waste collection tubes).

    - For small fragments or faint bands, use [NEB Monarch columns](https://www.neb.com/products/t1034-monarch-dna-cleanup-columns-5ug#Product%20Information) and a smaller volume of elution buffer to increase the DNA concentration.
    - If processing multiple tubes, use a [vacuum manifold](https://www.qiagen.com/us/products/discovery-and-translational-research/lab-essentials/vacuum-manifolds-and-accessories/qiavac-24-plus/#orderinginformation) can be a time-saver. Place labeled columns on the vacuum manifold.

1. Pour the dissolved solution into label-matched columns.

1. Centrifuge at ≥ 13,000 rpm for 1 min or use vacuum to drive it through the column.

1. Wash each column using 750 µL PE buffer.

    - Since the volume here does not need to be precise, I often use a 10 mL or 25 mL pipette to fill up the columns with PE buffer when using a vacuum manifold.

1. Centrifuge emptied columns and collection tubes at ≥ 13,000 rpm for 1.5 min to get rid of residual PE buffer.

1. During the centrifugation, arrange a new set of 1.5 mL tubes on a tube rack. Do not close the tubes or label them yet.

1. After the centrifugation, place the columns onto the new set of 1.5 mL tubes. Add 30-50 µL EB buffer to each column. Let sit for ≥ 1 min.

    - If using the [NEB Monarch columns](https://www.neb.com/products/t1034-monarch-dna-cleanup-columns-5ug#Product%20Information), use 5-10 µL EB buffer to elute.

1. Place the tubes in the centrifuge with the open lids towards the center. Put on the centrifuge lid and tighten it. Centrifuge at 9,000 rpm for 1 min in to elute the DNA.

1. Remove the columns and label the tubes one by one. This is when you can elaborate the labeling to your like.

1. Measure DNA concentrations on a nanodrop spectrometer.

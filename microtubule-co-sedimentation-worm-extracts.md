---
layout: protocols
title: Microtubule co-sedimentation from worm extracts
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-10-25
---

7/1
1. Start the worm culture for OD872 and OD894. ~11:30am.
Basically, I rinsed 15 plates of OD872 and OD894 with 15 mL M9 per 5 plates of worms. Pellet them down, resuspend in ~40 mL M9 for each genotype. Seed 13 mL in each 500 mL culture.
Let worms grow at 20C with 200 rpm shaking.

7/4
2. Harvest liquid culture of OD872 and OD894 worms. These are mixed stages of worms rather than synchronized worms.
For each genotype, I have 3x500mL culture. I combined all the 3 flasks, kept half of them for hatching and carrying on another round of liquid culture, while drop-freezing half of these mixed stages of worms.

7/5
5. Seed hatched L1 worms of OD872 and OD894 for round two liquid culture. Yeah!

7/7
2. ~6pm I checked the synchronized liquid worm culture of OD872 and OD894. The growth looks pretty good. All worms are L4’ish and healthy. I shifted the temperature from 20C down to 17C to ensure that they do not overgrow. Tomorrow morning I will harvest them!

7/8
1. Harvest OD872 and OD894 synchronized adult worms. They are slightly older than I would like, but should be good for my purpose.
While spinning down the worms, I noticed that OD872 worms are much harder than OD894 to pellet as a compact mass. 600g for 3 min is sufficient for OD894 worms to sit on the bottom so that it is safe to pour off the supernatent, while for OD872 the worms are still kind of loose and very easy to disturb. Does it indicate that OD872 worms are less dense or the cuticle is somehow defective? I think it is interesting.


Make Buffers:
1 x worm lysis buffer:
50 mM Hepes-KOH, pH 7.6, 1 mM MgCI2, 1 mM Na3 EGTA, 75 mM KCl, 0.5 mM DTT; add proteinase inhibitors before use

Glycerol Cushion:
50 mM Hepes-KOH, pH 7.6, 1 mM MgCI2, 1 mM Na3 EGTA, 40% glycerol, 75 mM KCl, 0.5 mM DTT and proteinase inhibitors

BRB80 buffer (microtubule assembly buffer): 80 mM Pipes-KOH, pH 6.8, 1 mM MgCi2, 1 mM Na3 EGTA. BRB80X buffer: BRB80 supplemented with 0.5 mM DTT, 1 mM GTP,  5 uM taxol, and protease inhibitors

	50 mL Lysis Buffer		10 mL Cushion
1 M Hepes-K 7.6	2.5 mL				500 uL
1 M MgCl2		50 uL				10 uL
500 mM EDTA	100 uL				20 uL
1 M DTT		25 uL				5 uL
3 M KCl		1250 uL			250 uL
1 mg/mL PepstatinA	50 uL				10 uL
50% Glycerol		-				8 mL
H2O			46 mL				1.2 mL

Make Worm Lysate
1.  Weigh out 1 g of frozen adults and add 1.5 mL of Lysis Buffer (plus protease inhibitors).
The total volume is ~2.5 mL.

2.  Setup sonication ice-water bath and sonicate. Since the volume is small, I need to do it in a 15 mL conical and use a fine sonication tip. Use Bradford reagent to monitor the release of proteins during sonication.
- 30% amplitude for 1 min total (0.5 s on, 0.5 s off)
(Save a CRUDE sample)

3.  Transfer crude extract and spin at 20,000 g (for TLA100.3 this is equivalent to 21706 rpm, so I used 22 krpm) for 10 min at 2° C, DECEL = 5.
(Save a LSS sample)

4.  Remove sup and pellet at 50,000 g (for TLA100.3 this is equivalent to 34321 rpm, so I used 34 krpm) for 20 min at 2° C.  Try to avoid any lipid and repellet if too cloudy.
(Save a HSS sample)

5.  Collect supe into a tube on ice.

Bradford assay to determine the concentration of worm lysate
BSA Standards (mg/mL)	CRUDE	HSS
	2.5	5	10	20
A595	.136	.275	.521	1.014	1.053		.847
Therefore, the CRUDE is ~20 mg/mL, HSS is ~16 mg/mL.

Co-pellet MAPs with taxol-stabilized MTs
1. Use 200 uL HSS for each pelleting condition.
(1) Supplement with (final) 0.5 mM DTT, 1 mM GTP, 10 ug/mL nocodazole or 20 uM taxol.
Sample volume: 200 uL
Stock concentration: DTT = 100 mM; GTP = 100 mM; Taxol = 10 mM; Nocodazole = 0.5 mg/mL (10 mg/mL dilute 1:20 in DMSO).
Warm up samples:
		no-MT-1	no-MT-2	endo-MT	DmPatronin	PTRN-1	NOCA
DTT		1		1		1		1		1		1
GTP		2		2		2		2		2		2
DMSO		0.4		-		-		-		-		-
Nocodazole	-		0.4		-		-		-		-
Taxol		-		-		0.4		0.4		0.4		0.4
BRB80		20		20		20		-		-		-
Protein		-		-		-		20		20		20

(2) For all warm up samples: warm to room temperature (22~23C) for 10 min and transferred to ice for 15 min to allow polymerization of the endogenous tubulin.

2. Centrifuge through the glycerol cushion at 48,000 g (~26872 rpm for TLS-55, use 27 krpm; ~36769 rpm for TLA120.2, use 37 krpm) for 30 min at 4C.
(Take the Supe sample by carefully remove 60 uL of the top, add into 20 uL 4x sample buffer)

3. Wash the cushion three times with 1x lysis buffer to clean up the wall of tubes.

4. Aspirate the supe and resuspend the pellet with equal volume of 1x sample buffer (200 uL).

Keep the samples at -20 for SDS-PAGE later.

3. Gel filtration analysis with the HSS worm lysate.
After the gel filtration, I collected all the samples from the void volume peak to the second last fraction. That was fractions 16-47 (32 samples).
First I took 60 uL of each fraction, added in 20 uL 4x sample buffer (this is the diluted sample). Then I took 400 uL of each fraction, added in 100 uL of 100% TCA for TCA precipitation. I mixed each sample by vortex, leave all tubes on ice in the cold room for O/N.
Note: there is an offset volume between the UV peaks and the elution volume, I need to account for it when calculating the elution volume.

4. Sucrose gradient analysis with the HSS worm lysate.
Standards: mix Yao’s standar, 10 mg/mL aldolase and 10 mg/mL catalase equal-volume.
HSS worm lysate: load 100 uL as it is.
After 8 hours spin down at 50 krpm, there is a sizable pellet at the bottom of the HSS worm lysate sample. I collected all the samples by 150 uL fractions, put at -20.

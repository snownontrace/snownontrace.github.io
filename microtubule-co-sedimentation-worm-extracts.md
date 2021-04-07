---
layout: protocols
title: Microtubule co-sedimentation from worm extracts
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-10-25
---

1. Please use detailed protocols described in [this paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3319706/) to make large amount of worm material that has been drop frozen in liquid nitrogen as frozen droplets ("worm beads") stored at -80°C.

1. Prepare or purchase general stock buffer reagents, including:

- 1 M Hepes-KOH (pH 7.6; use KOH for pH adjustment); store at 4°C
- 1 M Pipes-KOH (pH 6.8; use KOH for pH adjustment); store at 4°C
- 3 M KCl; store at room temperature
- 1 M MgCl<sub>2</sub>; store at room temperature
- 0.5 M EGTA (pH 8.0); store at room temperature
- 1 M DTT; store as frozen aliquots at -20°C
- 1 mg/mL Pepstatin A (in ethanol; may add 5% acetic acid); store at -20°C
- 100 mM GTP (e.g., )
- 10 mM Taxol (e.g., )
- 10 mg/mL Nocodazole (in DMSO; )

1. Prepare buffers for making worm lysate.

- Worm lysis buffer (50 mM Hepes-KOH, pH 7.6, 1 mM MgCl<sub>2</sub>, 1 mM EGTA, 75 mM KCl, 0.5 mM DTT; add proteinase inhibitors before use; store on ice):

	| Stock | for 10 mL | for 50 mL |
	|:---|---:|---:|
	| H<sub>2</sub>O	|	9.2 mL |	46 mL |
	| 1 M Hepes-KOH, pH 7.6 | 0.5 mL | 2.5 mL |
	| 3 M KCl | 0.25 mL | 1.25 mL |
	| 1 M MgCl<sub>2</sub> | 10 µL | 50 µL |
	| 0.5 M EGTA, pH 8.0 | 20 µL | 100 µL |
	| 1 M DTT | 5 µL | 25 µL |
	| 1 mg/mL Pepstatin A | 10 µL | 50 µL |

	Add 1 tablet of protease inhibitors (MilliporeSigma, 11836170001) per 10 mL buffer. Vortex to dissolve the tablet. Store on ice.

- Glycerol cushion (40% glycerol, 50 mM Hepes-KOH, pH 7.6, 1 mM MgCl<sub>2</sub>, 1 mM EGTA, 75 mM KCl, 0.5 mM DTT; add proteinase inhibitors before use; store on ice):

	| Stock | for 10 mL |
	|:---|---:|
	| 50% Glycerol | 8 mL |
	| H<sub>2</sub>O	|	1.2 mL |
	| 1 M Hepes-KOH, pH 7.6 | 0.5 mL |
	| 3 M KCl | 0.25 mL |
	| 1 M MgCl<sub>2</sub> | 10 µL |
	| 0.5 M EGTA, pH 8.0 | 20 µL |
	| 1 M DTT | 5 µL |
	| 1 mg/mL Pepstatin A | 10 µL |

	Add 1 tablet of protease inhibitors (MilliporeSigma, 11836170001) per 10 mL buffer. Vortex to dissolve the tablet. Store on ice.

- BRB80 buffer (80 mM Pipes-KOH, pH 6.8, 1 mM MgCl<sub>2</sub>, 1 mM EGTA; store on ice or at 4°C)

	| Stock | for 10 mL |
	|:---|---:|
	| H<sub>2</sub>O	|	1.2 mL |
	| 1 M Hepes-KOH, pH 7.6 | 0.5 mL |
	| 1 M MgCl<sub>2</sub> | 10 µL |
	| 0.5 M EGTA, pH 8.0 | 20 µL |

1. Make Worm Lysate.

1.  Weigh out ~1 g of frozen adults and add 1.5 mL of Lysis Buffer (plus protease inhibitors). The total volume is ~2.5 mL.

2.  Setup sonication ice-water bath and sonicate. Since the volume is small, I need to do it in a 15 mL conical and use a fine sonication tip. Use Bradford reagent to monitor the release of proteins during sonication.
- 30% amplitude for 1 min total (0.5 s on, 0.5 s off)
(Save a CRUDE sample)

3.  Transfer crude extract and spin at 20,000 g (for TLA100.3 this is equivalent to 21706 rpm, so I used 22 krpm) for 10 min at 2° C, DECEL = 5.
(Save a LSS sample)

4.  Remove sup and pellet at 50,000 g (for TLA100.3 this is equivalent to 34321 rpm, so I used 34 krpm) for 20 min at 2°C.  Try to avoid any lipid and repellet if too cloudy.
(Save a HSS sample)

5.  Collect supe into a tube on ice.

Bradford assay to determine the concentration of worm lysate
BSA Standards (mg/mL)	CRUDE	HSS
	2.5	5	10	20
A595	.136	.275	.521	1.014	1.053		.847
Therefore, the CRUDE is ~20 mg/mL, HSS is ~16 mg/mL.

1. Co-pellet MAPs with taxol-stabilized MTs

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

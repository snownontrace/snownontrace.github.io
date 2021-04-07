---
layout: protocols
title: Microtubule co-sedimentation from worm extracts
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2021-04-07
---

1. Please use detailed protocols described in [this paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3319706/) to make large amount of worm material that has been drop frozen in liquid nitrogen as frozen droplets ("worm beads") stored at -80°C.

1. Prepare or purchase buffers and reagents, including:

	- 1 M Hepes-KOH (pH 7.6; use KOH for pH adjustment); store at 4°C
	- 1 M Pipes-KOH (pH 6.8; use KOH for pH adjustment); store at 4°C
	- 3 M KCl; store at room temperature
	- 1 M MgCl<sub>2</sub>; store at room temperature
	- 0.5 M EGTA (pH 8.0); store at room temperature
	- 1 M DTT; aliquot and store at -20°C
	- 1 mg/mL Pepstatin A (in ethanol; may add 5% acetic acid); store at -20°C
	- 100 mM GTP (Thermo Fisher, R0461); aliquot and store at -20°C
	- 10 mM Taxol in DMSO (MilliporeSigma, PHL89806); aliquot and store at -20°C
	- 10 mg/mL Nocodazole in DMSO (MilliporeSigma, M1404); aliquot and store at -20°C
	- 4x Laemmli Sample Buffer (Bio-Rad, 1610747); add 2-mercaptoethanol before use; aliquot and store at -20°C after adding 2-mercaptoethanol

1. Prepare buffers.

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

		| Stock | for 10 mL | for 1 L |
		|:---|---:|---:|
		| H<sub>2</sub>O	|	9.17 mL | 917 mL |
		| 1 M Hepes-KOH, pH 7.6 | 0.8 mL | 80 mL |
		| 1 M MgCl<sub>2</sub> | 10 µL | 1 mL |
		| 0.5 M EGTA, pH 8.0 | 20 µL | 2 mL |

1. Make Worm Lysate.

	- Weigh out ~1 g of frozen adult worm beads and add 1.5 mL of Worm Lysis Buffer (see above) in a 15 mL conical tube. The total volume is ~2.5 mL. Keep on ice.
	- Use a microtip sonicator to lyse worms by sonication. Save a 100 µL CRUDE worm extract sample and keep on ice.
		- We use a Branson 450 Digital Sonifier set at 30% amplitude for 1 min total on time (0.5 s on, 0.5 s off). Usually 2-3 repeats (i.e. 2-3 min total sonication time) are needed to reach the optimal level of lysing. Samples should be chilled for at least 30 sec between sonication runs.
		- Before sonication, poke and stir the samples with a clean metal micro spatula to homogenize samples in the lysis buffer on ice.
		- Place the 15 mL tube in an ice-water bath during sonication to prevent heating. We usually use a beaker to set up the ice-water bath.
		- Monitor worm lysis using a Bradford assay by mixing a small sample (e.g., 2 µL) with 1 mL Bradford reagent. When worms are lysed the color should turn blue. Sonication can be stopped when the total protein concentration of lysate stops increase.
	- Transfer crude extract to a pre-cooled centrifuge tube for the TLA100.3 rotor and spin at 20,000 g (22,000 rpm) for 10 min at 2°C. Set DECEL = 5.
	- Transfer the supernatant (low speed supernatant; LSS) into a new pre-cooled centrifuge tube for the TLA100.3 rotor. Take care to avoid lipid when transferring. Repeat the centrifugation if the lysate is too cloudy. Save a 100 µL LSS sample and keep on ice.
	- Spin the LSS at 50,000 g (34,000 rpm) for 20 min at 2°C.
	- Transfer the supernatant (high speed supernatant; HSS) into a pre-cooled 15 mL tube on ice. Save a 100 µL HSS sample and keep on ice.
	- Use a Bradford assay to determine the concentration of worm lysate. From a typical prep, the CRUDE is 18-20 mg/mL and HSS is 12-16 mg/mL.
	- In a new set of tubes, mix 60 µL CRUDE, HSS and LSS samples with 20 µL 4x Sample Buffer.

1. (Optional) Make exogenous taxol stabilized microtubules.

	- On ice, dilute stock tubulin (10 mg/mL) to 2 mg/mL in BRB80 buffer supplemented with 1 mM DTT and 1 mM GTP. Incubate on ice for 5 min.
	- Clarify tubulin mix in a pre-cooled TLA120.2 rotor at 90 k rpm for 5 min at 2°C.
	- Warm up a TLA100.3 rotor in a 37°C incubator.
	- Transfer clarified tubulin supernatant into a new 1.5 mL tube pre-cooled on ice.
	- Incubate at 37C for 1-2 min to polymerize microtubules.
	- Add taxol stepwise to equimolar as follows (for 2 mg/ml tubulin). For each step, pipet in the taxol and immediately flick the tube to mix it in. If taxol is added all at once it will cause tubulin precipitation.
		- Add 1/10 vol 2 µM taxol; Incubate at 37°C for 10 min.
		- Add 1/10 vol 20 µM taxol; Incubate at 37°C for 10 min.
		- Add 1/10 vol 200 µM taxol; Incubate at 37°C for 15 min.
	- Pellet microtubules over a warm 40% glycerol in BRB80 cushion in a TLA100.3 rotor at 80 k rpm for 20 min, 25°C. Put rotor back at 4°C to cool down.
	- Aspirate and wash sample/cushion interface with warm BRB80 buffer.
	- Rinse pellet and resuspend in warm BRB80 + 200 µM taxol. The taxol should be at least equimolar and preferably in excess to the tubulin. 2 mg/mL tubulin is ~20 µM.

1. Co-sedimentation of MAPs (microtubule associated proteins) with taxol-stabilized MTs.

	- Dilute 1 M DTT 1:10 in water to obtain 100 mM stock.
	- Dilute 10 mg/mL Nocodazole 1:20 in DMSO to obtain 0.5 mg/mL stock.
	- (Optional) Mix 100 µL BRB80 with 1 µL 100 mM DTT and 1 µL 100 mM GTP to obtain BRB80++. This is only needed as control when including the exogenous microtubule group).
	- On ice, supplement 5 µL 100 mM DTT and 10 µL 100 mM GTP to 1 mL HSS worm lysate (HSS++).
	- On ice, set up the following experimental groups. The group including exogenous microtubules is optional. If omitting this group, BRB80 is unnecessary to add. Volumes are in µL. Final concentration of supplements: 0.5 mM DTT, 1 mM GTP, 10 ug/mL nocodazole or 20 uM taxol.

	| Stock | no-MT-1 | no-MT-2 |	endo-MT |	exo-MT |
	|:---|---:|---:|---:|---:|
	| HSS++	|	203 | 203 | 203 | 203 |
	| DMSO | 0.4 | - | - | - |
	| Nocodazole 0.5 mg/mL | - | 0.4 | - | - |
	| Taxol 10 mM | - | - | 0.4 | 0.4 |
	| BRB80++ | 20 | 20 | 20 | - |
	| Exo-MT ~20 µM | - | - | - | 20 |

	- Incubate all samples at room temperature (22~23°C) for 10 min to allow polymerization of the endogenous tubulin. The nocodazole in no-MT-2 group should prevent microtubule polymerization.
	- Transfer samples back to ice and incubate for 15 min. The cold temperature should depolymerize microtubules not protected by taxol in the no-MT-1 group.
	- In 4 pre-cooled centrifuge tubes for the TLA120.2 rotor, add 1 mL 40% glycerol cushion (see _Prepare buffers_) to each tube.
	- Carefully add the 4 mixtures prepared above (~200 µL each) onto the glycerol cushions.
	- Centrifuge through glycerol cushion at 48,000 g (37 k rpm) for 30 min at 4°C using a TLA120.2 rotor.
	- After centrifugation, take a SUPE (supernatant) sample by carefully removing 60 µL from the top and transfer into a pre-cooled 1.5 mL tube on ice. Add 20 µL 4x sample buffer.
	- Wash the sample/cushion interface three times. For each wash, remove the supernatant until the sample/cushion interface and add back 250 µL Worm Lysis Buffer. This washing step is to clean up the wall of centrifuge tubes that contacted the high-concentration lysate.
	- Aspirate the cushion and resuspend the pellet with 200 µL 1x SDS-PAGE sample buffer (PELLET).
	- Keep collected samples in sample buffers at -20°C if not loading them onto an SDS-PAGE gel on the same day.

1. Run SDS-PAGE gel(s) of CRUDE, LSS, HSS, SUPE (1-4) and PELLET (1-4) samples for Coomassie staining and/or Western blotting analysis.

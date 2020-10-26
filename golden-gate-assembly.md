---
layout: protocols
title: Golden Gate Assembly
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-10-25
---

[Site under construction]

[Golden Gate Assembly](https://www.neb.com/golden-gate/golden-gate) uses type IIS restriction enzymes to make sticky ends and allows many fragments to be ligated together in one reaction. However, we almost exclusively use Golden Gate Assembly to ligate a pair of annealed guide RNA oligos into a vector digested with a type IIS enzyme. Here, we demonstrate an example using the [lentiCRISPR v2](https://www.addgene.org/52961/) vector and Cas9 guide RNA(s).

<img src="/assets/img/Golden-gate-assembly-01.png" alt="Golden Gate Assembly schematics" />

### 1. Linearize backbone vectors

* Digest the [lentiCRISPR v2](https://www.addgene.org/52961/) vector with [Esp3I](https://www.neb.com/products/r0734-esp3i#Product%20Information) (isoschizomer of BsmBI). Set up a 50 μL digestion reaction in a 1.5 mL tube:

	| Stock | for 50 µL |
	|:---|---:|
	| Water	|	34.5 |
	| 10× CutSmart Buffer | 5 |
	| Plasmid (1 µg/µL) | 10 |
	| Esp3I (10 U/µL)	|	0.5 μL |

* Incubate the reaction at 37°C for 1-2 hours.

* During the incubation, make 1% agarose gel with 0.0001% crystal violet (stock is 0.2%, use at 2000x) for gel extraction.

* After incubation, run the reaction using the crystal violet gel at 100V for 20-30 min.

	- For the lentiCRISPR v2 vector, we are expecting 2 bands at 13 kb and 1873 bp (filler sequence).

* Cut the larger band at 13 kb and purify with the Qiagen gel purification kit.

	- Purified DNA fragments can be stored at -20°C and used for many freeze-thaws.

### 2. Anneal oligo pairs

Since most oligo pairs come as 100 μM solutions in a 96-well plate, it is most convenient to use a multichannel pipette to transfer and mix oligo pairs in a 96-well PCR plate.
(2-1) For each oligo pair, mix 10 μL oligo 1 + 10 μL oligo 2 + 80 μL water (10 μM duplex).  Heat the plate at 95°C for 5 mins, then cool on bench for 15-30 mins to promote duplex formation.
(2-2) Dilute the 10 μM duplex 1:200 in a new set of wells to obtain a final concentration of 0.05 μM.

### 3. Ligation of lentiviral vector backbone and sgRNA oligo duplex.  Each 20 μL reaction contains:

H2O				13 μL				x14	182
	Digested vector		1 μL (40-50 ng)			14
	T4 ligase buffer 		2 μL					28
	T4 PNK			2 μL					28
	T4 ligase			1 μL					14
	0.05 μM gRNA duplex	1 μL					to add
Make a master mix (N+1 or +2) without the gRNA duplex, and aliquot 19 μL into a new set of wells.  Use a multichannel to transfer 1 μL of each diluted duplex into these wells.  Ligate at room temperature for 10-15 min.


### 4. Transformation of the reaction

Use chemically competent cells such as [NEB Stable Competent _E. coli_ cells](https://www.neb.com/products/c3040-neb-stable-competent-e-coli-high-efficiency#Product%20Information):

  1. Turn on a water bath set at 42°C.
  1. Thaw a tube of 50 µL chemically competent cells on ice for 10 min.
  1. Mix 5 µL reaction with 50 µL competent cells.
  1. Incubate on ice for 10 min. Do not mix.
  1. Heat shock at 42°C for exactly 30 sec.
  1. Place on ice for 3 min.
  1. Spread onto a selection plate. Grow at 37°C overnight or 30°C for 24 h (for plasmids with high risk of recombination).

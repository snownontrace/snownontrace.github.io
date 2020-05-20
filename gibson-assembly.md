---
layout: protocols
title: Gibson Assembly
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-05-18
---

[Gibson Assembly](https://doi.org/10.1038/nmeth.1318) uses a mixture of DNA 5’-exonuclease, polymerase and ligase to ligate 2~6 fragments with ≥ 20 bp overlapping ends into a circular plasmid in one step of 1-hour incubation at 50°C. This method gives us a great deal of freedom and allows scarless ligation of arbitrary fragments, which can be obtained from __PCR__, __enzymatic digestion__ or __synthesis__.

### 1. Prepare the Gibson Assembly Mix

We use homemade Gibson Assembly mix, but it is available from [NEB](https://www.neb.com/products/e2611-gibson-assembly-master-mix#Product%20Information).

- Prepare 5× Isothermal Reaction Buffer (IRB) for 750 reactions using the recipe below, divide into 500 uL aliquots and store at -20°C.

  | Stock | for 3 mL |
  |:---|---:|
  | Water | ~500 µL |
  | 1M Tris-HCl, pH7.5 | 1.5 mL |
  | 400 mM dNTPs (each 100 mM) | 30 µL |
  | 50 mM [NAD](https://www.sigmaaldrich.com/catalog/product/sial/n7004?lang=en&region=US) | 300 µL |
  | PEG 8000 | 750 mg |

- Make the 1.33× Assembly Master Mix (AMM):

  | Stock | for 300 µL | for 600 µL |
  |:---|---:|---:|
  | Water	| 53.4 µL | 106.8 µL |
	| 5× IRB (see above) | 80 µL | 160 µL |
  | 50 mM MgCl<sub>2</sub> | 80 µL | 160 µL |
	| 100 mM DTT | 40 µL | 80 µL |
	| Taq DNA ligase (40 U/µL) <br> (NEB, ) | 40 µL | 80 µL |
  | Phusion DNA polymerase (2 U/µL) <br> (NEB, ) | 5 µL | 10 µL |
  | T5 exonuclease* (1 U/µL) <br> (Epicentre, T5E4111K) | 1.6 µL | 3.2 µL |


	--> 60 uL aliquots @ -20°C. Can freeze and thaw >10 times
(diluted in storage buffer; )

### 2. Design DNA fragments

---
layout: protocols
title: Gibson Assembly
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-05-18
---

[Gibson Assembly](https://doi.org/10.1038/nmeth.1318) uses a mixture of DNA 5’-exonuclease, polymerase and ligase to ligate 2~6 fragments with ≥ 20 bp overlapping ends into a circular plasmid in one step of 1-hour incubation at 50°C. This method gives us a great deal of freedom and allows scarless ligation of arbitrary fragments, which can be obtained from __PCR__, __enzymatic digestion__ or __synthesis__.

### 1. Prepare the Gibson Assembly Mix

We use homemade Gibson Assembly mix, but you can also buy [NEB Gibson Assembly Mix](https://www.neb.com/products/e2611-gibson-assembly-master-mix#Product%20Information).

- Prepare 5× Isothermal Reaction Buffer (IRB) for 750 reactions. Divide into 500 uL aliquots and store at -20°C.

  | Stock | for 3 mL |
  |:---|---:|
  | [PEG 8000](https://www.sigmaaldrich.com/catalog/product/aldrich/p2139?lang=en&region=US) | 750 mg |
  | 1M Tris-HCl, pH7.5 | 1.5 mL |
  | 100 mM [each dNTP](https://www.neb.com/products/n0446-deoxynucleotide-solutionset#Product%20Information) | 4× 30 µL |
  | 50 mM [NAD](https://www.sigmaaldrich.com/catalog/product/sial/n7004?lang=en&region=US) | 300 µL |
  | Water | ~500 µL |

- Make the 1.33× Assembly Master Mix (AMM). Divide into 60 µL aliquots and store at -20°C. It can be frozen and thawed for >10 times without obvious drop in activity.

  | Stock | for 300 µL | for 600 µL |
  |:---|---:|---:|
  | Water	| 53.4 µL | 106.8 µL |
	| 5× IRB (see above) | 80 µL | 160 µL |
  | 50 mM MgCl<sub>2</sub> | 80 µL | 160 µL |
	| 100 mM [DTT](https://www.sigmaaldrich.com/catalog/product/roche/dttro?lang=en&region=US) | 40 µL | 80 µL |
	| [Taq DNA ligase](https://www.neb.com/products/m0208-taq-dna-ligase#Product%20Information) (40 U/µL) | 40 µL | 80 µL |
  | [Phusion DNA polymerase](https://www.neb.com/products/m0530-phusion-high-fidelity-dna-polymerase#Product%20Information) (2 U/µL) | 5 µL | 10 µL |
  | [T5 exonuclease](https://www.neb.com/products/m0363-t5-exonuclease#Product%20Information)* (1 U/µL) | 1.6 µL | 3.2 µL |

  *T5 exonuclease was diluted to 1 U/µL in storage buffer (50 mM Tris-HCl, 100 mM NaCl, 1 mM DTT, 0.1 mM EDTA, 50% Glycerol, 0.1% Triton X-100, pH 7.5 @ 25°C) and stored at -20°C.

### 2. Design DNA fragments

We highly recommend the free software, [ApE](https://jorgensen.biology.utah.edu/wayned/ape/), for everyday editing of DNA sequences.
